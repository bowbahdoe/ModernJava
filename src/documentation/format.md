# Format

```java,no_run
import java.io.IOException;

/// This class serves as a place to put examples
/// of the different kinds of documentation as well
/// as how to write documentation properly.
///
/// When specified after the three slashes
/// you can write documentation using [Markdown](https://en.wikipedia.org/wiki/Markdown).
///
/// In Markdown you can just write text as you would in any file,
/// line after line.
///
/// # For headings you can use a single hash
///
/// ## For subheadings you can use two
///
/// ### And so on
///
/// You can make unordered lists using hyphens
///
/// - A
/// - B
/// - C
///
/// And numbered lists like so
///
/// 1. One
/// 2. Two
/// 3. Three
///
/// And so on. Definitely peruse up [tutorial on markdown](https://www.markdownguide.org/getting-started/)
/// when you have the time.
///
/// There are some additions specific to Java though.
/// We call these additions "tags."
///
/// One notable tag is the author tag. It lets you mark who worked
/// on a given unit of code
///
/// @author Ethan McCue
/// @see [https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html](https://www.oracle.com/technical-resources/articles/java/javadoc-tool.html)
public class DocumentationExample {
    /// You can document the purpose of parameters
    /// to constructors and methods with the param tag
    ///
    /// @param o Demonstrates a param tag on a constructor
    public DocumentationExample(Object o) {

    }

    /// Generic parameters can also be documented using the param tag
    /// as well.
    ///
    /// @param item The item to just return back
    /// @param <T> The type of the item.
    public static <T> T identity(T item) {
        return item;
    }

    /// The exceptions thrown by a method can also be documented
    ///  to explain under what conditions the exceptions might be thrown
    ///
    /// @param s A parameter to show that throws can be used alongside params
    /// @throws IOException whenever the method is called, no matter what
    public void crash(String s) throws IOException {
        throw new IOException();
    }

    /// You can reference other classes and methods on those classes with the
    /// link tag.
    ///
    /// For instance {@link String} and {@link String#length()}.
    public void seeMore() {

    }
}
```
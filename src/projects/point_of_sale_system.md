# Point of Sale System

## Problem Statement

Consider the operations of a grocery store.

Prospective customers walk in the store, perhaps acquiring a cart or a basket,
and gather the items they want to purchase. They then walk to the front of the 
store, purchase those items using money, and leave.

Some items are priced by quantity. For example, one [avocado](https://en.wikipedia.org/wiki/Avocado) might cost $0.77.
If they purchased 5 avocados they would have to pay $0.77 five times or $3.85 in total.

Other items are priced by weight. Bananas are [really cheap for some reason](https://en.wikipedia.org/wiki/Banana_republic)
and so 1 pound of bananas costs $0.39. If they purchase 1.5 pounds of bananas they would have to pay 1.5 times $0.39 or $0.585 in total. Currencies like the dollar do not have a "tenth of a penny" so after this math the amount will be rounded
either to $0.58 or $0.59 depending on the policy of the store in question.

Either way it is uncommon for someone to have exactly $3.85 or $0.59 on their person. So to facilitate purchases
using physical money they must accept larger bills and offer change for the difference. If someone tries to use a $10 bill
to buy $3.85 of avocados the store will provide $6.15 back to the customer in change.

While a business can operate this way without any sort of computer involved there are several benefits to having one.

The price a store wants to charge for any given item is bound to change over time. When training a cashier it can make
more sense to teach them short codes for different items and have the computer system figure out the price to use[^plu]. This would generally include telling them to weigh an item or count the quantity of said item.

In addition to the price, calculating change is easy for computers to do. While it is not hard for a human to do either,
a computer will make fewer mistakes calculating the difference between $45 and $13.53. This is especially true over the course of an 8 hour shift where mental fatigue can start to set in.

It is also helpful for a business to know how much they sold in a given day. Having computers in the mix makes it more practical to get these "end of day reports." They might use these reports to know that they need to order more onions because those are selling well recently.[^viral] They can also be used to catch cashiers who are stealing from the register
to support their families.[^common]

We call these systems that are used at the point products are sold Point of Sale Systems.

## Your Goal

Make a program that can be used as a point of sale system for a hypothetical produce stand.

The products the produce stand sells are as follows:

| Item | Cost |
|------|------ |
| Banana | $0.39 per pound |
| Avocado | $0.66 each |
| Plantains | $0.99 each |
| Watermelon | $6.99 each |
| Onion | $0.62 each |
| Celery |$0.31 per ounce|
| Carrot |$0.06 per ounce|
| Cabbage |$2.72 each|

Customers may purchase any amount of any items in any combination.

Make sure to at least:

* Track the total for an order.
* Prompt the cashier for the right quantities and weights.
* At the end of an order give the cashier the total and have them enter the amount given to them by the customer.
* Tell the cashier how much in change they need to provide.

## Future Goals

When you learn enough to do the following, come back to this project and expand it.

* Grow your program to support double or triple the number of available items.
* Make it so that the cashier has to "log in" to use the system
* Account for a manager whose job it is to record how much money is in the register before and after a day of operations
and note any unaccounted for funds.
* Make the program not lose information if the computer running it turns off then on again.
* Make the system work for "self check out," where the person entering the items is also the customer. Theft in
these cases is monitored via security cameras and punished via the might of the police state.
* Use a camera attached to the computer to scan a bar code which contains the product number.
* Optionally print a receipt for each order to a physical printer..



[^plu]: Here is a list of "[PLU](https://www.fsproduce.com/wp-content/uploads/2015/05/2011-PLU-Listing1.pdf)" codes. 4011 is banana.

[^viral]: Due to a viral onion tart recipie or something.

[^common]: This is common in no small part because cashiers, like many modern professions, are not paid a livable wage.
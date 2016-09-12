# lab04

All of these questions deal with the ticket machine example bundled in this repo. You should fork this repo and clone the fork to work on the code locally. 

## How can we tell from just its header that `setPrice` is a method and not a constructor?
```
public void setPrice(int cost)
```
We can tell just from the header that `setPrice` is a method and not a constructor, because in order for a header to be a constructor, it cannot have a return type, which in this case it has as void.

## Complete the body of the `setPrice` method so that it assigns the value of its parameter to the price field. Write your new method in the `lab04-ticket-machine`.

## Complete the body of the following method, whose purpose is to add the value of its parameter to a field named `score`.
```
/**
 * Increase score by the given number of points.
 */
public void increase(int points)
{
  ...
}
```
## Is the `increase` method in the previous question a mutator? If so, how could you demonstrate this?
Yes it is a mutator, because it is changing the value. You could demonstrate this by calling the get method to get the initial score, and then calling the increase method and then printing the new value with get to see a change in the score. 

## Complete the following method, whose purpose is to subtract the value of its parameter from a field named `price`. Add your new method to the `lab04-ticket-machine`.
```
/**
 * Reduce price by the given amount.
 */
public void discount(int amount)
{
  ...
}
```

## Write down exactly what will be printed by the following statement:
```
System.out.println("My cat has green eyes.");
My cat has green eyes.
```

## Add a method called `prompt` to the `TicketMachine` class in the `lab04-ticket-machine`. This should have a `void` return type and take no parameters. The body of the method should print the following single line of output: 
```
Please insert the correct amount of money.
```

## What do you think would be printed if you altered the fourth statement of `printTicket` so that `price` also has quotes around it, as follows?
```
System.out.println("# " + "price" + " cents.");
```
# price cents

## What would be printed here?
```
System.out.println("# price cents.");
```
# price cents
## Could either of the previous two versions be used to show the price of tickets in different ticket machines? Explain your answer.

No, the two previous versions cannot be used to show the price of the tickets in different ticket machines, because the term price in this case is a string since it has quotes around it, and thus the program will read it as a word price instead of as a variable.

## Add a `showPrice` method to the `TicketMachine` class in the `lab04-ticket-machine`. This should have a void return type and take no parameters. The body of the method should print (here `xyz` should be replaced by the value held in the `price` field when the method is called):
```
The price of a ticket is xyz cents.
```


## Create two ticket machines with differently priced tickets. Do calls to their showPrice methods show the same output, or different? How do you explain this effect?
```
TicketMachine tm1 = new TicketMachine(100);
TicketMachine tm2 = new TicketMachine(200);
```

## Modify the constructor of `TicketMachine` in the `lab04-ticket-machine` so that it no longer has a parameter. Instead, the price of tickets should be fixed at 1,000 cents. What effect does this have when you construct ticket-machine objects within BlueJ?
The effect that this has on constructing ticket-machine objects within BlueJ is that now the price will be a fixed value, and you will not be able to write your own cost when creating a ticket machine. All tickets will cost 1000 cents, and tm1 and tm2 will no longer cost 100 and 200 cents, but will instead cost 1000 cents. Although the price is a fixed amount, you can still change it by calling the setPrice method.

## Give the class two constructors. One should take a single parameter that specifies the price, and the other should take no parameter and set the price to be a default value of your choosing. Test your implementation by creating machines via the two different constructors.
```
public TicketMachine(int cost)
{
price = cost;
}

public TicketMachine ()
{
price = 1500;
}
```

## Implement a method, `empty`, that simulates the effect of removing all money from the machine. This method should have a `void` return type, and its body should simply set the `total` field to zero. Does this method need to take any parameters? Test your method by creating a machine, inserting some money, printing some tickets, checking the total, and then emptying the machine. Is the `empty` method a mutator or an accessor?

This method does not need to take any parameters, and it is a mutator, because it is changing the value of the amount of money left in the machine.  

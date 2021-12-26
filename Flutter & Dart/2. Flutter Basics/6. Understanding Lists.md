**You can skip this lecture if you're familiar with lists (or "arrays" in other programming languages).**

Lists are core feature of Dart - and actually of pretty much any programming language (in other languages, lists are also called "**arrays**").

Lists allow you to **group multiple values** (of any type you want) together - you can even have **lists of lists** if you want to (so-called "nested lists").

1.  var aListOfText = ['Hi', 'This is a list', 'of multiple text snippets (strings)'];

1.  var aNestedList = [[1,2,3], [1,2,3]]; 

Lists are created by wrapping the items that should be part of the list into square brackets. Often you have lists of the same type (i.e. a list with only `string`s or `int`s in it) but you can absolutely also have lists of mixed types:

1.  var aMixedList = ['Some text', 1, 5.99, ['a nested list!', 1]];

Data in lists can be accessed via the **index** of list items - the important thing here is, that this **index starts at zero (0)**!

1.  var names = ['Max', 'Manu', 'Julie'];
2.  // Max has index 0, Manu has index 1, Julie has index 2
3.  print(names[0]); // prints 'Max' in the console
4.  print(names[2]); // prints 'Julie' in the console
5.  print(names[3]); // would throw an error because there is no element with index 3 in the list

You can also find out **how many items** are in a list:

1.  print(names.length); // prints 3 - it does NOT print the highest index but simply the amount of items

Dart also offers **many methods** (functions that belong to an object) on the List object (like every other value in Dart, lists are an object).

1.  names.add('Chris'); // this adds 'Chris' as a new element to the end of the list 
2.  names.remove('Max'); // this removes 'Max' from the list, all other items would move and fill the gap

We'll use many methods throughout the course - so there's no need to explore them all right now.

If you still want to learn more about lists right now, have a look at this article (Warning: This article contains a lot of information, we'll only dive into later in the course - hence it might be overwhelming right now): [https://dart.dev/guides/language/language-tour#lists](https://dart.dev/guides/language/language-tour#lists)

You can also check out the official API docs to get more information + a complete list (how meta!) of all default methods you can call on Dart lists: [https://api.dartlang.org/stable/2.3.1/dart-core/List-class.html](https://api.dartlang.org/stable/2.3.1/dart-core/List-class.html)
Download Link: https://assignmentchef.com/product/solved-cs161-week-8
<br>
Define a class called Item that consists of a string called name, a double called price, and an int called quantity.  The price represents the price per unit, so if you have an Item with the name “apple”, the price “0.80” and the quantity 4, then it means that this Item represents 4 apples, with each apple costing 80 cents.  It should have get and set methods for each field (following the normal naming convention – getName, setName, getPrice, setPrice, getQuantity and setQuantity).  It should have a constructor that takes three parameters (in the order given above) and passes them to the set methods.  It should have a default constructor that sets name to “”, price to 0.0 and quantity to 0.

Define a ShoppingCart class which contains as a data member an array of pointer-to-Item (Item*) that can contain up to 100 Item pointers. It should also have an int data member called ​<em>arrayEnd</em>​ that keeps track of the index of the next empty spot in the array.  You should have a default constructor that initializes each element of the array to NULL and initializes arrayEnd to zero.  It should have a function called <em>addItem</em>​ that takes as a parameter a pointer to an Item and adds it to the array (and updates arrayEnd).  It should have a function called ​<em>totalPrice</em>​ that returns the total cost of all Items in the ShoppingCart (for which you must take into account the quantity of each Item).  Your classes may get used as follows:

Item a(“affidavit”, 179.99, 12);

Item b(“Bildungsroman”, 0.7, 20);

Item c(“capybara”, 4.5, 6);

Item d(“dirigible”, 0.05, 16);

ShoppingCart sc1;  sc1.addItem(&amp;a);  sc1.addItem(&amp;b);  sc1.addItem(&amp;c);  sc1.addItem(&amp;d);

double diff = sc1.totalPrice();

Potential parenthesis pitfalls: Remember not to use empty parentheses when declaring an object.  If you are invoking a constructor that takes parameters, then you would use parentheses with parameters inside, but if you are invoking the default constructor, you don’t use parentheses at all.  Also remember that all function calls must have parentheses – if a function doesn’t take any parameters, then you must put an empty pair of parentheses.

The files must be called: ​<strong>Item.hpp</strong>​, ​<strong>Item.cpp</strong>​, ​<strong>ShoppingCart.hpp</strong>​ and ​<strong>ShoppingCart.cpp</strong>​.

Item.cpp and ShoppingCart.hpp should both #include Item.hpp.  ShoppingCart.cpp should #include ShoppingCart.hpp.  The main method you write for testing will also need to include ShoppingCart.hpp.  If you named the file with your main method “cartMain.cpp”, then you can compile your program with “g++ Item.cpp ShoppingCart.cpp cartMain.cpp -o cart”.
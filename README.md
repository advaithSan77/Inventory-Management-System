Project Overview:

The Inventory Management System can be used to keep a record of the inventory of a store and also the sales made by it. It consists of a records.json file that keeps track of the inventory and a sales.json file that keeps track of all the sales made by the store.

First an initial records dictionary is created with 31 items. It consists of items such as Dairy Milk, Lays, Coke, etc. They have keys ranging from '1000' to '1030' and this can be added to. Each item has an ID key and its properties are stored in an internal dictionary which are ? name, price, quantity, category and brand.
Then an empty sales dictionary is initialized and the records and sales dictionaries are written in created records.json and sales.json files respectively. 

The main program starts with a function items_disp() which is defined to display the items available to purchase. It displays the ID, name, price and quantity. In this function if the quantity of any item is 0, it shows ?Out of stock?.

Next a function bill_disp() is defined to display the bill of purchased items. It displays the item ID, Item name, price of each item, quantity of each item and the total for each item using a for loop looping through the list of items passed to it. The quantity of each item is passed to this function as a dictionary with the purchased items? IDs as the keys and the quantity as values. It also calculates the total bill amount and displays it at the end.
 
Then a function add_sales() is defined with similar parameters as bill_disp() which is used to add a sale to the sales.json file. The sales.json file is opened and the dictionary is read and loaded. Then each of the sales are added using a for loop. The time of purchase is also determined using the datetime and timezone modules and the time zone of Asia/Kolkata is used. The keys start from 1 and go upwards. The values added are name, price, quantity, amount and time of purchase. Then the sales dictionary is written to the sales.json file.

A function view_sales() is defined to show all the sales made where the sales.json file is opened, read and the dictionary is loaded. The transaction ID along with the other values of the internal dictionary are displayed.

Then all the sales made until the ensuing moment can be viewed using view_sales() and also the items remaining in the inventory using items_disp() passing records.keys() as argument.

To add items to the inventory the records.json file is first opened and read and the dictionary is loaded into the records dictionary. Then the number of items to be added is inputted. Then using a for loop the items are inputted where the name of the item(suppose X) to be added is first entered. And then the number of Xs are entered. 
Then using another for loop we check if the item is already present in the inventory. We find if it is present using a flag f which sets to 1 if the item is present. If the item is not present, the price, category and brand of the item are inputted from the user. Then using the key str(co) which is the next ID available, all the properties of the item is stored and the quantity is updated. If the item is already present in the inventory, the quantity is just added to the quantity value of the inner dictionary. This process is repeated for all items to be added. Then this updated dictionary is written to the records.json file. 

To order items from the inventory the records.json file is opened and read and the dictionary is loaded. Then an empty list lis and empty dictionary dic are initialized to store the items to be purchased and quantity of each item respectively. Then the available items are printed by passing records.keys() to items_disp(). Then an infinite while loop is opened and the number of items(n) to be purchased is inputted. If the number is lesser than 1 or greater than the length of records then the loop is continued and the number of items is inputted again. A variable c is initialized to 1.
If n is valid then another infinite loop is opened and the IDs of the items to be purchased are to be entered. If the ID is invalid then the second infinite loop is continued. If the quantity of any entered item is 0, then using another for loop, the items of similar category are found and these IDs are stored in a list lis1. If items of the similar category are available then lis1 is passed to items_disp() and these items are displayed for the customer to chose from. If no items of the similar category are available then this is printed on the screen and the customer is asked to enter other IDs by continuing the second loop.
If the item ID entered is valid and has quantity greater than 0 then the ID is appended to the list lis. The value of c is incremented and if c is greater than n then the second infinite loop is broken. This goes on till all the item IDs are inputted.
A for loop is then opened in the first infinite loop which loops through the IDs in list lis. Here the number of each item(b) is inputted. If the number of an item to be bought is more than the number of that item present in the inventory then the available number is printed and b is assigned the value of this available number. The customer is asked whether he/she wants to buy all of those remaining items. If yes then the b is stored in dictionary dic with the key of item ID. If no then the loop is continued. This loop goes on.
Then in the first infinity loop another for loop loops through the items in lis and for every item it removes the quantity of items purchased(dic[i]) from the quantity of that item in the inventory(records[i][?quantity?]. 
If lis turns out empty then the customer is asked whether he/she would like to place another order. If yes then the first infinity loop is continued. If no then this list is broken. If lis is not empty then add_sales() and bill_disp() are called with the same parameters ? lis, dic. Then the first loop is broken.

Then the records.json file is opened and the updated records dictionary is written to this file.
Then the sales done can be viewed using the view_sales() function.

Features:

1. The available items is displayed before purchase and can be displayed manually.
2. While displaying these items if the product quantity is 0 then it displays 'Out of stock'.
3. It displays the bill after purchase.
4. It displays the sales records along with the transaction ID and time of purchase.
5. Multiple items can be added to the inventory along with multiple quantities of each.
6. While adding items to the inventory, it inputs the item name and checks if it is already present in  the inventory.If it is present then it adds to the already present quantity. If not then it assigns a new item ID and adds all properties which are inputted.
7. Multiple items can be purchased at one time and multiple quantities of each item can be purchased.
8. While purchasing if the customer enters an invalid number of items then the customer is asked to enter a valid number again.
9. If the customer enters and invalid item ID then the customer is asked to enter a valid ID again.
10. If the customer enters the ID of a product which is out of stock, then this is displayed on the screen. It also displays the available items of similar category for the customer to purchase. If no items of the similar category are available then that is also displayed.
11. If the customer enter a greater quantity of an item than what is present in the inventory then the appropriate message is displayed along with an option to purchase that remaining quantity.
12. The program uses a list to store purchased items' IDs and a dictionary to store quantity of each item purchased.
13. If somehow the customer's cart turns out empty then it is inquired whether the customer wants to place another order and if yes then another order is placed.


About:
 
Advaith Santhosh

MVJ College of Engineering 

Bangalore


Contact: 

Linkedin: https://www.linkedin.com/in/advaith-santhosh



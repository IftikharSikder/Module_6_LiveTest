Flutter app of "Shopping List".
Includes:
●     The page should have a Scaffold as the root widget.
●     Inside the Scaffold, create an AppBar with the title "My Shopping List".
●     Below the AppBar, create a ListView widget to display the list of shopping items.
●     Each item in the list should be represented by a ListTile widget.
●     Each ListTile should display an icon on the left, followed by the name of the shopping item.
●     The list should have at least 5 shopping items.
●     Add appropriate padding, spacing, and styling to make the app visually appealing.
●     Use the IconButton widget to add an icon button on the AppBar. When pressed, it should display a Snackbar with the message "Cart is empty".

![Module_6_Live_Test](https://github.com/IftikharSikder/Module_6_LiveTest/assets/101981180/d0fd4e1e-5f4f-4b31-aa37-f56be56e6726)

Code:
..........................................
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      title: 'My Shopping List',
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: MyHomePage(),
    );
  }
}

class MyHomePage extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('My Shopping List'),
        centerTitle: true,
        actions: [
          IconButton(
            icon: Icon(Icons.shopping_cart),
            onPressed: () {
              ScaffoldMessenger.of(context).showSnackBar(
                SnackBar(
                  content: Text('Cart is empty'),
                ),
              );
            },
          ),
        ],
      ),
      body: ListView(
        children: [
          ListTile(
            leading: Icon(Icons.shopping_basket),
            title: Text('Apples'),
          ),
          ListTile(
            leading: Icon(Icons.shopping_basket),
            title: Text('Bananas'),
          ),
          ListTile(
            leading: Icon(Icons.shopping_basket),
            title: Text('Bread'),
          ),
          ListTile(
            leading: Icon(Icons.shopping_basket),
            title: Text('Milk'),
          ),
          ListTile(
            leading: Icon(Icons.shopping_basket),
            title: Text('Eggs'),
          ),
          ListTile(
            leading: Icon(Icons.shopping_basket),
            title: Text('Mango'),
          ),
          ListTile(
            leading: Icon(Icons.shopping_basket),
            title: Text('Watermelon'),
          ),
          ListTile(
            leading: Icon(Icons.shopping_basket),
            title: Text('Pineapple'),
          ),

        ],
      )
    );
  }
}

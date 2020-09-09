# membuat-4-navigasi-menggunakan-stateless-widget
membuat 4 navigasi menggunakan stateles widget untuk kedepannya
import "package:flutter/material.dart";

void main() {
  runApp(
    MaterialApp(
      home: new Stkc1(),
    ),
  );
}

class Stkc1 extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        //leading: new Icon(Icons.home),
        title: new Text("POINT BLANK Mobile"),
        actions: <Widget>[
          IconButton(
            icon: Icon(Icons.menu),
            onPressed: () {},
          ),
          IconButton(
            icon: Icon(Icons.home),
            onPressed: () {},
          ),
        ],
      ),
      body: new Center(
        child: new Icon(Icons.home, size: 70.00, color: Colors.red),
      ),
      bottomNavigationBar: BottomNavigationBar(
        backgroundColor: Colors.black12,
        items: const <BottomNavigationBarItem>[
          BottomNavigationBarItem(
            icon: Icon(Icons.map, color: Colors.amber),
            title: Text('MAP '),
          ),
          BottomNavigationBarItem(
            icon: Icon(Icons.update, color: Colors.amber),
            title: Text('REPORT CHEATING'),
          ),
          BottomNavigationBarItem(
            icon: Icon(Icons.list, color: Colors.amber),
            title: Text('OWNER BASCAMP'),
          ),
        ],
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: () {
          // Add your onPressed code here!
        },
        child: Icon(Icons.navigation),
        backgroundColor: Colors.green,
      ),
      drawer: new Drawer(
        child: ListView(
          padding: EdgeInsets.zero,
          children: const <Widget>[
            DrawerHeader(
              decoration: BoxDecoration(
                color: Colors.blue,
              ),
              child: Center(
                child: Text("MENU"),
              ),
            ),
            ListTile(
              leading: Icon(Icons.list),
              title: Text('MY PROFIL'),
            ),
            ListTile(
              leading: Icon(Icons.upgrade),
              title: Text('PREMIUM SHOP'),
            ),
            ListTile(
              leading: Icon(Icons.party_mode),
              title: Text('LOGIN TO GAME'),
            ),
            ListTile(
              leading: Icon(Icons.inventory),
              title: Text('INVENTORY'),
            ),
            ListTile(
              leading: Icon(Icons.settings),
              title: Text('PUSAT ISI ULANG PB'),
            ),
            ListTile(
              leading: Icon(Icons.settings),
              title: Text('SETTINGS'),
            ),
            ListTile(
              leading: Icon(Icons.settings),
              title: Text('LOGOUT'),
            ),
          ],
        ),
      ),
    );
  }
}

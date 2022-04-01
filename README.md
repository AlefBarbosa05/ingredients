import 'package:flutter/material.dart';

const Color darkBlue = Color.fromARGB(255, 18, 32, 47);

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData.dark().copyWith(
        scaffoldBackgroundColor: darkBlue,
      ),
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: Center(
          child: MyWidget(),
        ),
      ),
    );
  }
}

class MyWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Card(
        color: Colors.white,
        elevation: 5,
        child: Container(
          padding: EdgeInsets.all (16.0),
            width: 300,
            height: 300,
            child: Column(children: [
              Row(mainAxisAlignment: MainAxisAlignment.spaceBetween, children: [
                Column(children: const [
                  const Text('Ingredients',
                    style: TextStyle(
                      color: Colors.black,
                      fontSize: 20.0,
                    )),
              ]),
              Icon(
                Icons.people,
                color: Colors.black,
                size: 30.0,
              ),
            ]),
              Divider (),
               Row(mainAxisAlignment: MainAxisAlignment.spaceBetween,
                 children: const [
                  const Text (' 3  cups water',
                   style: TextStyle(
                      color: Colors.black,
                      fontSize: 20.0,
                        ),
                 )],
                ),
              Divider (),
                Row(mainAxisAlignment: MainAxisAlignment.spaceBetween,
                 children: const [
                  const Text ('1/4 fresh ground pepper',
                   style: TextStyle(
                      color: Colors.black,
                      fontSize: 20.0,
                        ),
                 )],
                  ),
              Divider (),
              Row(mainAxisAlignment: MainAxisAlignment.spaceBetween,
                 children: const [
                  const Text (' 2 lemon zest',
                   style: TextStyle(
                      color: Colors.black,
                      fontSize: 20.0,
                        ),
                 )],
                  ),
              Divider (), 
               Row(mainAxisAlignment: MainAxisAlignment.spaceBetween,
                 children: const [
                  const Text ('1 TSP salt',
                   style: TextStyle(
                      color: Colors.black,
                      fontSize: 20.0,
                        ),
                 )],
                  ),
              Divider (),
              Row(mainAxisAlignment: MainAxisAlignment.spaceBetween,
                 children: const [
                  const Text ('1 onion',
                   style: TextStyle(
                      color: Colors.black,
                      fontSize: 20.0,
                        ),
                 )],
                  ),
            ])));
  }
}

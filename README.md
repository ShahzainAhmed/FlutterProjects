# Learning Flutter 
## Started on 10th March 2022
# Topics Covered
**Basic Widgets for User Interface in Flutter**
- MaterialApp
- Scaffold
- Container
- SizedBox
- Column
- Row
- SingleChildScrollView
- AppBar
- Center
- Textfield
- ElevatedButton
- StatelessWidget and StatefulWidget Classes
- EdgeInsets
- Margin and Padding
- Align
- Decoration

## MaterialApp 
**`(home: )`**
## Scaffold
**`(body: )` this means it takes the entire body**
## Container
**Container will take only 1 child.  `(child: )` meaning 1 widget only. (e.g. text button, container, etc)**
## Row/Column
**``children:`` meaning it takes more than 1 widget (e.g. text button, container, etc)**
## SizedBox
**It is also a widget, it is a box which is used for spacing**  
Example:

![image](https://user-images.githubusercontent.com/59369881/157589070-27d4e0e9-a1c6-4468-827a-c58ddab3d6f6.png)

## Column
```
import 'package:flutter/material.dart';

void main(){
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  
  
  const MyApp({ Key? key }) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return  MaterialApp(
      home: (
          Scaffold(
            body: Column(
            children: const [Text("Shahzain Ahmed 1st Column"), 
            SizedBox(height: 10,),
            Text("Shahzain Ahmed 2nd Column"),
             SizedBox(height: 10,),
            Text("Shahzain Ahmed 3rd Column"),
             SizedBox(height: 10,),
            Text("Shahzain Ahmed 4th Column"),
             SizedBox(height: 10,),
            Text("Shahzain Ahmed 5th Column")],
            
          ),)
      ),
    );
  }
}
```
Output:   

![image](https://user-images.githubusercontent.com/59369881/157589724-e6acc458-8ce8-487b-88a9-0f2a09d58eb8.png)

## Row
```
Scaffold(
            body: Row(
            children: const [Text("1st Row"), 
            SizedBox(width: 10,),
            Text("2nd Row"),
             SizedBox(width: 10,),
            Text("3rd Row"),
             SizedBox(width: 10,),
            Text("4th Row"),
             SizedBox(width: 10,),
            Text("5th Row")],
            
          ),)
```
Output:  

![image](https://user-images.githubusercontent.com/59369881/157590534-aa5bedeb-e8f4-4227-b936-2c0ae66e99bc.png)

## Properties of Row
### mainAxisAlignment (left to write)
### center
```
Scaffold(
            body: Row(
              mainAxisAlignment: MainAxisAlignment.center,
            children: const [Text("1st Row"), 
           Text("2nd Row"),
           Text("3rd Row"),]
            
            
          ),)
```
Output:

![image](https://user-images.githubusercontent.com/59369881/157591149-0daa65bf-da72-4825-95fa-f38a5e43d071.png)

### start
`mainAxisAlignment: MainAxisAlignment.start`

Output:  

![image](https://user-images.githubusercontent.com/59369881/157592087-33b9c797-1461-4b53-b958-d115ce9a0b96.png)

### end
`mainAxisAlignment: MainAxisAlignment.end`

Output:

![image](https://user-images.githubusercontent.com/59369881/157591267-affc6920-3312-46e8-9f37-80fc325413dd.png)

### spaceAround
`mainAxisAlignment: MainAxisAlignment.spaceAround`

Output:

![image](https://user-images.githubusercontent.com/59369881/157591396-5ffcd4d7-d0c9-423e-8d9a-097bc241eb2d.png)

### spaceBetween
`mainAxisAlignment: MainAxisAlignment.spaceBetween`  

Output:  

![image](https://user-images.githubusercontent.com/59369881/157591764-1e60df1c-f18d-4fe8-8fbf-fddfc169880d.png)

### spaceEvenly
`mainAxisAlignment: MainAxisAlignment.spaceEvenly`

Output:  

![image](https://user-images.githubusercontent.com/59369881/157591992-b4402028-0b72-41a7-9048-8421f2c03452.png)

## crossAxisAlignment (top to bottom)
### baseline

## Properties of Column
### mainAxisAlignment (top to bottom)

### crossAxisAlignment (left to write)

## Scrollable View
`body: SingleChildScrollView()`
```
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
          body: SingleChildScrollView(
            child: Center(
                  child: Column(
            children: [
              Container(
                height: 100,
                width: 100,
                color: Colors.pink,
              ),
              SizedBox(
                height: 30,
              ),
              Container(
                height: 100,
                width: 100,
                color: Colors.deepPurple,
              ),SizedBox(
                height: 30,),
              Container(
                height: 100,
                width: 100,
                color: Colors.grey[400],
              ),SizedBox(
                height: 30,),
                Container(
                height: 100,
                width: 100,
                color: Colors.blueGrey,
              ),SizedBox(
                height: 30,),
                Container(
                height: 100,
                width: 100,
                color: Colors.yellow,
              ),SizedBox(
                height: 30,),
                Container(
                height: 100,
                width: 100,
                color: Colors.deepOrange,
              ),SizedBox(
                height: 30,),
             
            ],
                  ),
                ),
          )),
    );
  }
}
```
Output:

![image](https://user-images.githubusercontent.com/59369881/157607669-365c86d1-7412-4ea8-a8b3-7b4328d48217.png)

## AppBar()
```
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
        debugShowCheckedModeBanner: false,
        home: Scaffold(
          appBar: AppBar(
            title: Center(child: Text("Login Page")),
          ),
        ));
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/157613518-60c582a8-0f7c-4fd7-982f-84e25e9802dd.png)

## Text Field
```
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
        debugShowCheckedModeBanner: false,
        home: Scaffold(
          appBar: AppBar(
            title: Center(child: Text("Login Page")),
          ), body: Column(
            children: [
              TextField(),
            ],
          ),
        ));
  }
}
```
Output:  

![image](https://user-images.githubusercontent.com/59369881/157703809-ff67c5b1-a2ad-4d67-b778-6ad93f716d14.png)

## Text Field with Simple Decoration of Border
```
TextField(
  decoration: InputDecoration(
    border: OutlineInputBorder(),
    hintText: 'Enter a search term',
  ),
),
```
Output:   

![image](https://user-images.githubusercontent.com/59369881/157706193-3f93edf3-03af-4efa-a9db-4e266357b581.png)

## Login Page with Elevated Button
```
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
        debugShowCheckedModeBanner: false,
        home: Scaffold(
          appBar: AppBar(
            title: Center(child: Text("Shahzain's Login Page")),
          ),
          body: Center(
            child: Column(
              // mainAxisAlignment: MainAxisAlignment.spaceAround,
              children: [
                SizedBox(
                  height: 30,
                ),
                Container(
                  width: 200,
                  child: TextField(
                    decoration: InputDecoration(
                        border: OutlineInputBorder(), hintText: "First name"),
                  ),
                ),
                SizedBox(height: 20),
                Container(
                  width: 200,
                  child: TextField(
                    decoration: InputDecoration(
                        border: OutlineInputBorder(), hintText: "Last name"),
                  ),
                ),
                SizedBox(height: 20),
                ElevatedButton(onPressed: () {}, child: Text("Click to Login"))
              ],
            ),
          ),
        ));
  }
}
```
Output:  

![image](https://user-images.githubusercontent.com/59369881/157722147-b4a20217-c860-46c2-87c0-c69321fc7bd5.png)

## StatelessWidget
**It is a class, where on screen, no changing is being done and no action is being performed. It remains static during runtime.** 

## StatefulWidget
**It is a class, where on screen, any changing is being done during runtime.**

## EdgeInsets
**It is a class, which tells us the edges of any box/container (i.e. left edge, right edge, bottom edge, top edge)**

## Margin
**Spacing outside the container.**
`margin: EdgeInsets.only(top: 30)`

## Padding
**Spacing inside the container.**
`padding: EdgeInsets.only(left: 20, top: 30)`

## Decoration
**If you are defining decoration, then must write** `color:Colors.yellow` **inside the decoration box, else it will give an error.**
```
decoration: BoxDecoration(
              color: Colors.yellow,
              borderRadius: BorderRadius.circular(30),
          )
```

## Align
**It is used to align, e.g. bottomRight, bottomLeft, topRight, topLeft**  

`Align(alignment: Alignment.bottomRight)`

## Align, Margin, Padding, Decoration (all together, 2 files linked - main.dart and home.dart)

### main.dart
```
import 'package:firstproject/home.dart';
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

// Stateless Class
class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: Home(),
      ),
    );
  }
}
```
### home.dart
```
import 'package:flutter/material.dart';

// Stateful Class
class Home extends StatefulWidget {
  @override
  State<Home> createState() => _HomeState();
}

class _HomeState extends State<Home> {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Align(
          alignment: Alignment.bottomRight,
          child: Container(
            margin: EdgeInsets.only(top: 30),
            padding: EdgeInsets.only(left: 20, top: 30),
            child: Center(child: Text("Box Decoration")),
            width: 200,
            height: 200,
            decoration: BoxDecoration(
              color: Colors.yellow,
              borderRadius: BorderRadius.circular(30),
            ),
          )),
    );
  }
}
```
Output:  

![image](https://user-images.githubusercontent.com/59369881/157735673-108f295a-eb06-4dd8-9ad9-026a63473d7f.png)

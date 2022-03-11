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
- Login Page with ElevatedButton
- StatelessWidget and StatefulWidget Classes
- EdgeInsets
- Margin and Padding
- Align
- Decoration
- Linking files together
- Gradient
- CircleAvatar
- Images in CircleAvatar
- - NetworkImage and AssetImage
- Stack
- Posiitoned
- MediaQuery

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

## Gradient
### LinearGradient
```
 decoration: BoxDecoration(
              gradient: LinearGradient(colors: [
              Colors.yellow, Colors.red,
          ]),
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/157809167-fe851733-ed52-4dd0-a109-5869017dc486.png)

### RadialGradient

```
 decoration: BoxDecoration(
              gradient: RadialGradient(colors: [
              Colors.yellow, Colors.red,
          ]),
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/157809735-0e5512b3-d7cf-488f-a27c-08155b45e142.png)

## Text Styling
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
      body: Center(
        child: Text("Hello Flutter", style: TextStyle(color: Colors.blue, fontSize: 30, fontWeight: FontWeight.bold))
    ));
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/157855757-216a9c0e-34bf-435c-9d32-fef9a0c1f94d.png)

## CircleAvatar()
**It gives us radius (size) and gives a rounded form to (a corner or edge).**

```
return Scaffold(
     body: CircleAvatar(
       radius: 100,
       backgroundColor: Colors.blue,
     ),
      );
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/157857991-c3748f5b-35e5-472b-886c-57e96ad055bc.png)

## Images in CircleAvatar()
### 1) NetworkImage(): Provide URL/Link in this to make the image appear.

```
return Scaffold(
        body: Center(
      child: CircleAvatar(
        radius: 200,
        backgroundImage: NetworkImage(
            "https://logowik.com/content/uploads/images/flutter5786.jpg"),
      ),
    ));
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/157860223-6c079df5-1823-47ac-b1f6-397bf014c44f.png)


### 2) AssetImage(): First download the image, then put it in your Flutter Project's folder, then use it.
```
 return Scaffold(
        body: Center(
      child: CircleAvatar(
        radius: 200,
        backgroundImage: AssetImage("assets/flutter.jpg"),
      ),
    ));
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/157862002-1f5df50d-3164-4e74-a9e3-874176c2afe7.png)

## Stack()
**It is a widget, which is children, meaning it can take many containers or other things at once.**

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
      body: Stack(
        children: [
          Align(
              alignment: Alignment.bottomLeft,
              child: Container(
                color: Colors.teal,
                height: 100,
                width: 100,
              )),
          Positioned(
            left: 20,
            top: 20,
            child: Container(
              color: Colors.black,
              height: 100,
              width: 100,
            ),
          ),
          Align(
            alignment: Alignment.bottomRight,
            child: Container(
              color: Colors.blue,
              height: 100,
              width: 100,
            ),
          ),
          Align(
            alignment: Alignment.topLeft,
            child: Container(
              color: Colors.purple,
              height: 100,
              width: 100,
            ),
          ),
          Align(
            alignment: Alignment.topRight,
            child: Container(
              color: Colors.yellow,
              height: 100,
              width: 100,
            ),
          ),
        ],
      ),
    );
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/157864694-b4db7082-5d09-4609-af37-c4ab1b9ea454.png)

## Positioned()
**It is a widget, which is used to change the positions from top, bottom, left, and right.**

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
      body: Stack(
        children: [
          Align(
              alignment: Alignment.topLeft,
              child: Container(
                color: Colors.teal,
                height: 100,
                width: 100,
              )),
          Positioned(
            left: 50,
            top: 50,
            child: Container(
              color: Colors.red,
              height: 100,
              width: 100,
            ),
          ),
          Align(
            alignment: Alignment.topRight,
            child: Container(
              color: Colors.blue,
              height: 100,
              width: 100,
            ),
          ),
          Align(
            alignment: Alignment.bottomLeft,
            child: Container(
              color: Colors.purple,
              height: 100,
              width: 100,
            ),
          ),
          Align(
            alignment: Alignment.bottomRight,
            child: Container(
              color: Colors.yellow,
              height: 100,
              width: 100,
            ),
          ),
        ],
      ),
    );
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/157866976-22bd31f1-4b01-4f4a-b42a-7bed44c9d165.png)

## MediaQuery()
**It is used for making the layout responsive, because every device has a different layout, if we use height and widths directly, it will not be responsive.**

### For Height : 
`MediaQuery.of(context).size.height`  
**by default height of MediaQuery is set to 100%**  
**To make it 50%, multiply height with 0.5, just like: `MediaQuery.of(context).size.height*0.5`**

### For Width :
`MediaQuery.of(context).size.width`  
**by default width of MediaQuery is set to 100%**  
**To make it 50%, multiply height with 0.5, just like: `MediaQuery.of(context).size.width*0.5`**

```
return Scaffold(
      body: Container(
        color: Colors.pink,
        height: MediaQuery.of(context).size.height*0.5,
        width: MediaQuery.of(context).size.width*0.5,
      )
    );
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/157873377-a647b784-7073-4c73-a661-a474d596c4bc.png)

## Navigator
### home.dart
```
import 'package:firstproject/app.dart';
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
        body: Center(
      child: ElevatedButton(
          onPressed: () {
            Navigator.push(context, MaterialPageRoute(builder: (context) => App()));
            },
          child: Text("Button"))
    ));
  }
}
```

### app.dart
```
import 'package:flutter/material.dart';

class App extends StatefulWidget {
  const App({ Key? key }) : super(key: key);

  @override
  State<App> createState() => _AppState();
}

class _AppState extends State<App> {
  @override
  Widget build(BuildContext context) {
    return Center(
      child: Scaffold(
        body: Text("App Page", style: TextStyle(fontSize: 30),)
        
      ),
    );
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/157877897-c316ebb9-113a-406a-84d9-8d708b4bafe9.png)

![image](https://user-images.githubusercontent.com/59369881/157877997-704cab65-30b7-4e07-b3c3-a18461206888.png)


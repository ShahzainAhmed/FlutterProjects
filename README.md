# Learning Flutter 
## Started on 10th March 2022
# Topics Covered
**Basic Widgets for User Interface in Flutter**
- Child vs Children
- Flutter Tooling Build Modes
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
- Positioned
- MediaQuery
- Navigator
- ListTile
- - leading
- - trailing
- Widget
- ListView
- - ListView.builder
- GridView
- Drawer
- DefaultTabController
- TabBar
- setState
- Counter Application (using setState)
- Calculator Application
- Todo Application
- http and https
- authority and unencodedPath
- async and await
- FutureBuilder
- API Integration
- Firebase (backend - in progress)
- sync and async

## Child vs Children
**Child means one widget, children means more than one widget.**

## Flutter Tooling Supports 3 Build Modes

- **Debug** 
- **Release**
- **Profile**.

**Debug mode is used to debug the application on the physical device, emulator, or simulator. Here, assertions, service extensions are enabled. Then compilation is optimized for fast deployment.**

**Release mode is enabled to deploy your app. Here, assertions, service extension and debugging are disabled. Finally, the compilation is optimized for fast startup, execution, and package sizes.**

**Profile mode is used to analyze the performance of your app. Here, some extensions and tracing are enabled.**

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
        body: Column(
          children: [
            Text("App Page", style: TextStyle(fontSize: 30),),
            ElevatedButton(onPressed: (){
              Navigator.pop(context);
            }, child: Text("Back"))
          ],
        )
        
      ),
    );
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/157877897-c316ebb9-113a-406a-84d9-8d708b4bafe9.png)

![image](https://user-images.githubusercontent.com/59369881/157879660-e5024131-c03f-4dbb-93b3-e0861c34f920.png)

## ListTile()

### leading
**A widget to be displayed before the title**

### trailing
**A widget to be displayed after the title**

```
// import 'package:firstproject/app.dart';
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
        backgroundColor: Colors.white,
        body: Column(
          children: [
            ListTile(
              leading: CircleAvatar(
                backgroundImage: AssetImage("assets/shahzain.jpg"),
                radius: 20,
              ),
              title: Text(
                "Shahzain Ahmed",
                style: TextStyle(fontWeight: FontWeight.bold),
              ),
              subtitle: Text("shahzainahmed57@gmail.com"),
              trailing: Column(
                mainAxisAlignment: MainAxisAlignment.spaceAround,
                children: [
                  Text("4.25 PM"),
                  CircleAvatar(
                    backgroundColor: Colors.green,
                    radius: 10,
                  ),
                ],
              ),
            )
          ],
        ));
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/157889203-63f5def8-47a4-413d-bf41-a7b17eb58a0b.png)

## Widget
**To create a widget, go completely out of the class, and then write** `widget widgetName(){}` 

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
        backgroundColor: Colors.white,
        body: Column(
          children: [
            myWidget(), // calling our own custom widget
            myWidget(), // calling our own custom widget
            myWidget(), // calling our own custom widget
          ],
        ));
  }
}

Widget myWidget() {
  return ListTile(
    leading: CircleAvatar(
      backgroundImage: AssetImage("assets/shahzain.jpg"),
      radius: 20,
    ),
    title: Text(
      "Shahzain Ahmed",
      style: TextStyle(fontWeight: FontWeight.bold),
    ),
    subtitle: Text("shahzainahmed57@gmail.com"),
    trailing: Column(
      mainAxisAlignment: MainAxisAlignment.spaceAround,
      children: [
        Text("4.25 PM"),
        CircleAvatar(
          backgroundColor: Colors.green,
          radius: 10,
          child: Text("86"), // to write the number of messages inside the green bubble 
        ),
      ],
    ),
  );
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/157890885-344f32eb-f906-4fd6-8246-0a8ee5207c0e.png)

### Parameter Widget (Calling Widget with Custom Values)

```
// import 'package:firstproject/app.dart';
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
        body: ListView(
      children: [
        abc("Shahzain Ahmed"),
        abc("I am Flutter Developer!!"),
        abc("18CS86")
      ],
    ));
  }
}

Widget abc(var name) {
  return Container(
    color: Colors.amber,
    height: 100,
    child: Row(
      children: [
        Container(
          color: Colors.teal,
          height: 95,
          width: 90,
        ),
        Padding(
          padding: const EdgeInsets.only(left: 10),
          child: Column(
            mainAxisAlignment: MainAxisAlignment.spaceBetween,
            children: [
              Text(name),
            ],
          ),
        )
      ],
    ),
  );
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/158000426-fb95ba21-2414-477f-8d90-cc1e0b4fb082.png)

## ListView()

**One widget per line (horizontally), goes top to bottom, it will only take one item of 100% width at one time, then the next item below that, then third below that etc.**

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
        body: ListView(
      children: [
        Container(
          color: Colors.amber,
          height: 100,
          child: Row(
            children: [
              Container(
                color: Colors.teal,
                height: 95,
                width: 90,
              ),
              Padding(
                padding: const EdgeInsets.only(left: 10),
                child: Column(
                  mainAxisAlignment: MainAxisAlignment.spaceBetween,
                  children: [
                    Text("Shahzain Ahmed"),
                    Row(
                      children: [
                        Text("Shahzain Ahmed"),
                        Text("Shahzain Ahmed"),
                      ],
                      
                    ),
                    Icon(Icons.notifications),
                    Icon(Icons.call),
                    Text("Shahzain Ahmed"),
                    
                  ],
                ),
              )
            ],
          ),
          
        )
      ],
    ));
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/157999857-0d76ec7d-d768-4061-8c4d-d36447e5ee1a.png)

## ListView.builder()

```
import 'package:flutter/material.dart';

// Stateful Class
class Home extends StatefulWidget {
  @override
  State<Home> createState() => _HomeState();
}

class _HomeState extends State<Home> {
  var lst = ["Shahzain Ahmed", "Murtaza Bozdar", "Raza Rehman"];
  var age = ["86", "30", "120"];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
        body: ListView.builder(
      itemCount: lst.length,
      itemBuilder: (context, index) {
        return ListTile(
          title: Text(lst[index]),
          subtitle: Text(age[index]),
        );
      },
    ));
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/158001365-7ad51e1d-82a4-430e-a96f-8fcbb8ed446b.png)

## ListView.builder (with images)

```
import 'package:flutter/material.dart';

// Stateful Class
class Home extends StatefulWidget {
  @override
  State<Home> createState() => _HomeState();
}

class _HomeState extends State<Home> {

  var lst = [
    "https://www.pngitem.com/pimgs/m/616-6164295_programming-language-logos-png-transparent-png.png",
    "https://miro.medium.com/max/800/1*wcEYa9AjnMZxXAau2iuhYw.png",
    "https://cdn.iconscout.com/icon-pack/preview-mockup/programming-language-logos-24701.png"
  ];

  var age = ["86", "30", "120"];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
        body: ListView.builder(
      itemCount: lst
          .length, // can write age.length also, only if the list is of same quantity
      itemBuilder: (context, index) {
        return Container(
          height: 200,
          width: 200,
          child: Image.network(lst[index]),
        );
      },
    ));
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/158010262-b87a50f1-aa9e-4b10-aef1-fa076065004f.png)

## GridView()

**We can give 2 or 3 widgets in one single line horizontally, it depends how many widgets do we want to give.**  

```
import 'package:flutter/material.dart';

// Stateful Class
class Home extends StatefulWidget {
  @override
  State<Home> createState() => _HomeState();
}

class _HomeState extends State<Home> {
  var lst = [
    "Shahzain Ahmed",
    "Flutter",
    "Mobile App Developer",
    "Computer Systems"
  ];

  var age = ["86", "30", "120"];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
        body: GridView.count(
      crossAxisCount: 2, // in one line, taking 2 widgets only
      crossAxisSpacing: 10, // left to right spacing (x-axis)
      mainAxisSpacing: 10, // top to bottom spacing (y-axis)

      children: List.generate(lst.length, (index) {
        return Padding(
          padding: const EdgeInsets.all(8.0),
          child: Container(
            color: Colors.blue,
            child: Center(child: Text(lst[index])),
          ),
        );
      }),
    ));
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/158014182-e352e398-30f4-4913-86d9-9b0f817d33a3.png)

## ListView() vs GridView()

**The main difference between ListView and GridView is how it lays out its child. With ListView you are laying your children one by one either vertically or horizontally only. With GridView, its a combination of both. It lays its children horizontally first**  

![image](https://user-images.githubusercontent.com/59369881/158013082-69f264a6-910f-4b08-8b20-7e8b15307d5e.png)

## Drawer 

**It takes child (one widget)**

```
import 'package:flutter/material.dart';

// Stateful Class
class Home extends StatefulWidget {
  @override
  State<Home> createState() => _HomeState();
}

class _HomeState extends State<Home> {
  var lst = [
    "Shahzain Ahmed",
    "Flutter",
    "Mobile App Developer",
    "Computer Systems"
  ];

  var age = ["86", "30", "120"];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text("Drawer by Shahzain Ahmed"),
      ),
      drawer: Drawer(
        child: ListView(
          children: [
            DrawerHeader(                   // adjusts height and width itself
                child: Container(
              color: Colors.amber,
              child: Text("HEADER"),
            )),
            ListTile(
              title: Text("Flutter"),
            ),
            ListTile(
              title: Text("App"),
            ),
            ListTile(
              title: Text("Developer"),
            )
            
          ],
        ),
      ),
    );
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/158014691-f214df38-80e1-4294-b466-7ccb286e4fc2.png)

![image](https://user-images.githubusercontent.com/59369881/158014706-f75769ff-97e1-4fac-8600-a9fb545551e6.png)

### Drawer (with images)

```
 DrawerHeader(                   // adjusts height and width itself
                child: Container(
              // color: Colors.amber,
              child: Image.network("https://wallpaperaccess.com/full/3792708.jpg"),
            )),
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/158026004-54197851-07e2-4173-ab8f-60ea0fe20c8c.png)

## DefaultTabController()

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
    return DefaultTabController(
      length: 2,
      child: Scaffold(
        appBar: AppBar(
          title: TabBar(tabs: [
            Tab(
              child: Text("Login"),
            ),
            Tab(
              child: Text("Register"),
            ),
          ]),
        ),
      ),
    );
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/158027168-8c8002fb-055d-40f0-ac5c-66f05609a569.png)

## TabBar()
**It comes in AppBar, and takes tabs:[]**

### home.dart

```
// import 'package:firstproject/app.dart';
import 'package:firstproject/login.dart';
import 'package:firstproject/register.dart';
import 'package:flutter/material.dart';

// Stateful Class
class Home extends StatefulWidget {
  @override
  State<Home> createState() => _HomeState();
}

class _HomeState extends State<Home> {
  @override
  Widget build(BuildContext context) {
    return DefaultTabController(
      length: 2, // 1) login (2) register
      child: Scaffold(
        appBar: AppBar(
          title: Text("Good Morning, Shahzain Ahmed!"),
          bottom: TabBar(
              unselectedLabelColor: Colors.black,
              labelColor: Colors.white,
              indicatorColor: Colors.amber,
              tabs: [
                Tab(
                  child: Text(
                    "Login",
                    style: TextStyle(fontWeight: FontWeight.bold),
                  ),
                ),
                Tab(
                  child: Text(
                    "Register",
                    style: TextStyle(fontWeight: FontWeight.bold),
                  ),
                ),
              ]),
        ),
        body: TabBarView(children: [
          Login(),
          Register(),
        ]),
      ),
    );
  }
}
```

### register.dart

```
// import 'package:firstproject/app.dart';
import 'package:flutter/material.dart';

// Stateful Class
class Register extends StatefulWidget {
  @override
  State<Register> createState() => _RegisterState();
}

class _RegisterState extends State<Register> {
  @override
  Widget build(BuildContext context) {
    return Container(
      child: Center(
          child: Text(
        "Register",
        style: TextStyle(fontWeight: FontWeight.bold, color: Colors.blue),
      )),
    );
  }
}
```

### login.dart

```
import 'package:flutter/material.dart';

class Login extends StatefulWidget {
  @override
  State<Login> createState() => LoginState();
}

class LoginState extends State<Login> {
  @override
  Widget build(BuildContext context) {
    return Container(
      child: Center(
          child: Text(
        "Login",
        style: TextStyle(fontWeight: FontWeight.bold, color: Colors.blue),
      )),
    );
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/158041507-9f1013ab-719d-4fdf-adc7-e2924d09809b.png)  

![image](https://user-images.githubusercontent.com/59369881/158041515-2d73aaec-b30e-4662-8d2f-da30b937d198.png)

## setState()

**Whenever we want any changing when the action is performed for example on a button, then we use setState(). Everthing which includes logic, e.g. Calculator, will be done using setState().**

### home.dart

```
import 'package:flutter/material.dart';

// Stateful Class
class Home extends StatefulWidget {
  @override
  State<Home> createState() => _HomeState();
}

class _HomeState extends State<Home> {
  var text = " ";

  one() {
    setState(() {
      text = "1";
    });
  }

  two() {
    setState(() {
      text = "2";
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text("Text: $text" , style: TextStyle(fontWeight: FontWeight.bold),),
            SizedBox(
              height: 20,
            ),
            ElevatedButton(onPressed: one, child: Text("Make 1")),
            SizedBox(
              height: 20,
            ),
            ElevatedButton(onPressed: two, child: Text("Make 2")),
          ],
        ),
      ),
    );
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/158042072-cc230c42-4455-4664-ba3f-a8cdc042ba21.png)  

![image](https://user-images.githubusercontent.com/59369881/158042085-8f6d0c94-f2a4-46c1-9d36-18ad4856895a.png)  


## Counter Application using setState()

```
import 'package:flutter/material.dart';

// Stateful Class
class Home extends StatefulWidget {
  @override
  State<Home> createState() => _HomeState();
}

class _HomeState extends State<Home> {
  var text = 1;

  one() {
    setState(() {
      text += 1; // text = text + 1;
    });
  }

  two() {
    setState(() {
      text = 0;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text("Shahzain Ahmed's", style: TextStyle(fontWeight: FontWeight.bold, fontSize: 20),),
            SizedBox(height: 20,),
            Text("Counter Application", style: TextStyle(fontWeight: FontWeight.bold, fontSize: 20),),
            SizedBox(height: 20,),
            Text("$text" , style: TextStyle(fontWeight: FontWeight.bold, fontSize: 30),),
            SizedBox(
              height: 20,
            ),
             ElevatedButton(onPressed: one, child: Text("Add +1", style: TextStyle(fontSize: 20),)),
              SizedBox(
              height: 20,
            ),
             ElevatedButton(onPressed: two, child: Text("Clear", style: TextStyle(fontSize: 20),)),
            
          ],
        ),
      ),
    );
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/158042730-9023b933-9a2c-4849-ac11-ca289b1a6bea.png)

## List dynamic

 **This means it can have Strings as well as integers.** 

## ListView() + GridView() (scrollable)
```
import 'package:flutter/material.dart';

class Home extends StatefulWidget {
  @override
  State<Home> createState() => _HomeState();
}

class _HomeState extends State<Home> {
  List<dynamic> lst = [1, 2, 3, 4, 5, 6, 7, 8];     // List<dynamic> means you can take String, as well as integers in list, e.g. [1,'2',3,"4"]

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: SingleChildScrollView(
        child: Column(
          // in column we don't define length, we can take multiple items in column
          children: [
            Container(
              child: Column(
                children: [
                  Container(
                    height: 200,
                    width: 200,
                    color: Colors.amber,
                    margin: EdgeInsets.only(top: 10),
                  ),
                  Container(
                    height: 200,
                    width: 200,
                    color: Colors.blue,
                    margin: EdgeInsets.only(top: 10),
                  ),
                  Container(
                    height: 200,
                    width: 200,
                    color: Colors.red,
                    margin: EdgeInsets.only(top: 10),
                  ),
                  Container(
                    height: 200,
                    width: 200,
                    color: Colors.green,
                    margin: EdgeInsets.only(top: 10),
                  ),
                  Container(
                    height: 200,
                    width: 200,
                    color: Colors.amber,
                    margin: EdgeInsets.only(top: 10),
                  ),
                  Container(
                    height: 200,
                    width: 200,
                    color: Colors.purple,
                    margin: EdgeInsets.only(top: 10),
                  ),
                  Container(
                    height: 200,
                    width: 200,
                    color: Colors.pink,
                    margin: EdgeInsets.only(top: 10),
                  ),
                  Container(
                    height: 200,
                    width: 200,
                    color: Colors.teal,
                    margin: EdgeInsets.only(top: 10),
                  ),
                  Container(
                    height: 200,
                    width: 200,
                    color: Colors.cyan,
                    margin: EdgeInsets.only(top: 10),
                  ),
                  Container(
                    height: 200,
                    width: 200,
                    color: Colors.lightBlue,
                    margin: EdgeInsets.only(top: 10),
                  ),
                  GridView.count(
                      physics:
                          NeverScrollableScrollPhysics(), // to enable scrolling
                      shrinkWrap: true,
                      crossAxisCount: 2,
                      crossAxisSpacing: 20,
                      mainAxisSpacing: 20,
                      children: List.generate(lst.length, (index) {
                        return Container(
                          color: Colors.amber,
                          child: Center(
                            child: Text("${lst[index]}"),
                          ),
                        );
                      }))
                ],
              ),
            ),
          ],
        ),
      ),
    );
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/158050697-3f0acb25-ae70-4de4-86f4-ba0cae466caa.png)

![image](https://user-images.githubusercontent.com/59369881/158050704-9f027558-bd40-4c11-93ad-accce4944132.png)


**If from one side it's scrolling, but from other side it is not, then we will use ``physics:NeverScrollableScrollPhysics() // to enable scrolling `` 

## Calculator Application

### main.dart

```
import 'package:flutter/material.dart';
import 'home.dart';

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
        body: Calculator(),
      ),
    );
  }
}
```

### home.dart
```
import 'package:flutter/material.dart';
import 'package:math_expressions/math_expressions.dart';

class Calculator extends StatefulWidget {
  @override
  State<Calculator> createState() => CalculatorState();
}

class CalculatorState extends State<Calculator> {
  var result = "";

  Widget button(var textt) {
    // parameter button/widget
    return ElevatedButton(
        onPressed: () {
          setState(() {
            result += textt;
          });
        },
        child: Text(textt));
  }

  clearr() {
    setState(() {
      result = "";
    });
  }

  output() {
    Parser p =
        Parser(); // to change anything from one to another, like from String to int, parser is used.
    Expression exp = p.parse(result);
    ContextModel cm = ContextModel();
    double eval = exp.evaluate(EvaluationType.REAL, cm);
    setState(() {
      result = eval.toString();
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text(
              result,
              style: TextStyle(fontWeight: FontWeight.bold, fontSize: 50),
            ),
            Row(
              mainAxisAlignment: MainAxisAlignment.spaceAround,
              children: [
                button("1"),
                button("2"),
                button("3"),
                button("4"),
              ],
            ),
            Row(
              mainAxisAlignment: MainAxisAlignment.spaceAround,
              children: [
                button("5"),
                button("6"),
                button("7"),
                button("8"),
              ],
            ),
            Row(
              mainAxisAlignment: MainAxisAlignment.spaceAround,
              children: [
                button("9"),
                button("0"),
                button("+"),
                button("-"),
              ],
            ),
            Row(
              mainAxisAlignment: MainAxisAlignment.spaceAround,
              children: [
                button("*"),
                button("/"),
                ElevatedButton(onPressed: clearr, child: Text("Clear")),
                ElevatedButton(onPressed: output, child: Text("=")),
              ],
            )
          ],
        ),
      ),
    );
  }
}
```

Output:  

![image](https://user-images.githubusercontent.com/59369881/158055820-db1f20da-b881-46d6-9705-3d84af6b5470.png)  

![image](https://user-images.githubusercontent.com/59369881/158055833-7552a210-2cc3-415f-a191-40fdb4413bca.png)

## GestureDetector()

**to make anything like text/icons clickable, use GestureDetector**

## Todo Application

### main.dart

```
import 'package:flutter/material.dart';
import 'home.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      home: Scaffold(
        body: Todo(),
      ),
    );
  }
}
```

### todo.dart

```
import 'package:flutter/material.dart';

class Todo extends StatefulWidget {
  @override
  State<Todo> createState() => _TodoState();
}

class _TodoState extends State<Todo> {
  var output = " ";
  List<dynamic> lst = [1, 2, 3];

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: ListView.builder(
        itemCount: lst.length,
        itemBuilder: (context, index) {
          return Container(
            height: 50,
            color: Colors.amber[300],
            margin: EdgeInsets.only(top: 15),
            child: ListTile(
              title: Text("${lst[index]}"),
              trailing: Container(
                width: 50,
                child: Row(
                  children: [
                    GestureDetector(
                      // to make anything like text/icons clickable, use GestureDetector
                      child: Icon(Icons.edit),
                      onTap: () {
                        showDialog(
                            context: context,
                            builder: (context) {
                              return AlertDialog(
                                title: Text("Edit Item"),
                                content: TextField(
                                  onChanged: (value) {
                                    output = value;
                                  },
                                ),
                                actions: [
                                  ElevatedButton(
                                      onPressed: () {
                                        setState(() {
                                          lst.replaceRange(index, index + 1, {
                                            output
                                          }); // using curly braces {output} to use dynamic
                                        });
                                        Navigator.of(context).pop();
                                      },
                                      child: Text("Edit"))
                                ],
                              );
                            });
                      },
                    ),
                    GestureDetector(
                        onTap: () {
                          setState(() {
                            lst.removeAt(index);
                          });
                        },
                        child: Icon(Icons.delete)),
                  ],
                ),
              ),
            ),
          );
        },
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: () {
          showDialog(
              context: context,
              builder: (context) {
                return AlertDialog(
                  title: Text("Add Item"),
                  content: TextField(
                    onChanged: (value) {
                      output = value;
                    },
                  ),
                  actions: [
                    ElevatedButton(
                        onPressed: () {
                          setState(() {
                            lst.add(output);
                          });
                          Navigator.of(context).pop();
                        },
                        child: Text("Add"))
                  ],
                );
              });
        },
        child: Text("Add"),
      ),
    );
  }
}
```

Output:   

![image](https://user-images.githubusercontent.com/59369881/158091993-07088750-6023-47b4-bbeb-47ef0a8fcbb0.png)  

![image](https://user-images.githubusercontent.com/59369881/158092041-6b0f0ea0-4397-42f3-b528-ee4248893ae4.png)

![image](https://user-images.githubusercontent.com/59369881/158092078-95c883f6-9825-4850-b544-be50c7dd1d9c.png)

![image](https://user-images.githubusercontent.com/59369881/158092114-2d47a401-c5ff-446c-bcc6-7cdb6ff4f9e2.png)

## http and https
**When it's http, write `(Uri.http(authority, unencodedPath));`, but if it's https, then write `(Uri.https(authority, unencodedPath));`**

## authority and unencodedPath
### authority
**In a website URL, the address before ( / backslash) like `shahzainahmed.com/users`, in this the authority is `shahzainahmed.com` that is called as authority.**

### unencodedPath
**In a website URL, the text which comes after the .com/(backslash) like `shahzainahmed.com/users`, in this `users` is called unencodedPath. **

**Example:**  
By default: **`http.get(Uri.https(authority, unencodedPath))`**  
After adding the authority and unencodedPath **`http.get(Uri.https("jsonplaceholder.typicode.com", "users"));`**

## async and await
### async
**This is a function which stops the entire function till we receive the entire data from the website.**

### await
**And when we use async, to get the data from the link, then we use await, either our data has been completely received or rejected, for that to see, we use await.**  

**Example:**
```
getUser() async {
  var response = await http.get(Uri.https("jsonplaceholder.typicode.com/", "users"));

}
```

## FutureBuilder()
**FutureBuilder is a widget that uses the result of a Future to build itself. For any data which is coming from API / internet, we use FutureBuilder()**

## API Integration

### main.dart

```
import 'package:flutter/material.dart';
import 'api.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      title: "Flutter Demo",
      home: Scaffold(
        body: Api(),
      ),
    );
  }
}
```

### api.dart

```
import 'dart:convert';
import 'package:flutter/material.dart';
import 'package:http/http.dart' as http; // as = alias

class Api extends StatefulWidget {
  @override
  State<Api> createState() => _ApiState();
}

class _ApiState extends State<Api> {
// making a function to get the data
  getUser() async {
    var users = [];
    var response =
        await http.get(Uri.https("jsonplaceholder.typicode.com", "users"));
    var jsonData = jsonDecode(response.body);

    // using for loop to receive data based on indexes
    for (var i in jsonData) {
      UserModel user = UserModel(i['name'], i['username'], i['company']['name']); 
      // we have written i[company][name] because we want companie's name to be in subtitle
      users.add(user);
    }

    return users;
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
        body: FutureBuilder(
      future: getUser(),
      builder: (context, AsyncSnapshot snapshot) {
        if (snapshot.data == null) {
          return Container(
            child: Text("Nothing in API"),
          );
        } else
          return ListView.builder(
              itemCount: snapshot.data.length,
              itemBuilder: (context, i) {
                return ListTile(
                  title: Text(snapshot.data[i].name),
                  subtitle: Text(snapshot.data[i].company),
                );
              });
      },
    )); // we use 'snapshot' just like we use 'i' in forloop
  }
}

class UserModel {
  var name;
  var username;
  var company;

  UserModel(this.name, this.username, this.company);
}
```

**Dataset copied from https://jsonplaceholder.typicode.com/users**

Output:  

![image](https://user-images.githubusercontent.com/59369881/158139097-66bb05c1-02c4-4fcc-a8d6-af50bb093c16.png)

## Firebase

### main.dart
```
import 'package:flutter/material.dart';
import 'login.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      debugShowCheckedModeBanner: false,
      title: "Flutter Demo",
      theme: ThemeData(
        primarySwatch: Colors.blue,
      ),
      home: Register(),
      
    );
  }
}
```

### login.dart
```
import 'package:flutter/material.dart';

class Register extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Container(
        padding: const EdgeInsets.symmetric(horizontal: 10),
        child: SafeArea(
            child: Column(
          children: [
            TextFormField(
              decoration: const InputDecoration(
                labelText: 'Enter your username',
              ),
            ),
            TextFormField(
              decoration: const InputDecoration(
                labelText: 'Enter your email',
              ),
            ),
            TextFormField(
              decoration: const InputDecoration(
                labelText: 'Enter your password',
              ),
            ),
            Padding(padding: EdgeInsets.symmetric(vertical: 10)),
            ElevatedButton(onPressed: () {}, child: Text("Register"))
          ],
        )),
      ),
    );
  }
}
```

## sync and async

### sync
**it means it will stop the execution till the sync process finishes, then it will move to the next line.**

### async 
**this will not stop the process, but it will be running its own async process in backgroud, while you can move to the next line simulataneously. Just like Facebook video uploading, while the video is uploading, you can still use facebook.**

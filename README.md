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

# Properties of Row
## mainAxisAlignment (left to write)
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

# Properties of Column
## mainAxisAlignment (top to bottom)

## crossAxisAlignment (left to write)


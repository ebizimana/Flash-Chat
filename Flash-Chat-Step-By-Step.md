# Step By Step
## FireBase
### Register an account with
1. Go to [Firebase](https://firebase.google.com/)
1. create a login
1. go to the console
1. create a new project
1. Give a project a name and click continue

### Set up Firebase for Develelopment
1. click the `Add Firebase on IOS app` icon
1. Register App: copy your `bundle Identifier` paste it into your first step
1. Download config file: click to download the config file
1. copy the download file into the `Supporting Folder` in your project
1. Add Firebase SDK: Follow the instrution on how to install using CocoaPods

### Create Pods
1. Firebase, Firebase/Auth, Firebase/Database, SVProgressHUB, ChameleonFramework
1. if possible try to install them by Swift Packcge Mananger
1. if everything went well then you should be able to see your app in the [Console](https://console.firebase.google.com/project/flash-chat-6c7ed/overview)

# Files:
## Message.swift:
* Location: In the Model Folder
* Description:
* Imports:
* Properties:
* Functions: None

## AppDelegate.swift :
* Location: In the Controller Folder
* Description: Comes with apple and it starts evrytime your app lanches
* Custom Imports:
  * Firebase
* Added Properties: none
* Functions:
  * `Firebase.config()`
    * Author: Firebase
    * Action: Called
    * Purpose: To configure the firebase database in our app

## RegisterViewController.swift:
* Location: In the Controller Folder
* Description: A class to help us register users to the firebase database
* Custom Imports:
  * Firebase
* Added Properties:
  * `@IBOutlet var emailTextfield`
      * Purpose: Holds the user email
  * `@IBOutlet var passwordTextfield`
      * Purpose: Holds the user password
* Added Functions:
  * [@IBAction func registerPressed](#registerPressed)
      * Author: Swift
      * Action: Created
      * Purpose: What to do when the user presses the register Button
      * To Do's:
        * [ ] Set up a new user on our Firebase database

# Functions
## <a name="registerPressed"> </a> func registerPressed
```swift
  func registerPressed{
    // Set up a new user on our Firebase database 
    var check = 1 + 3
  }
```

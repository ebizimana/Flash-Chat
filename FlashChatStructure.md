# Step By Step

# Flow
The Flow in making the Flash Chat app.
1. [ ] [Set up the Firebase](#firebase)
1. [ ] [Set up all your pods](#pods)
1. [ ] [Finish setting up `Main.storybord`](#main)
1. [ ] [Complete all the task in Registering new users](#register)
1. [ ] Complete all the  Log in functionality
1. [ ] Complete all functionality for the Chat View

## <a name="firebase"></a> FireBase
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

## <a name ="pods"></a> Create Pods
1. Firebase, Firebase/Auth, Firebase/Database, SVProgressHUB, ChameleonFramework
1. if possible try to install them by Swift Packcge Mananger
1. if everything went well then you should be able to see your app in the [Console](https://console.firebase.google.com/project/flash-chat-6c7ed/overview)

# Files:
## <a name = "main" ></a> Main.storybord
* Location: In the View Folder
* Description: To easly and visually ceate the represatation of your app
* Custom Imports:None
* Added Properties:None
* Added Functions: None
* Changes:
  * Add a `segue`
      * Connect: Welcome view to the LogIn View
      * Impact: Use the `LogIn` Button
      * Name: `goToLogIn`
  * Chage the `passwordTextfield` to be more secure
      * Click on it and under it's properties check the `Secure Text Entry`

## Message.swift:
* Location: In the Model Folder
* Description:
* Custom Imports:
* Added Properties:
* Added Functions: None


## AppDelegate.swift :
* Location: In the Controller Folder
* Description: Comes with apple and it starts evrytime your app lanches
* Custom Imports:
  * Firebase
* Added Properties: none
* Added Functions:
  * Name: `FirebaseApp.config()`
    * Author: Firebase
    * Action: Called
    * Purpose: To configure the firebase database in our app

## WelcomeViewController.swif:
* Location:
* Description:
* Custom Imports:
* Added Properties:
* Added Functions:
  * Name:
    * Author:
    * Action:
    * Purpose:
    * To Do's
    * InHouse Functions:

## LogInViewController.swift:
* Location:
* Description:
* Custom Imports:
* Added Properties:
* Added Functions:
  * Name:
    * Author:
    * Action:
    * Purpose:
    * To Do's
    * InHouse Functions:

## <a name = "register" ></a> RegisterViewController.swift:
* Location: In the Controller Folder
* Description: A class to help us register users to the firebase database
* Custom Imports:
  * Firebase
* Added Properties:
  * Name: `@IBOutlet var emailTextfield`
      * Purpose: Holds the user email
  * Name: `@IBOutlet var passwordTextfield`
      * Purpose: Holds the user password
* Added Functions:
  * Name: [@IBAction func registerPressed](#registerPressed)
      * Author: Swift
      * Action: Created and Modified
      * Purpose: What to do when the user presses the register Button
      * To Do's:
        * [ ] Set up a new user on our Firebase database
        * [ ] Send user to the chart view
      * InHouse Functions:
          * Name: createUser
            * Author: [Firebase](https://firebase.google.com/docs/auth/ios/password-auth)
            * Action: Call and Modifiy
            * Purpose:
                * To create a user with an email and password to the Firebase database
                * To check if there was an error in registering
                * To make sure the email entered is valid
                * To report info about the created `user`

## ChatViewController.swift
* Location:
* Description:
* Custom Imports:
* Added Properties:
* Added Functions:
  * Name:
    * Author:
    * Action:
    * Purpose:
    * To Do's
    * InHouse Functions:

# Functions
## <a name="registerPressed"> </a> func registerPressed
```swift
  func registerPressed { // Swift Autofil
    Auth.auth().createUser() {  // Swift Autofil, Inclosure
      (user, error) in
      if error != nil { // There was an Error
          print (error!)
        } else {
          // Success
          print("Regestration Success")
          self.perform(withIdentifier: "goToChart", sender: self)
        }

    }
  }
```

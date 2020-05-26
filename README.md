# Flutter Template

A Template which helps to build an Flutter Application quickly. Create a new flutter project which contains all the main components that you need for developing Complete Application.

## Features: 
* Provider Architecture
* Network Layer Structure
* Navigation Service
* Dialog Service
* Shared Preference Service
* Firebase Analytics
* Firebase Crashlytics
* Firebase Remote Config
* Basic Widgets



## Setup as Default Template 
* Download the [Template](https://github.com/SandyAra/flutter_template/archive/master.zip)
* Open Flutter SDK in your System and Navigate to templates folder.

  ```
  <flutter-sdk-path>/packages/flutter_tools/templates/
  ```
* Inside templates folder you find a folder named 'app'. This 'app' folder is the default template project structure that you see when creating a new flutter project.
* Replace the app folder with above downloaded template and give same folder name as app.
* All set and ready to create new Flutter Project.
* Now create Flutter Application using the following command.

  ```
  flutter create <project_name>
  ```
  (or) Start New Flutter Project in Android Studio
* Application will created with all Main Components



## Configure Firebase Remote Config before Running Application
* Add new Project on [Firebase Console](https://console.firebase.google.com/)
* Register [iOS](https://firebase.google.com/docs/ios/setup#register-app) and [Android](https://firebase.google.com/docs/android/setup#register-app) App in Firebase. [Refer], Follow until step 3
* Add the following parameters in Remote Config

  Parameter Key: 
  ```
  app_config
  ```

  Value:
  ```
    {
      "AppName": "{{projectName}}",
      "BaseApiUrl": "https://api.url/v1/",
      "OneSignalId": "",
      "AppStoreLinks": {
        "AndroidStore": {
          "Url": "https://play.google.com/",
          "AppID": "{{androidIdentifier}}",
          "Version": "1.0.0-dev-1",
          "ReviewUrl": "https://play.google.com/",
          "ForceUpdate": false
        },
        "IosStore": {
          "Url": "https://apps.apple.com/",
          "AppID": "{{androidIdentifier}}",
          "Version": "1.0.0-dev-1",
          "ReviewUrl": "https://apps.apple.com/",
          "ForceUpdate": false
        }
      },
      "AppLinks": {
        "SupportEmail": "support@{{projectName}}.com",
        "SupportUrl": "https://www.{{projectName}}.com/contactus",
        "Privacy": "https://www.{{projectName}}.com/privacy",
        "UserAgreement": "https://www.{{projectName}}.com/useragreement",
        "ContactPhone": "9876543210"
      }
    }
  ```
 


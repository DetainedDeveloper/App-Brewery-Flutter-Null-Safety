# AppBrewery Flutter : Null Safety Guide

## Read Before Starting

- **DISCLAIMER : This repository is not an official outcome of [London AppBrewery Team](https://github.com/londonappbrewery)**

- This repository is made to help new students get through [**AppBrewery Flutter Course**](https://www.udemy.com/course/flutter-bootcamp-with-dart/)

- This repository contains notes for **only coding (project) sections** and explains what has changed and what's the difference.

- If something is not covered here, **start a discussion**, not an issue! I will try to add it then.

- Use latest versions of required **`packages`** and **`plugins`**, find them on [**pub.dev**](https://pub.dev/)

## Table of Contents

#### 1. [Terminology](#terminology)

#### 2. [Common issues and fixes](#common-issues-and-fixes)

  1. #### [Using old Flutter SDK?](#1-using-old-flutter-sdk)
  
  2. #### [Android license status unknown](#2-android-license-status-unknown)
  
  3. #### [Option to create a new package is missing](#3-option-to-create-a-new-package-is-missing)
  
  4. #### [Migrating V2](#4-migrating-v2)
  
#### 3. [Resources](#resources)

#### 4. [Code to Update](#code-to-update)

  1. #### [Section 3 : I Am Rich App](#section-3--i-am-rich-app-lesson-28)
  
  2. #### [Section 7 : Dicee App](#section-7--dicee-app-lesson-53)
  
  3. #### [Section 9 : Xylophone App](#section-9--xylophone-app-lessons-76-77)
  
  4. #### [Section 10 : Quizzler App](#section-10--quizzler-app-lesson-94)
  
  5. #### [Section 12 : BMI Calculator App](#section-12--bmi-calculator-app-lessons-125-126-128-129)
  
  6. #### [Section 13 : Clima App](#section-13--clima-app-lesson-140)

  7. #### [Section 14 : Flash Chat App](#section-14--flash-chat-app-lessons-169-194)

## Terminology

##### [Go back to Index](#index)

### 1. Deprecated

- You will often come across **`deprecated`** code, where it says **This is `deprecated`**. This means it's **not recommended** to use it anymore in your projects. You should avoid it and use alternatives.

### 2. Null Safety

- **Null safety is not your enemy!** It's there you help you write code that is **safe**. It's a **feature** of Dart and many other languages. Null safety makes sure that you don't accidentally pass a null value to a function that requires a non-null value.

- Dart has **`sound null safety`**. If you're writing any code that the compiler thinks might end up being **`null`**, it will warn you about it.

- Read more : [**Sound Null Safety**](https://dart.dev/null-safety), [**Understanding Null Safety**](https://dart.dev/null-safety/understanding-null-safety), [**Null Safety in Flutter**](https://flutter.dev/docs/null-safety)

## Common Issues and Fixes

##### [Go back to Index](#index)

#### 1. Using old Flutter SDK?

- Use latest **`Flutter SDK`**, currently I am using **`2.2`** in **`stable channel`**

  - To upgrade your version to the latest, run **`flutter upgrade`** in your **`Terminal or Command Prompt (cmd)`**

#### 2. **`Android license status unknown`**

- There are couple of things that can cause this, among the common ones are:

  ##### Solution 1. Accept the new ones!

  - Just run **`flutter doctor --android-licenses`**

  - Normally, this does the job. If it doesn't, read the other solutions.

  ##### Solution 2. Install / Update SDK Command Line Tools

  - Open Settings panel by,
  
    - **`File > Settings`** (**Windows and Linux**)

    - **`Android Studio > Preferences`** (**Mac**)

  - Then navigate to,
  
    **`Appearance & Behavior > System Settings > Android SDK`**

  - Select the **`SDK Tools` Tab**

  - Select **`Android SDK Command Line Tools`** and click **`Apply`**

  - A dialog will pop up and ask you if you want to install these.
  
    Click Yes/OK and let it install, after that, close **`Android Studio`** and **`restart`** it.
  
    <img src="https://github.com/DetainedDeveloper/App-Brewery-Flutter-Null-Safety/blob/master/images/guide/android_studio_sdk_tools.png?raw=true" width=506 height=378>

#### 3. Option to create a new **`package`** is missing

  - When I first encountered this issue, I thought there must be something wrong with just this particular update.

  - I searched it online, posted on Reddit, twitter, but found nothing.

  - Later on, I got to know that **`New > Package`** and **`New > Directory (Folder)`** options have now merged!

  - So, to create a new **`package`** or just a **`folder`**, simply use **`New > Directory`** option.

#### 4. Migrating V2

  - As we know [**Sound Null Safety**](https://dart.dev/null-safety) was added to **Flutter 2**. 

  - And before **Flutter 2** old apps don't have [**Sound Null Safety**](https://dart.dev/null-safety) feature. 

  - So we need to fix this, and thank [**Flutter**](https://flutter.dev/) we have simple way to do.

  - To fix this issue easily , 

    * Delete all files and folders in App folder **`except`** course materials **`lib` - `assets` - `fonts` - `pubspec.yaml` etc.**

    * For Example;
 
![ww](https://user-images.githubusercontent.com/84624853/151516481-b0eb6102-215c-4cf7-9774-fccffc2e9245.jpg)


  - And then go to **`Terminal`** while its in project folder and

    - **Write this line to `Terminal`**

      - `flutter create .`

  - For Example;

![crate](https://user-images.githubusercontent.com/84624853/151516510-ae00c14b-5d79-42fc-9801-3dc9c822bfe4.jpg)


  - **Then Flutter starts rebuilding application with migrated version of it. And Done!**


## Resources

##### [Go back to Index](#index)

#### 1. Try out Null Safety on [DartPad](https://dartpad.dev/?null_safety=true)

#### 2. Read Updated [Flutter Docs](https://flutter.dev/docs)

#### 3. Watch and Follow [Flutter's Official Youtube Channel](https://www.youtube.com/channel/UCwXdFgeE9KYzlDdR7TG9cMw)
- To learn more about Null Safety and stay updated in general.

# Code to Update

## Section 3 : I Am Rich App (Lesson 28)

##### [Go back to Index](#index)

- You right clicked on **`res`** folder but didn't find **`Image Asset`**? Don't worry Follow these steps,

  - Right click on **`android`** folder and a pop-up menu will open up.
  
    From that, select **`Flutter > Open Android Module in Android Studio`**

    **If this doesn't work for you then follow these steps**,
  
  **1.** Close current project by pressing **`File > Close Project`**
  
  **2.** Now you will have the first screen of Android Studio.
  
  **3.** Press **`Open an Existing Project`**, then **`Open File or Project`** dialog will open.
  
  **4.** Here, navigate to your **Flutter project** in which, you want to add **`Image Asset`**
  
  **5.** Expand that and you will find **`android`** folder. Select that and press **`OK`**
  
- **Both ways** should open **Android Part** of your **Flutter Project** in **`Android Studio`**.
  
- Now, in the bottom right, if it's running any **`gradle`** processes, let it run. Don't interrupt it! However, if you close it, it will rebuild everything when you reopen it.
  
- After the build process has completed, you can find  **`Image Asset`** option when you click on **`res`** folder.
  
- Add assets and again, **`File > Close Project`**, **`Open an Existing Project`** and this time, select your **Flutter Project** and continue!

## Section 7 : Dicee App (Lesson 53)

##### [Go back to Index](#index)

## Section 9 : Xylophone App (Lessons 76, 77)

##### [Go back to Index](#index)

- Getting a lengthy error when trying to use **`audioplayers` plugin**?
  
  - All you need to do is open **`android > build.gradle` (Project Level `gradle` file)**
  
  - Inside **`buildscript {}`**, you'll find **`ext.kotlin_version` (Line 2 in file)**
  
  - Replace whatever version it is with [**Latest Stable Kotlin Version**](https://kotlinlang.org/docs/releases.html#release-details)
  
  - As of **August 12, 2022** it is, **`ext.kotlin_version = '1.7.10'`**
  
  - Now, **re-install** the app. If it's already running, press **Stop** then press **Run (Play)** again.

- **`FlatButton`** is **`deprecated`**, so use **`TextButton`** instead.

- By the end, the implementation of your **`TextButton`** should look like this:
  
  ```dart
  @override
  Widget build(BuildContext context) {
    return Expanded(
      child: TextButton(
        style: ButtonStyle(
          backgroundColor: MaterialStateProperty.all(color),
        ),
        onPressed: () {
          playSound(soundNumber);
        },
      ),
    );
  }
  ```
  
 - **`AudioCache`** is **`deprecated`**, so use **`AudioPlayer`** instead.
  - By the end, your solution to playing the audio should look like this:
  ```dart
  void playSound(int soundNumber) {
    final player = AudioPlayer();
    player.setSource(AssetSource('note$soundNumber.wav'));
  }
  ```

- An example of a working project as of 16/07/2022 has been linked below:
  - [Link to repository](https://github.com/vpatel-dev/xylophone-flutter)
  
## Section 10 : Quizzler App (Lesson 94)

##### [Go back to Index](#index)

- Due to **`null safety`**, all variables in a class must have a value assigned, when created. If not, they must be declared **`Nullable`** intentionally. This rule also applies to **`Stateless`** and **`Stateful`** widgets. On top of that, in classes extending **`StatelessWidget`**, all variables must be declared **`final`**

- So, make your **`Question`** class like this,
  ```dart
  class Question {
    String questionText;
    bool questionAnswer;

    Question(this.questionText, this.questionAnswer);

    // If you want named parameters
    // const Question({ required this.questionText, required this.questionAnswer }); // Recommended
  }
  ```

    - **`@required`** is replaced by just **`required` (Without @ sign)**
    
    - Here, the **Keyword `this`** points to **current context**, which happens to be **`Question`** class.

## Section 12 : BMI Calculator App (Lessons 125, 126, 128, 129)

##### [Go back to Index](#index)

- **`@required`** is replaced by just **`required` (Without @ sign)**

- So, while making **`ReusableCard`**, lesson shows you can skip using **`cardChild`** property, but that isn't possible, due to **`null safety`**
  
  - This part is tricky, because now you can't have null arguments anymore.
  
  - So, you must have to intentionally make it **`Nullable`**, by adding **`?`** to it, like this,
    ```dart
    class ReusableCard extends StatelessWidget {
      final Color color;
      final Widget? cardChild;

      ReusableCard({required this.color, this.cardChild});

      @override
      Widget build(BuildContext context) {
        return Container(
          decoration: BoxDecoration(
            color: color, 
          ),
          child: child,
        );
      }
    }
    ```
    
  - Use it like **`ReusableCard(color: Colors.amber)`** and your app won't crash.

- But, it's not same for **`IconContent`**, **`Icon`** can have **`null`** value, but **`Text`** can't!
    ```dart
    class IconContent extends StatelessWidget {
      final IconData? icon;
      final String? label;

      IconContent({this.icon, this.label});

      @override
      Widget build(BuildContext context) {
        return Column(
          children: [
            Icon(icon),
            Text(label ?? ''),
          ],
        );
      }
    }
    ```
  
  - So using **`??`** operator, you need to check if label is **`null`** or not, if it is, then you must provide a **`String`** value to it. Here, I provided an empty String.

  - Even if you don't pass any arguments like **`IconContent()`**, your app won't crash.

- According to **Lesson 129**, **`ReusableCard`** now has a parameter named **`onPress`**, to get it working, use this,
  ```dart
  class ReusableCard extends StatelessWidget {
    final Color color;
    final Widget? cardChild;
    final void Function()? onPress;

    const ReusableCard({ required this.color, this.cardChild, this.onPress });

    @override
    Widget build(BuildContext context) {
      return GestureDetector(
        onTap: onPress,
        child: Container(
          decoration: BoxDecoration(
            color: color, 
          ),
          child: child,
        ),
      );
    }
  }
  ```
  - Because **`GestureDetector`**'s **`onTap`** property wants **`void Function()?`** as argument.

- In **Lesson 128**, **`_InputPageState`** has a new variable which haven't been initialized. As I already told you, you must initialize them or make them **`Nullable`**.
  ```dart
  class _InputPageState extends State<InputPage> {
    Gender? selectedGender;
  }
  ```

  - Here, making it **`Nullable`** will do the job. Rest of the code will work perfectly fine.

## Section 13 : Clima App (Lesson 140)

##### [Go back to Index](#index)

- When running this app on a **Physical Device** running on: 

  - **`Android` :** you will need **Internet Permission** because the app sends a **`request`** to the OpenWeatherMap **`API`**. For this, open **`AndroidManifest.xml`** by navigating to,
    
    **`android > app > src > main > AndroidManifest.xml`**
    
    and add the following line,

    ```xml
    <uses-permission android:name="android.permission.INTERNET"/>
    ```

    **Keep the existing location permissions** and add this above/below them.
    Add it under **`manifest`** tag, like this,

    ```xml
    <manifest xmlns:android="http://schemas.android.com/apk/res/android"
      package="detaineddeveloper.example.clima">

      <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION"/>
      <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION"/>

      <!--Keep the existing location permissions above (whichever you have added previously)-->
      <uses-permission android:name="android.permission.INTERNET"/>
    
      <application
        android:label="clima"
        android:icon="@mipmap/ic_launcher">
        .
        .
        .
      </application>
    </manifest>
    ```

  - **`iOS` :**

    - There is **no required Internet Permission**.
    - When launching the app, you will probably have a message asking you for **Local Network Permission**: it is **not required** either.
    - To run your app on an iOS physical device, make sure that you selected a **Development Team** (refer to **Section 4 - Lesson 32** of the course):
      1. Open the Flutter project's Xcode target with open ios/Runner.xcworkspace
      
      2. Select the 'Runner' project in the navigator then the 'Runner' target in the project settings
      
      3. Make sure a 'Development Team' is selected under Signing & Capabilities > Team. You may need to:
          1. Log in with your Apple ID in Xcode first
          2. Ensure you have a valid unique Bundle ID (for example *"com.put-your-name-here.clima"*)
          3. Register your device with your Apple Developer Account
          4. Let Xcode automatically provision a profile for your app

      4. Select your iOS physical device as the target and click the Run button
        - You may have several pop-up asking you that "codesign" wants access to your Apple Development Team's key. Accept by entering your password (it's your Mac session's password, not your Apple ID's password)
        - :exclamation: **ATTENTION:** if you don't activate Internet on your physical device, it is likely that you will see a pop-up on your screen telling you that **an Internet connection is required** to verify if the developer (you) is reliable, so you would need to activate your Internet connection

- If your app cannot retrieve your current location on your **`iOS` physical device** it is probably because the [geolocator 8.2.1 flutter package](https://pub.dev/packages/geolocator) has been updated and you will need to apply the following changes:
  - As of now (June 2022), the geolocator package indicates to add both **`NSLocationWhenInUseUsageDescription`** and **`NSLocationAlwaysUsageDescription`** permissions to access **Location Service**. Since iOS 11, the **`NSLocationAlwaysUsageDescription`** property key is [deprecated](https://developer.apple.com/documentation/bundleresources/information_property_list/nslocationalwaysusagedescription). Use instead **only one** of those permissions:
    - the **`NSLocationAlwaysAndWhenInUseUsageDescription`** to enable the **Location Service** in foreground and background,
    - the **`NSLocationWhenInUseUsageDescription`** to enable the service in foreground only, as [recommended by Apple](https://developer.apple.com/documentation/corelocation/choosing_the_location_services_authorization_to_request).

    To do so, open **`Info.plist`** file by navigating to:

    **`ios > Runner > Info.plist`**

    and add the following line right under the `<dict>` tag (your can customise the message in the `<string>` tag, it has to explain why your app needs to have access to that particular permission):

    ```xml
    <dict>
        <key>NSLocationWhenInUseUsageDescription</key>
        <string>This app needs access to your location to provide weather data of your current location.</string>
    </dict>
    ```

  - In your code you will have to explicitly ask the user for permission to use the **Location Service**. For that, update the **`getCurrentLocation()`** method in the **`location.dart`** file:
    - Short version:
      ```dart
      Future<void> getCurrentLocation() async {
        try {
          LocationPermission locationPermission = await Geolocator.requestPermission();

          if (LocationPermission.whileInUse == locationPermission || LocationPermission.always == locationPermission) {
            Position position = await Geolocator.getCurrentPosition(desiredAccuracy: LocationAccuracy.lowest);
            latitude = position.latitude;
            longitude = position.longitude;
          }
        } catch (e) {
          print(e);
        }
      }
      ```
    - Long but more complete version:
      ```dart
      Future<void> getCurrentLocationCheckingPermissions() async {
        bool serviceEnabled;
        LocationPermission locationPermission;

        // Test if location services are enabled.
        serviceEnabled = await Geolocator.isLocationServiceEnabled();
        if (!serviceEnabled) {
          // Location services are not enabled don't continue
          // accessing the position and request users of the
          // App to enable the location services.
          return Future.error(
              'Location services are disabled. Please activate them.');
        } else {
          locationPermission = await Geolocator.checkPermission();
          if (LocationPermission.unableToDetermine == locationPermission) {
            return Future.error(
                'Unable to determine if location permissions are enabled.');
          } else if (LocationPermission.denied == locationPermission ||
              LocationPermission.deniedForever == locationPermission) {
            print(Future.error('Location permissions are denied: ' +
                locationPermission.toString()));
            locationPermission = await Geolocator.requestPermission();
          }

          if (LocationPermission.whileInUse == locationPermission ||
              LocationPermission.always == locationPermission) {
            Position position = await Geolocator.getCurrentPosition(
                desiredAccuracy: LocationAccuracy.lowest);
            this.latitude = position.latitude;
            this.longitude = position.longitude;
          }
        }
      }
      ```


## Section 14 : Flash Chat App (Lessons 169-194)

##### [Go back to Index](#index)

### Setting up Firebase

Following the AppBrewery course, you should have logged in Firebase with your Google account, and created a Firebase project that will be linked with your Flash Chat Flutter project.

#### Add Firebase to your Flutter project

- To do so, in the course it is showed that you have to go to your Firebase project and **add a new application**, selecting an **`Android application`** if you plan to deploy your app on Android, and/or an **`iOS application`** if you plan to deploy on iOS.
- As of now **(July 2022)**, it is now possible to directly add a **`Flutter application`** which will save you a lot of time in configuration :confetti_ball: , so choose that option instead, and follow the instructions that will be displayed:

#### Installing Firebase CLI and connect to it

- Depending on your Operating System (Windows, macOS or Linux), you will find the steps to do on the [documentation](https://firebase.google.com/docs/cli?authuser=0&hl=fr#install_the_firebase_cli).
- After the installation is done, connect to it by executing the following command in a terminal: **`firebase login`**.

#### Installing Flutter SDK and creating a Flutter project

- If you have arrived this far in the course, you have already installed the Flutter SDK a long time ago!
- The Flutter project has alo been created already, it's our Flash Chat Flutter project.


#### Installing the FlutterFire CLI
- Open a terminal and run the following command line: **`dart pub global activate flutterfire_cli`** (it doesn't matter in which directory you run this command)


#### Executing the FlutterFire CLI

- Before executing the **FlutterFire CLI**, make sure to change your **`Application ID`** for Android, and your **`iOS Bundle ID`** for iOS to make them **unique and personal** (if you have copied the Flash Chat Flutter project from the AppBrewery course, they are defined with their company ID which you have to change to make it your own):

  - **`Application ID`** for Android:
    - Open the **`build.gradle`** file located under **`android > app > build.gradle`**
    - Change the **`android > defaultConfig > applicationId`** property (the applicationId should be **co.appbrewery.flash_chat** --> change it for something unique and personal like **com.firstnamelastname.flash_chat**, or something you like that is unique and personal, or your domain name if you own one and wish to use it)

  - **`iOS Bundle ID`** for iOS:
    - Right-click on the "ios" folder and choose **`Flutter > Open iOS module in Xcode`**
    - Select "Runner" at the top of the left panel (the "Runner" with the blue icon), and in the center panel go to the **General tab**, then under it go to **`Identity > Bundle Identifier`**
    - You should find a Bundle Identifier like **co.appbrewery.flashChat** --> change it for something unique and personal like **com.firstnamelastname.flashChat**

- After changing the **`Application ID`** for Android, and/or the **`iOS Bundle Identifier`** for iOS, open a terminal and go to the **ROOT FOLDER** of your Flutter Flash Chat project, then execute the command line given in the instructions: 

  ```shell
  flutterfire configure --project=YOUR_FIREBASE_PROJECT_ID_HERE
  ```
  (You can check what is your Firebase Project ID by either looking on your Firebase account in a browser, or by running the command line **`firebase projects:list`**)
- After running the previous command, you should find in your Flutter project:

  - **`Flutter`**: your Firebase configuration file under **`lib > firebase_options.dart`** (the most important one, it contains both your Android and your iOS API keys to access Firebase services)

  - **`Android`**: your Firebase configuration file under **`android > app > google-services.json`**

  - **`iOS`**: a Firebase identifying file under **`ios > firebase_app_id_file.json`** (if the course is not updated, you might see that you should have a file called **`GoogleService-Info.plist`** instead under **`ios > Runner > GoogleService-Info.plist`** --> I am not an expert with Firebase, but my guess is that the **`GoogleService-Info.plist`** comes up when you configure your Firebase project by adding an iOS application instead of a Flutter application)


#### Initializing Firebase

- To initialize Firebase, start by adding to your Flutter project the **`firebase_core`** plugin:
  ```shell
  flutter pub add firebase_core
  ```
- Make sure that the Firebase configuration of your Flutter application is updated, by running the following command **in the root folder of your Flutter project directory**:
  ```shell
  flutterfire configure
  ```
- Then, if everything's fine, in your **`lib/main.dart`** file, change the main method to use the Firebase initializing method **`Firebase.initializeApp()`**
  ```dart
  import 'package:firebase_core/firebase_core.dart';
  import 'package:flash_chat/firebase_options.dart';


  Future<void> main() async {
    WidgetsFlutterBinding.ensureInitialized();

    await Firebase.initializeApp(options: DefaultFirebaseOptions.currentPlatform);

    runApp(FlashChat());
  }
  ```
  :exclamation::exclamation: It is **FUNDAMENTAL** that you add the parameter **`options: DefaultFirebaseOptions.currentPlatform`** because it will specify the configuration that will be used depending on the platform your application is running on (Android, iOS, macOS, Windows or Linux) --> feel free to explore the code of **`DefaultFirebaseOptions.currentPlatform`**, you will notice that it corresponds to your **`lib > firebase_options.dart`**, and that it simply verifies the platform on which your application is running, then returns the appropriate configuration.

- Finally, stop your application if it was running (to make a fresh start), and try to run it on Android and on iOS to verify that everything works on both platform (try to run it as well on macOS, Windows and/or Linux if you are developing for those platforms).

  If you encounter some errors, please have a look below to find some fixes that may be of help:

  - **`On Android`:** 

    - The **`firebase_core`** plugin (as well as all [Firebase plugins](https://firebase.google.com/docs/flutter/setup?authuser=0&hl=fr&platform=ios#available-plugins)) requires at least the **`Android SDK version 31`** now (July 2022), so make the modification if needed under **`android > app > build.gradle`**:

    ```gradle
      android {
        compileSdkVersion 31
        ...
      }
    ```

  - **`On iOS`:** 

    - There was no problem encountered on my side. Please add more details about yours in the **Discussions** section if you have troubles here.


#### Adding Firebase Plugins

- Add the **`firebase_auth`** and the **`cloud_firestore`** plugins in your Flutter project:
  ```shell
    flutter pub add firebase_auth
    flutter pub add cloud_firestore
  ```
  Click on **`Pub Get`** to make sure that you get the dependencies in your project.


- **`On Android`**:

  - You may need to upgrade the **`minSdkVersion`** of the Android part of your Flutter project, under **`android > app > build.gradle`**, because some Firebase plugins have a minimal requirement of the SDK version 21 now (July 2022), like the **`cloud_firestore`** plugin for instance, so apply that change:
    ```gradle
      android {
        ...
        defaultConfig {
          ...
          minSdkVersion 21
          ...
        }
        ...
      }
    ```

  - Those plugins require as well the **`Android SDK version 31`**, so make sure that you have it updated in your **`android > app > build.gradle`**:

    ```gradle
      android {
        compileSdkVersion 31
        ...
      }
    ```


  - After adding the dependencies in the AndroidManifest.xml file and the build.gradle files, you might get this error:
    ```shell
      ERROR:D8: Cannot fit requested classes in a single dex file (# methods: 104246 > 65536)
      com.android.builder.dexing.DexArchiveMergerException: Error while merging dex archives:
      The number of method references in a .dex file cannot exceed 64K.
       ...
      * What went wrong:
        Execution failed for task ':app:mergeExtDexDebug'.
      > A failure occurred while executing com.android.build.gradle.internal.tasks.DexMergingTaskDelegate
      > There was a failure while executing work items
      > A failure occurred while executing com.android.build.gradle.internal.tasks.DexMergingWorkAction
      > com.android.builder.dexing.DexArchiveMergerException: Error while merging dex archives:
      The number of method references in a .dex file cannot exceed 64K.
      Learn how to resolve this issue at https://developer.android.com/tools/building/multidex.html
    ```

    To fix this issue, inside the app-level build.gradle file, **`../android/app/build.gradle`**,
    the *minSdkVersion* property under the *defaultConfig* block in the *android* block should be set to **`21`** to avoid error.
    This is because multiDex support is enabled by default for sdkVersion 21.

  - Additional dependencies have to be added to the app-level build.gradle file, **`../android/app/build.gradle`**:
    ```
    dependencies {
      ...
      implementation platform('com.google.firebase:firebase-bom:30.0.1')
      implementation 'com.google.firebase:firebase-auth'
      implementation 'com.google.firebase:firebase-firestore'
      ...
    }
    ```

  - To enable internet connectivity on a physical device, add `<uses-permission android:name="android.permission.INTERNET" />` to the AndroidManifest.xml file.



- **`On iOS`** :
  
  - Before running the application to check if everything is fine, update **`CocoaPods`**:
    ```shell
      pod repo update
      sudo gem install cocoapods
      pod setup
    ```
  - Run your app to check if it's working:
    - If you encounter the following error:
      ```shell
        Error output from Cocoapods:
          [!] Automatically assigning platform 'iOS' with version '9.0' on target 'Runner' because no platform was specified. Please specify a platform for this target in your Podfile.android
        Error running pod install
        Error launching application on iPhone.
      ```
      update your **`Podfile`** file under **`ios > Podfile`** by uncommenting the "platform" line and changing the version from 9.0 to 10.0 --> this specifies the minimum OS version that you are going to support for the pod project:
      ```
        # Uncomment this line to define a global platform for your project
        platform :ios, '10.0'
      ```
      then try to run your app again (it might take a long time, it took me around 30 minutes to make all the cocoapods installation).
      You should see in the "Run tab" the information **"Running pod install..."**: Flutter is initiating that to be able to install all of the Firebase plugin packages (firebase_core, firebase_auth and cloud_firestore) as cocoapods to our iOS app.


### Code Part

- In **chat_screen.dart** file, the object type for the *loggedInUser* was previously **`FirebaseUser`**, and should now be replaced with **`User`**. Moreover, the Firestore instance is now retrieved with `FirebaseFirestore.instance` instead of `Firestore.instance`:

  ```dart
    class _ChatScreenState extends State<ChatScreen> {
      final _firestore = FirebaseFirestore.instance;
      final _auth = FirebaseAuth.instance;

      User loggedInUser;
      String message;
      ...
    }

  ```


- When retrieving the messages from your Firestore Database, you will notice some changes in the API:
  
  - The `getDocuments` method has been renamed to `get`:
    ```dart
      _firestore.collection('messages').getDocuments(); // <-- BEFORE

      _firestore.collection('messages').get(); // <-- NOW
    ```

  -  The **QuerySnapshot** property, **documents**, has been renamed to **docs**.
      ```dart
        void getMessages() async {
          final messages = await _firestore.collection('messages').get();

          for (var message in messages.documents) { // <-- BEFORE
            print(message.data());
          }

          for (var message in messages.docs) { // <-- NOW
            print(message.data());
          }
        }
      ```

- When using a `StreamBuilder`, it is better to give it the type of data that will stream through, as it will greatly help you when manipulating the `AsyncSnapshot` and the data it contains (`snapshot.data`) - you can find the type of data by looking at the return type of the Firestore snapshots method (`_firestore.collection('messages').snapshots()`):
  ```dart
    StreamBuilder<QuerySnapshot<Map<String, dynamic>>>( // <-- By adding the type <QuerySnapshot<Map<String, dynamic>>...
      stream: _firestore.collection('messages').snapshots(),
      builder: (BuildContext context, AsyncSnapshot snapshot) {

        final messages = snapshot.data.docs; // <-- ... you will be able to access the 'docs' property because we manipulate a Stream of QuerySnapshot

        for (var message in messages) {
          final messageText = message.data()['text'];  // <-- ... you will be able to access the Map with `message.data()` because we manipulate a Stream of QuerySnapshot of Map<String, dynamic>
          final sender = message.data()['sender'];
          ...
        }
        ...
      },
    );
  ```

- To deal with the case where we would have no data in our `StreamBuilder`, we do add a `CircularProgressIndicator` after checking the value of `!snapshot.hasData`. To center it on the screen, add a margin using `MediaQuery` to retrieve the height of the screen (if you want to see how it looks like, you can simply temporarily change the if condition with `true`):
  ```dart
    StreamBuilder<QuerySnapshot<Map<String, dynamic>>>(
      stream: _firestore.collection('messages').snapshots(),
      builder: (context, snapshot) {

        if (!snapshot.hasData) { // <-- change it temporarily to 'if (true)' to quickly see the result
          return Container(
            margin:
                EdgeInsets.only(top: MediaQuery.of(context).size.height / 3),
            child: CircularProgressIndicator(
              backgroundColor: Colors.lightBlueAccent,
            ),
          );
        }
        ...
      },
    );
  ```
  :exclamation::information_source: To avoid your `CircularProgressIndicator` to be stretched horizontally and look weird, make sure that the column in which your `MessagesStream` is into doesn't have the property **`crossAxisAlignment: CrossAxisAlignment.stretch`**:
  ```dart
    body: SafeArea(
      child: Column(
        mainAxisAlignment: MainAxisAlignment.spaceBetween,
        // crossAxisAlignment: CrossAxisAlignment.stretch, // <-- remove this if you have it
        children: <Widget>[
          MessagesStream(),
          Container(...),
          ...
  ```


- The sorting of the messages in the chat screen is still chaotic even after the reversal in ***lesson 191***.
  To fix this problem, we need to add a **timestamp** field to the messages and sort the collection based on it as shown here:
  ```dart
  ...
  TextButton(
    onPressed: () {
      controller.clear();
      _firestore.collection('messages').add({
        'text': messageText,
        'sender': loggedInUser.email,
        'timestamp': FieldValue.serverTimestamp(), // Here is the **timestamp** field.
      });
    },
  ...
  ```

  We use the server time instead of generating a timestamp with the user device because:
  - Our users may be in different timezones so the time differences will affect our app.
  - Some devices could be set to incorrect times.

  ```dart
  class MessagesStream extends StatelessWidget {

  @override
  Widget build(BuildContext context) {
    return StreamBuilder<QuerySnapshot>(
      stream: _firestore.collection('messages').orderBy('timestamp').snapshots(), // Here, the **.orderBy** sorts the messages according to the server timestamps.
      builder: (context, snapshot) {
      ...
  
  ```


### More Configuration on Firebase

#### Cloud Firestore Authorization and Security Rules

- In ***lesson 192***, we change the **Security Rules** of our **Firestore Database** to allow read and write access to **authenticated** users only. In the course, we add the following condition **`request.auth.uid != null`**. As of now (July 2022), we have to change this condition with the following one, regarding the [documentation](https://firebase.google.com/docs/rules/rules-and-auth#identify_users): **`request.auth != null`**
  ```
    rules_version = '2';
    service cloud.firestore {
      match /databases/{database}/documents {
        match /{document=**} {
          allow read, write: if
              request.auth != null // <-- here it is
      
              && request.time < timestamp.date(2022, 8, 5); // <-- if you wish to, you can add this condition that will only allow access to your database **before** a specified date
        }
      }
    }
  ```
  :exclamation::exclamation::information_source: Keep in mind that the above rules are not secure enough at all. They are only good for developing purpose, but the moment you release your application in production (or even when you simply share it with other people that you don't know), you have to reinforce your **Security Rules** to be less permissive and have better and stronger control on whose accessing your database, and what data they have access to.


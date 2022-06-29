# AppBrewery Flutter : Null Safety Guide

## Read Before Starting

- **DISCLAIMER : This repository is not an official outcome of [London AppBrewery Team](https://github.com/londonappbrewery)**

- This repository is made to help new students get through [**AppBrewery Flutter Course**](https://www.udemy.com/course/flutter-bootcamp-with-dart/)

- This repository contains notes for **only coding (project) sections** and explains what has changed and what's the difference.

- If something is not covered here, **start a discussion**, not an issue! I will try to add it then.

- Use latest versions of required **`packages`** and **`plugins`**, find them on [**pub.dev**](https://pub.dev/)

## Index

#### 1. [Terminology](#terminology)

#### 2. [Common issues and fixes](#common-issues-and-fixes)

  1. #### [Using old Flutter SDK?](#1-using-old-flutter-sdk)
  
  2. #### [Android license status unknown](#2-android-license-status-unknown)
  
  3. #### [Option to create a new package is missing](#3-option-to-create-a-new-package-is-missing)

#### 3. [Resources](#resources)

#### 4. [Code to Update](#code-to-update)

  1. #### [Section 3 : I Am Rich App](#section-3--i-am-rich-app-lesson-28)
  
  2. #### [Section 7 : Dicee App](#section-7--dicee-app-lesson-53)
  
  3. #### [Section 9 : Xylophone App](#section-9--xylophone-app-lessons-76-77)
  
  4. #### [Section 10 : Quizzler App](#section-10--quizzler-app-lesson-94)
  
  5. #### [Section 12 : BMI Calculator App](#section-12--bmi-calculator-app-lessons-125-126-128-129)
  
  6. #### [Section 13 : Clima App](#section-13--clima-app-lesson-140)

## Terminology

##### [Go back to Index](#index)

### 1. Deprecated

- You will often come across **`deprecated`** stuff, where it says **This is `deprecated`**. This means it's **not recommended** to use it anymore in your projects. You should avoid it and use alternatives.

### 2. Null Safety

- **Null safety is not your enemy!** It's there you help you so you don't accidentally make something null and crash your app.

- Dart has **`sound null safety`**. Basically, if you're writing any code that compiler thinks might end up being **`null`**, it will notify you right away! Isn't that cool?

- Read more : [**Sound Null Safety**](https://dart.dev/null-safety), [**Understanding Null Safety**](https://dart.dev/null-safety/understanding-null-safety), [**Null Safety in Flutter**](https://flutter.dev/docs/null-safety)

### 3. Migrating V2

As we know [**Sound Null Safety**](https://dart.dev/null-safety) was added to **Flutter 2**. 

And before **Flutter 2** old apps don't have [**Sound Null Safety**](https://dart.dev/null-safety) feature. 

So we need to fix this, and thank [**Flutter**](https://flutter.dev/) we have simple way to do.

To fix this issue easily , 

Delete all files and folders in App folder **except** course materials **lib folder-Assets-Fonts-pubspec.yaml**

For Example;
 
![ww](https://user-images.githubusercontent.com/84624853/151516481-b0eb6102-215c-4cf7-9774-fccffc2e9245.jpg)


and then go to **Terminal** while its in project folder and

**write this line to Terminal**

`flutter create .`

For Example;

![crate](https://user-images.githubusercontent.com/84624853/151516510-ae00c14b-5d79-42fc-9801-3dc9c822bfe4.jpg)


**And then Flutter starts rebuilding application with migrated version of it. And Done!**

Hope this works.

## Common Issues and Fixes

##### [Go back to Index](#index)

#### 1. Using old Flutter SDK?

- Use latest **`Flutter SDK`**, currently I am using **`2.2`** in **`stable channel`**

  - To upgrade old one, run **`flutter upgrade`** in your **`Terminal / Command Prompt (cmd)`**

#### 2. **`Android license status unknown`**

- There are couple of things that can cause this, I'll keep adding them in future! For now I have these solutions,

  ##### Solution 1. Accept the new ones!

  - Just run **`flutter doctor --android-licenses`**

  - Normally, this does the job. If it doesn't, go ahead.

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

## Resources

##### [Go back to Index](#index)

#### 1. Try out Null Safety on [DartPad](https://dartpad.dev/?null_safety=true)

#### 2. Read Updated [Flutter Docs](https://flutter.dev/docs)

#### 3. Watch and Follow [Flutter's Official Youtube Channel](https://www.youtube.com/channel/UCwXdFgeE9KYzlDdR7TG9cMw)
- To learn more about Null Safety and staying updated in general.

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
  
- Now, at bottom right, if it's running any **`gradle`** processes, let it run. Don't interrupt! However, if you close it, it'll rebuild everything when you reopen it. So, no need to worry!
  
- After that long build process completes, you can find  **`Image Asset`** option when you click on **`res`** folder, **Yay**!
  
- Add assets and again, **`File > Close Project`**, **`Open an Existing Project`** and this time, select your **Flutter Project** and continue!

## Section 7 : Dicee App (Lesson 53)

##### [Go back to Index](#index)

- **`FlatButton`** is **`deprecated`**, so use **`TextButton`** instead.

## Section 9 : Xylophone App (Lessons 76, 77)

##### [Go back to Index](#index)

- Getting a lengthy error when trying to use **`audioplayers` plugin**?
  
  - All you need to do is open **`android > build.gradle` (Project Level `gradle` file)**
  
  - Inside **`buildscript {}`**, you'll find **`ext.kotlin_version` (Line 2 in file)**
  
  - Replace whatever version it is with [**Latest Stable Kotlin Version**](https://kotlinlang.org/docs/releases.html#release-details)
  
  - As of **July 23, 2021** it is, **`ext.kotlin_version = '1.5.21'`**
  
  - Now, **re-install** the app. If it's already running, press **Stop** then press **Run (Play)** again.

- **`FlatButton`** is **`deprecated`**, so use **`TextButton`** instead.

  - **HOWEVER**, for this module, you won't be adding any **`child`** to **`FlatButton`**, this will throw an error because **`child`** is a **`required`** property.
  
  - So, for **Xylopone Keys**, use **`MaterialButton`** instead of **`FlatButton`**

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
    // Question({required this.questionText, required this.questionAnswer});
  }
  ```

    - **`@required`** is replaced by just **`required` (Without @ sign)**
    
    - Here, the **Keyword `this`** points to **current context**, which happens to be **`Question`** class.

- **`FlatButton`** is **`deprecated`**, so use **`TextButton`** instead.

## Section 12 : BMI Calculator App (Lessons 125, 126, 128, 129)

##### [Go back to Index](#index)

- **`@required`** is replaced by just **`required` (Without @ sign)**

- So, while making **`ReusableCard`**, lesson shows you can skip using **`cardChild`** property, but that isn't possible, due to **`null safety`**
  
  - This part is tricky, because now you can't have null arguments anymore.
  
  - So, you must have to intentionally make it **`Nullable`**, by adding **`?`** to it, like this,
    ```dart
    class ReusableCard extends StatelessWidget {
      final Color colour;
      final Widget? cardChild;

      ReusableCard({required this.colour, this.cardChild});

      @override
      Widget build(BuildContext context) {
        return Container(
          decoration: BoxDecoration(
            color: colour, 
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
    final Color colour;
    final Widget? cardChild;
    final void Function()? onPress;

    ReusableCard({required this.colour, this.cardChild, this.onPress});

    @override
    Widget build(BuildContext context) {
      return GestureDetector(
        onTap: onPress,
        child: Container(
          decoration: BoxDecoration(
            color: colour, 
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

- When running this app on a **Physical Device**, you will need **Internet Permission** because app is sending a **`request`** to **`API`**

  - **`Android` :** For this, open **`AndroidManifest.xml`** by navigating to,
    
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

  - **`iOS` :** I don't know, I don't have an **`iOS`** device!


## Section 14 : Flash Chat (Lessons 169 194)

##### [Go back to Index](#index)

- After adding the dependencies in the AndroidManifest.xml file and the build.gradle files, you might get this error:
  ```
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

- Before the FirebaseAuth can work, we must initialize it in the **main.dart** file:
  ```dart
  import 'package:firebase_core/firebase_core.dart';

  Future<void> main() async {
  WidgetsFlutterBinding.ensureInitialized();

  await Firebase.initializeApp();

  runApp(FlashChat());
  }
  ```

- In the **chat_screen.dart** file, the object type for the *loggedInUser*, **`FirebaseUser`**, should be replaced with **`User`**

- The **QuerySnapshot** property, **documents**, has been renamed to **docs**.

- The sorting of the messages in the chat screen is still chaotic even after the reversals in *lesson 191*.
  To fix this problem, we need to add a **timestamp** field to the messages and sort and sort the collection based on it as shown here:
  ```
  ...
  TextButton(
    onPressed: () {
      controller.clear();
      _firestore.collection('messages').add({
        'text': messageText,
        'sender': loggedInUser.email,
        "timestamp": FieldValue.serverTimestamp(), // Here is the **timestamp** field.
      });
    },
  ...
  ```

  We use the server time instead of generating a timestamp with the user device because:
  - Our users mey be in different timezones so the time differences will affect our app.
  - Some devices could be set to incorrect times.

  ```
  class MessagesStream extends StatelessWidget {

  @override
  Widget build(BuildContext context) {
    return StreamBuilder<QuerySnapshot>(
      stream: _firestore.collection('messages').orderBy('timestamp').snapshots(), // Here, the **.orderBy** sorts the messages according to the server timestamps.
      builder: (context, snapshot) {
      ...
  
  ```

- In the **chat_screen.dart** file, the object type for the *loggedInUser*, **`FirebaseUser`**, should be replaced with **`User`**

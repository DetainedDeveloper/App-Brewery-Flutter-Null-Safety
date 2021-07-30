# AppBrewery Flutter : Null Safety Guide

## Read Before Starting

- **DISCLAIMER : This repository is not an official outcome of [London AppBrewery Team](https://github.com/londonappbrewery)**

- This repository is made to help new students get through [**AppBrewery Flutter Course**](https://www.udemy.com/course/flutter-bootcamp-with-dart/)

- This repository contains notes for **only coding (project) sections** and explains what has changed and what's the difference.

- If something is not covered here, **start a dicussion**, not an issue! I will try to add it then.

- Use latest verions of required **`packages`** and **`plugins`**, find them on [**pub.dev**](https://pub.dev/)

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

- Dart has **`sound null safety`**. Basically, if you're writng any code that compiler thinks might end up being **`null`**, it will notify you right away! Isn't that cool?

- Read more : [**Sound Null Safety**](https://dart.dev/null-safety), [**Understanding Null Safety**](https://dart.dev/null-safety/understanding-null-safety), [**Null Safety in Flutter**](https://flutter.dev/docs/null-safety)

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

  - I searched it online, posted on reddit, twitter, but found nothing.

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

  - Right click on **`android`** folder and a pop-up menu wiil open up.
  
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

- Getting a LOOONNNGGG error when trying to use **`audioplayers` plugin**?
  
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
    
  - Use it like **`ReusabledCard(color: Colors.amber)`** and your app won't crash.

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
  - Because **`GestureDetector`**'s **`onTap`** propery wants **`void Function()?`** as argument.

- In **Lesson 128**, **`_InputPageState`** has a new variable which haven't been initialized. As I already told you, you must initialize them or make them **`Nullable`**.
  ```
  class _InputPageState extends State<InputPage> {
    Gender? selectedGender;
  }
  ```

  - Here, making it **`Nullable`** will do the job. Rest of the code will work perfectly fine.

## Section 13 : Clima App (Lesson 140)

##### [Go back to Index](#index)

- When running this app on a **Physical Device**, you will need **Internet Permisson** because app is sending a **`request`** to **`API`**

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

      <uses-permission android:name="android.permission.ACCESSS_COARSE_LOCATION"/>
      <uses-permission android:name="android.permission.ACCESSS_FINE_LOCATION"/>

      <!--Keep the existing location permisions above (whichever you have added previously)-->
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

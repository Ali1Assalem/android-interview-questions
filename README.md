## Android Interview Questions

After so many interview with many android developer, I decided to document my questions which ask in the interview meeting.

<br>


#### This document is suitable for you if ...

1. You want to **interview** with a new company.
2. You are working in a company but want to know which questions are typically **mentioned** in interviews.
3. You are an interviewer and need some **useful** questions or want to **challenge** the interviewee
4. You just want to **improve** your knowledge about android problems and basics.


<br>


| <span style="color:red">*__IMPORTANT NOTICE__*: There is no need to know and read all the questions will be mentioned later. According to the field, size, products and requirements of the company, select and read the appropriate questions. </span>     
| :-------------


<br>

---
#### Table of contents

1. [Object-oriented](https://github.com/javadhme/android-interview-questions#Lifestyle "Object-oriented")
2. [Java](https://github.com/javadhme/android-interview-questions#Lifestyle "Java")
3. [Kotlin](https://github.com/javadhme/android-interview-questions#Lifestyle "Kotlin")
4. [Android](https://github.com/javadhme/android-interview-questions#Android "Android")
5. [Architecture and coding](https://github.com/javadhme/android-interview-questions#"Android "Architecture and coding")
6. [Tools and libraries](https://github.com/javadhme/android-interview-questions#"Android "Tools and libraries")
7. [Gradle](https://github.com/javadhme/android-interview-questions#Gradle "Gradle")
8. [Design patterns](https://github.com/javadhme/android-interview-questions# "Design patterns")
9. [Data structure and algoritms](https://github.com/javadhme/android-interview-questions# "Data structure and algoritms")
10. [Git](https://github.com/javadhme/android-interview-questions# "Git")

---
<br>

### 1. Object-Oriented

- What is and Object?
- What is the main feature of OOP ? <br>
    `Encapsulation`, `Polymorphism`, `Inheritance`, `Abstraction`

- What is encapsulation?
- What is Polymorphism?
- Difference between abstract and interface?
- What is the difference between static and dynamic Polymorphism?
- Can Interfaces to be extended?
- What is the difference between overriding and overloading?

| Method Overloading      | Method Overriding     |
| :-------------   | :------------- |
| Method overloading is a compile time polymorphism.         | Method overriding is a run time polymorphism.       |
| It help to rise the readability of the program. | While it is used to grant the specific implementation of the method which is already provided by its parent class or super class. |
| It is occur within the class.	 | 	While it is performed in two classes with inheritance relationship. |
| Method overloading may or may not require inheritance. | While method overriding always needs inheritance. |
| In this, methods must have same name and different signature. | While in this, methods must have same name and same signature. |
| In method overloading, return type can or can not be be same, but we must have to change the parameter. | While in this, return type must be same or co-variant. |

<br>

### 2. JAVA

- How to prevent a class to be extended?

- What is the use of the finalize method?
- Overriding for static method, possible?
- What is an abstract class? Benefits?
- What is an object cloning? Is it enable for all objects?
- Multiple inheritances? Possible? How can we do that?
- Object scopes?
- Override private methods, possible?
- What is a static variable in Java?
- Java reference types?
- What is Generic in Java?
- How String class is implemented? Is it mutable or immutable? Why was it made immutable?
- What is the difference between int and Integer?
- What are Autoboxing and unboxing?
- What is the difference between initialization and instantiation?
- How does a static block work?
- What does the keyword `synchronized` mean?
- What is the memory leak? How to handle it?
- What is `transient` modifier?
- What is the difference between `==` and `.equal`?
- What is `reflection`?
- What is the `volatile` modifier?
- What is the `hashCode()` used for?
- What are "annotations"?



<br>

### 3. Kotlin

- What are the benefits of Kotlin?

- What does "Null safety" meaning?
- Why Kotlin does not support primitive type?
- What is Lazy initialization?
- What is the data class?
- Is it possible to inherit a class/method/property by default?
- Difference between apply, also?
- What `==` exactly do in Kotlin in comparison to Java?
- What is the difference between parameter and argument?
- What is the difference between function and method?
- What is the "receiver" in the extension function?
- What is operator overloading?
- Is it possible to write a static method as java as has?
- What is a sealed class?
- How does an extension function work?
- What is `reified` keyword?
- What is an inline function?
- What are the cons of using an inline function?
- What is the best practice of using an inline function?
- How does the `companion object` block work?
- Is it possible to create an extension function on the `companion object` of a class?
- Extension function as a member, possible? What are the benefits of declaring an extension function as a member?
- What is a spread operator? What is the recommended place to use it?
- What is the producer’s function? how to demonstrate it in Kotlin?
- What is the consumer’s function? how to demonstrate it in Kotlin?
- What is the higher-order function?
- How to compare two Strings in Kotlin?
- What is the difference between `==` and `===` ?

<br>

### 4. Android

- What is `Application` class?

- Difference between `Activity` and `Service`?
- Why do android apps need to ask permission like `INTERNET` or `LOCATION`?
- Differences between `serializable` and `Parcalable`?
- Why `serializable` body is empty? How is it doing?
- Which method in `fragment` runs only once?
- How does the activity respond when orientation is changed?
- How to know `configChange` happens in `onDestroy()` function?
- How to prevent the data from reloading when orientation is changed? <br>

  The most basic approach would be to use a combination of `ViewModels` and `onSaveInstanceState()`. A `ViewModel` is LifeCycle-Aware. In other words,
  a `ViewModel` will not be destroyed if its owner is destroyed for a
  configuration change (e.g. rotation). The new instance of the owner will
  just re-connected to the existing `ViewModel`. So if you rotate an `Activity`
  three times, you have just created three different `Activity` instances, but
  you only have one `ViewModel`. So the common practice is to store data in the
  `ViewModel` class (since it persists data during configuration changes) and
  use `OnSaveInstanceState()` to store small amounts of UI data.

- How to handle multiple screen sizes?
- What is `sw` keyword in `layout-sw600` folder meaning?
- What is the difference between `sw` and `w` and `h` as postfix in order to define the resources folder?
- What are the major differences between `ListView` and `RecyclerView`?
  - **ViewHolder Pattern**: `Recyclerview` implements the ViewHolders pattern
    whereas it is not mandatory in a ListView. A `ViewHolder` object stores
    each of the component views inside the tag field of the Layout, so you can
    immediately access them without the need to look them up repeatedly.
    In `ListView`, the code might call `findViewById()` frequently during the
    scrolling of `ListView`, which can slow down performance. Even when the
    `Adapter` returns an inflated view for recycling, you still need to look up
    the elements and update them. A way around repeated use of `findViewById()`
     is to use the "view holder" design pattern.

  - **LayoutManager**: In a `ListView`, the only type of view available is
    the `vertical` ListView. A `RecyclerView` decouples list from its container
    so we can put list items easily at run time in the different containers
    (linearLayout, gridLayout) by setting LayoutManager.

  - **Item Animator**: `ListViews` are lacking in support of good animations,
    but the `RecyclerView` brings a whole new dimension to it.

- Difference between `Intent` and `IntentService`?
  - `Service` is the base class for Android services that can be extended to
    create any service. A class that directly extends `Service` runs on the main
    thread so it will block the UI (if there is one) and should therefore either
    be used only for short tasks or should make use of other threads for longer
    tasks.

  - `IntentService` is a subclass of `Service` that handles asynchronous requests
   (expressed as `Intents`) on demand. Clients send requests through
   `startService(Intent)` calls. The service is started as needed, handles each
   `Intent` in turn using a worker thread, and stops itself when it runs out of
   work. [Read More on Mindorks's blog]("https://blog.mindorks.com/service-vs-intentservice-in-android")

- How to pass items to `fragment`?
- What is `Fragment`?
- How would you communicate between two `fragments`?
- Difference between adding/replacing `fragment` in `backstack`?
  - `replace` removes the existing `fragment` and adds a new `fragment`.
    This means when you press back button the fragment that got replaced will
    be created with its onCreateView being invoked.

  - `add` retains the existing fragments and adds a new `fragment` that means
    existing fragment  will be active and they wont be in 'paused' state hence
    when a back button is pressed onCreateView is not called for the existing
    fragment(the fragment which was there before new fragment was added).

    In terms of fragment’s life cycle events `onPause()`, `onResume()`,
    `onCreateView()` and other life cycle events will be invoked in case of
    `replace` but they wont be invoked in case of `add`.

- What is the difference between `dialog` and `dialogFragment`?
- What is the difference between `Thread` and `AsyncTask`?

- What is the relationship between the life cycle of an `AsyncTask` and an `Activity`? What problems can this result in? How can these problems be avoided? <br>

  An AsyncTask is not tied to the life cycle of the Activity that contains it.
  So, for example, if you start an AsyncTask inside an Activity and the user
  rotates the device, the Activity will be destroyed (and a new Activity
  instance will be created) but the AsyncTask will not die but instead goes
  on living until it completes.

  Then, when the AsyncTask does complete, rather than updating the UI of the
  new Activity, it updates the former instance of the Activity (i.e., the one
  in which it was created but that is not displayed anymore!). This can lead to
  an Exception (of the type java.lang.IllegalArgumentException: View not attached
  to window manager if you use, for instance, findViewById to retrieve a view
  inside the Activity).

  There’s also the potential for this to result in a memory leak since the
  AsyncTask maintains a reference to the Activity, which prevents the Activity
  from being garbage collected as long as the AsyncTask remains alive.

  For these reasons, using AsyncTasks for long-running background tasks is
  generally a bad idea . Rather, for long-running background tasks, a different
  mechanism (such as a service) should be employed.

- What is `lopper` and how it works?
- What are Handlers?
- What is the difference between `Foreground` and `Background` and `Bounded` service?
  - __Foreground Service:__ A foreground `service` performs some operation that
  is noticeable to the user. For example, we can use a foreground service to
  play an audio track. A `Notification` must be displayed to the user.

  - __Background Service:__ A background `service` performs an operation that
  isn’t directly noticed by the user. In Android API level 26 and above, there
  are restrictions to using background services and it is recommended to use
  WorkManager in these cases

  - __Bound Service:__ A `service` is bound when an application component binds
  to it by calling `bindService()`. A bound service offers a client-server
  interface that allows components to interact with the `service`, send requests,
  receive results. A bound service runs only as long as another application
  component is bound to it. [Read More](https://developer.android.com/guide/components/services)

- What are the limitations of using `Services` in android 8 and higher?
- What is `JobScheduling`?
- What is `contentProvider` and what is typically used for?

  A `ContentProvider` provides data from one application to another, when
  requested. It manages access to a structured set of data. It provides mechanisms for defining data security. [Learn more]("https://medium.com/@sanjeevy133/an-idiots-guide-to-android-content-providers-part-1-970cba5d7b42" "An idiot guide to android content providers").
  For further reading see the [official android documentation]("https://developer.android.com/guide/topics/providers/content-provider-basics" "Android official documentation")

  ![Conent Provider diagram](/assets/images/content-provider-diagram.png)

- What is the difference between `apply()` and `commit()` in `sharedPreferences`?
  - `commit()` writes the data **synchronously** and returns a boolean value of
    success or failure depending on the result immediately.

  - `apply()` is **asynchronous** and it won’t return any boolean response. Also
    if there is an `apply()` outstanding and we perform another `commit()`,
    The `commit()` will be blocked until the `apply()` is not completed.

- How you load your `Bitmaps`? What do you do for loading large bitmaps?
[Loading Large Bitmaps Efficiently in Android](https://android.jlelse.eu/loading-large-bitmaps-efficiently-in-android-66826cd4ad53 "Loading Large Bitmaps Efficiently in Android")

- How Android apps compiled and run?
  1. First step involves compiling the resources folder (/res) using the aapt
    (android asset packaging tool) tool. These are compiled to a single class
    file called R.java. This is a class that just contains constants.

  2. Second step involves the java source code being compiled to .class files
    by javac, and then the class files are converted to Dalvik bytecode by the
    “dx” tool, which is included in the sdk ‘tools’. The output is classes.dex.

  3. The final step involves the android apkbuilder which takes all the input
    and builds the apk (android packaging key) file.

- Do you know any about how `Dalvik` is working?
- What are the benefits of `ART` in comparison to `Dalvik`?
- What is `AAPT` ?
- What is Doze mode?

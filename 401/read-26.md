# Android fundamentals

**Android apps can be written using Kotlin, Java, and C++ languages. The Android SDK tools compile your code along with any data and resource files into an APK or an Android App Bundle.**

**An Android package, which is an archive file with an `.apk` suffix, contains the contents of an Android app that are required at runtime and it is the file that Android-powered devices use to install the app.**

**An Android App Bundle, which is an archive file with an `.aab` suffix, contains the contents of an Android app project including some additional metadata that is not required at runtime. An AAB is a publishing format and is not installable on Android devices, it defers APK generation and signing to a later stage. When distributing your app through Google Play for example, Google Play's servers generate optimized APKs that contain only the resources and code that are required by a particular device that is requesting installation of the app.**

**Each Android app lives in its own security sandbox, protected by the following Android security features:**

+ **The Android operating system is a multi-user Linux system in which each app is a different user.**

+ **By default, the system assigns each app a unique Linux user ID (the ID is used only by the system and is unknown to the app). The system sets permissions for all the files in an app so that only the user ID assigned to that app can access them.**

+ **Each process has its own virtual machine (VM), so an app's code runs in isolation from other apps.**

+ **By default, every app runs in its own Linux process. The Android system starts the process when any of the app's components need to be executed, and then shuts down the process when it's no longer needed or when the system must recover memory for other apps.**

**The Android system implements the principle of least privilege. That is, each app, by default, has access only to the components that it requires to do its work and no more. This creates a very secure environment in which an app cannot access parts of the system for which it is not given permission. However, there are ways for an app to share data with other apps and for an app to access system services:**

+ **It's possible to arrange for two apps to share the same Linux user ID, in which case they are able to access each other's files. To conserve system resources, apps with the same user ID can also arrange to run in the same Linux process and share the same VM. The apps must also be signed with the same certificate.**

+ **An app can request permission to access device data such as the device's location, camera, and Bluetooth connection. The user has to explicitly grant these permissions. For more information, see Working with System Permissions.**

## App components

**App components are the essential building blocks of an Android app. Each component is an entry point through which the system or a user can enter your app. Some components depend on others.**

**There are four different types of app components:**

+ **Activities**

+ **Services**

+ **Broadcast receivers**

+ **Content providers**

**Each type serves a distinct purpose and has a distinct lifecycle that defines how the component is created and destroyed.**

## Activating components

**Three of the four component types—activities, services, and broadcast receivers—are activated by an asynchronous message called an intent. Intents bind individual components to each other at runtime. You can think of them as the messengers that request an action from other components, whether the component belongs to your app or another.**

**An intent is created with an `Intent` object, which defines a message to activate either a specific component (explicit intent) or a specific type of component (implicit intent).**

**For activities and services, an intent defines the action to perform (for example, to view or send something) and may specify the URI of the data to act on, among other things that the component being started might need to know. For example, an intent might convey a request for an activity to show an image or to open a web page. In some cases, you can start an activity to receive a result, in which case the activity also returns the result in an Intent. For example, you can issue an intent to let the user pick a personal contact and have it returned to you. The return intent includes a URI pointing to the chosen contact.**

**For broadcast receivers, the intent simply defines the announcement being broadcast. For example, a broadcast to indicate the device battery is low includes only a known action string that indicates battery is low.**

**Unlike activities, services, and broadcast receivers, content providers are not activated by intents. Rather, they are activated when targeted by a request from a `ContentResolver`. The content resolver handles all direct transactions with the content provider so that the component that's performing transactions with the provider doesn't need to and instead calls methods on the `ContentResolver` object. This leaves a layer of abstraction between the content provider and the component requesting information (for security).**

**There are separate methods for activating each type of component:**

+ **You can start an activity or give it something new to do by passing an `Intent` to `startActivity()` or `startActivityForResult()` (when you want the activity to return a result).**

+ **With Android 5.0 (API level 21) and later, you can use the `JobScheduler` class to schedule actions. For earlier Android versions, you can start a service (or give new instructions to an ongoing service) by passing an `Intent` to `startService()`. You can bind to the service by passing an `Intent` to `bindService()`.**

+ **You can initiate a broadcast by passing an `Intent` to methods such as `sendBroadcast()`, `sendOrderedBroadcast()`, or `sendStickyBroadcast().**

+ **You can perform a query to a content provider by calling `query()` on a `ContentResolver`.**

## The manifest file

**Before the Android system can start an app component, the system must know that the component exists by reading the app's manifest file, `AndroidManifest.xml`. Your app must declare all its components in this file, which must be at the root of the app project directory.**

**The manifest does a number of things in addition to declaring the app's components, such as the following:**

+ **Identifies any user permissions the app requires, such as Internet access or read-access to the user's contacts.**

+ **Declares the minimum API Level required by the app, based on which APIs the app uses.**

+ **Declares hardware and software features used or required by the app, such as a camera, bluetooth services, or a multitouch screen.**

+ **Declares API libraries the app needs to be linked against (other than the Android framework APIs), such as the Google Maps library.**

### Declaring components

**The primary task of the manifest is to inform the system about the app's components. For example, a manifest file can declare an activity as follows:** <br>

![26](../img/26.png)<br>

**In the <application> element, the android:icon attribute points to resources for an icon that identifies the app.**

**In the <activity> element, the android:name attribute specifies the fully qualified class name of the Activity subclass and the android:label attribute specifies a string to use as the user-visible label for the activity.**

**You must declare all app components using the following elements:**

+ **`<activity>` elements for activities.**

+ **`<service>` elements for services.**

+ **`<receiver>` elements for broadcast receivers.**

+ **`<provider>` elements for content providers.**

**Activities, services, and content providers that you include in your source but do not declare in the manifest are not visible to the system and, consequently, can never run. However, broadcast receivers can be either declared in the manifest or created dynamically in code as BroadcastReceiver objects and registered with the system by calling registerReceiver().**


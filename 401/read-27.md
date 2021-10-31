# Intents, Activities, and SharedPreferences

**A task is a collection of activities that users interact with when trying to do something in your app. These activities are arranged in a stack—the back stack—in the order in which each activity is opened. For example, an email app might have one activity to show a list of new messages. When the user selects a message, a new activity opens to view that message. This new activity is added to the back stack. Then, if the user presses or gestures Back, that new activity is finished and popped off the stack.**

## Lifecycle of a task and its back stack

**The device Home screen is the starting place for most tasks. When a user touches the icon for an app or shortcut in the app launcher (or on the Home screen), that app's task comes to the foreground. If no task exists for the app (the app has not been used recently), then a new task is created and the main activity for that app opens as the root activity in the stack.**

**When the current activity starts another, the new activity is pushed on the top of the stack and takes focus. The previous activity remains in the stack, but is stopped. When an activity stops, the system retains the current state of its user interface. When the user performs the back action, the current activity is popped from the top of the stack (the activity is destroyed) and the previous activity resumes (the previous state of its UI is restored). Activities in the stack are never rearranged, only pushed and popped from the stack—pushed onto the stack when started by the current activity and popped off when the user leaves it using the Back button or gesture. As such, the back stack operates as a last in, first out object structure. Figure 1 visualizes this behavior with a timeline showing the progress between activities along with the current back stack at each point in time.**<br>

![1](https://developer.android.com/images/fundamentals/diagram_backstack.png)<br>

**Figure 1. A representation of how each new activity in a task adds an item to the back stack. When the user presses or gestures Back, the current activity is destroyed and the previous activity resumes.**

## Back press behavior for root launcher activities

**Root launcher activities are activities that declare an Intent filter with both ACTION_MAIN and CATEGORY_LAUNCHER. These activities are unique because they act as entry points into your app from the app launcher and are used to start a task.**

**When a user presses or gestures Back from a root launcher activity, the system handles the event differently depending on the version of Android that the device is running.**

### System behavior on Android 11 and lower

**The system finishes the activity.**

### System behavior on Android 12 and higher

**The system moves the activity and its task to the background instead of finishing the activity. This behavior matches the default system behavior when navigating out of an app using the Home button or gesture.**

**In most cases, this behavior means that users can more quickly resume your app from a warm state, instead of having to completely restart the app from a cold state.**

**If you need to provide custom back navigation, we recommend using the AndroidX Activity APIs, rather than overriding onBackPressed(). The AndroidX Activity APIs automatically defer to the appropriate system behavior if there are no components intercepting the system Back press.**

**However, if your app overrides onBackPressed() to handle Back navigation and finish the activity, update your implementation to call through to super.onBackPressed() instead of finishing. Calling super.onBackPressed() moves the activity and its task to the background when appropriate and provides a more consistent navigation experience for users across apps.**

### Background and foreground tasks

**A task is a cohesive unit that can move to the background when a user begins a new task or goes to the Home screen. While in the background, all the activities in the task are stopped, but the back stack for the task remains intact—the task has simply lost focus while another task takes place, as shown in figure 2. A task can then return to the foreground so users can pick up where they left off.**

**Consider for example, the following task flow for a current task (Task A) that has three activities in its stack, including two under the current activity:**

+ **The user uses the Home button or gesture, then starts a new app from the app launcher.**
**When the Home screen appears, Task A goes into the background. When the new app starts, the system starts a task for that app (Task B) with its own stack of activities.**

+ **After interacting with that app, the user returns Home again and selects the app that originally started Task A.**
**Now, Task A comes to the foreground—all three activities in its stack are intact and the activity at the top of the stack resumes. At this point, the user can also switch back to Task B by going Home and selecting the app icon that started that task (or by selecting the app's task from the Recents screen).**<br>

![2](https://developer.android.com/images/fundamentals/diagram_multitasking.png)<br>

**Figure 2. Two tasks: Task B receives user interaction in the foreground, while Task A is in the background, waiting to be resumed.**<br>

## Save key-value data 

**If you have a relatively small collection of key-values that you'd like to save, you should use the SharedPreferences APIs. A SharedPreferences object points to a file containing key-value pairs and provides simple methods to read and write them. Each SharedPreferences file is managed by the framework and can be private or shared.**

 **how to use the SharedPreferences APIs to store and retrieve simple values.**

### Get a handle to shared preferences

**You can create a new shared preference file or access an existing one by calling one of these methods:**

+ **`getSharedPreferences()` — Use this if you need multiple shared preference files identified by name, which you specify with the first parameter. You can call this from any `Context` in your app.**

+ **`getPreferences()` — Use this from an `Activity` if you need to use only one shared preference file for the activity. Because this retrieves a default shared preference file that belongs to the activity, you don't need to supply a name.**

**For example, the following code accesses the shared preferences file that's identified by the resource string `R.string.preference_file_key` and opens it using the private mode so the file is accessible by only your app:**

```Context context = getActivity();
SharedPreferences sharedPref = context.getSharedPreferences(
        getString(R.string.preference_file_key), Context.MODE_PRIVATE);
```

**When naming your shared preference files, you should use a name that's uniquely identifiable to your app. An easy way to do this is prefix the file name with your application ID. For example: `"com.example.myapp.PREFERENCE_FILE_KEY"`.**

**Alternatively, if you need just one shared preference file for your activity, you can use the `getPreferences()` method:**

```
SharedPreferences sharedPref = getActivity().getPreferences(Context.MODE_PRIVATE);
```

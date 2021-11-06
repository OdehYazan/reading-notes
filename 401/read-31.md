[Reading-notes](https://odehyazan.github.io/reading-notes/)

# Espresso

![image](../401img/esprsso.png)<br>

## Espresso Testing (read Overview, Basics, and Recipes, plus any others that look interesting)

* Use Espresso to write concise, beautiful, and reliable Android UI tests.

```java
public void greeterSaysHello() {
    onView(withId(R.id.name_field)).perform(typeText("Steve"));
    onView(withId(R.id.greet_button)).perform(click());
    onView(withText("Hello Steve!")).check(matches(isDisplayed()));
}
```

* The core API is small, predictable, and easy to learn and yet remains open for customization. Espresso tests state expectations, interactions, and assertions clearly without the distraction of boilerplate content, custom infrastructure, or messy implementation details getting in the way.

### Target audience

* Espresso is targeted at developers, who believe that automated testing is an integral part of the development lifecycle. While it can be used for black-box testing

### Synchronization capabilities

* Each time your test invokes onView(), Espresso waits to perform the corresponding UI action or assertion until the following synchronization conditions are met:

1. The message queue is empty.
2. There are no instances of AsyncTask currently executing a task.
3. All developer-defined idling resources are idle.

### Packages

1. espresso-core - Contains core and basic View matchers, actions, and assertions. See Basics and Recipes.
2. espresso-web - Contains resources for WebView support.
3. espresso-idling-resource - Espresso's mechanism for synchronization with background jobs.
4. espresso-contrib - External contributions that contain DatePicker, RecyclerView and Drawer actions, accessibility checks, and CountingIdlingResource.
5. espresso-intents - Extension to validate and stub intents for hermetic testing.
6. espresso-remote - Location of Espresso's multi-process functionality.

## Ridiculous superpower: the Espresso Test Recorder

* The Espresso Test Recorder tool lets you create UI tests for your app without writing any test code. By recording a test scenario

* Espresso Test Recorder then takes the saved recording and automatically generates a corresponding UI test that you can run to test your app.

* Espresso Test Recorder writes tests based on the Espresso Testing framework

* The Espresso API encourages you to create concise and reliable UI tests based on user actions.

## Turn off animations on your test device

* Before using Espresso Test Recorder, make sure you turn off animations on your test device to prevent unexpected results.

## Record an Espresso test

* Espresso tests consist of two primary components: UI interactions and assertions on View elements.

* UI interactions include tap and type actions that a person may use to interact with your app
* Assertions verify the existence or contents of visual elements on the screen.

## Record UI interactions

* To start recording a test with Espresso Test Recorder, proceed as follows:

1. Click Run > Record Espresso Test.
2. In the Select Deployment Target window, choose the device on which you want to record the test. If necessary, create a new Android Virtual Device. Click OK.
3. Espresso Test Recorder triggers a build of your project

## Add assertions to verify UI elements

* Assertions verify the existence or contents of a View element through three main types:

1. text is: Checks the text content of the selected View element
2. exists: Checks that the View element is present in the current View hierarchy visible on the screen
3. does not exist: Checks that the View element is not present in the current View hierarchy

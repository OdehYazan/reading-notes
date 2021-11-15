[Reading-notes](https://odehyazan.github.io/reading-notes/)

# Notifications

## SNS: Getting Started

### To get start with Simple Notification Service (SNS):

1. **Create a topic**

2. **Create a subscription to the topic**
3. **Publish a message to the topic** 
4. **Delete the subscription and topic**


## SNS with Amplify (and Firebase)

### Usage of SNS(adding Push Notifications into their mobile app) with amplify:

1. **Asynchronous actions**, such as when an order is placed through an app, and confirmation or status notifications are sent to the user.
2. **Scheduled reminders**
3. **Instant messaging**, where your app provides two-way communication (i.e., chat).


---
## How ro create platform application in Amazon Simple Notification Service (Amazon SNS) to send push notifications to Android devices.

### - Add your project to Firebase

- To create your Android platform application in Amazon SNS, you must have credentials from Firebase Cloud Messaging (FCM).

### - Copy your FCM project's API key

1. In the Firebase console, choose your project.

2. Choose Project settings.

3. Choose Cloud Messaging.

4. Copy your FCM project's API key to your clipboard.

### - Create a platform application in Amazon SNS

1. Open the Amazon SNS console.

2. Choose Mobile. Then, choose Push notifications.

3. Choose Create platform application.

4. On the Create platform application page, under Details, do the following:

- Enter the name of your application.

- Choose Firebase Cloud Messaging (FCM).
- Enter the server key that you copied earlier, Under Firebase Cloud Messaging Credentials

5. (Optional) Set up event notifications and delivery status logging.

6. Choose Create platform application.




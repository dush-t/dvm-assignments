# **WhatsApp Clone**  
A simple clone of the popular app 'WhatsApp'. Go through the task given below to get started.  
## **Task**  
You have to create a simple app similar to WhatsApp in functionality and appearance. In other words, you would be creating UI similar to WhatsApp and adding chat functionality along with image sharing facility (user registration is also required).  
The app has been divided into multiple phases which are described below.  
### Phase 1: Clone the UI
1. Make a non-functional clone of the app. Take a look at [Building layouts](https://flutter.dev/docs/development/ui/layout/tutorial) page on Flutter Docs to get a basic idea of how to implement basic UI design. While working on the UI, following things have to be implemented -  
    - Create different screens for the 'CHATS', 'STATUS' and 'CALLS' tabs, similar to the original app.  
    - Work on the navigation feature for navigating from any one of the above tabs to another tab.  
    - Create the chat screen, which would be visible once the user taps on any of the personal chats (which are displayed under the 'CHATS' tab) on their device. 
    - Create two screens, which would allow the user to login or register in the app.
2. The user should be able to navigate from any tab to another by tapping on another tab.  
3. The user should be able to get to the personal chat screen whenthey tap on any of their contacts on 'CHATS' tab.  
4. You have to implement the app in Light mode only.  
### Phase 2: Implement authentication, Link the app to device contacts list  
1. Implement user authentication using ''. This can be done using Google's [Firebase authentication](https://firebase.google.com/docs/auth). This is necessary to identify the person to whom a message should be sent.  
2. For the app to send messages, the app would have to get the contacts list stored on the device using [contacts_service ](https://pub.dev/packages/contacts_service) package (Flutter) or [contacts-provider](https://developer.android.com/guide/topics/providers/contacts-provider) package (Android).  
### Phase 3: Chat Functionality  
1. Implement chat functionality. This means the users should be able to chat with each other i.e. the users should be able to see the messages they send or have been sent to them by other users.  
2. This will be done using [Cloud Firestore](https://firebase.google.com/docs/firestore) service of Google Firebase. The app chats can be saved and retrieved using this feature and messages can be seen again even if user closes the app and restarts it.  
### Phase 4: Implement Image Sharing  
1. Users should be able to share images with each other through chats.  
2. The image to be shared can be selected using [image_picker](https://pub.dev/packages/image_picker) package (Flutter). The image then needs to compressed using [flutter_image_compress](https://pub.dev/packages/flutter_image_compress) package (Flutter) before sending it to the server. 
3. After the image has been compressed, it can be sent to the server using [Cloud Storage](https://firebase.google.com/docs/storage) service of Google Firebase. The app would be able to store image shared by a user in the storage on the server, and display the image to the user with whom the images have been shared.  
### Time allotted -  
   - Phase 1:   
   - Phase 2:   
   - Phase 3:   
   - Phase 4:   
#
_Task compiled by [mihir1607](https://github.com/mihir1607) from BITS-ACM_

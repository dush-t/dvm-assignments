# **WhatsApp Clone**  
A simple clone of the popular app 'WhatsApp'. Go through the task given below to get started.  
## **Task**  
You have to create a simple app similar to WhatsApp in functionality and appearance. In other words, you would be creating UI similar to WhatsApp and adding chat functionality along with image sharing facility (the app would have offline support as well).  
The app has been divided into multiple phases which are described below.  
### Phase 1: Clone the UI
1. Make a non-functional clone of the app. While working on the UI, following things have to be implemented -  
    - Create different screens for the 'CHATS', 'STATUS' and 'CALLS' tabs, similar to the original app.  
    - Work on the navigation feature for navigating from any one of the above tabs to another tab.  
    - Create the chat screen, which would be visible once the user taps on any of the personal chats (which are displayed under the 'CHATS' tab) on their device.  
2. The user should be able to navigate from any tab to another by tapping on another tab.  
3. The user should be able to get to the personal chat screen whenthey tap on any of their contacts on 'CHATS' tab.  
4. You have to implement the app in Light mode only.  
### Phase 2: Chat Functionality  
1. Implement chat functionality. This means the users should be able to chat with each other i.e. the users should be able to see the messages they send or have been sent to them by other users.  
2. This will be done using [Cloud Firestore](https://firebase.google.com/docs/firestore) service of Google Firebase. The app chats can be saved and retrieved using this feature and messages can be seen again even if user closes the app and restarts it.  
### Phase 3: Add Offline Support  
1. Even if the device is offline and the app cannot interact with the server to send or retrieve data, existing chats should be visible to users.  
2. The messages can be saved offline using local database with the help of a Database Management System or DBMS ([MySQL](https://www.mysql.com/), for instance).  
3. As soon as the app is able to access the server, the app should be able to send any changes (that were made when the device was offline) to the server.  
### Phase 4: Implment Image Sharing  
1. Users should be able to share images with each other through chats.  
2. This can be done using [Cloud Storage](https://firebase.google.com/docs/storage) service of Google Firebase. The app would be able to store images shared by a user in the storage on the server, and display the images to the user with whom the images have been shared.  
### Time allotted -  
    - Phase 1:   
    - Phase 2:   
    - Phase 3:   
    - Phase 4:   
Task compiled by 

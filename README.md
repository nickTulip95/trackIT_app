# Project Description
 The purpose of this project will be to develop a social media application that is based around shared personal calendars. The app will be designed to run on Android systems. There are plenty of calendar applications that already exist, but they operate as an isolated calendar/agenda for an individual. Our application will allow external data/events from other users' calendars to be linked together allowing the app to create a shared calendar between users. This is beneficial over calendar apps that only show personal events/schedules as this app may also show the schedules of a user's friends, family, co-workers, etc...


 In our application users will have unique accounts. Users will have access to their own calendar and will be able to create events to add to their calendar. They can add events from other user's calendar. (friends/groups) They can allow events from this individual calendar to be shared to friends/groups. Users can add friends / create and join groups and can select which events from their personal calendar can be seen/linked to friends/groups. Users will be able to view a friend's calendar, but only see events that the friend has made public to them. Users in a group will be able to see a group calendar that contains events from other users in the group if those users have made those events public to the group. Shared calendar events will appear in a different colour than private calendar events. There will be an included chat messaging feature with a notification system for unread chat messages and upcoming events.


  We will also be including the following APIs to aid in the app's functionality:
   - Google Sign-In (https://developers.google.com/identity/sign-in/android)
    - We are planning for users to use their Google accounts to register with the app.
   - Google Calendar (https://developers.google.com/calendar/overview)
   - Google Maps (https://developers.google.com/maps/documentation/android-sdk/overview)

   For the back-end component, we will use Firebase. Firebase is a platform that allows for cloud NoSQL database storage called "Firestore". It has authentication integration with third party providers like Google and Facebook, putting less of a security burden on the login aspect of our application. It also has a *pay-as-you-scale* service, meaning that it would be free for our use case.
   - Firebase, Cloud Firestone (https://firebase.google.com/products/firestore)
   - Firebase, Authentication (https://firebase.google.com/products/auth)
   

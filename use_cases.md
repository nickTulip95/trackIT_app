## Creating A Group (done by Nick)

### Actor (User)
User with a verified google account.

### Pre-conditions
User must be logged into the application.

### Main-Flow
1. User selects Groups tab from the app's navigation bar.
2. The system loads and displays the user's groups with a create group option.
3. User selects create group option.
4. The system displays a create group window with empty fields.
5. User enters information for the group for each field.
6. User selects save option from the create group window.
7. The system confirms there are no mandatory fields missing information and prompts the user with a confirmation box.
8. User selects confirm option.
9. The system saves the group and displays an invite friend window for the user.
10. User selects zero or more friends from the window and selects invite option.
11. The system returns display to the Groups window.

### Alternate Flows
- If user does not enter mandatory information when creating the group and attempts to save:
	- The system will display an error message, informing the user that information is missing from mandatory fields.
	- The system will return back to the create group window.
- If user clicks on Back instead of Confirm when creating the group:
	- The system will return back to the create group window.
- If the user has no friends linked to the account:
	- The system will not prompt the user to invite friends after creating the group.

### Postconditions
After the group has been created an email notification will be sent to the user confirming the creation of the group. Any users invited to the group will receive an invitation in the Groups tab of their application as well as receive an email notification.

---
 
## Removing Event (done by Nick)

### Actor (User)
User with events registered in a calendar.

### Pre-conditions
User must have events in personal calendar and/or have administration rights to a group calendar that has events.

### Main-Flow
1. User selects event from a calendar.
2. The system opens a new UI window with more details and options for the selected event.
3. User selects remove event option from the new window.
4. The system creates a confirmation box for the user to confirm the removal.
5. User selects confirm option.
6. The system removes the event from the calendar and returns display to a grid view of the calendar the event was removed from. 

### Alternate Flows
- If a user attempts to remove an event from a calendar they do not have permissions for (eg. a group calendar):
	- The system will display an error message, informing the user they do not have permissions to remove events from this calendar and return display to the detailed view of the event.
- If a user clicks on cancel instead of confirm:
	- The system will return display to detailed view of the event.

### Postconditions
After event has been successfully removed, the system will send an email notification detailing the removal of the event to any users with permission to view the event.

---

## Updating Event (done by Nick)

### Actor (User)
User with events registered in a calendar.

### Pre-conditions
User must have events in personal calendar and/or have administration rights to a group calendar that has events.

### Main-Flow
1. User selects event from a calendar.
2. The system opens a new UI window with more details and options for the selected event.
3. User selects edit event option.
4. The system displays the edit event window with the current information from the event automatically filled into correct fields.
5. User selects field that needs to be updated.
6. User updates information in selected field.
7. Repeat steps 5 & 6 for all fields that need updating.
8. User selects Save option from the edit event window.
9. The system prompts the user with a confirmation box.
10. User selects confirm option.
11. The system changes the information for the event that has been updated by the user.
12. The system returns to display the detailed view of the event.

### Alternate Flows
- If a user attempts to update an event from a calendar they do not have permissions for (eg. a group calendar):
	- The system will display an error message, informing the user they do not have permissions to update events from this calendar and return display to the detailed view of the event.
- If a user clicks on cancel instead of confirm:
	- The system will return back to the edit event window.

### Postconditions
After event has been successfully updated, the system will send an email notification detailing the changes to the event to any users with permission to view the event.

---

## Creating and sharing calendar event (done by Aayushi)

### Actor (User)
User with a verified google account. 

### Pre-conditions
User must be authenticated into the application.

### Main-Flow
1. User navigates to "Calendar" icon on the bottom navigation bar.
2. The system UI presents a combined calendar view by default.
3. User clicks on + sign to create a new calendar event.
4. UI pops a view to add event details.
5. User adds the mandatory input fields and clicks "ok".
6. The system creates a calendar event an adds it according to the user's configuration. 

### Alternate Flows
- User clicks "cancel" instead of "ok" to calendar event
	- The event is not created.
- User does not add all the mandatory input fields.
	- The system highlights in red which fields are insufficiently filled.
- If a user adds another user to a calendar event that the other user may not want in their calendar.
	- The other user will receive a notification that they have been added to an event.
   	- User denies request.
      		- The event will not be added to their calendar
   	- User accepts request.
      		- The event is added to their calendar and appear in a different color to indicate that it's a shared event.
- User wants another event in their own calendar (wants a duplicate event).
   	- User clicks on the public/shared event
   	- Once the event expands, user clicks to view options
   	- User clicks copy
	- The system creates a duplicate event in the user's own calendar. The UI view pops and displays the top-view navigation.


### Postconditions
After a user has added a calendar event and shared it with other people.
- Notifications will be sent to the other user
- User profile will show their public/tagged events in calendar.

---

## Sending a Message in the Chats (done by Aayushi)

### Actor (User)
User with a verified google account.

### Pre-conditions
User must be authenticated into the application.

### Main-Flow
1. User clicks on the "Chat" icon on the bottom navigation bar.
2. The system opens a list of all recents chats and a search feature that allows user to look up other users to interact with.
3. User clicks the search bar.
4. The UI window opens a scrollable card list view of all other users. UI also shows the search icon.
5. User types into the search bar.
6. The system performs queries for characters matching users in the friends list. UI shows users in most-character-matching order.
7. User selects a user to chat with.
8. The UI window displays the chat abilities and most recent message exchanges between the users.
9. User types in a message, and hits the send button.
10. The UI shows the message chat bubble sent with a buffer icon next to it.
11. Message is sent to the server and delivered to the other user. (which they will receive notification for). 
12. The UI shows the message has been delivered by adding a small checkmark icon next to the chat bubble. The system adds the new message to the users chat history.

### Alternate Flows
- If a user has an empty search entry.
	- UI will show its default: all users in a scrollable card list view.
- If a user has no friends linked to the account
	- The system will have a card view that prompts the user to add friends.
- If a user’s message isn’t delivered.
	- Instead of the small checkmark, there will be an exclamation icon.
- If a user's message isn't delivered and they exit the chat between the users.
	- The system does not add undelivered messages to chat history & chat bubble of undelivered message(s) is deleted.
	

### Postconditions
After the user's message has been delivered, UI shows all message exchanges between the users with the most up-to-date information. 

---

## Responding to Friend Requests (done by Aayushi)

### Actor (User)
User with a verified google account.

### Pre-conditions
User must be authenticated into the application.

### Main-Flow
1. User clicks on the "Notifications" icon on the bottom navigation bar.
2. The UI window displays all notifications and friend requests. Friend requests notifications prompt “view” and “delete”.
3. User clicks on one of the friend request “view” button.
4. The system fetches the other user’s profile, and two buttons on top of the UI allows “accept” or “deny” request.
5. User accepts friend request.
6. The system adds the friend to the user’s friends list. The system also removes the friend request notification, closes the other user’s profile and navigates back to notifications. 

### Alternate Flow
- If a user clicks “delete” instead of “view” friend request.
	- The system removes the friend request notification.
- If a user clicks “deny” instead of “accept” request after viewing the profile.
	- The system removes the friend request notification, closes the other user’s profile and navigates back to notifications. 

### Postconditions
After the user accepts the friend request, the friend will be sent a notification that the user and the friend are now friends on the application.
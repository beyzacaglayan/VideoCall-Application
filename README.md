<>main.html

On this page; I created two classes that allow us to enter username and room number input values. I created a separate class for the login button. I made all the visual arrangements, title,
logo and all button designs of this home page using css files. I implemented the process of creating a room with the username, participant ID, and room number using the JavaScript codes that
I will explain shortly.

JSmain.js

The username we received as display_name in the HTML file became the value of the DisplayName variable. The inviteCode variable took the value of the 'room' variable, i.e. the room number, 
in the Html file. If the inviteCode variable does not have a value, that is, if the room number is left blank, the system assigns a random number between 1 and 1000 as the room number. 
When the browser send button was pressed, it redirected us to a room with the value of the inviteCode variable.

![main](https://github.com/beyzacaglayan/VideoCall-Application/assets/54523165/d1bebd9f-f5e7-41aa-9248-4c095c2a82b7)

<>room.html

There are 3 separate screens on this page for the participant list, for messaging and for use during video calls. I created variables for the participant list and counter, the message 
screen, the screen where the camera will open, and its elements to be edited later via JavaScript. I gave the names of the 4 buttons on the camera screen: turning on the camera, turning on 
the microphone, sharing the screen and turning off these sharing.

JSroom.js

With getMembers, the list of all users in the room is displayed and their numbers are shared. With handleChannelMessage, when a user entered or left the room, when a message was shared, 
it was shown in this interface. When a message was sent with sendMessage, this message was displayed in the interface and the message writing area was cleared. Synchronously with 
addMessageToDom, the name of the user who wrote the message and the content of the message were added to the interface.

Using the switchToCamera variable, permissions were created for the user to turn on the camera, mute the microphone and video, and allow other users to join the conversation. 
handleUserPublished is called when another user turns on their microphone or camera. A new file was created to access the user's audio and video. The image of the new user who joined 
was placed in the appropriate place within the window.

handleUserLeft is called when a user leaves the conversation. With remoteUser, the user's data was deleted and the user's file was removed. With userIdInDisplayFrame, the user's image 
was deleted from the screen. ToggleMic was used to mute and unmute the user's microphone and video audio when the required buttons were pressed. With toggleCamera, the current status 
of the camera was monitored and the sound was turned on and off depending on the situation. At the same time, the status of the button has been set to turn the camera off or on.

When screen sharing was turned on, sharingScreen was set to «true» and the camera was turned off because a video was being shared at the same time. The user's camera permission has been
removed from the screen. The new value of userIdInDisplayFrame has been changed to shared display. The shared screen has been adjusted to be larger than other users' camera view. When 
the screen sharing button was clicked again, sharingScreen changed to «false» and the camera was shown again.

leaveStream is called when a user logs out. All parts of the user are stopped and turned off. The user's image was removed, the camera images on the screen were relocated, and a message
indicating that the user had left was displayed

![room](https://github.com/beyzacaglayan/VideoCall-Application/assets/54523165/14489fdb-b724-4606-9637-17004054de91)

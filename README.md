# Drawsome

Drawsome is a multi-player drawing app that allows friends to draw pictures and send them to one another to guess. It is written in Swift 3 (XCode8) using WebSockets.

## How it works
When a user launches the app, they are presented with two tabs: a drawing page and a guessing page. Once the first user opens the drawing page, they are presented with a word to draw as well as a timer, giving them 20 seconds to complete their drawing. As the user is drawing on the screen using their finger, the coordinates of the drawing are being stored in an array. 

This array is converted into a string, sent via the WebSocket, and then converted back into an array of coordinates before being output onto the guessing page to any other user with the app open on their device. 

The second user will go to the guessing page and see the drawing the first user has submitted. The word is also sent via the WebSocket so that once the second user guesses the drawing correctly, they see a success message. 

![Alt text](http://full/path/to/img.jpg "Optional title")

## Analysis
My team and I decided to go all out for our final project and use a new language (Swift), a new environment (XCode) and a new web technology (WebSockets) that none of us had used before. With just ten days to build the app from start to finish, using the user stories outlined below, it was a pretty difficult challenge. We made big leaps at the beginning, with a fully-outlined idea on day one and an MVP, a simple Swift app that allowed a user to draw on the screen with their finger, by day three. We hit some struggles once we tried to implement WebSockets, not having anticipated how tricky it would be to send drawing coordinates using a real-time technology. Despite the struggles, we not only achieved the fundamentals of the app but managed to implement a number of other features including a timer, colour-picker and guessing functionality.

## Project User stories
```
As a User
So I can draw a picture
I want to open the app and see a welcome screen
```
```
As a User
So I can draw a picture
I want to be able to use my finger to draw a line on the screen
```
```
As a User
So I can express my creativity
I want to be able to select from different colors to draw with
```
```
As a User
So I can show my drawings to friends
I want to be able to send my picture to them via the app
```
```
As a User
So I can create different drawings
I want to be to choose from diffrerent brushes
```
```
As a User
So I can play with friends
I want to be prompted to draw something by the app
```
```
As I User
So I can play with friends
I want to my friend to be able to guess what my drawing is
```
```
As a User
So I know if I guessed the picture correctly
I want to receive a message letting me know if I am right
```
```
As a User
So I don't dwell on my drawings
I want to be pressured with a timer to complete my drawing
```

# About the project

This is the code I wrote following the Classed tutorial on building a social network using React, Node & Firebase and is based on the SocialApe app ([back end repository](https://github.com/hidjou/classsed-react-firebase-functions), [front end repository](https://github.com/hidjou/classsed-react-firebase-client)) from the [Classed Full Stack React & Firebase tutorial series](https://www.youtube.com/watch?v=RkBfu-W7tt0&list=PLMhAeHCz8S38ryyeMiBPPUnFAiWnoPvWP) by [Ahmed Hadjou](https://github.com/hidjou)

#

# How to run the code:

The app is deployed on Google Firebase. Here is the [demo](https://socialape-69760.firebaseapp.com)

## 1: API Base URL

Add https://europe-west1-socialape-69760.cloudfunctions.net/api as the 'proxy' value in package.json

## 2: Install packages

run `npm install`

## 3: Run project

run `npm start`

## 4: Open it

go to http://localhost:3000

#

# User stories

## Description and features

For now, the application will have the following feature set:

// users routes

1. The user can sign up to create an account
   Back end: `app.post("/signup", signup);`
   Front end: `home` component with a pop up `signup` component using path `/signup`

2. The user can log into their account
   Back end: `app.post("/login", login);`
   Front end: `home` component with a pop up `login` component using path `/login`

3. An authenticated user can upload a picture via their profile screen
   Back end: `app.post("/user/image", FBAuth, uploadImage);`
   Front end: `home` component with an embedded `Profile` component without any path specified

4. An authenticated user can edit other profile details (other than their picture) in their profile screen
   Back end: `app.post("/user", FBAuth, addUserDetails);`
   Front end: `home` component with an embedded `Profile` component without any path specified

5. An authenticated can go to their user feed which will list their profile and posts that they created
   Back end: `app.get("/user", FBAuth, getAuthenticatedUser);`
   Front end: n/a

6. The app can fetch unauthenticated user details to be displayed in various components
   Back end: `app.get("/user/:handle", getUserDetails);`
   Front-end: `user` component with embedded list of `Screams` and a `StaticProfile` component with path `/users/:handle`

7. The app can fetch the authenticated user's list of notifications for unread likes and comments
   Back end: `app.post("/notifications", FBAuth, markNotificationsRead);`
   Front end: `Navbar` component with an embedded `Notifications` component without any path specified

// Scream routes

8. An unauthenticated user can get a list of posts
   Back end: `app.get("/screams", getAllScreams);`
   Frond end: `home` component displays feed with path `/`

9. An authenticated user can create a new post
   Back end: `app.post("/scream", FBAuth, postOneScream);`
   Front end: `Navbar` component with an embedded `PostScream` component opens up dialog box, no path specified.

10. An unauthenticated user can get the details of a post to be displayed in a dialog box
    Back end: `app.get("/scream/:screamId", getScream);`
    Front end: `Scream` component with a pop up `ScreamDialog` component using path `/users/${userHandle}/scream/${screamId}`

11. An authenticated user can delete a post that they created
    Back end: `app.delete("/scream/:screamId", FBAuth, deleteScream);`
    Front end: `Scream` component with a pop up `DeleteScream` component without any path specification

12. An authenticated user can like a post
    Back end: `app.get("/scream/:screamId/like", FBAuth, likeScream);`
    Front end: `Scream` component with an embedded `LikeButton` component without any path specification

13. An authenticated user can unlike a post
    Back end: `app.get("/scream/:screamId/unlike", FBAuth, unlikeScream);`
    Front end: `Scream` component with an embedded `LikeButton` component without any path specification

14. An authenticated user can comment on a post and read other comments displayed
    Back end: `app.post("/scream/:screamId/comment", FBAuth, commentOnScream);`
    Front end: `Scream` component with a pop up `ScreamDialog` component using path `/users/${userHandle}/scream/${screamId}`

#

This web applicaion is built using React, Node & Firebase and is based on the SocialApe app ([back end repository](https://github.com/hidjou/classsed-react-firebase-functions), [front end repository](https://github.com/hidjou/classsed-react-firebase-client)) from the [Classed Full Stack React & Firebase tutorial series](https://www.youtube.com/watch?v=RkBfu-W7tt0&list=PLMhAeHCz8S38ryyeMiBPPUnFAiWnoPvWP) by [Ahmed Hadjou](https://github.com/hidjou)

To be modified further by Kgotso Koete
Johannesburg, October 2019

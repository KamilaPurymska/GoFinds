# GoFinds

## Description

GoFinds is an app meant to be used for those moments where you are in a foreign city and want to know the name and history of a landmark. With GoFinds you can just take a picture of a landmark and you will get the name and the history of the given landmark. GoFinds also has a feature where you can check out the landmarks other users have travelled to by looking at their uploads in an instagram type of way.

## User Stories

- **404** - As a user I want to see a nice 404 page when I go to a page that doesn’t exist so that I know it was my fault 
- **500** - As a user I want to see a nice error page when the super team screws it up so that I know that is not my fault
- **sign up** - As a user I want to sign up on the webpage so that I can see all the events that I could attend
- **login** - As a user I want to be able to log in on the webpage so that I can get back to my account
- **logout** - As a user I want to be able to log out from the webpage so that I can make sure no one will access my account
- **add a post** - As a user I want to be able to add a post with a title, a description and a photo so I can post my landscape visits.
- **list of users** - As a user I want to be able to look at the list of all users so I can look at other users posts.
- **list of post** - As a user I want to see all the posts of a user so I can see where the user has been.
- **post detail** - As a user I want to be able to see the details of a post so I can understand the context of the post.
- **remove a post** - As a user I want to be able to remove a post so I can get rid of an unwanted post.
- **edit a post** - As a user I want to be able to edit a post so I can change the post in case of a mistake or change of mind.

## Backlog

- Landmark recognition
- Automatic landmark info
- User profile
- Favourites page
- Search for users
- Filter posts
- Search for location
- Responsive
- Tags

## Rutes

- GET /
  - render the homepage
- GET /auth/signup
  - redirect to / if logged in
  - reder signup(with flash msg)
- POST /auth/signup
  - redirect to / if logged in
  - Body:
    - Username
    - Password
- GET /auth/login 
  - redirect to / if logged in
  - reder login(with flash msg)
- POST /auth/login
  - redirect to / if logged in
  - Body:
    - Username
    - Password
- POST /auth/logout
  - redirect to / if logged out
  - Body: empty
- GET /users
  - renders the users list
- GET /users/:userid
  - renders users posts
- GET /posts/:postid
  - reders posts details
- POST /posts/:postid/remove
  - redirect to /users/:userid/posts/:postid if user id is not the same as logged in
  - body:
    - empty
- GET /posts/createpost
  - redirect to / if logged out
  - renders the createpost form
- POST /posts/createpost
  - redirect to / if logged out
  - body:
    - title
    - description
    - img

## Models

User Model
```
-Username
  -type: string
  -required: true
  -unique: true
-Password
  -type: string
  -required: true
```
  
Post Model
```
-ID
-Title
  type: string
  required: true
-Description
  type: string
-Image
  type: string
  required: true
-User ID owner
  type: string
  required: true
```

## Links

### Wire frame

[Wireframe link](https://rb2xgr.axshare.com/#g=1&p=wireframes)

### Kanban

[Kanban Link](https://drive.google.com/file/d/15ywGdLa5WJ4j7CFvKpGtPCQ-bx-wZO-j/view)

### Git

[Repository Link](http://github.com)

[Deploy Link](http://heroku.com)

### Slides

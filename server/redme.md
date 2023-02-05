# Capstone back_end

### **.gitignore file**

- all file  that we don't want to published on github will be mention here 

### **Difference  between helper and utils folder and lib**


- function that's not having  peer dependencies on project is created in utils folder **(stateless function)**
- function that have  dependencies on project will create inside helper folder **(statefull function)**
- all lower level component that might be used in more than one place and behave like component will store here `example emailValdiation,passwordValidation,...`


### **Assets folder**
-  all file that  are static will be add in the assetd folder
###  **config**
- db configuration or apllication level configuration will be store here example-
```javascript
{
port:4040,
 DB_URL: 'mongodb://localhost/capstone', 
 SECRET_KEY: 'block_app'
}
```

### **middleware folder**

- all thinks that will perform before performing  actual or targeted task will created iniside middleware folder
example - `token creation ,token verification..`


## **model** 
> schema  related file will store in model it's initial skeleton  for a particular feature  in a application

` it's  has different file in it  `

- `auth.model` **(all schema  file relate to auth will be created in auth.model folder )**
- `post.model` **(all  schema  file related to post will be created in post.model folder) initially a singale schema file for a project may be in future will  seprate blog or post by it's type to increase search optimization using indexing method that's why we create a folder for it**

- `message.model` **(all schema relate to message will created here in this folder example- message schema , message-like schema and others)**


- `notification.model.js` ** will create simple model file for it because we just want to  store status about particular information that user perfor and that's `send or unsend` **

- `conversation.model.js` **skeleton for conversation between two user**

## **Router**

> api related file will be add in router folder

### auth.router.js

- **POST req** `/capstone/api/v1/auth/signup`
- **GET req** `/capstone/api/v1/auth/signin`
- **PATCH req**` /capstone/api/v1/auth/forgetpassword`
### profile.router.js 
- **GET req**   ` /capstone/api/v1/profile/profile/:userId` to get profile details of a particular user
- **GET req**   ` /capstone/api/v1/profile/profilepic` get all profile pic added by a particular user
- **PATCH req**   ` /capstone/api/v1/profile/currentprofilepic` update profile pic of particular user by that user
- **PATCH req**   ` /capstone/api/v1/profile/userDetails` update details of particular user by that user
- **GET req**   ` /capstone/api/v1/profile/:userId/post` get all post created by a particular user

### post.router.js

**GET req** `/capstone/api/v1/post/recentpost`  get recent post
**POST req** `/capstone/api/v1/post/addpost` create a new post
**DELETE req** `/capstone/api/v1/post/:postId` delete a  post

- **PATCH req**   ` /capstone/api/v1/post/:postId` update post of 
- **GET req** `/capstone/api/v1/post/:postId` view a particular  post
### like.router.js

- **GET req**   ` /capstone/api/v1/like/:postId` get all like of a particular blog
- **POST req**   ` /capstone/api/v1/like/:postId` add new  like of a particular blog
**GET req**   ` /capstone/api/v1/dislike/:postId` get all dislike of a particular blog
- **POST req**   ` /capstone/api/v1/dislike/:postId` add new  dislike of a particular blog

### comment.router.js

- **GET req**   ` /capstone/api/v1/comment/:postId` get all comment of a particular blog
- **POST req**   ` /capstone/api/v1/comment/:postId` add new  comment of a particular blog
- **DELETE req**   ` /capstone/api/v1/comment/:postId` add new  comment of a particular blog
- **GET req**   ` /capstone/api/v1/like/:postId/:commentId` get all like of a particular comment
- **POST req**   ` /capstone/api/v1/like/:postId/:commentId` add new  like of a particular comment
- **GET req**   ` /capstone/api/v1/dislike/:postId/:commentId` get all dislike of a particular comment
- **POST req**   ` /capstone/api/v1/dislike/:postId/:commentId` add new  dislike of a particular comment
- **get req**   ` /capstone/api/v1/replay/:postId/:commentId` view all replay to a particular comment
- **POST req**   ` /capstone/api/v1/replay/:postId/:commentId` add new replay to a particular comment
- **DELETE req**   ` /capstone/api/v1/replay/:postId/:commentId/:replayId` delete replay to a particular comment

### **conversation.router.js**

- **GET req**   ` /capstone/api/v1/message/:userId` get all message from a particular user
- **POST req**   ` /capstone/api/v1/message/:userId` send a  new message to a particular user
- **DELETE req**   ` /capstone/api/v1/message/:userId/:messageId` delete a message from particular user
- **POST req**   ` /capstone/api/v1/message/:userId/:messageId/like` like a message from particular user
- **POST req**   ` /capstone/api/v1/message/:userId/:messageId/dislike` dislike a message from particular user



## **controller**

- `for every set of define routes we have controller`

- - auth.controller.js
- - profile.controller.js
- - post.controller.js
- - comment.controller.js
- - like.controller.js
- - message.controller.js




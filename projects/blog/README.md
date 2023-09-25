# Blog Project

This is a full stack blog application which has similar features to [Medium](https://medium.com/) or [Dev.to](https://dev.to/). This is overall a well rounded project and a good option to choose if you are looking to explore web development more in depth, or if you are learning a new language or framework and want to explore its features.

For this project we assume you will be creating a separate front end and back end project, each with a different technology or framework. A common stack for this project is the [MERN stack](https://www.mongodb.com/mern-stack) but any stack can be used.

## Backend (API)

### User stories

* A new user can register to the system.
* A new user must verify their email after registration.
* A user can login to they system if their email is verified.
* A user can update their bio.
* A user can create articles.
* A user can update their own articles.
* A user can delete their own articles.
* A user can search all articles in the system by title, body and user.
* A user can create a comment on an article.
* A user can create a comment on a comment.
* A user can like an article.
* A user can unlike an article.
* A user can like a comment.
* A user can unlike a comment.
* A user can follow another user.
* A user can unfollow another user.

### Bonus Features

* A user can change their email.
* A user can reset their password.
* A user can edit a comment.
* A user can delete a comment.
* A user can see if their username is available on register.

### API Routes

This is a list of all routes required in this project.

#### To authenticate attach token returned from login route to request Authorization header.

``` js
Authorization: Bearer <token>
```

<details>
<summary>Auth</summary>

``` js
// New user register
POST: '/auth/register',
query: [],
body: ['username', 'email', 'password']
```

``` js
// New user verify
POST: '/auth/register/verify',
query: [],
body: ['username', 'token']
```

``` js
// User login
POST: '/auth/login',
query: [],
body: ['username', 'password']
```

</details>

<details>
<summary>User</summary>

``` js
// Get all users and search by username and bio
GET: '/user',
query: ['username', 'bio'],
body: []
```

``` js
// Get individual user with articles
GET: '/user/:userId',
query: [],
body: []
```

``` js
// Update individual user (Only for requesting user)
PATCH: '/user/:userId',
query: [],
body: ['bio']
```

``` js
// Follow user
POST: '/user/:userId/follow',
query: [],
body: []
```

``` js
// Unfollow user
DELETE: '/user/:userId/follow',
query: [],
body: []
```

</details>

<details>
<summary>Article</summary>

``` js
// Get all articles and search by title, body and username
GET: '/article',
query: ['title', 'body', 'username'],
body: []
```

``` js
// Get individual article with likes and comments
GET: '/article/:articleId',
query: [],
body: []
```

``` js
// Create article
POST: '/article',
query: [],
body: ['title', 'body']
```

``` js
// Update article (Only for requesting user articles)
PATCH: '/article/:articleId',
query: [],
body: ['title', 'body']
```

``` js
// Delete article (Only for requesting user articles)
DELETE: '/article/:articleId',
query: [],
body: []
```

``` js
// Create comment on article
POST: '/article/:articleId/comment',
query: [],
body: ['body']
```

``` js
// Like article
POST: '/article/:articleId/like',
query: [],
body: []
```

``` js
// Unlike article
DELETE: '/article/:articleId/like',
query: [],
body: []
```

</details>

<details>
<summary>Comment</summary>

``` js
// Create comment on comment
POST: '/comment/:commentId/comment',
query: [],
body: ['body']
```

``` js
// Get comment with child comments
GET: '/comment/:commentId',
query: [],
body: []
```

``` js
// Like comment
POST: '/comment/:commentId/like',
query: [],
body: []
```

``` js
// Unlike comment
DELETE: '/comment/:commentId/like',
query: [],
body: []
```

</details>

### ERD

![ERD diagram](/projects/blog/ERD.png)

## Frontend (SPA)

### Pages

These are the pages that our SPA will render and the corresponding routes.

```
/auth/register
  - A new user can submit email password and username to register with the system.

/auth/verify
  -  A new user can enter the verification code from their email to verify account.

/auth/login
  - A user can submit their username and password to login

/
  - Home shows articles from all users you follow.

/user
  - Shows list of all users and allows you to search them.

/user/:userID
  - Shows user profile and their articles.

/article
  - Shows list of all articles and allows you to search them.

/article/create
  - Allows you to create a new article.

/article/:articleID
  - Shows article with comments.

/article/:update
  - Allows you to edit a given article.
```

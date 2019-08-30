# This Is Not Reddit (Title in Progress): Let's post some messages!

This application allows users to be able to see posts already on the website and
comments associated with the post. Once a user is signed in, they can create
their own posts and comments. When looking at a specific post, if the user is
the owner, they can edit or delete it. Users can currently only delete their
comments.

I chose this project as I am constantly on Reddit and sometimes with it had a
different layout or a Language feature on the button (this is something I'd
like to work on a future iteration).

## Setup Steps

1. [Fork and clone](https://github.com/elody-ramirez/capstone-frontend) this repository.
2. Run `npm install` to install all dependencies
3. Use `npm run start` to spin up the server.

## Important Links

- [Other Repo](https://github.com/elody-ramirez/capstone-frontend)
- [Deployed API](https://pacific-tundra-49128.herokuapp.com/)
- [Deployed Client](https://elody-ramirez.github.io/capstone-frontend/#/)

## Planning Story
When it comes to the server, I decided to create the post resource first as it would be the parent of comments. A post will have many comments. After setting up the model, routes, and adding it to server, I would test with curl scripts to ensure everything was working correctly. Then I would create the comment resource and do the same. I knew I wanted to populate owner and comments of a resource in the back end so I incorporated that as well.

Later on I found out that I need the owner of the comments to populate as well so I could access the owner's username. In order to do so I had to incorporate deep populate which was an interesting concept.

### User Stories

Version 1
- As a unregistered user, I would like to sign up with email and password.
- As a registered user, I would like to sign in with email and password.
- As a signed in user, I would like to change password.
- As a signed in user, I would like to sign out.
- As a unregistered user, I would like to see all users posts.
- As a unregistered user, I would like to see comments on those posts.
- As a signed in user, I would to create posts.
- As a signed in user, I would to comment on other users' posts.
- As a signed in user, I would to delete my posts and comments.
- As a signed in user, I would to update my posts.

Version 2
- As a signed in user, I would like to like or unlike posts and their comments.
- As a signed in user, I would to update my comments.
- As a unregistered user, I would like to see likes and unlikes on posts and their comments.

Version 3
- As a signed in user, I would like to add an icon for my user profile.
- As a signed in user, I would to update an icon for my user profile.

### Technologies Used

- Javascript
- Express.js
- Node.js
- MongoDB
- Mongoose
- NoSQL
- Heroku
### Catalog of Routes

Verb         |	URI Pattern
------------ | -------------
POST | /sign-up
POST | /sign-in
DELETE | /sign-out
PATCH | /change-password

Verb         |	URI Pattern
------------ | -------------
GET | /posts
GET | /posts/:id
POST | /posts
PATCH | /posts/:id
DELETE | /posts/:id

Verb         |	URI Pattern
------------ | -------------
GET | /comments
POST | /comments
DELETE | /comments/:id

### Unsolved Problems

- Still need to make it visually appealing
- Would like to eventually incorporate AWS so users can have user icons
- AWS would also help so users can post images

## Images

#### App Screenshot:
![screenshot](https://i.imgur.com/EOOBZbF.png)

---

#### ERD & Wireframes:
![ERD & Wireframes](https://i.imgur.com/2EhPojI.jpg.png)

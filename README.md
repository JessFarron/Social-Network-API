# Social-Network-API    [![Github license](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

## Table of Contents
* [Description](#description)
* [Installation and Setup](#installation-and-setup)
* [Usage](#usage)
* [Walkthrough Video](#walkthrough-video)  
* [API routes](#api-routes)
 
 ## Description
 This API provides the backend functionality for a social network web application. It allows users to share their thoughts, react to friends' thoughts, and create a friend list. The API is built using Express.js for routing, MongoDB as the database, and the Mongoose ODM. You can also choose to use a JavaScript date library or the native JavaScript Date object to handle timestamps.

## Installation and Setup
1. Clone the starter code repository to your local machine.
2. Create your own repository with the cloned code. Note: Do not fork the starter code repository.
3. Install the required dependencies using npm:
```npm i``` or ```npm install```

4. Start the API server:
```npm start```
The API server should now be running on http://localhost:3001.

## Usage
### API Routes
#### USER
```/api/users```
* GET /api/users: Retrieve all users.
* GET /api/users/:userId: Retrieve a single user by their _id along with populated thought and friend data.
* POST /api/users: Create a new user.
Request body json example:
```
{
  "username": "lernantino",
  "email": "lernantino@gmail.com"
}
```
* PUT /api/users/:userId: Update a user by their _id.
* DELETE /api/users/:userId: Remove a user by their _id.
BONUS: Associated thoughts of the deleted user will also be removed.
#### FRIEND
```/api/users/:userId/friends/:friendId```
* POST /api/users/:userId/friends/:friendId: Add a new friend to a user's friend list.
* DELETE /api/users/:userId/friends/:friendId: Remove a friend from a user's friend list.
#### THOUGHT
```/api/thoughts```
* GET /api/thoughts: Retrieve all thoughts.
* GET /api/thoughts/:thoughtId: Retrieve a single thought by its _id.
* POST /api/thoughts: Create a new thought.
Request json body example:
```
{
  "thoughtText": "Here's a cool thought...",
  "username": "lernantino",
  "userId": "5edff358a0fcb779aa7b118b"
}
```
* PUT /api/thoughts/:thoughtId: Update a thought by its _id.
* DELETE /api/thoughts/:thoughtId: Remove a thought by its _id.
#### REACTION
```/api/thoughts/:thoughtId/reactions```
* POST /api/thoughts/:thoughtId/reactions: Create a reaction stored in a single thought's reactions array field.
* DELETE /api/thoughts/:thoughtId/reactions/:reactionId: Pull and remove a reaction by the reactionId value.

Please refer to the walkthrough video for a practical demonstration of these API routes.

## Walkthrough Video
Please watch the following video to see the Social Network API in action and to understand how to use its routes effectively: 

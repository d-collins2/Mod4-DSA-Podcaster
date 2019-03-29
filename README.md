# Podcaster Back-End

This Rails app was deisgned to handle the database and API for Podcaster. 

## Contents

- [Essential Gems](#essentual-gmes)
- [Installation](#installation)
- [Models](#models)

## Essential Gems

This app was created by running ```rails new backend --api --database=postgresql``` , which prepared the application to perform as an API and to be configured for postgreSQL databases. [Json](https://github.com/flori/json) which allows us to parse and generate JSON. [Active Model Serializers](https://github.com/rails-api/active_model_serializers/tree/v0.9.3) is used to create custom JSON responses. 
## Installation 

To get started with this application, fork and clone the respository to your hard drive. ```CD``` into the project folder and run ```bundle install```. Once the gems have been installed, run ```rake db:setup``` to establish and seed the database. Make sure you have [postgreSQL](https://postgresapp.com/) installed and already running. Run ```rails start``` once the database has been set up to host the backend on your local server. If you're hosting both the front-end and back-end applications locally, also make sure you change the necessary URL variables in the React application so that changes will reflect your personal database. 

## Models

There are 3 models which Podcaster utilizes: 

### Playlist 

The ```Playlist``` model is a join table between a ```User``` and a ```Podcast``` which shows all of the relationships between users. The current user is only shown their relationships through a filter on the front-end. 

### Podcast 

The ```Podcast``` model is the most utilized model in the app. The one to many relationship between a ```Podcast``` and its ```Episodes``` allows any user to play the podcast's many episodes. Any ```User``` is allowed to save a podcast and store it in their own playlist for future use. 

### User
The User model handles all aspects of user accounts, including login/signup, and editing information.

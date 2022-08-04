
# Coffee Store 


### Notes
* For Frontend bootstrap must be added
* For Frontend and backend code must be indeded 
* All Error must be handle using try catch 
* All Notification managed with toast


## What it includes
* Password must be encrypted/hased with bcrypt js 
* Token using the jwt token 
* Send the email to new registered user
* Flash messages for errors and successes
* Add cron job for new registered users once user registerd after the one hour send email to that user

### User Model

| Column Name | Data Type | Notes |
| --------------- | ------------- | ------------------------------ |
| id | Integer | Serial Primary Key, Auto-generated |
| name | String | Must be provided |
| email | String | Must be unique / used for login |
| password | String | Stored as a hash |
| image | String | Not required  |
| createdAt | Date | Auto-generated |
| updatedAt | Date | Auto-generated |



### Coffee Model
| Column Name | Data Type | Notes |
| --------------- | ------------- | ------------------------------ |
| id | Integer | Serial Primary Key, Auto-generated |
| name | String | Must be provided |
| size | String | Must be provided |
| shots | String | Must be provided |
| typeOfMilk | String | Must be provided |
| createdAt | Date | Auto-generated |
| updatedAt | Date | Auto-generated |
| userId | Integer | From user table |



### Default Routes for user 

| Method | Path | File Name | Purpose |
| ------ | ---------------- | -------------- | ------------------- |
| POST | /auth/login | auth.js | Login user, return the jwt token |
| POST | /auth/signup | auth.js | Creates or Register User, Password must be encrypt using bcrypt  |
| GET | /profile | auth.js | Regular User Profile |



### Default Routes for coffee 

| Method | Path | File Name | Purpose |
| ------ | ---------------- | -------------- | ------------------- |
| GET | /api/coffees | coffee.js | Get all Coffes, It includes pagination, offset and searching option |
| POST | /api/coffees | coffee.js | Create new coffee |
| GET | /api/coffees/:id | coffee.js | Display a specific coffee |
| PUT | /api/coffees/:id | coffee.js | Edit a specific coffee |
| DELETE | /api/coffees/:id | coffee.js | Delete a specific coffee |


## User Stories
* As an unregistered user, I would like to sign up with email and password.
* As an unregistered user, I want to view a list of coffee.
* As a registered user, I would like to sign in with email and password.
* As a signed in user, I would like to change password.
* As a signed in user, I would like to sign out.
* As a signed in user, I would like to create, update a coffee which is added by me.
* As a signed in user, I would like to list my Coffee which is added by me.


### Advance 
* Added social login open like facebook, google
* Add google recaptch 



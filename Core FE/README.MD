
# Book Store 


### User Model

| Column Name | Data Type | Notes |
| --------------- | ------------- | ------------------------------ |
| id | Integer | Primary Key, Auto-generated |
| name | String | Must be provided |
| email | String | Must be unique / used for login |
| password | String | Stored as a hash |
| gender | String | Male / Female |
| interest | JSON | Stored as array |
| image | String | Not required  |
| created_at | Datetime | Auto-generated |
| updated_at | Datetime | Auto-generated |



### Book Model

| Column Name | Data Type | Notes |
| --------------- | ------------- | ------------------------------ |
| id | Integer | Primary Key, Auto-generated |
| userId | Integer | From user table (foreign key) |
| name | String | Must be provided |
| description | String | Must be provided |
| no_of_page | Integer | Must be provided |
| auther | String | Must be provided |
| category | String | Must be provided |
| price | Decimal | Must be provided |
| released_year | Integer | Must be provided |
| status | Boolean | True / False |
| created_at | Datetime | Auto-generated |
| updated_at | Datetime | Auto-generated |



### User Stories
* As an unregistered user, I would like to sign up with email and password.
* As a registered user, I would like to sign in with email and password.
* As a signed in user, I would like to change password.
* As a signed in user, I would like to sign out.
* As a signed in user, I would like to create, update and delete a books which is added by me.
* As a signed in user, I would like to list my books which is added by me.



### List view
* Show list in table view with (Book Id, Book Name, Book Desc, Book Author, No of Pages, Category, Price, Released Year, Options[Edit / Delete]) details.
* User can search by all fields (Book Name, Book Desc, Book Author, No of Pages, Category, Price, Released Year)
* Add pagination for long list of books.

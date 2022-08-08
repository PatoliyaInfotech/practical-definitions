
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
| author | String | Must be provided |
| category | String | Must be provided |
| price | Decimal | Must be provided |
| released_year | Integer | Must be provided |
| status | Boolean | True / False |
| created_at | Datetime | Auto-generated |
| updated_at | Datetime | Auto-generated |



### Default Routes for user 

| Method | Path | Purpose | Response|
| ------ | ---------------- | -------------- | ------------------- |
| POST | /auth/login | Login user | Return token |
| POST | /auth/signup | Creates User, Password must be encrypted  | Return result |
| GET | /profile | Get User Profile | Return user profile object |



### Default Routes for book 

| Method | Path | Purpose | Response |
| ------ | ---------------- | -------------- | ------------------- |
| GET | /api/books | Get all Books, It includes pagination, offset and searching option | All books array | 
| POST | /api/books | Create new book | Return book object | 
| GET | /api/books/:id | Get a specific book | Return book object | 
| PUT | /api/books/:id | Edit a specific book | Return book object | 
| DELETE | /api/books/:id | Delete a specific book | Return result | 
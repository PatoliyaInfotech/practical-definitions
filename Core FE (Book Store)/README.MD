
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
* Create two tables to display data 
    * (1) Using DataTable JQuery
    * (2) Custome Table
        * Create all possible function separately and reuse it
        For example - 
            * Show details of all books.
            * Show Book by Book Id.
            * Show Book by Book Name.
            * Show Book by Book Author and Book Name.
            * Show Book by having pages More than 100.
            * Show Book by Having pages Less than 90 & More than 25.
            * Show Book by Having pages Less than 90 & More than 25 & but not 80 Pages.
            * Show Book by having pages zero Pages.
            * Show Book which Released Year is 2015 & 2001.
            * Delete Book by Book Id.
            * Delete Book by Book Name.
            * Delete Book by Book Author and Book Description.
            * Delete Book by Book Name and Book Category.
            * Update Book by Book Id.
            * Update Book by Book Name.
            * Update Book by Book Author and Book Name.
            * Sort Book by Book Name.
            * Sort Book by Book Price.
            * Sort Book by Book Author.
            * Sort Book by Book No Of Pages.
            * Sort Book by Book Category.
            * Sort Book by Book Released Year.
        * Validations for all above.
        * ![Main](https://github.com/PatoliyaInfotech/practical-definitions/blob/master/Core%20FE%20(Book%20Store)/1.png)


### Development Tools and Frameworks
* JS
* Angular JS
* React JS
* Vue JS
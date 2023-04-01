# Third-party API integration


# Assignment

### General tips and tricks:

- Create a new Symfony, Laravel or “vanilla” PHP project, push it to
GitHub/Bitbucket/Gitlab repository, and when the assignment is done, send us a link
or an invite to the repository.
- Feel free to ignore the frontend part - save your time on CSS and styling. Functionality is
the most important part.
- Setup of the project must be as simple as possible - i.e. it is enough to use
Symfony/PHP built-in web server.
- Document the setup process - the simpler, the better. If you have further questions or
are unsure about something
- PHP 7.4 is the minimum, and if you can do it with 8.0+ - go right ahead!
- Minimal validation is enough, don't waste too much time on it - if the request passes,
it's ok


### Client

- Create a client for connection on Symfony Skeleton API
- Swagger documentation: [click here](https://symfony-skeleton.q-tests.com/docs)
    - Credentials:
        + email: ahsoka.tano@q.agency
        + password: Kryze4President
- Create a login page that uses Symfony Skeleton API, retrieve the access token
- Store the token using any storage you want


### Authors

- Fetch the list of Authors from the API, and display them in a table layout
- Enable a user to delete the author if there are no related books for this author
- Create a view page of single authors and their books
- Extra Bonus Part: Symfony CLI command to add a new author


### Books

- On single author view, enable the user to delete books (one by one)
- Create a page where the user can add a new Book and select Authors from a
dropdown menu
- Profile
- After the user logs in - show his first and last name on the base page layout.
- Add a logout link or button
# Practicle Definition (PHP Laravel)



### Title

- Product Data Importer with User Interface


### Objective

- Develop a Laravel application to fetch and display products from [DummyJSON.com](DummyJSON.com) API [https://dummyjson.com/products](https://dummyjson.com/products).


### Key Requirements

- Scheduled Data Fetching: Set up Laravel task scheduler for data fetching every 2 hours.
- API Pagination: Fetch 10 products per request, covering the first 3 pages.
- Database Storage: Use MySQL to store product details (ID, name, description, price, etc.).
- Error Handling: Implement robust error handling for API interactions and data processing.
- Data Update Mechanism: Update existing database entries to avoid duplicates.
- User Authentication: Create a system for user registration, login, and logout.
- Product Display: Implement a paginated display for authenticated users, showing 5 products per page
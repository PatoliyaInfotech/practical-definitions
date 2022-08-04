# Project Organizer

To practice N:M associations, we'll be adding the ability to categorize projects in an existing project organizer.

### Project Uses

Keeping track of projects is a necessary part of peoples' personal lives and businesses. Another individual has created a project organizer that allows you to create and view projects, but it'd be nice to categorize projects. Let's add this functionality!


### Routes Details 
* Routes
  * `GET /` - home page that lists all projects
  * `POST /projects` - creates a new project, then redirects back to `GET /`
  * `GET /projects/new` - page that has a form for creating a new project
  * `GET /projects/:id` - page that shows a specific project
* Models
  * `project`
   * Attributes: `name`, `githubLink`, `deployedLink`, `description`

## User Stories

* As a user, I want to categorize projects using different names. For example, all of my Node projects will be under the category "Node".
* As a user, I want to assign multiple categories to a single project.
* As a user, I want to view a list of categories I've assigned.
* As a user, I want to view projects associated with a category I've selected.

## Requirements

#### Part 1: Create a Category model

In order to add categories, create a model to store categories. It's recommended that you name this model `category`. It will store one attribute: the name of the category (a string).

#### Part 2: Create a Join model

In order to associate a category to many projects, and a project to many categories, we'll need to create an intermediate model. It's recommended that you name this model `categoriesProjects`. It will store two attributes: the id of a category (an integer) and the id of a project (an integer).

Once created, add the associations need to create a many-to-many association between categories and projects, using the join table you just created. Be sure to test this functionality by creating categories and projects, then seeing if you can include them in different queries.


#### Part 3: Integrate the model with the app

Now that the models have been created, you'll want to add the ability to create categories, view categories, and view projects by category to the rest of the application. Here is an approach you can take:

* Add a field to the existing view associated with `GET /projects/new`. This new field should accept a new category name. 
* Add to the `POST /projects` route to add the category to the project being created.
  * Category names should be unique; the category model should have no duplicates (HINT use `findOrCreate`).
  * Keep in mind that categories should be associated with projects (HINT use the `addCategory` method).
* Create the following routes for viewing categories and viewing projects by category:
  * `GET /categories` - show all the categories that exist
  * `GET /categories/:id` - show a specific category and all the projects with that category

## Bonuses

* Add the ability to edit and delete projects
* Add the ability to input and assign multiple tags via a comma separated list.
* Example: Inputting `node, pizza, music` would add all three tags to a project at once.

## Deliverables

Here are some example screenshots. Your finished deliverable will differ and include the desired functionality.

![New Project page/ categories](https://raw.githubusercontent.com/WDI-SEA/express-project-organizer/main/example-project-categories.jpg)

![Category page](https://raw.githubusercontent.com/WDI-SEA/express-project-organizer/main/example-categories.jpg)

![Category show page](https://raw.githubusercontent.com/WDI-SEA/express-project-organizer/main/example-categories-show.jpg)
# rails-interview-project-recipe-book
Quick Interview Project, that can be used to test candidate's ability. Feel free to use. 

# Recipie Book (Rails/JS)
Please write a simple recipe book management tool that lets you create recipes and search them. You are need to use Ruby on Rails (>=4.2) and any of the following frontend technologies React, Elm, VanillaJS or Stimulus for development.

## Requirements

Your app will implement 3 models.
* `Recipe` which contains the following attributes/validations:
  * `title` (string (0-1024 chars), unique)
  * `cuisine` (enum with 5 predefined values) 
  * `planning_to_cook_on` (datetime, must be in the future)
  * `tried_before` (boolean)
  * `instructions` (text, required, allows HTML tags, but no JS)
* `Ingredient` which contains the following attributes/validations:
  * `name` (string (0-255 chars), unique)
* `RecipeIngredient` which contains the following attributes/validations:
  * `qty` decimal
  * `unit` enum

`Ingredient` will represent ingredients such as salt, apples, chicken, etc
`RecipeIngredient` will contain qty and unit of measurement required for recipe,  `RecipeIngredient` should reference `Recipe`and `Ingredient`.

Your app will have thse 2 pages:

* The Recipe Create page. This should contain a form with the required Recipe. The form should have a button that lets a user add more ingredients & qty/measurement to the recipe. In the end there should be a save button which lets the user know if validations passed and a record was saved or not. 

* The Listing page. This page lists the recipes created (sorted by number of ingredients) and their details (including ingredients & qty/measurement). The Listing page also should contain a search field which dynamically searches recipe names and updates the listing page with the filtered results using React, Elm, VanillaJS or Stimulus 


## Q&A

* **Your app must be developed using Ruby on Rails (>= 4.2).**
* You may use a database of your choice.
* The search functionality on the listing page **must be** implemented using React, Elm, VanillaJS or Stimulus .
* The Recipe Create page can be developed using rails templating engine or React, Elm, VanillaJS or Stimulus . **It's completely up to you to choose.** There is no penalty for not using React, Elm, VanillaJS or Stimulus  for this development section.
* The forms **do not** need to be styled. You may leave the pages unstyled using only simple html tags if you wish to. However please add CSS / SCSS styling to indicate errors on the form. 
* HAML or SLIM for view templates is preferred but ERB is fine too. 
* The app should contain some basic tests using Minitest or Rspec. 
* There is no need to implement authentication or authorization.
* You may use any gem or library in your app to complete your project. 
* Github and stackoverflow are there to be used. :) 
* Your solution **must be uploaded to github.com** and **should include a README file** containing instructions on setting up the database and running the app, if anything special is required. 

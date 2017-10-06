## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 

1. List the five common HTTP verbs and what the purpose is of each verb.

GET - Displays information
PUT - Creates a new thing
POST - Updates entire entry
PATCH - Updates partial entry
DELETE - Destroys entry

2. What is Sinatra?

Like a simple version of rails. Useful for spinning up a small app

4. What is MVC?

The Model, Views and Controller

5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?

You want them to be as conventional as possible so it is easy for you or anyone else to read and navigate

6. What types of variables are accessible in our view templates without explicitly passing them?

instance variables

7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  
  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

  ```ruby
  get '/horses' do
    name = 'Mr. Ed'
    erb :index
  end
  ```

9. What's the purpose of ERB?

So you can interpolate ruby into an html file

10. Why do I need a development AND test database?

One for your actaul site and one just for your testing purposes

11. What is CRUD and why is it important?

Create Read Update Destroy. It is important because it is how

12. What does HTTP stand for? 

Hyper Text Transfer Protocol

13. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?

<% %> and <%= %>. The first way is how you interpolate without rendering to the page. The second is how you interpolate WITH rendering to the page

14. What's an ORM?

Object Relational Mapper. ActiveRecord does this. This is how you can turn a bunch of CSV data into OBJECTS on a table so they can be more easily manipulated.

15. What's the most commonly used ORM in ruby (Sinatra & Rails)?

ActiveRecord

16. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

GET - Read - Index page
GET - Read - Show page
GET - Create - New form
POST - Create - Creating new thing
GET - Update - Edit form
PUT/PATCH - Update - Update existing thing
DELETE - Destroy - Delete thing

17. What's a migration?

How you set up your database tables in your schema

18. When you create a migration, does it automatically modify your database?

No you have to run rake db:migrate for it to modify your database

19. How does a model relate to a database?

A model holds your validations and relationships for your database

20. What is the difference between `#new` and `#create`?

New just displayes the form for the creation method. Create actually saves it to the database

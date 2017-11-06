1. How do we make flash messages display on a page?

flash[:notice] = "Whatever"

and putting <p class="flash"><%= flash.notice %></p> in the application.html.erb

2. Where is cart information/temporary information usually stored?

cart info is contained in the cart poro
temporary info is stored in the session or with cookies


3. What might be some reasons not to store cart in our database? Are there any reasons why we would want to persist that information?

there would be no reason to keep temporary cart data in the database. once an order is placed i can see a reason to put it in the an order data table. but other than that i would think we would just store cart data in a cart session.

4. What is the purpose of the asset pipeline?

to precompile assets (stylesheets, images, javascript) to make them load faster into our webpage

5. Why do we precompile our assets?

it makes them load faster

6. What do each of the following tags do?

```ruby 
<%= stylesheet_link_tag "application" %>
- links the files in your assets/stylesheets folder to your application.html.erb
<%= javascript_include_tag "application" %>
- links the files in your assets/javascripts folder to your application.html.erb
<%= image_tag "rails.png" %>
- links the "rails.png" image in your assets/images folder to your application.html.erb
```

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?

When it tells you what is required to run it. Telling you if you need to bundle first or common bugs or issues there are and the work around for them. Benefits would be so your readme doesnt end up like factory_bot and it doesnt make any sense with minimal documentation for setting it up and using it.

8. What are the top four accessibility issues that we as developers should be aware of?

visual
audible
motor skills
cognitive ability

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?

in a controller. to execute an action before a thing is saved.

10. Given the following object, how would we create a scope for all users who are active?

```ruby 
User.create(name: "Happy", active: true)
```
create a current_user method in the users controller?

11. What is the difference between a scope and a class method?

a class method is a method to be called on a collection of objects. a scope is called on a collection that meet a certain criteria.

## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?

rails new <project_name> -T --database=postgresql --skip-spring --skip-turbolinks

2. What do Models generally inherit from in rails?

ApplicationRecord

3. What do Controllers generally inherit from in a rails project?

ApplicationController

4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?

resources :horses, only: [:show]

5. What rake task is useful when looking at routes, and what information does it give you?

rake routes

gives you your prefix, verb, URI pattern and controller action.

6. What is an example of a route helper? When would you use them?

items_route vs "/items"... to me, i think it is just preference? i like route helpers more

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?

_path returns everything after localhost:3000. _url returns the entire address including the https:// at the beginning

8. What are strong params and why are the necessary?

a private method to ensure only the params you allow can be passed through

9. What role does `form_for` play in helping us create our forms?

it is a helper method for making a form for a new instance of something or editing something

10. How does `form_for` know where to submit the user's input?

with the f.submit as the last line before the end

11. Create a form using a `form_for` helper to create a new `Horse`. 

<%= form_for @horse do |f| %>
  <%= f.label :name %>
  <%= f.text_field :name %>
  <%= f.label :breed %>
  <%= f.text_field :breed %>

  <%= f.submit %>
<% end %>

12. Why do we want to validate our models?

so no duplicate or partial instances can be saved to the database

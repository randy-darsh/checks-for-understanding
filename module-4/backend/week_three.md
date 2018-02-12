## Week Three - Module 4 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week. 

Note: When you're done, submit a PR. 

1. At a high level, what is Node?

node is the backend for javascript

2. What is Express? What is Express similar to in the Ruby world?

express is a framwork for node. and it is similar to rails in the ruby world.

3. How do we setup a route when creating an API with Node and Express? Please provide a code snippet.

`router.get('/welcome', function (req, res, next) { database.raw('query goes here') }`

4. What do we use Knex for?

knex is used as shorthand for SQL queries. very similar to ActiveRecord in ruby/rails

5. How could you organize your code to follow the MVC design pattern in your Quantified Self project?

i split the code out into models and controllers. controllers held the actions and the collections of data to be passed around. models held the SQL queries.

6. How do you execute raw SQL in node?

`database.raw('SQL querie')`

7. What are some advantages to having your front end and back end code live in separate applications? What are some disadvantages?

so they can be maintained separately. personally i think if i have my back end solid and i know it's done correctly. that makes it easier to do the front end afterwards. kind of like how we had to rails backend done for us first in QS. it allowed me to focus on front end because i know backend was done correctly. i would say a disadvantage would be if it's not done correctly you will probably spent a lot of time chasing a problem that wont be very hard to fix.

#### Review  

8. Describe DNS.

Domain Name Servers. It's how the internet interperets the name of the website you type into your nav bar and converts it to the actual numbered IP address.

9. What does writing clean code mean to you?

not repeating yourself. separating things out to keep SRP. when code looks aesthetically appealing. for example, i think the semicolons in javascript are disgusting. and since they arent really neccessary i dont use them.

10. If you were building an application that models hotels, what classes would you need? What classes would be responsible for what functionality?

hotel class with attributes like name, reservation_id, guest_id.
reservation class would have the guest information through the guest table
guests would have a reservation on the reservation table.
probably have a join table for guest reservations.
put a hotel id on the reservation table so they could have reservations at multiple hotels.

## Week Four Recap

### Instructions
Fork this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

* What is a cookie?

A cookie is your browser storing temporary data when you are not logged it

* What’s the difference between a session and a cookie?

a session is like a cookie but when you are logged in

* What’s a flash and when do you want to use flashes?

a flash is a temporary message that displays when an action is completed. for example: when you log in to an account or log out

* Why do people say “HTTP is stateless”?

because in and of itself it is stateless. state is held in your params or your session data

* What’s authentication? Explain.

that you are who you say you are. like when you log into an account you need your username and password that signifies you are you and not another user.

* What’s the difference between authentication and authorization?

authorization uses authentication as well. but, when authorization is implemented. you would be giving certain permissions to a user. like an admin.

* What’s a before filter?

so certain things arent displayed. for example: if you use it in your base controller for admin. before you allow them to see the page, check if they are authorized. otherwise render a 404.

* How do we keep track of a user once they’ve logged in?

with sessions

* When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?

namespace for admin and nest for a thing that belongs to something else. so namespace for /admin/categories so that only an admin can view it. and nest /categories/1/thing/1 for when you want to show a thing that is attached to a specific category

* At a high level, what tools can you use to implement authorization? How would you use them?

namespaceing and a base controller with a before action for current admin.

* What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?

enum is useful for when an attribute can only be a finite amount of things. so if an order is completed, cancelled you could put and enum and declare ordered? or cancelled? on it to quickly determine its status. you create them in the controller and call them wherever you need them.

* What are some strategies you can use to keep your views DRY?

making use of the body in your application.html.erb file

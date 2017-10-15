## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR.

1. At a high level, what is ActiveRecord? What does it do/allow you to do?

ActiveRecord is like short-hand SQL. It allows you to make querys to a database.


2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?

Because it inherits from ActiveRecord, you can call any methods ActiveRecord provides.

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?

a = Team.find(4)
a.name

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?

a =  Team.find(4)
a.owner

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.

https://www.dropbox.com/s/7k3ly3b6mqqtkyn/Screenshot%202017-08-27%2023.40.37.png?dl=0

6. Define foreign key, primary key, and schema.

foreign key - is another tables data column inserted into another table
primary key - is that colum on the other table
schema - is how your database knows what is what. the "schematic" for which your database knows what goes where when importing or storing data.

7. Describe the relationship between a foreign key on one table and a primary key on another table.

owner_id is the foreign key on the team table through id on the owner table

8. What are the parts of an HTTP response?


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.

group - takes an argument of a colum on a table to group the data together by the column
joins - joins takes an argument of another table to make them into a even larger table so you can manipulate both tables at once
count - turns the previous query into a hash with the key of whatever you gave it previously and the value of the number of items in that column 
find - finds the row of the id you pass it
maximum - finds the maximum value in the column you pass it

2. Name your three favorite ActiveRecord rake tasks and describe what they do.

rake db:drop - drops your database tables
rake db:create - creates your database tables
rake db:migrate - pushes your migrations into your schema

3. What two columns does `t.timestamps null: false` create in our database?

created at and updated at

4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?

one to many

5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?

a teacher will belongs_to :school
and a school will has_many :teachers
https://www.dropbox.com/s/ox07fk1hq83z6t8/Capture.PNG?dl=0

6. Give an example of when you might want to store information besides ids on a join table.

not sure on this one

7. Describe and diagram the relationship between patients and doctors.

a doctor will has_many :patients
a patient will belongs_to :doctor
https://www.dropbox.com/s/f7pnegirensup49/Capture1.PNG?dl=0

8. Describe and diagram the relationship between museums and original_paintings.

a museum will has_many :original_paintings
an original_painting will belongs_to :museum
https://www.dropbox.com/s/qp7z1imh7fsngni/Capture2.PNG?dl=0

9. What could you see in your code that would make you think you might want to create a partial?

edit and new forms being the same. so linking a partial will make it so you can just link to it in the erb file instead of making 2 files with the whole form in them

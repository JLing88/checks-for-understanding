## Week Two - Module 2 Recap

Fork or re-pull this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!).

Note: When you're done, submit a PR.


### Week 2 Questions

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
  
  `ActiveRecord is a ORM the enables us to generate SQL queries using Ruby methods and object models.`

2. Assume you have the following model:

```ruby
class Team << ActiveRecord::Base
end
```

What are some methods you can call on `Team`? If these methods aren't defined in the class, how do you have access to them?
    `all
    where
    find
    find_by
    update
    order
    group_by
    joins
    create
    new`

3. Assume that in your database, a team has the following attributes: "id", "name", owner_id". How would you find the name of a team with an id of 4? Assuming your class only included the code from question 2, how could you find the owner of the same team?
    `Team.find(4)
    Team.find_by(id: 4).pluck(:name)`

4. Assume that you added a line to your `Team` class as follows:

```ruby
class Team << ActiveRecord::Base
  belongs_to :owner
end
```

Now how would you find the owner of the team with an id of 4?
  `Team.join(:owners).where("id = 4").pluck(:name)`

5. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
  `Teacher has many students. Student belongs to teacher. Not sure how to draw in a text editor...`

6. Define foreign key, primary key, and schema.
  `Foreign key - an attribute which is a primary key in another table. It is how the two tables are related.`
  `Primary key - a unique (usually integer) attribute that identifies a record in a table.`
  `Schema - a diagram of the structure of a database. It includes table names and attributes`
  
7. Describe the relationship between a foreign key on one table and a primary key on another table.
  `The table with the foreign key 'belongs to' the other table. The table with the primary key 'has many' of the other table`
  
8. What are the parts of an HTTP response?

  `Status Line - protocol and status code`
  `Headers - additional information about the response. Server age, document type, etc`
  `Body - contains the actual information requested, typically an html file.`
  


### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
  `find - returns an object with a specific id`
  `where - finds an object matching a condition`
  `all - returns all objects in the table`
  `pluck - selects specified attributes`
  `joins - full inner join of two tables.`
  
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
  `rake db:migrate - runs all migrations`
  `rake db:drop - drops entire db`
  `rake db:create - creates db`
  
3. What two columns does `t.timestamps null: false` create in our database?
  `created_at and updated_at`
  
4. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
  `Schools have many teachers, teachers belong to schools. One to many. (In most cases. There are occasions where a teacher could work at mulitple schools.`
  
5. In the same database, what will you need to do to create this relationship (draw a schema diagram)?

  
6. Give an example of when you might want to store information besides ids on a join table.

  
7. Describe and diagram the relationship between patients and doctors.
  `many to many - doctors see many patients and patients could see many doctors`
  
8. Describe and diagram the relationship between museums and original_paintings.
  `one to many - museums have many paintings, while paintings belong to a single museum`
  
9. What could you see in your code that would make you think you might want to create a partial?

  `partials are used when html views are used in multiple places. for example forms for creating/updating things are usually very similar and a partial could be used to preserve the DRY principle`

### Self Assessment:
Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:

* I feel comfortable with the content presented this week
  `I'm somewhere in the middle. It's getting better, but still feeling a bit overwhelmed`
* I feel overwhelmed by the content presented this week


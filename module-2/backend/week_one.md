## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 1 Questions

1. List the five common HTTP verbs and what the purpose is of each verb.

  GET
  PUT
  POST
  DELETE
  PATCH

2. What is Sinatra?

  A Ruby framework for creating web apps.

3. What is MVC?

  Design pattern for creating web apps.

  Model
  View
  Controller

4. Why do we follow conventions when creating our actions/path names in our Sinatra routes?

  It provides a pattern for easy data manipulation, interacting with URI paths, and to make it easier for others to read.

5. What types of variables are accessible in our view templates without explicitly passing them?

  Anything that's declared within that block.

6. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?

  ```ruby
  get '/horses' do
    @count = 1
    erb :index
  end
  ```

7. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed` to the view?

get '/horses' do
  @name = 'Mr. Ed'
  erb :index
end

8. What's the purpose of ERB?

  It allows us to use Ruby statements and methods within the HTML code.

9. Why do I need a development AND test database?

  We can intentionally populate the test database with known values and keep the test sample small without affecting the real data. Having a smaller data set enables our tests to run much faster as well.

10. What is CRUD and why is it important?

  CRUD is important because it details all of the various database operations.

  Create
  Read
  Update
  Delete

11. What does HTTP stand for?

  HyperText Transport Protocol

12. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?

  <%= %>
  <% %>

13. What's an ORM? What does it do?

  Object relational model. It allows us to store objects in a database and interact with those objects. 

14. What's the most commonly used ORM in ruby (Sinatra & Rails)?

  ActiveRecord

15. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.

  GET - '/' goes to homepage
  GET - '/restaurants/new' goes to form to create new restaurant
  GET - '/restaurants' - shows all restaurants
  GET - '/restaurants/:id/edit' - goes to form to edit a restaurant
  POST - '/restaurants' - creates new restaurant
  PUT - '/restaurants/:id - updates a restaurant
  DELETE - '/restaurants/:id' - deletes a restaurant


16. What's a migration?

  Instructions on how to create a database. Contains the structure.

17. When you create a migration, does it automatically modify your database?

  No, you have to tell it what to do in the migration file.

18. How does a model relate to a database?

  The model represents the actions involved in interacting with the DB. A model represents the records stored in the DB.

19. What is the difference between `#new` and `#create`?

  New creates an object, create creates an object and enters it into the database.

20. Given a table named `animals`, What is the SQL query that will return all info from that table?
    `id     name        number_of_legs
    -----   ------      --------------
      1     panda       4
      2     giraffe     4
      3     whale       0
      4     bird        2
    `
    SELECT * FROM animals;

21. Using the same table, What is the SQL query that will return only the animals that has 4 legs?

  SELECT * FROM animals WHERE number_of_legs=4;

### Review Questions:  
22. Given a CSV file (“films.csv”) with these headers [id, title, description], how would you load these into your database to create new instances of Film?  

  CSV.foreach("path/to/file.csv", headers: true, header_converters: :symbol) do |row|
    Film.create(row)
  end

23. Given the following hash:
```
activities = {
  hiking: {cost: $0, supplies: ['hiking shoes', 'water', 'compass']},
  karaoke: {cost: $10, supplies: ['courage', 'microphone']},
  brunch: {cost: $35, supplies: ['mimosa flutes']},
  antiquing: {cost: $200, supplies: ['list of antique stores']}
}
```
How would I add 'granola bar' to things you should have when hiking?

  activities[:hiking][:supplies] << "granola bar"

24. What are the 4 Principles of OOP? Give a one sentence explanation of each.

  Inheritance - Child classes inherit all instance vars and methods of their parents
  Encapsulation - The concept of limiting data accessibility and packaging related data together.
  Polymorphism - The process of overriding an inherited method of child class to do something different that the parent method does.
  Abstraction - The idea of only having to deal with objects at a high level and having to know their inner-workings. Black box analogy.

### Self Assessment:
Choose One: (erase the others)
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:

* I feel overwhelmed by the content presented this week

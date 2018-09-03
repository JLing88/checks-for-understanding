## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 3 Questions

1. What is the entry at the command line to create a new rails app? 

  `rails new`

2. What do Models generally inherit from in rails?  

`ApplicationRecord::Base`

3. What do Controllers generally inherit from in a rails project? 

`ApplicationController`

4. How would I create a route if I wanted to see a specific horse in my routes file assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality? 

`resources :horses, only: [:show]`

5. What rake task is useful when looking at routes, and what information does it give you? 

`rake routes - gives the Prefix, Verb, URI Pattern and Controller Actions`

6. What is an example of a route helper? When would you use them? 

`ideas_path - it allows you to use the helper instead of writing out the full URI path. You can use them throughout the controller.` 

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix? 

`absolute vs relative path`

8. What are strong params and why are they necessary? 

`strong params enable us to pull out only the information we are looking for and prevent any malicious information getting passed into our methods. `

9. What role does `form_for` play in helping us create our forms? `form_for tells us what the form is being used for. `

10. How does `form_for` know where to submit the user's input? `It is a 'new' action uses the instance variable associated with it to pass the information into the create method.`

11. Create a form using a `form_for` helper to create a new `Horse`. 
  `<%= form_for @horse do |f| %>
     <%= f.label :breed %>
     <%= f.text_field :breed %>
    <% end %>`
     
12. Why do we want to validate our models? 
`It prevents objects being created in the db that have invalid or nil values. `

13. What are the steps of the DNS lookup? 
  `Look in the browser cache, Look in OS cache, ISP cache, Root server, back to client, who can then access the page`

### Review Questions
14. Within a feature test and given the following HTML, write the code necessary to target the following section and check the person's name?

  `<section id="personal-info">
    <h3><%= @person.name%></h3>
   </section>
  `
15. How would you call the method `prance` from within the method `move` on a `Horse` instance?

  `horse.move`
  
16. Given the following hash:

```ruby
furniture = {table: {height: 3, color: "red"}, purchased: true}
```
What is the different between how you would return true vs returning 3?  
  `furniture[table][height] == 3 furniture[purchased] == true`

17. What is inheritance?

  `When a class inherits from another class, it receives all of the variables and methods that are defined in the superclass`

### Self Assessment:
Choose One:

* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:

* I feel overwhelmed by the content presented this week

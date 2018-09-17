### Week 5 Questions

Re-pull from this repository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!).

Note: When you're done, submit a PR.

### Week 5 Questions
1. How do we make flash messages display on a page?
`You need to create the flash message in the controller, and then put a flash message html bit in the application.html file`

2. Where is cart information/temporary information usually stored?
`session`

3. What might be some reasons not to store a cart in our database? Are there any reasons why we would want to persist that information?
`It would make the database unneccessarily large storing cart objects that were never 'checked out' You might want to store that information for marketing efforts. For example, when Amazon tells you that you left something in your cart and never paid for the items.`

4. What is the purpose of the asset pipeline?
`The asset pipeline is for concatenating all css and js files. It allows for fewer calls from the browser to load a page. Speed would be the main purpose`

5. Why do we precompile our assets?
`Precompiling the assets compresses them into smaller files and makes lookups on that file much quicker.`

6. What do each of the following tags do?

```ruby 
<%= stylesheet_link_tag "application" %>
<%= javascript_include_tag "application" %>
<%= image_tag "rails.png" %>
```
`stylesheet_link_tag - allows up to 'link' a css/sass file to the html files`
`javascript_include_tag - does the same thing but for javascript .js files`
`image_tag - embeds an image in the html`

7. What are some of the elements of a great read me? What are some of the benefits of taking the time to update a readme for our project?
`A readme is usually the first thing someone looks at when looking at a project on Github. It should detail what the code does, as well as well-written instructions on how to use it. This could include a link to a live site if it is a standalone application.`

8. What are the top four accessibility issues that we as developers should be aware of?
`Vision impairment, Hearing impairment, Dexterity impairment, Cognitive impairments`

9. `before_save` is an example of a what? Where in our Rails application would we find a `before_save`?

`It is a callback. It would be found in a controller`

10. Given the following object, how would we create a scope for all users who are active?

```ruby 
User.create(name: "Happy", active: true)
```
```
scope :active, -> { where(active: true) }
```
11. What is the difference between a scope and a class method?
 `A scope is basically shorthand for a class method.`

### Review Questions:  
12. Given the following hash:  

```ruby
{cart: {"17" => 4, "204" => 52, "29" => 22}}
```

  12a. How would you add item with id of 48 with a quantity of 4?
  `session[:cart]["48"] = 4`
  12b. How would you increase the quantity of item 29? 
  `session[:cart]["29"] + whatever you want to increase it by`
  
  12c. How would you find out how many items your user is thinking about purchasing?  
   ```
   total = 0
   session[:cart].each do |item, quantity|
    total += quantity
   end
   ```
  
13. What is polymorphism? How does it relate to duck-typing? What are two ways you use this in everyday Rails applications?
`polymorphism is tied into inheritance in that a class that inherits from another is able to define a method also defined in the parent class and make the method have different behavior. Duck-typing essentially looks at the object calling the method and chooses the method that will work with that data type. You could use it in ruby in classes inheriting from other classes or with AR relations`

14. How would you clean the string "(630) 854-5483" to "630.854.5483"?  


### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few


Choose One:
* I feel comfortable with the content presented this week


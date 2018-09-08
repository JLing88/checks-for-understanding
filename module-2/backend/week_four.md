## Week Four Recap

### Instructions
Fork or re-pull this repository. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Week 4 Questions

1. What is a cookie?

 `A cookie is a file that essentially allows a user to experience a stateful web experience. It is stored on the client computer.`
 
2. What’s the difference between a session and a cookie?

`A cookie is stored on the client computer, a session is stored on the server.`

3. What’s a flash and when do you want to use flashes?

`A flash is a message that displays on a website. They are often used to let the user know of actions that are happening, errors, etc.`

4. Why do people say “HTTP is stateless”?

`Once a a connection between a client and server is terminated, the information about the user and their interaction with the site is lost. Cookies and sessions allow that information to be stored and accessed over multiple visits`

5. What’s authentication? Explain.

`Authentication is the process of a user proving their identification. It is often a username/password combination that is used for this process`

6. What’s the difference between authentication and authorization?

`Authentication is proving the user is who they say they are, while authorization is what they are allowed to do once authenticated. Authorization is essenstially limiting what users can and can't do. `

7. What’s a before filter?

`A before filter is a method that is run before any controller actions are taken`

8. How do we keep track of a user once they’ve logged in?

`Store the user information in a session hash.`

9. When do you want to namespace a resource? When do you want to nest a resource? What's the differences between those two approaches?

`Namespacing can be used for limiting page access such as actions that only an admin should be able to do. You essentially have 2 controllers which interact with the same models, but have different permissions. Nesting is used when a resource is dependent on another. For example, if a user should only be able to access their own items, you would nest item resources under the user resources.`

10. At a high level, what tools can you use to implement authorization? How would you use them?

`Adding a role attribute to a user object will allow different users to interact differently with a site. Also, storing the user information in the session will allow the logged in user info to persist between different pages. `

11. What's an enum, and what advantages does it offer? What data type needs to be in your database to use an enum? Where do you declare an enum?

`An enum is essentially an array that can store different user roles. It is accessed by using the array index. Enums in rails allow the use of methods to determine what value is stored in the attribute such as user? or admin?.`

12. What are some strategies you can use to keep your views DRY?

 `_form partials are a great way to reduce duplicate code in views.`


### Reviews Questions 
13. Given the following array of hashes, how would I print an alphabetical list of holidays?
```ruby
[
 {holiday: {name: "St Patrick's Day", supplies: ["Corned Beef and Cabbage"]}},
 {holiday: {name: "Halloween", supplies: ["Candy", "Costume"]}},
 {holiday: {name: "Hanukkah", supplies: ["Menorah"]}}
]
```  

```
array.sort_by do |element|
    puts element[:holiday][:name]
end
```

14. How would you clean incoming data to ensure "$300" or "300.00" is stored as 300? 

`.gsub(/\D/,'').to_i`

### Self Assessment:
Choose One:
* I was able to answer most questions independently, but utilized outside resources for a few

Choose One:
* I feel comfortable with the content presented this week

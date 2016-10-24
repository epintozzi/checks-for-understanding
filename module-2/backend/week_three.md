## Week Three Recap

### Instructions
Fork this repository. Be sure to pull the latest changes to your local repo. Answer the questions to the best of your ability.

Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week.

Note: When you're done, submit a PR with a reflection in the comments about how this exercise went for you.

### Questions

1. What is the entry at the command line to create a new rails app?
`rails new project_name`
<br>
<br>

2. What do Models generally inherit from in rails?
ActiveRecord
<br>
<br>

3. What do Controllers generally inherit from in a rails project?
ApplicationController
<br>
<br>

4. How would I create a route if I wanted to see a specific horse in my routes fitle assuming I'm sticking to standard conventions and that I didn't want other CRUD functionality?
If you only wanted the `index` route for example:
`resources :horse, only: [:index]`
or
`get '/horse' => 'horse#index'`
<br>
<br>

5. What rake task is useful when looking at routes, and what information does it give you?
`rake routes` shows you all the routes you have available, as well as the prefix, verb, url patter, and which controller and method you'd need to use for each.
<br>
<br>

6. What is an example of a route helper? When would you use them?
A route helper is a rails short cut that helps to link to the various routes without having to manually enter the path. You can use them in your views to link to any of your available routes.

<br>
<br>

7. What's the difference between what `_url` and `_path` return when combined with a routes prefix?
`_url` will return the full url and `_path` will just return the relative path.
<br>
<br>

8. What are strong params and why are the necessary?
Strong params are the permissible params that can be passed through our app.

<br>
<br>

9. What role does `form_for` play in helping us create our forms?
`form_for` is a shortcut that helps us create forms in rails. 
<br>
<br>

10. How does `form_for` know where to submit the user's input?
It knows depending on which http verb we're using.
<br>
<br>

11. Create a form using a `form_for` helper to create a new `Horse`. 
```ruby
<%= form_for @horse do |f| %>
  <%= f.label :horse_name %>
  <%= f.text_field :horse_name %>
  <%= f.submit %>
<% end %>

```
<br>
<br>

12. Why do we want to validate our models?
We validate our models to make sure they contain all the required attributes when they are created and to ensure uniqueness (when necessary).

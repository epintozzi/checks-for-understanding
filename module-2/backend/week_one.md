## Week One - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON!). 

Note: When you're done, submit a PR. 
<br/>
1. List the five common HTTP verbs and what the purpose is of each verb.
<br/>
* GET - used to retrieve data
* PUT - create a resource and we already know the URI to direct to
* POST - create a resource and the URI
* DELETE - delete a requested resource
* PATCH - update a resource
<br/>
<br/>
2. What is Sinatra?
<br/>
Sintra is a framework written in Ruby and is dependent on RACK. 
<br/>
<br/>
4. What is MVC?
<br/>
MVC stands for Model-View-Controller as a structure for creating a web app where each is responsible for a piece of an interconnected web app.
<br/>
<br/>
5. Why do we follow conventions when creating our actions/path names in our Sinatra routes?
<br/>
To be consistent with other applications and what other developers are doing.
<br/><br/>
6. What types of variables are accessible in our view templates without explicitly passing them?
<br/>
instance variables
<br/><br/>
7. Given the following block of code, how would I pass an instance variable `count` with a value of `1` to my `index.erb` template?
  <br/>
  ```ruby
  get '/horses' do
    erb :index
  end
  ```
<br/><br/>
@count = 1
<br/><br/>
8. In the same code block, how would I pass a local variable `name` with a value of `Mr. Ed`?
<br/>
name = "Mr. Ed"
erb: index, :locals => {:name => name}
<br/><br/>

9. What's the purpose of ERB?
<br/>
ERB is embedded ruby and we use this file type to pass ruby in to web pages
<br/><br/>
10. Why do I need a development AND test database?
<br/>
Development is what I use locally and test is for testing/on the server
<br/><br/>
11. What's responsive design?
<br/>
Responsive design accounts for all device/screen types and automatically adjusts based on the screen size that is in use.
<br/><br/>
12. What is CRUD and why is it important?
<br/>
C- create
R- read
U- update
D- delete
CRUD is important because it is so heavily used in many apps and cover the 4 primary actions taken upon pieces of data.
<br/><br/>
13. What does HTTP stand for? 
<br/>
Hyper text transfer protocol
<br/><br/>
14. What are the two ways to interpolate Ruby in an ERB view template? What's the difference between these two ways?
<br/>
<% ruby %> : this version executes code only
<%= ruby %> : this version executes code and returns a result
<br/><br/>
15. What's an ORM?
<br/>
Object Relational Mapping
<br/><br/>
16. What's the most commonly used ORM?
<br/>
java? 
<br/><br/>
17. Let's say we have an application with restaurants. There are seven verb + path combinations necessary to provide full CRUD functionality for our restaurant application. List each of the seven combinations, and explain what each is for.
<br/>

* GET: `/table` displays all items in the table
* GET `/table/:id` displays one itme in the table
* GET `/table/new` shows form for creating new item in the table
* POST `/table` creates new item in table
* GET `/table/:id/edit` shows for for user to update item in table
* PUT `/table/:id` updates item in table (from form)
* DELETE `/table/:id` deletes item from table
<br/><br/>
18. What's a migration? 
<br/>
A migration gives us the setup to create a new table in a database
<br/><br/>
19. When you create a migration, does it automatically modify your database?
<br/>
The database is updated after we create the table and run `db:migrate`
<br/><br/>
20. How does a model relate to a database?
<br/>
A model creates the table in a database and also manages validations and relationships with other models.

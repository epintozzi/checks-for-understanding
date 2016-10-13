## Week Two - Module 2 Recap

Fork this respository. Answer the questions to the best of your ability. Try to answer them with limited amount of external research. These questions cover the majority of what we've learned this week (which is a TON - YOU are a web developer!!!). 

Note: When you're done, submit a PR. 

1. At a high level, what is ActiveRecord? What does it do/allow you to do?
</br>
ActiveRecord is a tool that streamlines the CRUD process with built in methods for accomplishing CRUD tasks like create, edit, new, show, delete, and update. 
</br>
</br>

2. What is a migration?
</br>
When you create a migration, you are identifying what the migration is for (example: Create Students) and then it gives you the class you need to fill in with the information for creating the table of the model. Once you actually migrate, the table should be created in your database with the specified attributes. You can also use a migration for updating an existing table.
</br>
</br>

3. How does a table relate to a model?
</br>
Every model has a table in the database. The table defines the attributes of the model. For example, if the model is for `student` the table might define attributes like `id`, and `name`.
</br>
</br>

4. What kind of methods are `belongs_to`, and `has_many`? (i.e. class or instance) Give an example.
</br>
They are class methods. They are used to relate tables to each other. If you have a table for `students` and one for `teachers`, a `teacher` has many students assigned to their table (probably via a `student_id`) and a `student` will belong to only one teacher (in this example). If students actually do have more than one teacher, you'd need a joiner table to relate `students` and `teachers` to each other.
</br>
</br>

5. What do they allow you to do?
</br>
As noted above, the `has_many` and `belongs_to` methods allow us to relate tables to each other so that we can separate data to their own relevant tables (to follow the normal form) but then also allow us to still retrieve that related information from the appropriate table.
</br>
</br>

6. What's the difference between agile workflow and waterfall method?
</br>

 * Agile: Work happens in iterations. You plan for a small piece, build it out, test it, and then reconvene to plan the next piece and/or make changes to the previous iteration based on any new information we now have. 
 * Waterfall: All planning, design, decisions, etc are made up front for a very specific product. Then the work is completed exactly to spec and is tested. There is no room for changing or updating the planned spec with waterfall methodology.
</br>
</br>

7. What is the difference between `#new` and `#create`?
</br>

 * New instantiates a new object on a table, but does not save it unless told to do so.
 * Create both instantiates and saves a new object on a table.
</br>
</br>

8. At a basic level, what does cURL allow you to do?
</br>

</br>
</br>

9. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
</br>

</br>
</br>

10. Define foreign key, primary key, and schema.
</br>

</br>
</br>

11. Describe the relationship between a foreign key on one table and a primary key on another table.
</br>

</br>
</br>

12. What are the parts of an HTTP response?
</br>

</br>
</br>

13. `Rack::Test` allows us to test our controllers in isolation. What are some of the methods it gives us to simulate the request/response cycle?
</br>

</br>
</br>

14. Describe some techniques to make our Sinatra views more DRY. Give an example of when you would use these techniques.
</br>

</br>
</br>

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
2. Name your three favorite ActiveRecord rake tasks and describe what they do.
3. What's the difference between agile workflow and waterfall method?
4. What can you expect from a group as you begin working together? As you continue working together?
5. What two columns does `t.timestamps null: false` create in our database?
6. What cURL flag can you use to send a `POST` request?
7. What case does JSON (and JavaScript) use for multi-word variables?
8. What case does Ruby use for multi-word variables?
9. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
10. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
11. Give an example of when you might want to store information besides ids on a join table.
12. Describe and diagram the relationship between patients and doctors.
13. Describe and diagram the relationship between museums and original_paintings.
14. What are some examples of acceptable values for the parts of an HTTP response?
15. What types of output do we want to test when we test our controllers?
16. What could you see in your code that would make you think you might want to create a partial?
17. Why might you use a helper method?

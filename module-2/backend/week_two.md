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
cURL allows you to make GET and POST requests from the command line
</br>
</br>

9. In a database that's holding students and teachers, what will be the relationship between students and teachers? Draw the schema diagram.
</br>
	Teachers
	Has_many :students
  
  Students
  Belongs_to :teachers


</br>
</br>

10. Define foreign key, primary key, and schema.
</br>

* Primary key is the ID that is automatically assigned to a new item when it's created on a table.
* The Foreign key is the value that is used on one table to identify a related item on a different table. For example, on a table of students, there might be a column for `teacher_id` that represents the teacher of that student where the `teacher_id` matches that teacher's primary key on the table of teachers.
* The schema is created/updated when we do a migration. The schema creates our development database when we migrate and is also used as a blueprint for when we prepare our test database

</br>
</br>

11. Describe the relationship between a foreign key on one table and a primary key on another table.
</br>

As noted above, the primary key is the identifier of an object on its own table where the foreign key is the identifier of an object that is being related to on a table other than its own.

</br>
</br>

12. What are the parts of an HTTP response?
</br>

* Headers - This contains a lot of meta data with things like a timestamp, IP address, and format the body will be in.
* Status Code - the code is a number between 100-600. Each number means something about whether the request was successful or not, and if not, gives a clue as to what went wrong.
* Body - This is the information sent back; this may be empty or it may include content

</br>
</br>

13. `Rack::Test` allows us to test our controllers in isolation. What are some of the methods it gives us to simulate the request/response cycle?
</br>

</br>
</br>

14. Describe some techniques to make our Sinatra views more DRY. Give an example of when you would use these techniques.
</br>

* Views should not have any logic in them. Any logic that might be used over and over could be extracted out to its own method either in the model or a helper depending on what it does. One example might be when you are trying to format output to appear a certain way. You could write a method that does the formatting and call the formatted result in your view

</br>
</br>

### Optional Questions

1. Name your five favorite ActiveRecord methods (i.e. methods your models inherit from ActiveRecord) and describe what they do.
<br/>

* `Find_and_create_by` - this method takes the information for a new object in a table and checks to see if the object already exists. If it does, it just  performs the "find_by" portion. If it does NOT, then it creates a new record for the object. 
* `Exists?` - This method checks to see if a specific record exists or not
* `New_record?` - The method checks to see if the current data/record we're working with is new or not. If a record has already been saved, this will return `false`.
* `Pluck` - this method gives you an array of attributes based on whatever key you specify (ex: name, id, etc)
* `Where` - this method finds all records that contain the specified parameter. For example, `Object.where(name: "Erin")` would return an array of all record in the table where the name is equal to "Erin".
</br>
</br>

2. Name your three favorite ActiveRecord rake tasks and describe what they do.
</br>
</br>

* Db:create - this creates a database if it doesn't already exist
* Db:create_migration - this preps the migration file so we can indicate the columns/attributes that should be in the table.
* Db:migrate - this creates or updates tables in our database
</br>
</br>
3. What's the difference between agile workflow and waterfall method?
</br>
</br>

* Agile - Agile workflow uses many iterations where we start by determining one problem, writing code, testing, and analysis before we begin working on a new problem/feature. 
* Waterfall - This methodology calls for fully planning upfront. All decisions about the project/code are made before any code is written or tested. There are no iterations. 

</br>
</br>
4. What can you expect from a group as you begin working together? As you continue working together?
</br>
</br>

In the beginning when groups are just getting to know each other, they are often very polite/pleasant and just kind of feeling each other out. Over time, as members become more comfortable, more ideas will come up as well as sometimes conflict and tension as the group learns how to work together better.

</br>
</br>
5. What two columns does `t.timestamps null: false` create in our database?
</br>
</br>

* `Created_at`
* `Updated_at`
</br>
</br>
6. What cURL flag can you use to send a `POST` request?
</br>
</br>
7. What case does JSON (and JavaScript) use for multi-word variables?
</br>
camel
</br>
8. What case does Ruby use for multi-word variables?
</br>
snake
</br>
9. In a database that's holding schools and teachers, what will be the relationship between schools and teachers?
</br>

* A school `has_many` teachers and a teacher `belongs_to` a school.

</br>
10. In the same database, what will you need to do to create this relationship (draw a schema diagram)?
11. Give an example of when you might want to store information besides ids on a join table.
</br>

* You might do this if data on the join table is distinct from any of the info stored on the tables it joins. For example on a  join table of students and teachers, there might also be an attribute indicating which classroom they are in (though there migth be an argument for separating that to its own table as well).
</br>
12. Describe and diagram the relationship between patients and doctors.
13. Describe and diagram the relationship between museums and original_paintings.
14. What are some examples of acceptable values for the parts of an HTTP response?
</br>

* Header - 
* Status code - 404
* Body  - "Page not found"
</br>
15. What types of output do we want to test when we test our controllers?
</br>
Status codes?
</br>
16. What could you see in your code that would make you think you might want to create a partial?
</br>
Duplicate information

</br>
17. Why might you use a helper method?
</br>
To help keep methods/classes single responsibility

</br>

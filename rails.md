# Rails Assessments

Try your best to answer each question on your own before looking up the answer online. Once you're done writing your first answer, you can google the question and write the best answer you find.

### 1. What are some advantages of using Ruby on Rails?

The Rails framework is excellent for quick application development. It can absorb changes easily. Its good testing and test automation further promote rapid development and better quality of the product. With Ruby on Rails, web design gets more comfortable, and website development and maintenance more cost-effective.

### 2. How does Ruby on Rails use the Model View Controller (MVC) framework?

M: Maintains the relationship between Object and Database and handles validation, association, transactions
V: A presentation of data in a particular format, triggered by a controller’s decision to present the data.
c: The facility within the application that directs traffic, on the one hand querying the models for specific data, and on the other hand organizing that data (searching, sorting) into a form that fits the needs of a given view.

### 3. Using the information given, complete the steps for creating a new view in a rails app by filling in the blanks:

  1. Create a route: 
  
  code: 
  ```
  get '/about' => 'statics#about' 
  ```
  file: config/routes
  
  2. Create the controller
  
  code: 
  ```
  class Statics < ApplicationController
  
  def about 
    render "about.html.erb"
  end
  ```
  
  file: app/controllers
  
  3. Create the View
  
  code: 
  
  ```
  <div>This is the About page!</div>
  ```
  
  file: app/views/statics
  
  
### 4. Look at these sets of Rails routes, they are an example of which principle/term that we touched on briefly in class? Find the term, and explain why it is important.

```
/users/       method="GET"     # :controller => 'users', :action => 'index'
/users/1      method="GET"     # :controller => 'users', :action => 'show'
/users/new    method="GET"     # :controller => 'users', :action => 'new'
/users/       method="POST"    # :controller => 'users', :action => 'create'
/users/1/edit method="GET"     # :controller => 'users', :action => 'edit'
/users/1      method="PUT"     # :controller => 'users', :action => 'update'
/users/1      method="DELETE"  # :controller => 'users', :action => 'destroy'
```
These routes are created when we generate resources for rails. They are an easy-to-follow guide in order to make all the methods necessary for your app to have full CRUD functionality. CRUD is important because it allows the user to interact with the database in more ways than just GETting information.

### 5. What is the public folder used for in Rails?

The public folder contains dumb files that don't interact w/the backend.

### 6. Write a rails route for a controller called "main" and a page called "game" that takes in a parameter called "guess"

get '/guess' => 'main#game'

### 7. What are cookies for? How do they work? What is the difference between a session and a cookie?

The main difference between a session and a cookie is that session data is stored on the server, whereas cookies store data in the user's browser. Data stored in cookie can be stored for months or years, depending on the lifespan of the cookie. But the data in the session is lost when the web browser is closed.

### 8. In an html form, what does the "action" attribute tell you about the form?  How do you designate the HTTP verb for the form?

the action attribute will say whether the form item is a GET or a POST. you designate GET or POST in all caps.

### 9. Why would you use an instance variable in a rails controller?

The @version is available to be reused by all methods of the class instance. Unlike variables without the @ symbol which are called local variables. This means you can only access these local variables within THAT DECLARED METHOD. Limited to the local scope.

### 10. Name two rails generator commands and what files they create:

rails g model : Create rails files for model generator.
rails g resource: Creates a model, a migration file, a controller, and appropriate routes.

### 11. Rails has a great community and lots of free tutorials to help you learn. Here is a list of some tutorials to choose from, choose one, do it, and then report back here at least one thing you learned. You can also use a different resource if you find one that you like better. 

- https://www.tutorialspoint.com/ruby-on-rails/index.htm
- http://railsforzombies.org
- http://guides.rubyonrails.org/getting_started.html

I learned about some of the security measures available in Rails. I learned what SSL is. SSL (Secure Sockets Layer) is the standard security technology for establishing an encrypted link between a web server and a browser. This link ensures that all data passed between the web server and browsers remain private and integral. 
If you want to provide a secure connection through SSL, you can add "config.force_ssl = true" to your application config file.
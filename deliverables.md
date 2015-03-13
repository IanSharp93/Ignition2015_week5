#### Deliverables for week 5 Rails MVC
##### Odin Project Routing Guide Questions:
1. What is the "Root" route?  
    The most improtant route out there in the file. It is the Root of the url. It is where we land wih the url of the website or         app. 

  2. What are the seven RESTful routes for a resource?  
    The seven RESTful routes are : get or "index" all the post, "show" one specific post, the route that lests you create a         "new" post page, creating the data that we just posted, edit a post page, the route that allows us to update our existing         post, the last one allows us to delete the post.

  3. Which RESTful routes share the same URL but use different verbs?  
    The two routes that share the URL are: post "/posts" => and put "/posts/:id" =>
    
  4. How do you specify an ID or other variable in a route?  
    The way to specify an ID is wiht a colon. The colon allows Ruby to look for something to save as a ID in in the params hash. 
  5. How can you easily write all seven RESTful routes in Rails?  
    We can easily write these RESTful route by using this # in config/routes.rb

  6. What is the Rails helper method that creates the HTML for links?  
    Rails automatically generates helper methods for you which correspond to the names of all your routes. These methods end         with _path and _url. path, as in edit_post_path(3), will generate just the path portion of the URL, which is sufficient for         most applications. url will generate the full URL. The _url. one should be able to create the HTML link. 

1. Read the [Odin Project Controller Guide](http://www.theodinproject.com/ruby-on-rails/controllers)
1. Read the [Odin Project Views Guide](http://www.theodinproject.com/ruby-on-rails/views) and use it to <strong>answer the following questions</strong>
  1. What is a layout?  
    A layout has all the tags you need in making a webpage. It is the place where we need to put anything that will be in our         webpage. They live in the directory app/views/layouts. 

  2. What's the difference between a "view template" and a "layout"?
    The view template is simply the outline of of where the layout is. It is the template or folder that contains the layout.         where the layout its self holds all the rest of teh material for the website. 

  3. What is a "Preprocessor"?
    The preprocessors are these <%= and %> tags. They show waht will be embedded inside of our ruby code. They start and end the         part of code or information. This is Embedded Ruby (ERB). It's a special way of executing ruby code inside your HTML

  4. Why are preprocessors useful?  
    They are usually gems that either already come with Rails or can easily be attached to it. Rails then runs them                 automatically, so all you have to worry about is whether your file has the right extension(s) to tell the preprocessor to         run. They are also useful because they are easily able to define and get to work. 

  5. How do you make sure a preprocessor runs on your file?  
    You have to make sure that Rails starts from the outside in with extra extensions. So it first processes the file using ERB,         then treats it as regular HTML. That's fine because ERBs should output good clean HTML.

  6. What's the outputted filetype of a preprocessed *.html.erb file? What about a *.css.scss file?
    The outoutted filetype of *.html.erb is an ERB adn the filestyle for *.css.scss is a SASS file that then turns into a         regular CSS file. 

  7. What is the difference between the <%= and <% tags? 
    The difference between <% and <%= is that the <%= version actually displays whatever is returned inside the ERB tags. If you         use <%, it will execute the code but, no matter what is returned by that line, it will not actually display anything in         your HTML template

  8. What is a view partial?  
    View partial is a way to break our views up into partials in the Ruby on Rails. It allows our code to be more concise and         much easier to read. 

  9. How do you insert a partial into your view?  
    To insert a partial into the view we will have the partial named wiht an underscore such as _user_form.html.erb although the         partial is the user_form part of the code. So it is placed in behind the #. 

  10. How can you tell that a view file is a partial?
    We can tell that a view is a partial by being able to render the code using something like this <%= render                         "shared/some_partial"%>, although the folder of the partial would actually be called app/views/shared. 

  11. How do you pass a local variable to a partial?  
    To pass a local variable to a partial with the "render" code that should allow somehting like the @user variable to be              passed to the partial so the code can render the right form with that "render." The code may look like this <%= render          "shared/your_partial", :locals=> { :user => @user } %>.     

  12. What's the magical Rails shortcut for rendering a User? A bunch of Users?
    The magical extraordinary way to to render one user goes something like this. 
      # app/views/index.html.erb
      <h1>Users</h1>
      <ul>
        <% @users.each do |user|%>
          <%= render user %>
        <% end %>
      </ul>
    Then for a bunch of user the way is somehting more like dis.
      # app/views/index.html.erb
      <h1>Users</h1>
      <ul>
        <%= render @users %>
      </ul>

  13. What are asset tags and why are they used?
    These asset tags allows us to snag some images. It is a way to locate those files for you based on their name and then it they render the proper HTML tag. An example may look somehting like this. 
        <%= stylesheet_link_tag "your_stylesheet" %>
        <%= javascript_include_tag "your_javascript" %>
        <%= image_tag "happy_cat.jpg" %> 
  Which will then render this 
        <link data-turbolinks-track="true" href="/assets/your_stylesheet.css" media="all" rel="stylesheet">
        <script data-turbolinks-track="true" src="/assets/your_stylesheet.js"></script>
        <img src="/assets/happy_cat.jpg">

##### Link to Odin Project Basic Routes, Views and Controllers repo: [my odin repo](<https://odin-project-iansharp93.c9.io>)
        My Repo On GitHub: https://github.com/IanSharp93/Odin_Project.git 

##### Link to Hartl's Rails Tutorial Chapter 5 repo: [my hartl's repo](<https://github.com/IanSharp93/sample_app-1>)

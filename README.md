# Ignition2015_week5
Diving deeper in the MVC aspects of Rails

# Week 5: Rails MVC

#### Required 
1. Read the [Odin Project Routing Guide](http://www.theodinproject.com/ruby-on-rails/routing) and use it to <strong>answer the following questions</strong>
  1. What is the "Root" route?  
    The most improtant route out there in the file. It is the Root of the url. It is where we land wih the url of the website or app. 

  2. What are the seven RESTful routes for a resource?  
    The seven RESTful routes are : get or "index" all the post, "show" one specific post, the route that lests you create a "new" post page, creating the data that we just posted, edit a post page, the route that allows us to update our existing post, the last one allows us to delete the post.

  3. Which RESTful routes share the same URL but use different verbs?  
    The two routes that share the URL are: post "/posts" => and put "/posts/:id" =>
    
  4. How do you specify an ID or other variable in a route?  
    The way to specify an ID is wiht a colon. The colon allows Ruby to look for something to save as a ID in in the params hash. 
  5. How can you easily write all seven RESTful routes in Rails?  
    We can easily write these RESTful route by using this # in config/routes.rb
  ...
  resources :posts
  ...

  6. What is the Rails helper method that creates the HTML for links?  
    Rails automatically generates helper methods for you which correspond to the names of all your routes. These methods end with _path and _url. path, as in edit_post_path(3), will generate just the path portion of the URL, which is sufficient for most applications. url will generate the full URL. The _url. one should be able to create the HTML link. 

1. Read the [Odin Project Controller Guide](http://www.theodinproject.com/ruby-on-rails/controllers)
1. Read the [Odin Project Views Guide](http://www.theodinproject.com/ruby-on-rails/views) and use it to <strong>answer the following questions</strong>
  1. What is a layout?
  1. What's the difference between a "view template" and a "layout"?
  1. What is a "Preprocessor"?
  1. Why are preprocessors useful?
  1. How do you make sure a preprocessor runs on your file?
  1. What's the outputted filetype of a preprocessed *.html.erb file? What about a *.css.scss file?
  1. What is the difference between the <%= and <% tags?
  1. What is a view partial?
  1. How do you insert a partial into your view?
  1. How can you tell that a view file is a partial?
  1. How do you pass a local variable to a partial?
  1. What's the magical Rails shortcut for rendering a User? A bunch of Users?
  1. What are asset tags and why are they used?
1. (By Monday 3/9) By yourself, complete the [Odin Project: Basic Routes, Views and Controllers](http://www.theodinproject.com/ruby-on-rails/basic-routes-views-and-controllers)
  1. Skip step 1 of the Application Skeleton section.  As we did last week, you will:
    1. Create a new Rails workspace on C9
    1. Add `/.c9` to your `.gitignore` file
    1. Setup git and commit the project:
      1. `git init`
      2. `git add .`
      3. `git commit -m 'initial commit'`
    1. Create a new repo on GitHub without a `README` or `.gitignore`
    1. Add your remote and push to github (replace the `<username>` and `<repo>` with your username and repo name)
      1. `git remote add origin https://github.com/<username>/<repo>.git`
      2. `git push -u origin master`
1. (By Thursday 3/12) As a group, complete the Rails tutorial [Chapter 5](https://www.railstutorial.org/book/filling_in_the_layout#top). Make sure to trade off coding, one person should not write everything.  
  1. Pick up where you left on your week 4 assignment with your new partner.  One person should be new to the codebase, one should have been working on it the previous week.

#### Optional
- Read the [Rails Guide on Routing](http://guides.rubyonrails.org/routing.html)
- Read the [Rails Guide on Controllers](http://guides.rubyonrails.org/action_controller_overview.html)
- Read the [Rails Guide on Layouts](http://guides.rubyonrails.org/layouts_and_rendering.html)
- Read the [Odin Project Guide on Asset Pipelines](http://www.theodinproject.com/ruby-on-rails/the-asset-pipeline)

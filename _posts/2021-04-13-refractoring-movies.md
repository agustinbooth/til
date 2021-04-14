## Useful things from refractoring

# Routes

routes can be simplified by writing this way: (root is index page)

```
  root "movies#index"

  # Routes for the Movie resource:

  # CREATE
  post "/movies" => "movies#create"
```

routes can be name and appear in link/rails/info/routes

```
get "/movies/:id" => "movies#show", as: :details
```

to call routes we can use things like:

```
datails_path(42) #42 is the id
details_url(42) #42 is the id
```

instead of using "a href" we can use /link_to/ (rails can figure almost all the link if we are conventional)
  
 ```
   <%= link_to "Add a new movie", new_movie_path %>
   <%= link_to 'Edit movie', edit_movie_path %>
 ```
 # Render
 
 We can take out almost all render code if we are conventional
 
 ```
 #Example
 render "new"
 ```

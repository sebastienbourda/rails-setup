# Start new rails project

## Create new app

With tailwind CSS and postgresql as DB

```
rails new MY_NEW_APP_NAME --css tailwind --database=postgresql
```

## Customize homepage

1. Create pages controller

```
rails g controller Pages
```

2. Create routes

Add following to routes.rb :

```
root "pages#home"
```

3. Create home view

```
touch app/views/pages/home.html.erb
```

4. Create DB

```
rails db:create
```

## Install Devise

1. Add gem 'devise' to gemfile and run :
```
bundle install
```

2. Run :

```
rails generate devise:install
```

3. Follow instructions in console.
```
  <% if notice %>
    <p class="notice bg-green-100 border border-green-400 text-green-700 px-4 py-3 rounded relative" role="alert">
      <%= notice %>
    </p>
  <% end %>

  <% if alert %>
    <p class="alert bg-red-100 border border-red-400 text-red-700 px-4 py-3 rounded relative" role="alert">
      <%= alert %>
    </p>
  <% end %>
```


4. Set User model (change if you need "admin or other"):
```
rails generate devise User
```

5. Run :
```
rails db:migrate
```

6. Run project with :
```
bin/dev
```

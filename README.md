# My first heroku app!

Used a Udacity course.

## The steps:

1. (heroku account)
2. (heroku toolbelt)
3. `heroku login`
4. (git)
5. (fork)
6. (clone)
7. `cd galeria`
8. `git status`
9. `heroku create`
10. `git remote -v`
11. `git push heroku master`
12. `heroku open`
13. (I changed my app’s URL/name to "my-galeria" at https://dashboard.heroku.com/)
14. `git remote rm heroku`
15. `heroku git:remote -a my-galeria`
16. `heroku open` (should take you to https://my-galeria.herokuapp.com/)

## Staging = mock test; Deploying = final production push

https://devcenter.heroku.com/articles/multiple-environments

## Local computer vs remote server

local computer:

`<command>`

remote server:

`heroku run <command>`

## Setting up a database for the app:

1. `git checkout -b pg origin/pg` ("pg" = PostgreSQL database for Ruby as required by Heroku)
2. (postgresql: http://postgresapp.com/ or http://www.postgresql.org/download/windows/ or http://www.postgresql.org/download/linux/ubuntu/)
3. `bundle install` (to check the ActiveRecord gem that translates ruby to sql is stable locally)
4. `ruby app.rb`
5. (visit localhost:4567 to see a Sinatra error)
6. (shut down server)
7. `rake db:migrate` (to create database table)
8. `ruby app.rb`
9. (localhost:4567)
10. `git branch` (check on pg branch)
11. `git push heroku HEAD:master`
12. `heroku open` (should get internal server error)
13. `heroku run rake db:migrate`
14. 

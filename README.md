# TeamLunchRoulette

Are you tired to create the typical todo-list project? 

Here not another todo list app, it is an project to try Vue and Elixir in a real world application.

This app is a simple tool that allow teams to choose where to eat everyday randomly.

    
## Development requirements

- Elixir 1.5.1
- Docker 17.09.1 
- npm 5.6.0

## Test

 Running the frontend tests:
 ```
 cd assets && npm test
 ```
 Running the backend tests:
  ```
  mix test
  ```

## Run in your local machine

First step, phoenix will look for some secret passwords you need in order to compile:

- /config/dev.secret.exs
- /config/prod.secret.exs 

These files should contain the expected secret configuration like:

  ```
  use Mix.Config
 
  config :team_lunch_roulette, google_api_places_web_service: "<YOUR_API_KEY>" 

  ```

To start your Phoenix server:

  * Install dependencies with `mix deps.get`
  * Install Node.js dependencies with `cd assets && npm install`
  * Pull mongo docker image with `docker pull mongo`
  * Run mongo image with `docker run --name mongo-team-lunch-roulette -p 27017:27017 -it --rm -d mongo` 
  * Start Phoenix endpoint with `mix phx.server`



Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.


## Packaging for prod

```
cd assets && node_modules/cross-env/dist/bin/cross-env.js NODE_ENV=production node_modules/webpack/bin/webpack.js
```

Ready to run in production? Please [check deployment guides](http://www.phoenixframework.org/docs/deployment).

## Tech stack

- Front-end: 
    - vue 2 
    - vue blue 
    - Web pack
    - scss
    - ES6
    - Jest & vue-test-utils
    
- Back-end:
    - Elixir
    - Phoenix
    - Mix
    
- Repository:
    - MongoDB
    

## Implementation guidelines 
 
### Frontend

 All the front is located at /assets
 
### Backend

   * Official website: http://www.phoenixframework.org/
   * Guides: http://phoenixframework.org/docs/overview
   * Docs: https://hexdocs.pm/phoenix
   * Source: https://github.com/phoenixframework/phoenix
   
### Useful docker commands

```
docker run --name mongo-team-lunch-roulette -p 27017:27017 -it --rm -d mongo 

docker ps

docker inspect <id>

docker exec -t -i <id> /bin/bash

or

docker exec -t mongo-team-lunch-roulette /bin/bash
```

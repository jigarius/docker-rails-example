# Docker Compose: Ruby on Rails Example

A simple example of using Docker Compose for developing and deploying
Ruby on Rails applications with the `bitnami/rails` image.

Read the full article on [jigarius.com](https://jigarius.com/).

## Getting started

Follow the steps mentioned under _existing app_ if you have one. Otherwise,
just make sure the `ror` directory is empty. After that, follow these steps:

  * Copy `.env.example` to `.env` and modify (if required).
  * Put the files of your existing Rails app in the `ror` directory.
    * The `Gemfile` should be at `ror/Gemfile`.
    * Skip this step if you don't have an existing Rails app.
  * Boot up the application.
    ```
    docker-compose up
    ```
  * When you see the following message, press `Ctrl+C`.
    ```
    Listening on http://0.0.0.0:3000
    Use Ctrl+C to stop
    ```
  * Create `config/database.yml` based on `docker/ror/example.database.yml`.
  * Boot up the application (again).
    ```
    docker-compose up
    ```

Cool! Now your Rails app should be available at
[localhost:3000](http://localhost:3000).

## Commands

Here are some helpful commands.

  * `docker-compose start`: Starts app containers.
  * `docker-compose stop`: Stops app containers.
  * `rake -T`: For some other helpful commands.

See [docker compose docs](https://docs.docker.com/compose/) for further info on
Docker Compose.

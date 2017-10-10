# A Phoenix Elm App with Nanobox

*A hip hipster way?*

We want to run [Phoenix Framework (1.3)](http://phoenixframework.org/) and [elm (0.18)](http://elm-lang.org/) out of a single application within a docker environment. We'll use [Nanobox](https://nanobox.io) to make life extremely simple.

You need the Nanobox cli. You do not need a paid account or any deployable cloud providers initially.

## Getting started

Clone the repository.

From the project root, run `nanobox dns add local nanobox-phoenix-elm.dev`*

From the project root, run `nanobox run` & wait while Nanobox creates the containers. Eventually you'll be in the Nanobox container at `/app`

Check it out:
* `elixir -v`
* `mix list`

\*  If you use a different local DNS entry, be sure to read & modify the `assets/webpack.config.js` file.

Running phoenix is easy.
* `cd /app && mix ecto.create` - Sets up the database.
* `cd /app/assets && yarn` - Installs the JS dependencies.
* `cd /app && mix deps.get` - Installs the elixir application dependencies.
* `cd /app && mix phx.server` - Starts the Phoenix endpoint.
* Open a browser to http://phoenix-elm.dev:4000


## How we got here

Installing the JS/webpack/elm stack from within the nanobox runnign container for the application do the following:

* `cd assets`
* `yarn add babel-core babel-loader babel-preset-es2015 extract-text-webpack-plugin css-loader node-sass sass-loader style-loader webpack elm-webpack-loader --dev`
* `rm brunch-config.js`
* Add `webpack.config.js`

## Learn more

  * Official website: http://www.phoenixframework.org/
  * Guides: http://phoenixframework.org/docs/overview
  * Docs: https://hexdocs.pm/phoenix
  * Mailing list: http://groups.google.com/group/phoenix-talk
  * Source: https://github.com/phoenixframework/phoenix

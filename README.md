# A Phoenix Elm App with Nanobox

*A hip hipster way?*

We want to run [Phoenix Framework (1.3)](http://phoenixframework.org/) and [elm (0.18)](http://elm-lang.org/) out of a single application within a docker environment. We'll use [Nanobox](https://nanobox.io) to make life extremely simple.

You need the Nanobox cli. You do not need a paid account or any deployable cloud providers initially.

## Getting started

Clone the repository.
From the project root, run `nanobox dns add local phoenix-elm.dev`
From the project root, run `nanobox run`
Wait while nanobox creates the containers.
Eventually you'll be in the nanobox container at `/app`
Check it out:
* `elixir -v`
* `mix list`

Running phoenix is easy.
* `cd /app && mix ecto.create` - Sets up the database.
* `cd /app/assets && yarn` - Installs the JS dependencies.
* `cd /app && mix deps.get` - Installs the elixir application dependencies.
* `cd /app && mix phx.server` - Starts the Phoenix endpoint.
* Open a browser to http://phoenix-elm.dev:4000





## Learn more

  * Official website: http://www.phoenixframework.org/
  * Guides: http://phoenixframework.org/docs/overview
  * Docs: https://hexdocs.pm/phoenix
  * Mailing list: http://groups.google.com/group/phoenix-talk
  * Source: https://github.com/phoenixframework/phoenix

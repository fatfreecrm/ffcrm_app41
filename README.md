# Fat Free CRM as an Engine

This is the experimental Rails 4.1 Fat Free CRM app running as an engine.
It's designed to help those testing the [rails4](https://github.com/fatfreecrm/fat_free_crm/tree/rails4) branch of Fat Free CRM in engine mode.

Documentation largely taken from [here](https://github.com/fatfreecrm/fat_free_crm/wiki/Running-as-a-Rails-Engine)

## Getting started

Clone this repository and run

    bundle install

Create and migrate the database (MUST run these commands separately)

    rake db:create
    rake db:migrate

Get some demo data

    rake ffcrm:demo:load

Start the rails server

    bin/rails s

## How this project was setup

Installed rails 4.1

    gem install rails

Created a new rails app (these are my preferred settings)

    rails new ffcrm_app41 --skip-keeps --database=postgresql --skip-test-unit

Added the following to the Gemfile

    gem 'fat_free_crm', github: 'fatfreecrm/fat_free_crm', branch: 'rails4'

Removed all files inside the `/app` folder

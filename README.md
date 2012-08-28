Spree Commerce 
==============

Summary
-------

Spree is a complete open source e-commerce solution built with Ruby on Rails. It was originally developed by Sean Schofield
and is now maintained by a dedicated [core team](http://spreecommerce.com/core-team).  You can find out more
by visiting the [Spree e-commerce project page](http://spreecommerce.com).

Installation
------------

Create new Rails Project

    rails new spree
    cd spree

Include Spree Gem

    gem 'spree', '1.1.3'
    $ bundle update

Setup Application

    $ rails g spree:install [ --migrate=false --sample=false --seed=false ]

Setup Database

    $ bundle exec rake db:drop
    $ bundle exec rake db:create

    $ bundle exec rake db:migrate
    $ bundle exec rake db:seed

To load sample products, orders, etc., run the following rake task

    $ bundle exec rake spree_sample:load

Performance Improvements
------------------------

Precompile Assets

    $ bundle exec rake assets:clean
    $ bundle exec rake assets:precompile:nondigest

Use Thin Server

    gem 'thin'
    
Deploying on Stackato
---------------------

    $ stackato push -n

Browse Admin Interface
----------------------

    http://<app-url>/admin

U: spree@example.com
P: spree123

LICENSE
-------

This project is maintained by a core team of developers and is freely available for commercial use under the terms of the New BSD License.

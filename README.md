Usage
-----

Run

    bin/suspenders projectname

This will create a Rails 3.2 app in `projectname`. This script creates a new
new git repository. It is not meant to be used against an existing repo.

Gemfile
-------

Suspenders adds a set of standard gems to the Gemfile. See
[template/Gemfile_additions](/kmckelvin/suspenders/blob/master/templates/Gemfile_additions),
which will be appended to the default generated projectname/Gemfile.

It includes application gems like:

* [Carrierwave](/jnicklas/carrierwave) for file uploads
* [Clearance](/thoughtbot/clearance) for authentication
* [Compass](/Compass/compass-rails) for Sass mixins
* [Flutie](/thoughtbot/flutie) for default CSS styles
* [Honeybadger](/honeybadger-io/honeybadger-ruby) for exception notification
* [Simple Form](/plataformatec/simple_form) for form markup and style
* [Slim](/stonean/slim) for cleaner markup

And testing gems like:

* [Bourne](/thoughtbot/bourne) and [Mocha](/freerange/mocha) for stubbing and
  spying
* [Capybara](/jnicklas/capybara) and
  [Capybara Webkit](/thoughtbot/capybara-webkit) for integration testing
* [Factory Girl](/thoughtbot/factory_girl) for test data
* [RSpec](https://github.com/rspec/rspec) for unit testing
* [Shoulda Matchers](/thoughtbot/shoulda-matchers) for common RSpec matchers
* [Timecop](/jtrupiano/timecop) for testing time

Other goodies
-------------

Suspenders also comes with:

* Override recipient emails in staging environment.
* Rails' flashes set up and in application layout.
* A few nice time formats set up for localization.
* [Heroku-recommended asset pipeline
  settings](https://devcenter.heroku.com/articles/rails3x-asset-pipeline-cedar/).
* Quiet Assets

Heroku
------

You can optionally create Heroku staging and production apps:

    suspenders app --heroku true

This has the same effect as running:

    heroku create app-staging --remote staging
    heroku create app-production --remote production

Github
------

You can optionally create a Github repository:

    suspenders app --github organization/project

This has the same effect as running:

    hub create organization/project

Clearance
---------

You can optionally not include Clearance:

    suspenders app --clearance false

Capybara Webkit
---------------

You can optionally not include Capybara Webkit (which depends on QT being
installed on your machine):

    suspenders app --webkit false

Dependencies
------------

Some gems included in Suspenders have native extensions. You should have GCC installed on your
machine before generating an app with Suspenders.

Use [OS X GCC Installer](/kennethreitz/osx-gcc-installer/) for Snow Leopard
(OS X 10.6).

Use [Command Line Tools for XCode](https://developer.apple.com/downloads/index.action)
for Lion (OS X 10.7) or Mountain Lion (OS X 10.8).

We use [Capybara Webkit](/thoughtbot/capybara-webkit) for full-stack Javascript
integration testing. It requires QT. Instructions for installing QT are
[here](/thoughtbot/capybara-webkit/wiki/Installing-Qt-and-compiling-capybara-webkit).

PostgreSQL needs to be installed and running for the `db:create` rake task.

Credits
-------

Suspenders is maintained and funded by [thoughtbot, inc](http://thoughtbot.com/community)

The names and logos for thoughtbot are trademarks of thoughtbot, inc.

License
-------

Suspenders is Copyright © 2008-2012 thoughtbot. It is free software, and may be
redistributed under the terms specified in the LICENSE file.

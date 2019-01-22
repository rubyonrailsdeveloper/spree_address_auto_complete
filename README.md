SpreeAddressAutoComplete
=======

SpreeAddressAutoComplete allows you to use suggested address functionality using Google maps api. Once installed the user will be given with a field in the address step of checkout page, using which he can select one of the suggested addresses by Google, instead of typing the whole address by himself.

Demo
----
Try Spree Address Auto Complete for Spree 3-4 with direct deployment on Heroku:

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/vinsol-spree-contrib/spree-demo-heroku/tree/spree-address-auto-complete-3-4)

Try Spree Address Auto Complete for Spree master with direct deployment on Heroku:

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/vinsol-spree-contrib/spree-demo-heroku/tree/spree-address-auto-complete-master)

Installation
------------
1. Add this extension to your Gemfile with this line:

  #### Spree >= 3.2

  ```ruby
    gem 'spree_address_auto_complete', git: 'https://github.com/vinsol-spree-contrib/spree_address_auto_complete', branch: 'master'
  ```

  #### Spree < 3.2

  ```ruby
    gem 'spree_address_auto_complete', git: 'https://github.com/vinsol-spree-contrib/spree_address_auto_complete', branch: 'X-X-stable'
  ```

  The `branch` option is important: it must match the version of Spree you're using.
  For example, use `3-0-stable` if you're using Spree `3-0-stable` or any `3.0.x` version.

2. Install the gem using Bundler:
  ```ruby
  bundle install
  ```

3. Copy & run migrations
  ```ruby
  bundle exec rails g spree_address_auto_complete:install
  ```

4. Go to general_setting in admin section to add your Google maps api key.

5. Restart your server

  If your server was running, restart it so that it can find the assets properly.

Testing
=======

  #### Spree > 3.1

  For Building Dependencies:
  ```shell
  appraisal install
  ```

  The dummy app can be regenerated by using:
  ```shell
  appraisal spree-3-1 rake test_app

  ```
  This will run rake test_app using the dependencies configured for Spree 3.1. Similarly you can use spree-3-2 and spree-master for generating dummy applications using dependencies for Spree 3.2 and latest version of Spree


  ```shell
  appraisal spree-3-1 rspec
  ```
  This will run rspec using the dependencies configured for Spree 3.1. Similarly you can use spree-3-2 and spree-master to run rspec using dependencies for Spree 3.2 and latest version of Spree


  #### Spree 3.0 and Spree 2.x

  First bundle your dependencies, then run `rake`. `rake` will default to building the dummy app if it does not exist, then it will run specs. The dummy app can be regenerated by using `rake test_app`.

  ```shell
  bundle
  bundle exec rspec spec
  ```
  
## See It In Action

<a href="http://www.youtube.com/watch?feature=player_embedded&v=F-8sa9izVqw
" target="_blank"><img src="http://img.youtube.com/vi/F-8sa9izVqw/0.jpg" 
alt="Youtube Video Tutorial" /></a>

Credits
-------

[![vinsol.com: Ruby on Rails, iOS and Android developers](http://vinsol.com/vin_logo.png "Ruby on Rails, iOS and Android developers")](http://vinsol.com)

Copyright (c) 2017 [vinsol.com](http://vinsol.com "Ruby on Rails, iOS and Android developers"), released under the New MIT License
Installation
------------
1. Add this extension to your Gemfile with this line:
  ```ruby
    gem 'spree_address_auto_complete', github: 'rubyonrailsdeveloper/spree_address_auto_complete'
  ```
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


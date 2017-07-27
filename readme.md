### capistrano-recipes

#### About
Provides recipes:generate rake task to generate capistrano recipes for deployment.

```
rake recipes:generate APPLICATION=application_name SERVER=server_address RUBY=ruby_version
```

- APPLICATION: this is the namem of the application and directory i.e. /var/www/production/app_name
- RUBY: ruby version string i.e. ruby-2.4.1

Which will generate

```
config/deploy.rb
config/deploy/develop.rb
config/deploy/staging.rb
config/deploy/production.rb
config/environments/develop.rb
config/environments/staging.rb
config/environments/production.rb
```

prefill everything accordingly and modify your Gemfile adding all gems necessary to install capistrano

#### Installation

Add to your gemfile

```
gem 'capistrano_recipes_gitlab', require: false, git: 'https://github.com/ekohe/capistrano-recipes-gitlab'
```

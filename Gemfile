source "https://rubygems.org"
git_source(:github) { |repo| "https://github.com/#{repo}.git" }
ruby "4.0.6"

# Gems moved from the default stdlib to bundled gems in Ruby 4.0. Rails already
# depends on these, but we pin them explicitly so an upstream change can't
# silently drop them and break boot. Add more here if bundle surfaces a LoadError.
gem "benchmark"
gem "logger"
gem "ostruct"

# Use Active Model has_secure_password [https://guides.rubyonrails.org/active_model_basics.html#securepassword]
gem "bcrypt"
# Reduces boot times through caching; required in config/boot.rb
gem "bootsnap", require: false
# Job queue/processor (Sidekiq 8.1 requires connection_pool >= 3.0)
gem "connection_pool", ">= 2.5"
# Environment Variables
gem "dotenv-rails"
# Redis client for hiredis
gem "hiredis-client"
# For JWT authentication (pinned to 2.x; jwt 3.0 changes encode/decode API and
# needs an auth-code migration — tracked as a separate follow-up)
gem "jwt", "~> 2.10"
# Use an opinionated customizable logging library
gem "lograge"
# Use mysql as the database for Active Record
gem "mysql2", "~> 0.5"
# Use the Puma web server [https://github.com/puma/puma]
gem "puma", "~> 7.0"
# Security
gem "rack-attack"
# Use Rack CORS for handling Cross-Origin Resource Sharing (CORS), making cross-origin Ajax possible
gem "rack-cors"
# Bundle edge Rails instead: gem "rails", github: "rails/rails", branch: "main"
gem "rails", "~> 8.1.3"
# Use Redis adapter to run Action Cable in production
gem "redis-client", "~> 0.24.0"
# API documentation
gem "rswag"
# Background job processing with Redis
gem "sidekiq", ">= 8.0"
# Windows does not include zoneinfo files, so bundle the tzinfo-data gem
gem "tzinfo-data", platforms: %i[windows jruby]

# HTTP client
# gem "faraday"
# Use Active Storage variants [https://guides.rubyonrails.org/active_storage_overview.html#transforming-images]
# gem "image_processing", "~> 1.2"

group :development, :test do
  # Security analysis
  gem "brakeman", require: false
  gem "bundler-audit", require: false
  # See https://guides.rubyonrails.org/debugging_rails_applications.html#debugging-with-the-debug-gem
  gem "debug", platforms: %i[mri windows], require: "debug/prelude"
  # Setup dummy data
  gem "faker"
  # Linting
  gem "rubocop", require: false
  gem "rubocop-performance", require: false
  gem "rubocop-rails", require: false
  gem "rubocop-rspec", require: false
end

group :development do
  # IDE tools
  gem "ruby-lsp", require: false
  gem "solargraph", require: false
  # Autoloading
  gem "spring"
  # Documentation
  gem "yard", require: false
end

group :test do
  gem "database_cleaner"
  gem "factory_bot_rails"
  gem "rspec-rails"
  gem "simplecov", require: false

  # Mock external HTTP requests
  # gem "webmock"
  # gem "vcr"
end

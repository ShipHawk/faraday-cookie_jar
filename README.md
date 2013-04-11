# Faraday::CookieJar

Faraday middleware to manage client-side cookies

## Description

This gem is a piece of Faraday middleware that adds client-side Cookies management, using [cookirjar gem](https://github.com/dwaite/cookiejar).

## Installation

Add this line to your application's Gemfile:

    gem 'faraday-cookie_jar'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install faraday-cookie_jar

## Usage

```ruby
require 'faraday-cookie_jar'

conn = Faraday.new(:url => "http://example.com") do |builder|
  builder.use :cookie_jar
end

conn.get "/foo"  # gets cookie
conn.get "/bar"  # sends cookie
```

## Author

Tatsuhiko Miyagawa
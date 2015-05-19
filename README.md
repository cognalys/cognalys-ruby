# Cognalys-ruby (GEM)

 International mobile number verification without an SMS gateway ( GEM ).

## Initial Step:
 Grab app_id,token by creating an OTP app after registring an account on (https://www.cognalys.com) . 

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'cognalys'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install cognalys

## Configure

```ruby
    #config/initializers/cognalys.rb
    Cognalys.setup(app_id,token)
```

## Usage

To request validation

```ruby
    require 'cognalys'
    cognalys = Cognalys::Request.new
    cognalys.request_verification( :mobile => phone )

```

To verify OTP

```ruby
    require 'cognalys'
    cognalys = Cognalys::Request.new
    cognalys.validate_otp( :keymatch => key_match, :otp => full_otp )
```



## Contributing

1. Fork it ( https://github.com/cognalys/cognalys-ruby/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

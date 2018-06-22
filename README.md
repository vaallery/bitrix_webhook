# BitrixWebhook

Welcome to your new gem! In this directory, you'll find the files you need to be able to package up your Ruby library into a gem. Put your Ruby code in the file `lib/bitrix_webhook`. To experiment with that code, run `bin/console` for an interactive prompt.

TODO: Delete this and the text above, and describe your gem

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'bitrix_webhook'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install bitrix_webhook
    
Then run:

    $ rails g bitrix_webhook:config

which will generate default settings files:

    config/initializers/bitrix_webhook.rb

Then configurate bitrix_webhook.rb file:

Get webhook at  https://your-portal.bitrix24.ru/marketplace/hook

You get https://your-portal/rest/your-webhook-id/your-webhook-key/profile/

**https://your-portal.bitrix24.ru/rest/2/zdfmoz6nub3uacft/profile/**



 config.bitrix24_url = your-portal.bitrix24.ru
 config.hook = zdfmoz6nub3uacft
 config.webhook_hook_id = 2
 

```ruby
BitrixWebhook.configuration do |config|
  config.bitrix24_url = 'URL' # Like this b21-6l64i7.bitrix24.ru
  config.hook = 'Hook' # Like this  ak75dm93k5eq8215
  config.webhook_hook_id = 'id' # Like this  1
end
```

## Usage

Now available only **crm.lead.add** 

*I'm sorry i didn't have time to write all methods.*

```ruby
BitrixWebhook::CRM::LEAD.add(fname:'Serhii',lname:'Danovskyi',phone:'+380675807873',email:'serhii.danovskyi@gamil.com')
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/bitrix_webhook.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
# bitrix_webhook

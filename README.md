# To generate some random data
1. docker run -it -v `pwd`:`pwd` -w `pwd` ruby:2.5-alpine sh
 2. ``gem install ffaker``
 3. irb

 ## Banks:
```ruby
require 'ffaker'
require 'json'
a = Array.new(30) {|i| {id: i + 1, logo: "https://fakeimg.pl/180x40/#{FFaker::Color.hex_code}/", name: FFaker::Company.name, created_at: FFaker::Time.datetime, updated_at: FFaker::Time.datetime} }

 File.open('banks', 'w') { |file| file.write(JSON.dump(a))}
```

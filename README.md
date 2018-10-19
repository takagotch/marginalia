### marginalia
---
https://github.com/basecamp/marginalia

```
Account Load (0.3ms) SELECT `accounts`.* FROM `accounts`
WHERE `accounts`.`queenbee_id` = 1234567890
LIMIT 1

```


```ruby
gem 'marginalia'
Marginalia::Railtie.insert

Marginalia::Comment.components = [:application, :controller, :action]

module Marginalia
  module Comment
    def self.mycommentcomponent
      "TEST"
    end
  end
end
Marginalia::Comment.components = [:application, :mycommentcomponent]

```


```
bundle
rake db:mysql:create
rake db:postgresql:create

```


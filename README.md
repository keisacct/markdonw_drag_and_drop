# Action Text
## インストール方法
```$ rails action_text:install```

## Gemの追加
```ruby
省略
...
# Use Active Storage variant
gem 'image_processing', '~> 1.2' # コメントアウトする

...
省略
```

```$ bundle install```

## モデルに記述追加
```ruby
class Question < ApplicationRecord
    has_rich_text :content

end
```

## フォームの編集
```html.erb
<%= form_with(model: question, local: true) do |form| %>
    ...
    省略
    ...
    <%= form.rich_text_area :content %>
    ...
    省略
    ...
<% end %>
```

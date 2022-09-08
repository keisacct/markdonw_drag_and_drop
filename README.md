# Action Text
## インストール方法
```$ rails action_text:install```

## Gemの追加
```ruby
    ：
# Use Active Storage variant
gem 'image_processing', '~> 1.2' # コメントアウトする
    ：
```

```$ bundle install```

## モデルに記述追加
```ruby
class Question < ApplicationRecord
    has_rich_text :content

end
```

## フォームの編集
```html
<%= form_with(model: question, local: true) do |form| %>
    ：
    <%= form.rich_text_area :content %>
    ：
<% end %>
```

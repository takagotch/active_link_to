### active_link_to
---

https://github.com/comfy/active_link_to

```ruby
active_link_to 'Users', '/users'
# => <a href="/users" class="active">Users</a>
active_link_to 'Users', '/users', active: :inclusive
# => <a href="/users" class="active">Users</a>
active_link_to 'Users', users_path, active: :exclusive
# => <a href="/users" class="active"></a>
active_link_to '', users_path, active: :exclusive
# => <a href="/users">Users</a>
active_link_to 'Users', users_path, active: /^\/use/


```



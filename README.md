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
active_link_to 'Users', users_path(role_eq: 'admin'), active: :exact
active_link_to 'User Edit', edit_user_path(@user), active: [['people', 'news'], ['show', 'edit']]
active_link_to 'User Edit', edit_user_path(@user), active: [people: :show, news: :edit]
active_link_to 'User Edit', edit_user_path(@user), active: [['people', 'news'], []]
active_link_to 'User Edit', edit_user_path(@user), active: [[], ['edit']]
active_link_to 'Users', users_path, active: true
active_link_to 'Admin users', users_path(role_eq: 'admin'), active: { role_eq: 'admin' }

active_link_to 'Users', users_path, class_active: 'enabled'
# => <a href="/users" class="enabled">Users</a>
active_link_to 'News', news_path, class_inactive: 'disabled'
# => <a href="/news" class="disabled">News</a>
active_link_to 'Users', users_path, active_disable: true
# => <span class="active">Users</span>
active_link_to 'Users', users_path, wrap_tag: :li
# => <li class="active"><a href="/users">Users</a></li>
active_link_to '', users_path, wrap_tag: :li, wrap_class: 'nav-item'
# => <li class="nav-item active"><a href="/users">Users</a></li>
is_active_link?(users_path, :inclusive)
# => true
active_link_to_class(users_path, active: :inclusive)
# => 'active'
```



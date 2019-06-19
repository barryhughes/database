---
layout: project
version: 4.x
title: Insert records
description: Insert new records into a table
---

Adding new records into a table is done using the `insert` method. 
The method accepts a single argument that represents a `key => value` mapped array
where the `key` is the name of the column and `value` is the actual value that 
will be inserted into the column.

{% capture php %}
```php
$result = $db->insert(array(
                'name' => 'John Doe',
                'email' => 'john.doe@example.com'
            ))
            ->into('users');
```
{% endcapture %}
{% capture sql %}
```sql
INSERT INTO `users` (`name`, `email`) 
VALUES ("John Doe", "john.doe@example.com")
```
{% endcapture %}
{% include_relative _tabs.html %}

This method returns `true` on success and `false` otherwise.
 
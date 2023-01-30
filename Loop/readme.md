```php
@foreach ($users as $user)
  {{ $loop->index }}     // start with 0
  {{ $loop->iteration }} // start with 1
  {{ $user->name }}
@endforeach
```

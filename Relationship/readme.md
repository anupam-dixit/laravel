In model
```php
public function coach_info()
    {
        return $this->hasOne(User::class,'_id','created_by');
    }
```

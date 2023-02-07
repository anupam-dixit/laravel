### Accessor
Use Below code in your model
```php
protected $appends = ['workshop_members_count'];
...
...
public function getWorkshopMembersCountAttribute()
{
  return DATA_YOU_WANT; 
}
```
This provided key automatic will be appended whenever model called.
### My case get count or other data with relashipship
```php
public function membersCount()
{
    return $this->hasMany(WorkshopBooking::class, 'workshop_id', '_id')->count();
 }
public function getWorkshopMembersCountAttribute()
 {
    return $this->membersCount(); 
 }
 ```

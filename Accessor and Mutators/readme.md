## Accessor
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

## Mutator
To mutate existing key with custom conditions
For example we have ***domain*** named field in database and we are using this Mutator on ***Domain*** model then
```php
public function getDomainAttribute($value)
{ 
   $domain=Domain::find($value);
   return array('domain_id'=>$value,'title'=>$domain->title);
}
```
>Here get _CamelCase_ Attribute to be noted

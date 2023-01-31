### Create new project
```php
composer create-project laravel/laravel:^8.* ProjectName
```
### Migration error
>/app/Providers/AppServiceProvider.php
```php
use Illuminate\Support\Facades\Schema;
/**
 * Bootstrap any application services.
 *
 * @return void
 */
public function boot()
{
    Schema::defaultStringLength(191);
}
```
### Upload file via CMD
#### GoTO
```shell
wamp64\bin\mysql\mysql8.0.31\bin>
```
and 
```shell
mysql -u root -p invoiceskyviewad_insurance < C:\Users\ThinkPad\Downloads\invoiceskyviewad_insurance_latest_live.sql
```

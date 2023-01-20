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

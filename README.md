# TCP Analysis Web Application

## Installation 
### Installation Laravel
```php
composer create-project laravel\laravel TCP-Analysis-web-app
```
### Install Ratchet
```php
composer require cboden/ratchet
```
### Create Command 
```php 
php artisan make:command WebServer
```
### Use WebServer
```php
php artisan websocket:init
```

### Create Controller
```php
php artisan make:controller WebSocketController
```
### Use Library & Packget
```php
use Ratchet\Server\IoServer;
use Ratchet\Http\HttpServer;
use Ratchet\WebSocket\WsServer;
use App\Http\Controllers\WebSocketController;

```

### Command and function call WebSocketController 
```php
        $server = IoServer::factory(
            new HttpServer(
                new WsServer(
                    new WebSocketController()
                )
            ),
            8090
        );
        $server->run();

```
# Support for us
Paypal 
Git 

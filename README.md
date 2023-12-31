# TCP Analysis Web Application

## Installation 
### Installation Laravel
```bash
composer create-project laravel\laravel TCP-Analysis-web-app
cd TCP-Analysis-web-app
```
### Install Ratchet
```bash
composer require cboden/ratchet
```
### Create Command 
```bash 
php artisan make:command WebServer
```
### Use WebServer
```bash
php artisan websocket:init
```

### Create Controller
```bash
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
### [Support for us](https://maaeyeng.com)
[Paypal](https://paypal.me/maaeyeng)
[Gift](https://gift.com/)

## debug

This one returns the value of `var_dump` instead of outputting it.
```php
function var_dump_ret($mixed = null) {
  ob_start();
  var_dump($mixed);
  $content = ob_get_contents();
  ob_end_clean();
  return $content;
}
```

## Автоматизація

1. Форматування коду (phpcsfixer)
2. Запуск тестів
3. Статаналіз (PHPStan vs Psalm)

## composer

install one package
```sh
composer require doctrine/doctrine-fixtures-bundle:2.1.*@dev
```

install global one package
```sh
composer global require doctrine/doctrine-fixtures-bundle:2.1.*@dev
```

update
```sh
composer update doctrine/doctrine-fixtures-bundle
```

or ignore platform
```sh
composer update doctrine/doctrine-fixtures-bundle --ignore-platform-reqs
```

update autoload
```sh
composer dump-autoload
```


## php local

```sh
sudo apt install php-cli php-curl php-dom
```

### composer local

```sh
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
php -r "if (hash_file('sha384', 'composer-setup.php') === '55ce33d7678c5a611085589f1f3ddf8b3c52d662cd01d4ba75c0ee0459970c2200a51f492d557530c71c15d8dba01eae') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;"
php composer-setup.php
php -r "unlink('composer-setup.php');"
sudo mv composer.phar $HOME/.local/bin/composer
```

## php commands

```sh
php -v
php -i | grep "error"
php -i | grep "memory_limit"
php -i | grep "max_children"
php -i | grep "php.ini"
cd {folder_conf}
grep -rn "memory_limit" ./

# xdebug
php -v | grep -i "xdebug"

php -m
```

## conf files examples

```
/usr/local/php
/usr/local/etc/php-fpm.d/www.conf
/var/log/fpm-php.www.log


/etc/php/7.4/fpm/php.ini
/etc/php/7.4/fpm/pool.d/www.conf
```

## run php-cli with config

```sh
php -a -c /etc/php5/cli/php.ini
```

## php-cli log

/usr/local/etc/php/conf.d/dev-cli.ini
```ini
log_errors = On
error_log = syslog
error_log = /var/log/php/php-cli-error.log
; memory_limit = -1
memory_limit = 256MB
```

Necessarily create log file
```sh
mkdir /var/log/php/ && touch /var/log/php/php-cli-error.log
# fix permission
```

## php ip

```php
echo '<pre>';
print_r($_SERVER['REMOTE_ADDR']);
echo '</pre>';
exit('debug');


if (preg_match("/^198\.0\.10\.1/", $_SERVER['REMOTE_ADDR'])) {
        exit(1);
}



$args = print_r($_SERVER, true) . "\n";
file_put_contents('/var/www/app/logs/debug.log', $args, FILE_APPEND);
```

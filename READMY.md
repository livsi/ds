# Докер окружение

## Установка платформы для разработки
docker-compose up --build

## Копирование вендоров из докера
docker cp dockersymfonyenv_php_1:/var/www/symfony/vendor symfony/vendor

## Копирование вендоров в докер
docker cp symfony/vendor dockersymfonyenv_php_1:/var/www/symfony/vendor

## XDEBUG
brew install socat
socat TCP-LISTEN:9001,reuseaddr,fork,bind=localhost UNIX-CONNECT:/var/run/docker.sock
В настройках устанавливаем php интерпретатор

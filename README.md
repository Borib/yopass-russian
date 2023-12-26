# yopass - Russian language file
<hr style="border-width: 3px;">

## English
Russian language File for yopass by Johan Haals (jhaals/yopass)<br>
<a href="https://github.com/jhaals/yopass">Yopass - Share Secrets Securely</a>

### Installation
Copy the website/public/locales/ru.json file to the corresponding directory in your yopass installation.<br>
yopass will automatically detect the new language and activate it if your Browser presents that language to yopass.

### Container
Check this repository out and build your own container with the polish language file included to the original Yopass-Image from docker.io.
```javascript copy
git clone https://github.com/jhaals/yopass.git
git clone https://github.com/Borib/yopass-russian.git
```
Copy russian language file into locales folder inside yopass build directory:
```javascript copy
cp /root/yopass-russian/website/public/locales/ru.json /root/yopass/website/public/locales/
cd /root/yopass
```
When building image: borib - author name; yopassru - image name; v1 - version tag.<br>
Dot at the end means to search Dockerfile in current directory.<br>
Image and author name (borib/yopassru) must be entered in lower case.
```javascript copy
docker build -t borib/yopassru:v1 .
docker run --name memcached_yopass -d memcached
docker run --name yopass-russian -p 127.0.0.1:80:1337 --link memcached_yopass:memcached -d borib/yopassru:v1 --memcached=memcached:11211
```
<hr style="border-width: 3px;">

## Русский
Файл русского перевода для yopass от Johan Haals (jhaals/yopass)<br>
<a href="https://github.com/jhaals/yopass">Yopass - Share Secrets Securely</a>

### Установка
Скопируйте файл site/public/locales/ru.json в соответствующий каталог вашей установки yopass.<br>
yopass автоматически обнаружит новый язык и активирует его, если ваш браузер поддерживает этот язык для yopass.

### Контейнер
Исследуйте этот репозиторий и создайте свой собственный контейнер с файлом русского языка, включенным в исходный Yopass-Image из docker.io.
```javascript copy
git clone https://github.com/jhaals/yopass.git
git clone https://github.com/Borib/yopass-russian.git
```
Cкопировать файл с русификацией в папку locales внутри сборки:
```javascript copy
cp /root/yopass-russian/website/public/locales/ru.json /root/yopass/website/public/locales/
cd /root/yopass
```
В сборке контейнера borib - имя автора; yopassru - название для сборки; v1 - тег с указанием версии.<br>
Точка на конце указывает, что поиск Dockerfile выполняем в текущей директории.<br>
Имя образа (borib/yopassru) вводить только в нижнем регистре.
```javascript copy
docker build -t borib/yopassru:v1 .
docker run --name memcached_yopass -d memcached
docker run --name yopass-russian -p 127.0.0.1:80:1337 --link memcached_yopass:memcached -d borib/yopassru:v1 --memcached=memcached:11211
```

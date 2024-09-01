# Развертывание selenoid кластера

**0) На удаленном сервере(linux) должны быть установлены:**
- docker
- openssh-server

**1) Скопировать папку на удаленный сервер:**

`scp -r .\selenoid remote-user@remote-host:/path/to/file`

**2) Пред запуском необходимо загрузить образы всех необходимых браузеров указанных в `browser.json`:**

`docker pull selenoid/chrome:127.0`

**3) Запустить `docker-compose.yaml`:**

`docker compose up -d`

**4) Для остановки и удаления использовать:**

`docker compose rm -f -s`
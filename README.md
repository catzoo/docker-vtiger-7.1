# VTiger CRM 7.1
This repository includes the dockerfiles for running VTiger CRM 7.1. This was made for testing and is not recommended for production use.

There are two folders with dockerfiles, `maria` and `vtiger`.

#### vtiger
This dockerfile has Apache and PHP 5.4 for running vtiger.

#### maria
VTiger requires a mysql database with changes to `sql_mode`. The maria dockerfile uses [`mariadb:latest`](https://hub.docker.com/_/mariadb) image and copys the custom config to `/etc/mysql/conf.d`

# Running

### Docker Compose
You can run this image with Docker Compose. You can clone this repository and use the included `compose.yaml` file.

### Docker run
You can use this command to run the image
```sh
docker run -d -p 80:80 ghcr.io/catzoo/vtiger
```
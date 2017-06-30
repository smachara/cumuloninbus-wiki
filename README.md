# dokuwiki-cumuloninbus
**Why use Bitnami Images?**
    Bitnami closely tracks upstream source changes and promptly publishes new versions of this image using our automated systems.
    With Bitnami images the latest bug fixes and features are available as soon as possible.
    Bitnami containers, virtual machines and cloud images use the same components and configuration approach - making it easy to switch between formats based on your project needs.
    Bitnami images are built on CircleCI and automatically pushed to the Docker Hub.
    All our images are based on minideb a minimalist Debian based container image which gives you a small base container image and the familiarity of a leading linux distribution.

**What is DokuWiki?**
    DokuWiki is a simple to use and highly versatile Open Source wiki software that doesn't require a database. It is loved by users for its clean and readable syntax. The ease of maintenance, backup and integration makes it an administrator's favorite
https://www.dokuwiki.org/

**Prerequisites**
  To run this application you need Docker Engine 1.10.0. Docker Compose is recomended with a version 1.6.0 or later.
**How to use this image**
  Run the application using Docker Compose

This is the recommended way to run Dokuwiki. You can use the following docker compose template:

version: '2'
services:
  dokuwiki:
    image: 'bitnami/dokuwiki:latest'
    restart: always
    ports:
      - '80:8080'
      - '443:4433'
    volumes:
      - '/srv/dokuwiki-persistence:/bitnami/dokuwiki'
      - '/srv/apache-persistence:/bitnami/apache'
      - '/srv/php-persistence:/bitnami/php'

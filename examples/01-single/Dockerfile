FROM php:5.6-cli
MAINTAINER Rocco Palladino <rpalladino@gmail.com>

EXPOSE 8000

RUN mkdir -p /srv/app/web
COPY . /srv/app/web

WORKDIR /srv/app/web

CMD ["php", "-S", "0.0.0.0:8000", "-t", "/srv/app/web"]

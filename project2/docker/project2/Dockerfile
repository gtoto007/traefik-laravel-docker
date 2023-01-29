FROM debian:bullseye-slim

RUN groupadd -g 1000 www
RUN useradd -u 1000 -ms /bin/bash -g www www
COPY ../../ /var/www
# Copy existing application directory permissions
COPY --chown=www:www ../../ /var/www
# Change current user to www
USER www
#VOLUME /var/www
CMD tail -f /dev/null

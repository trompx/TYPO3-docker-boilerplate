FROM ubuntu:14.04

COPY conf/php.ini          /etc/php5/mods-available/typo3.ini
COPY conf/supervisord.conf /etc/supervisor/conf.d/supervisord.conf
COPY conf/locale.conf      /opt/docker/locale.conf
COPY bin/*                 /opt/docker/

RUN bash /opt/docker/install.sh

EXPOSE 9000

VOLUME /docker/
WORKDIR /docker/

ENTRYPOINT ["/opt/docker/entrypoint.sh"]
CMD ["supervisord"]
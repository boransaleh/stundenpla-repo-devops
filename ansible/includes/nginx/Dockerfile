FROM nginx:alpine

USER root
EXPOSE 80
EXPOSE 443
RUN rm -rf /etc/nginx/conf.d/default.conf
COPY stundenplan.conf.tmpl /etc/nginx/conf.d/
COPY docker-entrypoint.sh /
RUN chmod 0777 /docker-entrypoint.sh
ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["nginx", "-g", "daemon off;"]



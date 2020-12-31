FROM docker.elastic.co/kibana/kibana-oss:7.10.0
# install open distro security plugin to Kibana
RUN bin/kibana-plugin install https://d3g5vo6xdbdb9a.cloudfront.net/downloads/kibana-plugins/opendistro-security/opendistroSecurityKibana-1.12.0.0.zip
USER root
WORKDIR /usr/share/kibana/

RUN chown kibana:kibana config/kibana.yml

USER kibana

EXPOSE 5601

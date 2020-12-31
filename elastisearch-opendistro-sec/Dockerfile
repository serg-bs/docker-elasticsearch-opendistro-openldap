FROM docker.elastic.co/elasticsearch/elasticsearch-oss:7.10.0
USER root
WORKDIR /usr/share/elasticsearch/

# install open distro security plugin
RUN bin/elasticsearch-plugin install -b https://d3g5vo6xdbdb9a.cloudfront.net/downloads/elasticsearch-plugins/opendistro-security/opendistro_security-1.12.0.0.zip
RUN sh /usr/share/elasticsearch/plugins/opendistro_security/tools/install_demo_configuration.sh -y -i

USER elasticsearch

EXPOSE 9200

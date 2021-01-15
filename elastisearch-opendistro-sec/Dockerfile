FROM bitnami/elasticsearch:7.10.0

RUN elasticsearch-plugin install -b https://d3g5vo6xdbdb9a.cloudfront.net/downloads/elasticsearch-plugins/opendistro-security/opendistro_security-1.12.0.0.zip
RUN touch /opt/bitnami/elasticsearch/config/elasticsearch.yml

USER root
RUN /bin/bash /opt/bitnami/elasticsearch/plugins/opendistro_security/tools/install_demo_configuration.sh -y -i
RUN mv /opt/bitnami/elasticsearch/config/elasticsearch.yml /opt/bitnami/elasticsearch/config/my_elasticsearch.yml
COPY my_elasticsearch.yml /opt/bitnami/elasticsearch/config/my_elasticsearch.yml
USER 1001

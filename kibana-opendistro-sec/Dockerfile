FROM sergbs/elastic as base
FROM bitnami/kibana:7.10.0

# install open distro security plugin to Kibana
RUN kibana-plugin install https://d3g5vo6xdbdb9a.cloudfront.net/downloads/kibana-plugins/opendistro-security/opendistroSecurityKibana-1.12.0.0.zip
COPY --from=base /opt/bitnami/elasticsearch/config/*.pem /opt/bitnami/kibana/certificates/

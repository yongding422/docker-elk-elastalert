FROM bitsensor/elastalert:latest

COPY config/elastalert_config.yaml /opt/elastalert/config.yaml
COPY config/config.json /opt/elastalert-server/config/config.json
COPY rules/emailrule.yaml /opt/elastalert/rules/emailrule.yaml

# FROM docker.elastic.co/beats/heartbeat:7.7.1
# COPY config/heartbeat.yml /usr/share/heartbeat/heartbeat.yml
# USER root
# RUN chown root:heartbeat /usr/share/heartbeat/heartbeat.yml
# USER heartbeat
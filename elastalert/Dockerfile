FROM rdrg/elastalert-docker
ENV RULES_DIRECTORY /opt/rules
ENV CONFIG_DIR /opt/config

COPY config/elastalert_config.yaml ${CONFIG_DIR}
COPY config/elastalert_supervisord.conf ${CONFIG_DIR}
COPY rules/emailrule.yaml ${RULES_DIRECTORY}

FROM docker.elastic.co/beats/heartbeat:7.7.1
COPY config/heartbeat.yml /usr/share/heartbeat/heartbeat.yml
USER root
RUN chown root:heartbeat /usr/share/heartbeat/heartbeat.yml
USER heartbeat
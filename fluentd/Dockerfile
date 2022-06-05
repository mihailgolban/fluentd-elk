# fluentd/Dockerfile

FROM fluent/fluentd:v1.14.0-debian-1.0
USER root
RUN gem install elasticsearch -v 8.2.2
RUN ["gem", "install", "fluent-plugin-elasticsearch", "--no-document", "--version", "5.2.2"]
USER fluent
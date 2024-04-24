FROM bitnami/airflow:latest

USER root

RUN apt update && \
  apt-get install -y openjdk-17-jdk;

ENV JAVA_HOME=/usr/lib/jvm/java-17-openjdk-arm64
ENV PATH=$PATH:$JAVA_HOME/bin

RUN apt-get install -y wget && \
  wget https://archive.apache.org/dist/spark/spark-3.5.1/spark-3.5.1-bin-hadoop3.tgz && \
  tar -xzf spark-3.5.1-bin-hadoop3.tgz -C /opt/

ENV SPARK_HOME=/opt/spark-3.5.1-bin-hadoop3
ENV PATH=$PATH:$SPARK_HOME/bin:$SPARK_HOME/sbin

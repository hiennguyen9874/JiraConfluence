ARG BASE_CONTAINER=atlassian/jira-software:8.22.3

FROM ubuntu:latest as zip

RUN export DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -yq --no-install-recommends zip unzip wget && \
    apt-get autoremove -y && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /tmp

RUN wget --no-check-certificate https://github.com/hiennguyen9874/JiraConfluence/releases/download/v0.1/atlassian-agent-v1.3.1.zip

RUN unzip atlassian-agent-v1.3.1.zip

FROM $BASE_CONTAINER as base

USER root

# Add proxy unpacking to container
COPY --from=zip /tmp/atlassian-agent-v1.3.1/atlassian-agent.jar /opt/atlassian/jira/

# Set Startup Loading Agent Package
RUN echo 'export CATALINA_OPTS="-javaagent:/opt/atlassian/jira/atlassian-agent.jar ${CATALINA_OPTS}"' >> /opt/atlassian/jira/bin/setenv.sh

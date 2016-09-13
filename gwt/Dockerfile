FROM openjdk:8-jdk

MAINTAINER Ryan Mills <ryan@koancode.com>

RUN apt-get update -qq && apt-get install -y -qq ant pylint
ENV PATH "./:$PATH"

# GWT 2.7
RUN mkdir -p ~/share/java; wget -O - --quiet http://goo.gl/t7FQSn -O gwt-2.7.zip; unzip gwt-2.7.zip -d ~/share/java
ENV GWT_HOME ~/share/java/gwt-2.7.0

# SDKMAN
RUN curl -s https://get.sdkman.io | bash
RUN "$HOME/.sdkman/bin/sdkman-init.sh"

# Gradle 2.11
RUN sdk install gradle 2.11
ENV GRADLE_HOME "$HOME/.sdkman/candidates/gradle/current"
ENV PATH "$GRADLE_HOME/bin:$PATH"

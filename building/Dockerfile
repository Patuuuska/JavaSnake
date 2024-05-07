FROM bitnami/java:latest
RUN apt-get update -y && apt-get upgrade -y

RUN apt-get install git -y
RUN apt install default-jdk -y
RUN apt install gradle -y

RUN git clone https://github.com/sloenthran/JavaSnake.git
WORKDIR /JavaSnake

RUN gradle build
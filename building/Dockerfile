FROM bitnami/java:latest
RUN apt-get update -y && apt-get upgrade -y

RUN apt-get install git -y
RUN apt-get install default-jdk -y
RUN apt-get install gradle -y
RUN apt-get install openjfx -y

RUN git clone https://github.com/sloenthran/JavaSnake.git
WORKDIR /JavaSnake

RUN ./gradlew build
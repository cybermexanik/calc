FROM openjdk:11-jdk-slim

RUN apt-get update && apt-get install -y \
    libx11-6 libxext6 libxrender1 libxtst6 libfreetype6 \
    fontconfig fonts-dejavu \
    && rm -rf /var/lib/apt/lists/*

ENV DISPLAY=host.docker.internal:0

COPY calc.jar /app/calc.jar

WORKDIR /app

CMD ["java", "-jar", "calc.jar"]
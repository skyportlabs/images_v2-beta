# Usar uma imagem base do Ubuntu
FROM ubuntu:22.04

# Instalar dependências e OpenJDK 17
RUN apt-get update && apt-get install -y \
    openjdk-17-jdk \
    curl \
    ca-certificates \
    openssl \
    git \
    tar \
    bash \
    sqlite3 \
    fontconfig \
    --no-install-recommends && \
    rm -rf /var/lib/apt/lists/*

# Definir JAVA_HOME e PATH
ENV JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64
ENV PATH="$JAVA_HOME/bin:$PATH"

WORKDIR /app/data

CMD sh -c "$START"

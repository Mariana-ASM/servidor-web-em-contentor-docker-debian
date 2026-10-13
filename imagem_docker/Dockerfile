# Minha contribuição: Imagem base usando o sistema operacional Ubuntu oficial
FROM ubuntu:22.04

# Minha contribuição: Metadados padronizados OCI para documentar a autoria e versão
LABEL org.opencontainers.image.authors="Seu Nome" \
      org.opencontainers.image.description="App simples em Python sobre Ubuntu" \
      org.opencontainers.image.version="1.0"

# Minha contribuição: Variáveis de ambiente para evitar telas interativas no apt
ENV DEBIAN_FRONTEND=noninteractive \
    PYTHONUNBUFFERED=1

# Minha contribuição: Define o diretório de trabalho padrão dentro do contentor
WORKDIR /app

# Minha contribuição: Atualiza pacotes do SO e instala o Python 3
RUN apt-get update && \
    apt-get install -y --no-install-recommends python3 && \
    rm -rf /var/lib/apt/lists/*

# Minha contribuição: Copia o ficheiro da aplicação para o contentor
COPY app.py .

# Minha contribuição: ENTRYPOINT define o executável principal e CMD os parâmetros padrão
ENTRYPOINT ["python3"]
CMD ["app.py"]

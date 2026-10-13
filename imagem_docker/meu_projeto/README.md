# Servidor Web em Contentor Docker (Debian)

Projeto prático com servidor Nginx implementado sobre imagem `debian:trixie`.

## Estrutura
- `Dockerfile`: Configura o Debian, instala o Nginx e adiciona o conteúdo estático.
- `meu_site.tar`: Ficheiro compactado contendo o `index.html`.

## Como executar localmente
```bash
docker build -t marianamonteiro1998/meu_site:1.0 .
docker run -d -p 8080:80 --name container-web marianamonteiro1998/meu_site:1.0

Aceda através do navegador em http://localhost:8080.

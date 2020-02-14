## docker-python

*"These are simple Python images that contain dependencies used in [@ditceuma](https://github.com/ditceuma) projects and maintained by [Mark Team](https://github.com/ditceuma-mark-team)."*

### Bibliotecas

**Bibliotecas Globais**

- curl
- apt-transport-https
- make
- build-essential
- unixodbc
- unixodbc-dev
- gnupg2
- tzdata

**Para manipulação com arquivos em PDF e suas dependências**

- wkhtmltopdf
    - xvfb
    - xfonts-100dpi
    - xfonts-75dpi
    - xfonts-scalable
    - xfonts-cyrillic

**Driver ODBC para conexão com SQL Server**

- msodbcsql17
- mssql-tools

### Outras informações

Para mais informações verifique o [Dockerhub da Imagem](https://hub.docker.com/r/markteam/docker-python).

Para a ver um exemplo de uso da imagem em um projeto, acesse: [flask-skeleton-api](https://github.com/ditceuma-mark-team/flask-skeleton-api).

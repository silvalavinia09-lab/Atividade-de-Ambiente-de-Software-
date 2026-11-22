# Atividade-de-Ambiente-de-Software- 17/11/2026


Questão 1

a) FROM python:3.11-slim

b) WORKDIR /app

c) COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

d) COPY . .

e) EXPOSE 5000

f) CMD ["python", "app.py"]


Questão 2

a) docker build -t meu-sistema:1.0 .

b) docker run -d --name sistema-web -p 8080:5000 meu-sistema:1.0

c) docker ps

d) docker logs sistema-web

e) docker stop sistema-web

f) docker rm sistema-web


Questão 3

a) Uma imagem Docker é um modelo que contém os arquivos e dependências necessários para executar uma aplicação. Já o container é uma instância dessa imagem em execução, funcionando de forma isolada.

b) Isso aconteceu porque o container estava utilizando uma imagem antiga, que ainda continha a versão anterior do arquivo app.py.
Para resolver, o aluno precisa construir uma nova imagem com as alterações e criar um novo container utilizando essa imagem atualizada.

Comandos:

docker build -t meu-sistema:1.0 .
docker stop sistema-web
docker rm sistema-web
docker run -d --name sistema-web -p 8080:5000 meu-sistema:1.0

# Estudo Docker - Containers

## Sobre

Este repositório documenta meu aprendizado sobre Docker e containerização.

**Autor:** Daniel André de Oliveira

**Curso:** Técnico em Segurança Cibernética - 2026.2

**Disciplina:** Banco de Dados

**Data:** 17/09/2026

## O que estou aprendendo

- Conceitos fundamentais do Docker

- Como criar e gerenciar containers

- Trabalhar com imagens Docker

- Configurar bancos de dados em containers

- Usar Docker Compose para aplicações multi-container

## Estrutura do Projeto

- `containers/` - Dockerfiles e configurações de containers

- `compose/` - Arquivos docker-compose.yml

- `scripts/` - Scripts de configuração e inicialização

- `README.md` - Este arquivo de documentação

## Status do Estudo
- [ ✅ ] Tarefa 1 - Primeiro container

- [ ✅ ] Tarefa 2 - Container personalizado

- [ ✅ ] Tarefa 3 - Banco de dados

- [ ✅ ] Tarefa 4 - Docker Compose

- [ ✅ ] Tarefa 5 - Aplicação completa

# Reflexão Final

1. Qual a principal vantagem de usar containers com Docker em vez de instalar um banco de dados e um servidor web diretamente na sua máquina?

A principal vantagem é o isolamento e a facilidade de configuração. Com Docker, o banco de dados e o servidor web ficam dentro de containers, sem precisar instalar e configurar tudo diretamente no sistema operacional. Isso facilita a instalação, evita conflitos entre versões e permite reproduzir o mesmo ambiente em outra máquina com mais facilidade.

2. Explique com suas palavras o propósito de um Dockerfile. Por que ele é tão importante para a reprodutibilidade de ambientes?

O dockerfile basicamente contém as instruções necessárias para criar uma imagem Docker, como qual imagem base utilizar, quais arquivos copiar e quais comandos executar.Ele é importante para a reprodutibilidade porque permite criar o mesmo ambiente de forma padronizada em diferentes máquinas, evitando que seja necessário configurar tudo manualmente novamente, sendo um poupa-tempo absurdo!! 🔥

3. Em que cenário o Docker Compose se torna essencial? Por que não usar apenas múltiplos comandos docker run?

O Docker Compose se torna essencial quando uma aplicação precisa de vários containers funcionando juntos, como no nosso caso, em que temos um container para a aplicação Flask e outro para o banco de dados MySQL. Em vez de executar e configurar vários comandos `docker run` manualmente, o Compose permite definir toda a configuração em um único arquivo e iniciar os serviços juntos com um único comando. Isso facilita a organização, a configuração e a reprodução do ambiente.

4. Qual a importância dos volumes do Docker (como o que usamos para o banco de dados MySQL)? O que aconteceria com os dados se não usássemos um volume?

Os volumes são importantes porque permitem armazenar os dados de forma persistente, separando-os do ciclo de vida do container. No caso do MySQL, o volume permite que os dados continuem existindo mesmo se o container for removido e criado novamente. Sem um volume, os dados armazenados dentro do container seriam perdidos quando ele fosse removido.

5. Como o uso de containers pode facilitar o trabalho em equipe em um projeto de desenvolvimento de software?

O uso de containers facilita o trabalho em equipe porque permite que todos utilizem o mesmo ambiente de desenvolvimento, com as mesmas versões e configurações. Dessa forma, diminui a chance de problemas causados por diferenças entre os computadores dos integrantes. Além disso, arquivos como o `Dockerfile` e o `docker-compose.yml` permitem que o ambiente seja recriado de forma padronizada.

---
layout: default
title: Dia 2 - Autenticação e Design Inseguro
nav_order: 3
---

# Dia 2: Autenticação, Falhas Criptográficas e Design Inseguro

## Hoje vamos focar em exercícios práticos sobre autenticação, falhas criptográficas e design inseguro.

Mas primeiro vamos revisar alguns conceitos importantes.

## Requisições HTTP e HTTPS

HTTP (Hypertext Transfer Protocol) é o protocolo usado para comunicação entre clientes (como navegadores) e servidores web. Ele é baseado em texto e não criptografado, o que significa que os dados transmitidos podem ser interceptados e lidos por terceiros.

HTTPS (Hypertext Transfer Protocol Secure) é uma versão criptografada do protocolo HTTP. Ele utiliza SSL/TLS (Secure Sockets Layer/Transport Layer Security) para criptografar os dados transmitidos entre o cliente e o servidor, garantindo *confidencialidade e integridade*. Essas garantias são apenas para a origem, o destino e o canal (o que isso quer dizer?).

![WAT]({{ '/assets/images/wat.png' | relative_url }})

## API (Application Programming Interface)

APIs são conjuntos de definições e protocolos que permitem que diferentes softwares se comuniquem entre si. Elas definem como os componentes de software devem interagir, facilitando a integração e a troca de dados entre sistemas. APIs restful são um estilo arquitetural para projetar APIs que utilizam os princípios do REST (Representational State Transfer). Elas são baseadas em recursos, que são representações de dados, e utilizam métodos HTTP (GET, POST, PUT, DELETE) para realizar operações sobre esses recursos.

![API]({{ '/assets/images/api.png' | relative_url }})

CRUD é um acrônimo que representa as quatro operações básicas que podem ser realizadas em um banco de dados ou sistema de armazenamento de dados:
- **Create (Criar)**: Adicionar novos dados ou registros ao sistema.
- **Read (Ler)**: Recuperar ou visualizar dados existentes no sistema.
- **Update (Atualizar)**: Modificar ou alterar dados existentes no sistema.
- **Delete (Excluir)**: Remover dados ou registros do sistema.

![CRUD]({{ '/assets/images/crud.png' | relative_url }})]
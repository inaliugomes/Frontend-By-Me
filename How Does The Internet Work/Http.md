# HTTP e HTTPS

**HTTP (HyperText Transfer Protocol)** é um protocolo criado para permitir o envio e recebimento de dados na internet.

Os dados enviados pelo HTTP são **stateless**, ou seja, **cada requisição é independente** e não depende de estados anteriores.

---

## Métodos HTTP

- **GET** – Permite obter dados do servidor. Na ausência de outra indicação, esse é o método padrão.
- **POST** – Utilizado para **criar novos** dados no servidor.
- **PUT** – Utilizado para **atualizar** dados já existentes no servidor.
- **DELETE** – Utilizado para **excluir** registros existentes no servidor.

---

## HTTP vs HTTPS

De forma geral, o **HTTPS** é uma versão **mais segura** do HTTP. Ele utiliza **criptografia (SSL/TLS)** para proteger os dados durante a transmissão entre o cliente e o servidor.

A comunicação entre cliente e servidor (HTTPS) ocorre utilizando o modelo **TCP/IP**, ou seja:

- O **cliente** (por exemplo, o navegador) possui um **IP de origem**.
- O **servidor** tem um **IP de destino**.
- Os dados são enviados através da rede de forma confiável, e o servidor sabe para qual IP deve enviar a resposta.

---

## Status Codes

Ao fazer uma requisição HTTP, o servidor responde com **códigos de status (status codes)** no cabeçalho (headers) da resposta. Eles indicam o resultado da requisição:

- **200 OK** – Requisição bem-sucedida.
- **404 Not Found** – O recurso solicitado não foi encontrado.
- **401 Unauthorized** – Requisição feita sem autenticação ou com autenticação inválida.
- **403 Forbidden** – Acesso ao recurso proibido.

> Cada requisição é independente. Ou seja, se você fizer 30 requisições, elas serão executadas individualmente. Isso pode afetar a **performance** da aplicação.

---

## Three-Way Handshake (TCP)

Antes de iniciar o envio de dados entre cliente e servidor, ocorre um processo chamado **Three-Way Handshake**, que estabelece a conexão TCP:

1. **SYN** – O cliente envia um número aleatório ao servidor para iniciar a conexão.
2. **SYN-ACK** – O servidor reconhece a solicitação e envia de volta um pacote ACK com o número do cliente + 1.
3. **ACK** – O cliente confirma e envia um ACK com o número do servidor + 1.

Após isso, a conexão está estabelecida.

---

## HTTP/2

Lançado em **2015**, o **HTTP/2** trouxe melhorias significativas para o desempenho da web:

- Transmissão de dados em **binário** (em vez de texto).
- Suporte a **requisições assíncronas múltiplas** em uma única conexão TCP.
- **Server Push** – O servidor pode enviar múltiplas respostas de uma vez, mesmo antes do cliente pedir.
- **Maior segurança** e desempenho.

> Uma das principais limitações do HTTP/1.1 era permitir apenas **uma requisição por conexão**. O HTTP/2 resolve esse problema com **multiplexação**.


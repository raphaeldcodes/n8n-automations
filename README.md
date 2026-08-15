# Automação de Consulta de CEP com n8n e ViaCEP

Este é um projeto de automação no n8n onde construí um fluxo integrado a uma API pública para consultar dados de endereços a partir de um CEP e formatar a resposta final de maneira limpa.

## O que este projeto faz?

A automação simula uma integração de dados em tempo real conectando requisições HTTP a nós de transformação:

* **Entrada de Dados (Edit Fields):** Define o CEP de entrada (utilizando o CEP da Av. Paulista) para dar início ao processamento.
* **Consumo de API Externa (HTTP Request):** Faz uma requisição `GET` para a API pública do **ViaCEP**, enviando o CEP parametrizado e recebendo os dados completos do endereço em JSON.
* **Tratamento de Saída (Edit Fields):** Filtra e formata os dados retornados pela API, entregando no `output` final apenas as informações essenciais desejadas: a **Cidade** e o **UF**.

## Tecnologias Utilizadas

* **n8n** (Ferramenta de Automação de Fluxos)
* **API Pública do ViaCEP** (Serviço de consulta de CEPs)
* **JSON / REST**

## Estrutura do Fluxo

O projeto utiliza os seguintes nós integrados:

* `Edit Fields (Input)`: Configura as variáveis iniciais da consulta (CEP da Av. Paulista).
* `HTTP Request`: Realiza a chamada à API externa do ViaCEP.
* `Edit Fields (Output)`: Estrutura a resposta final exibindo apenas a cidade e o estado (UF).

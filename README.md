# 🦷 ETL de Pacientes em Clínica Odontológica com Gemini API

## 📋 Sobre o Projeto

Este projeto demonstra um processo simples de **ETL (Extract, Transform, Load)** em Python, adaptado a partir do desafio da Santander Dev Week 2023. O objetivo é simular a personalização da comunicação com clientes (neste caso, pacientes) usando o poder da **Inteligência Artificial Generativa (Gemini API)** para gerar mensagens de follow-up pós-tratamento.

O foco principal do estudo é a substituição da chamada a uma API externa de terceiros pela integração direta com o **Google GenAI SDK (Gemini)**.

### Fluxo de Execução

1.  **Extract (Extração):** Dados simulados de pacientes (ID, Nome e Tratamento) são carregados diretamente no script Python, representando o que seria extraído de um banco de dados ou CSV.
2.  **Transform (Transformação):** A API do **Gemini** é utilizada para analisar o nome e o tratamento de cada paciente e **gerar uma mensagem de follow-up** personalizada e persuasiva, incentivando a manutenção e o agendamento de consultas futuras.
3.  **Load (Carga):** A mensagem gerada pelo Gemini é anexada aos dados do paciente, simulando o envio para um sistema de comunicação ou a atualização de um registro em um banco de dados.

## 🚀 Execução no Google Colab

A maneira mais rápida de executar e testar este projeto é através do Google Colab, pois ele facilita a instalação de bibliotecas e a configuração de variáveis de ambiente.

Clique no link abaixo para abrir o notebook e começar:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/11haexUjexOLdjjj9rvcKUaSFB9_ogbz0?usp=sharing)

---

## 🔑 Pré-requisitos e Configuração

Para rodar o projeto, você precisará de uma chave de acesso à API do Gemini.

### 1. Obter a Chave API

1.  Acesse o **Google AI Studio** ou o **Google Cloud Console**.
2.  Gere uma nova chave API (ela é gratuita para o nível de uso de estudo).

### 2. Instalação (No Colab/Ambiente Local)

Instale o SDK oficial do Google GenAI:

```bash
!pip install google-genai

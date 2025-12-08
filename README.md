# 🦷 ETL de Pacientes em Clínica Odontológica com Gemini API

## 📋 Sobre o Projeto

Este projeto demonstra um processo simples de **ETL (Extract, Transform, Load)** em Python. Foi adaptado a partir de um desafio de engenharia de dados, com o objetivo de simular a personalização da comunicação com clientes, neste caso, **pacientes de uma clínica odontológica**.

Utilizamos o poder da **Inteligência Artificial Generativa (Gemini API)** para criar mensagens de follow-up pós-tratamento de forma inteligente e escalável.

O foco principal do estudo é a substituição de uma API externa de terceiros pela integração direta com o **Google GenAI SDK (Gemini)** para a etapa de transformação de dados.

### Fluxo de Execução

O projeto segue as três etapas clássicas do ETL: 

[Image of ETL process diagram showing Extract, Transform, Load steps]


1.  **Extract (Extração):** Dados simulados (ID, Nome e Tipo de Tratamento) são carregados diretamente no script Python, representando o processo de obtenção de dados de um banco de dados interno ou CSV.
2.  **Transform (Transformação):** A API do **Gemini** é invocada para ler o nome e o tratamento de cada paciente. O modelo atua como um especialista em marketing de saúde, gerando uma **mensagem de follow-up** personalizada e persuasiva, incentivando a manutenção e o agendamento de consultas futuras.
3.  **Load (Carga):** A nova mensagem gerada pelo Gemini é anexada ao registro de cada paciente, simulando a atualização de um sistema de comunicação ou a inserção em uma fila de envio de mensagens (e-mail, SMS, etc.).

***

## 🚀 Execução e Acesso ao Código

O código completo do projeto está disponível em um notebook **Google Colab**, facilitando a execução e o teste, sem a necessidade de uma configuração de ambiente local complexa.

Clique no link abaixo para acessar o notebook:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/11haexUjexOLdjjj9rvcKUaSFB9_ogbz0?usp=sharing)

***

## 🔑 Pré-requisitos (Conceitual)

Para que este projeto funcione, é necessário:

1.  **SDK:** Ter a biblioteca `google-genai` instalada no ambiente Python.
2.  **Chave API:** Possuir uma chave de acesso à **API do Gemini** (obtida no Google AI Studio).
3.  **Configuração:** A chave API deve ser configurada como uma variável de ambiente (`GEMINI_API_KEY`) no ambiente de execução do script (Colab, terminal, etc.).

***

## 📂 Estrutura de Dados (Conceitual)

Os dados de entrada (simulados) são uma lista de objetos JSON. O campo `follow_up_messages` é inicialmente vazio e é preenchido pelo resultado da API.

**Exemplo de Objeto de Paciente:**

* `"id"`: Identificador do paciente.
* `"name"`: Nome do paciente (ex: Ana Silva).
* `"treatment"`: Tratamento realizado (ex: Limpeza Profissional).
* `"follow_up_messages"`: Lista onde a mensagem gerada pelo Gemini será inserida.

***

## 🧠 Detalhes da Transformação (Gemini)

A transformação é realizada por uma função que constrói um **prompt** detalhado com as informações do paciente.

* **Modelo Utilizado:** O **`gemini-2.5-flash`** é o modelo escolhido para a transformação, devido à sua alta velocidade e eficiência para a geração de texto conciso.
* **Função:** A função central do Python envia o prompt ao Gemini, que retorna a mensagem formatada para ser utilizada na comunicação com o paciente.

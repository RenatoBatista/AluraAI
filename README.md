# Assistente IA para Pais de Primeira Viagem - O PapAI

Este projeto é um assistente virtual interativo, construído em Python e executado no Google Colab, projetado para fornecer informações e conselhos a pais de primeira viagem sobre diversos temas relacionados aos cuidados com o bebê. Ele utiliza a API Gemini do Google para gerar respostas personalizadas e empáticas.

## Funcionalidades Principais

* **Agentes Especialistas:** O assistente conta com diferentes agentes de IA, cada um especializado em um tema:
    * Sono do Bebê
    * Alimentação do Bebê
    * Cuidados Diários com o Bebê
    * Vacinas do Bebê (com sub-tópicos para calendário geral e reações)
    * Choro e Cólicas do Bebê
    * Saltos de Desenvolvimento
    * Dúvidas Gerais
* **Interface Interativa no Colab:** Utiliza `ipywidgets` para criar uma interface com botões e campos de texto, facilitando a interação do usuário.
* **Personalização:** Calcula a idade do bebê com base na data de nascimento fornecida e permite a entrada de informações opcionais sobre a rotina e o ambiente para contextualizar melhor os conselhos.
* **Fluxo de Conversa:**
    1.  Coleta da data de nascimento do bebê.
    2.  Seleção de um tema principal de interesse.
    3.  Coleta de dados opcionais para personalizar o conselho.
    4.  Apresentação do conselho pelo agente especialista.
    5.  Opções pós-conselho:
        * Tirar mais dúvidas sobre o mesmo tema.
        * Voltar ao menu de temas principais.
        * Encerrar a consulta.
* **Foco em Segurança:** Inclui disclaimers importantes, reforçando que o assistente não substitui a orientação de profissionais de saúde.

## Configuração

1.  **API Key do Google Gemini:**
    * Obtenha uma API Key do Google AI Studio (ou da plataforma correspondente do Google Cloud).
    * No Google Colab, clique no ícone de chave (🔑) na barra lateral esquerda ("Secrets").
    * Adicione um novo secret com o nome `GOOGLE_API_KEY`.
    * Cole sua chave da API no campo de valor.
    * Certifique-se de que a opção "Notebook access" está ativada para este secret.

2.  **Instalação de Bibliotecas:**
    * Execute a primeira célula do notebook Colab para instalar as bibliotecas necessárias (se ainda não estiverem instaladas no seu ambiente):
        ```python
        # !pip install -q google-generativeai
        # !pip install -q google-adk
        # !pip install -q ipywidgets
        ```

## Como Executar

1.  Abra o notebook (`.ipynb`) no Google Colab.
2.  Certifique-se de que a API Key está configurada conforme descrito acima.
3.  Execute todas as células do notebook em ordem.
4.  A interface interativa aparecerá na área de saída da célula principal, começando com a solicitação da data de nascimento do bebê. Siga as instruções na tela para interagir com o assistente.

## Estrutura do Código

* **Etapa 0:** Instalação de bibliotecas.
* **Etapa 1:** Configuração da API Key do Google Gemini.
* **Etapa 2:** Funções auxiliares (chamada aos agentes, formatação de texto, cálculo de idade).
* **Etapa 3:** Definições dos agentes especialistas (instruções/prompts para cada tema).
* **Etapa 4:** Lógica principal do programa interativo (gerenciamento da UI com `ipywidgets`, fluxo de interação).
* **Etapa 5:** Ponto de entrada para executar o assistente.

## Modelo de IA Utilizado

* O assistente utiliza, por padrão, o modelo `gemini-1.5-flash-latest` da API Gemini do Google.

## Observações

* Este é um projeto de demonstração e aprendizado. As informações fornecidas pelo assistente são para fins informativos e não devem substituir o conselho de um pediatra ou outro profissional de saúde qualificado.
* A qualidade das respostas do assistente depende significativamente das instruções (prompts) fornecidas aos agentes de IA e da capacidade do modelo subjacente.



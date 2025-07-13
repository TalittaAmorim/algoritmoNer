
# Mini-Projeto: Reconhecimento de Entidades Nomeadas (NER) em Português

Este repositório contém um mini-projeto de Reconhecimento de Entidades Nomeadas (NER) desenvolvido como parte de um estágio em Ciência de Dados e Inteligência Artificial. O projeto foca em demonstrar a aplicação básica de técnicas de NER para extrair informações estruturadas de textos, com um olhar para um domínio específico (reuniões).

## 1\. Visão Geral do Projeto

O principal objetivo deste mini-projeto é consolidar o entendimento prático do NER e sua aplicação, especialmente na identificação de entidades comuns e na simulação da extração de entidades customizadas relevantes para um contexto específico de negócios. O projeto utiliza a biblioteca SpaCy para processamento de linguagem natural e o Pandas para estruturação dos dados.

## 2\. Funcionalidades e Aprendizados

  * **Aplicação de NER Pré-treinado:** Utiliza um modelo pré-treinado da biblioteca SpaCy (especificamente para o português, `pt_core_news_sm`) para identificar e extrair entidades padrão (como Pessoas, Locais, Organizações e Datas) de textos não estruturados.
  * **Simulação de Entidades Customizadas:** Para demonstrar a necessidade e o potencial do NER em domínios específicos, o projeto simula a extração de entidades customizadas como `CARGOS`, `ÁREA` e `TERMOS_TECNOLÓGICOS`, que são cruciais para a análise de atas de reunião.
  * **Estruturação de Dados com Pandas:** As entidades extraídas (tanto as padrão do SpaCy quanto as customizadas simuladas) são organizadas e apresentadas em um Pandas DataFrame. Essa estruturação é um esboço prático de como os dados de entrada e saída de um sistema NER seriam representados em um pipeline de IA maior.
  * **Conexão com o Projeto Principal (PDW):** Este mini-projeto serve como um fundamento prático para o desenvolvimento futuro de um algoritmo de NER para o projeto PDW, ajudando a visualizar a modelagem de dados e o formato esperado das saídas.

## 3\. Como Executar o Projeto

Para rodar este mini-projeto em sua máquina local, siga os passos abaixo:

1.  **Clone o Repositório:**
    ```bash
    git clone <URL_DO_SEU_REPOSITÓRIO>
    cd seu-projeto-ner
    ```
2.  **Crie e Ative um Ambiente Virtual:**
    É altamente recomendável utilizar um ambiente virtual para gerenciar as dependências do projeto.
    ```bash
    python -m venv .venv
    # No Windows (Cmd): .\.venv\Scripts\activate.bat
    # No Windows (PowerShell): .\.venv\Scripts\Activate.ps1
    # No macOS/Linux: source ./.venv/bin/activate
    ```
3.  **Instale as Dependências:**
    Com o ambiente virtual ativado, instale as bibliotecas necessárias listadas no arquivo `requirements.txt`.
    ```bash
    pip install -r requirements.txt
    ```
    *Obs: Certifique-se de que o modelo do SpaCy (`pt_core_news_sm` ou `en_core_web_sm`) também foi baixado. Se não, execute no terminal com o ambiente ativo: `python -m spacy download pt_core_news_sm`.*
4.  **Execute o Notebook/Script:**
    Abra o arquivo Jupyter Notebook (`seu_notebook.ipynb`) no VS Code (certifique-se de que o kernel do ambiente virtual está selecionado) e execute as células, ou execute o script Python (`seu_script.py`) diretamente.



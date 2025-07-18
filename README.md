Algoritmo Híbrido de Reconhecimento de Entidades (NER)
Um protótipo para extrair e classificar entidades nomeadas de transcrições de reuniões, utilizando uma abordagem híbrida com SpaCy.

Este projeto foi desenvolvido como uma tarefa prática para aplicar conhecimentos em Processamento de Linguagem Natural (PLN). O objetivo principal é analisar textos não estruturados, como a transcrição da reunião da PDW, e extrair informações valiosas de forma automatizada.

Principais Funcionalidades
Análise de Texto em Inglês: O algoritmo é configurado para processar textos no idioma inglês.

Extração Híbrida de Entidades: Utiliza uma abordagem em duas camadas para garantir tanto a amplitude quanto a precisão:

Modelo Pré-treinado: Usa o modelo en_core_web_lg do SpaCy para identificar entidades genéricas como PERSON (Pessoas), ORG (Organizações) e DATE (Datas).

Regras Customizadas: Emprega o PhraseMatcher para encontrar e classificar com precisão um dicionário de termos específicos do negócio, como CARGO e TERMO_TEC.

Visualização de Resultados: Gera um gráfico de barras com a biblioteca Matplotlib, mostrando a contagem total de cada tipo de entidade encontrada, facilitando a análise dos resultados.

Exportação do Gráfico: Salva o gráfico gerado como um arquivo de imagem (.png) no diretório do projeto.

Como Funciona (Pipeline)
O fluxo de trabalho do algoritmo segue 4 etapas principais:

Leitura do Arquivo: O script inicia lendo um arquivo de texto (.txt) que contém a transcrição da reunião.

Processamento Híbrido: O texto é processado pelo SpaCy. O modelo de IA identifica as entidades gerais, enquanto o PhraseMatcher busca no mesmo texto os termos customizados definidos nas listas.

Análise e Contagem: Todas as entidades coletadas (padrão e customizadas) são organizadas em um DataFrame com a biblioteca Pandas para facilitar a manipulação.

Geração do Gráfico: A contagem de cada tipo de entidade é calculada e um gráfico de barras horizontal é gerado com Matplotlib, exibindo visualmente a frequência de cada categoria.

Configuração do Ambiente
Siga os passos abaixo para executar o projeto.

Pré-requisitos
Python 3.8 ou superior

pip (gerenciador de pacotes do Python)

Instalação
Clone este repositório (ou simplesmente crie uma pasta com os arquivos).

Instale as bibliotecas necessárias:

pip install spacy pandas matplotlib

Baixe o modelo de linguagem do SpaCy para inglês:

python -m spacy download en_core_web_lg

Como Usar
Coloque o arquivo com a transcrição da reunião na mesma pasta que o script principal. O código espera um arquivo chamado PDW_Meeting_Follow_UP_03122024.txt.

Execute o script Python pelo terminal:

python seu_script.py

O script irá:

Exibir no terminal uma tabela com as entidades encontradas.

Gerar e salvar um gráfico chamado contagem_entidades.png no mesmo diretório.

Exemplo de Saída
Após a execução, um gráfico como este será gerado, mostrando a distribuição das entidades encontradas:

Próximos Passos
Este protótipo serviu como uma base fundamental para validar a tecnologia e planejar a evolução do projeto. Os próximos passos incluem:

Validação de Casos de Uso: Detalhar e priorizar as aplicações práticas do NER para o negócio.

Criação de Dataset Customizado: Iniciar o processo de coleta e anotação de dados internos para treinar um modelo especialista.

Fine-Tuning do Modelo: Utilizar o dataset customizado para especializar um modelo de linguagem (como os da família BERT/Transformers), visando uma precisão e capacidade de generalização ainda maiores.
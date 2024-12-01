# Problema
Executar o fine-tuning de um foundation model (Llama, BERT, MISTRAL etc.), utilizando o dataset `AmazonTitles-1.3MM`.

O modelo treinado deverá:
- Receber perguntas com um contexto obtido por meio do arquivo json `trn.json` que está contido dentro do dataset.
- A partir do prompt formado pela pergunta do usuário sobre o título do produto, o modelo deverá gerar uma resposta baseada na pergunta do usuário trazendo como resultado do aprendizado do fine-tuning os dados da sua descrição.

## Fluxo de trabalho atualizado:

### 1. Escolha do Dataset:
O dataset `AmazonTitles-1.3MM` consiste em consultas textuais reais de usuários e títulos associados de produtos relevantes encontrados na Amazon e suas descrições, medidos por ações implícitas ou explícitas dos usuários.

### 2. Preparação do Dataset:
Faça o download do dataset [`AmazonTitles-1.3MM`](https://drive.google.com/file/d/12zH4mL2RX8iSvH0VCNnd3QxO4DzuHWnK/view) e utilize o arquivo `trn.json`.
Nele, você utilizará as colunas `title` e `content`, que contêm título e descrição respectivamente.
Prepare os prompts para o fine-tuning garantindo que estejam organizados de maneira adequada para o treinamento do modelo escolhido.
Limpe e pré-processe os dados conforme necessário para o modelo escolhido.

### 3. Chamada do Foundation Model
Importe o foundation model que será utilizado e faça um teste apresentando o resultado atual do modelo antes do treinamento (para que se obtenha uma base de análise após o fine-tuning), e então será possível avaliar a diferença do resultado gerado.

### 4. Execução do Fine-Tuning:
Execute o fine-tuning do foundation model selecionado (por exemplo, BERT, GPT, Llama) utilizando o dataset preparado.
Documente o processo de fine-tuning, incluindo os parâmetros utilizados e qualquer ajuste específico realizado no modelo.

### 5. Geração de Respostas:
Configure o modelo treinado para receber perguntas dos usuários.
O modelo deverá gerar uma resposta baseada na pergunta do usuário e nos dados provenientes do fine-tuning, incluindo as fontes fornecidas.

#### O que esperamos para o entregável?
- Documento detalhando o processo de seleção e preparação do dataset.
- Descrição do processo de fine-tuning do modelo, com detalhes dos parâmetros e ajustes utilizados.
- Código-fonte do processo de finetuning.
- Um vídeo demonstrando o modelo treinado gerando respostas a partir de perguntas do usuário e utilizando o contexto obtido por meio treinamento com o fine-tuning.
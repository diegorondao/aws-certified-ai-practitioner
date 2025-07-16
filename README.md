# AWS Certified AI Practitioner (AIF-C01) - Anotações de Estudo

## Links Úteis
- [Guia Oficial do Exame](https://d1.awsstatic.com/training-and-certification/docs-ai-practitioner/AWS-Certified-AI-Practitioner_Exam-Guide.pdf)
- [Preparação Oficial para o Exame - Amazon Skill Builder](https://explore.skillbuilder.aws/learn/course/internal/view/elearning/19554/exam-prep-standard-course-aws-certified-ai-practitioner-aif-c01) - recomendo assistir em 1.5x
- [Questões Oficiais de Prática](https://explore.skillbuilder.aws/learn/course/internal/view/elearning/19790/exam-prep-official-practice-question-set-aws-certified-ai-practitioner-aif-c01-english) - No nível do exame real.

### General AI
- **Definição**: Refere-se ao conceito mais amplo de inteligência artificial, com o objetivo de construir sistemas capazes de executar qualquer tarefa intelectual que um humano possa realizar. É frequentemente usado para descrever objetivos de longo prazo de criar sistemas de IA altamente autônomos e flexíveis.
- **Conceito-chave**: IA com capacidade ampla de executar múltiplas tarefas em diferentes domínios, ao contrário de sistemas de IA especializados.
- **Exemplos**: **Sistemas Especialistas**, **Engines de Regras** (ex: MYCIN), que usam lógica e regras pré-definidas para tomar decisões.

### Machine Learning (ML)
- **Definição**: Um subconjunto de IA que permite que sistemas aprendam a partir de dados e façam previsões ou decisões sem programação ou regras explícitas.
- **Conceito-chave**: IA que opera por meio de padrões de dados e treinamento, em vez de instruções codificadas explicitamente.
- **Exemplos**: **Regressão Linear**, **Árvores de Decisão**, **Máquinas de Vetores de Suporte** — algoritmos de aprendizado supervisionado usados para tarefas preditivas.

### Deep Learning
- **Definição**: Um subconjunto de machine learning que utiliza redes neurais com múltiplas camadas (por isso "deep") para modelar padrões complexos em dados.
- **Conceito-chave**: Eficaz para tarefas como reconhecimento de imagens, processamento de linguagem natural e sistemas autônomos.
- **Exemplos**: **Redes Neurais Convolucionais (CNNs)** para processamento de imagens, **Redes Neurais Recorrentes (RNNs)** para dados sequenciais como séries temporais ou modelos de linguagem.

### Generative AI
- **Definição**: Um subconjunto de deep learning focado em criar novos conteúdos (como texto, imagens ou música) a partir de dados aprendidos. Modelos de Generative AI geralmente são baseados em **foundation models**, que são modelos grandes e pré-treinados que podem ser adaptados para uma ampla gama de tarefas.
- **Conceito-chave**: Sistemas de IA que geram saídas inéditas com base em padrões aprendidos durante o treinamento. Foundation models fornecem a versatilidade necessária para fine-tuning em tarefas específicas.
- **Exemplos**: **ChatGPT** para geração de texto, **DALL·E** para geração de imagens, **DeepDream** para geração visual artística.

### Large Language Models (LLMs)
- **Definição**: Um tipo de **Generative AI** focado em compreender e gerar texto semelhante ao humano. LLMs são treinados com grandes volumes de dados textuais para aprender padrões de linguagem, gramática e contexto.
- **Conceito-chave**: LLMs geram texto coerente e de alta qualidade com base em prompts de entrada e são capazes de realizar tarefas como sumarização, tradução e resposta a perguntas.
- **Exemplos**: **GPT-4**, **BERT**, **T5**, **Claude 2** — usados para tarefas como geração de texto, análise de sentimento, sumarização e compreensão de linguagem natural.

---

## Conceitos

### In-Context Learning
- **Definição**: Método de aprimorar modelos generativos de IA adicionando dados e exemplos extras ao prompt, ajudando o modelo a resolver tarefas de forma mais eficaz.

### Tipos de Prompt
- **Few-Shot Prompt**: Fornece alguns exemplos no prompt para guiar o comportamento do modelo.
- **Zero-Shot Prompt**: Não fornece exemplos no prompt, pedindo ao modelo para realizar a tarefa sem orientação.
- **One-Shot Prompt**: Fornece exatamente um exemplo para guiar o comportamento do modelo.
- **Prompt Template**: Um formato ou estrutura pré-definida para prompts, padronizando e melhorando a interação com modelos de IA.
- **Chain-of-Thought Prompting**: Método em que o prompt incentiva o modelo a dividir o raciocínio em etapas.
- **Prompt Tuning**: Processo de ajustar prompts para melhorar o desempenho do modelo em tarefas específicas.

### Latent Space
- **Definição**: O conhecimento ou padrões codificados capturados por LLMs que armazenam relações entre dados.
- **Uso**: Representa o entendimento interno de linguagem ou dados que os modelos de IA usam para gerar saídas.

### Embeddings
- **Definição**: Representações numéricas vetorizadas de tokens (palavras, frases, etc.) que capturam seu significado semântico.
- **Caso de uso**: Usado em tarefas como busca semântica, onde o significado de uma palavra ou token é importante.
- **Armazenamento**: Podem ser armazenados em um banco de dados vetorial para busca e recuperação eficiente.

### Tokens
- **Definição**: As unidades básicas de texto (ex: palavras, subpalavras ou caracteres) processadas por modelos de linguagem. No contexto de LLMs, tokens representam tanto entradas (texto fornecido) quanto saídas (texto gerado).

### Context-Window
- **Definição**: A quantidade máxima de tokens que um modelo LLM pode processar de uma vez, incluindo tanto o prompt de entrada quanto a saída gerada. Se o número de tokens exceder o context-window do modelo, partes anteriores do texto podem ser truncadas.
- **Uso**: O context-window é um fator chave para determinar quanta informação pode ser fornecida ao modelo de uma só vez e afeta tarefas como geração de texto longo, análise de documentos ou conversas multi-turno.

### Alucinações
- **Definição**: Ocorrem quando um modelo de linguagem gera informações incorretas ou sem sentido que podem soar plausíveis, mas não são fundamentadas em dados factuais ou no input fornecido.
- **Mitigações**:
  - Retrieval Augmented Generation (RAG): Reduz alucinações recuperando dados externos relevantes durante o processo de geração, garantindo que o modelo gere respostas baseadas em informações precisas.
  - Fine-Tuning: Treinar o modelo com dados mais relevantes e precisos pode ajudar a reduzir alucinações, alinhando a saída do modelo com conhecimento factual.
  - Human-in-the-Loop (HITL): Incorporar revisão humana em áreas de baixa confiança pode evitar que saídas alucinadas sejam usadas em aplicações críticas.

### Modelos Multi-Modais
- **Definição**: Modelos que trabalham com múltiplos tipos de dados, incorporando texto, imagens ou até áudio em um espaço compartilhado. São usados em tarefas multimodais, como criar legendas para imagens ou gerar visuais a partir de descrições textuais, aproveitando diferentes tipos de input para produzir saídas mais ricas e contextuais.
  
---

### Métodos de Busca
- **Keyword Search**: Busca por termos exatos na consulta.
- **Semantic Search**: Usa embeddings para entender o significado por trás da consulta, permitindo resultados mais precisos e relevantes.

---

### Bancos de Dados Vetoriais
- **Definição**: Tipo de banco de dados projetado para armazenar e consultar vetores (embeddings), útil para tarefas como busca semântica.

#### Opções de Banco de Dados Vetoriais na AWS
- **Amazon OpenSearch Service**: Suporta busca de k-vizinhos mais próximos (k-NN) para bancos de dados vetoriais. Útil para análise de logs, monitoramento de aplicações em tempo real e busca.
- **Amazon Aurora PostgreSQL-Compatible Edition & Amazon RDS for PostgreSQL**: Suporta a extensão __pgvector__, permitindo o armazenamento eficiente de embeddings e buscas por similaridade.
- **Amazon Neptune ML**: Usa Redes Neurais Gráficas (GNNs) para fazer previsões com base em dados de grafo, suportando dados vetorizados em bancos de dados de grafo.
- **Amazon MemoryDB**: Suporta armazenamento e recuperação de vetores em alta velocidade com tempos de consulta de milissegundos e dezenas de milhares de consultas por segundo (QPS).
- **Amazon DocumentDB**: Suporta busca vetorial com compatibilidade com MongoDB, permitindo armazenamento, indexação e busca de milhões de vetores com tempos de resposta de milissegundos.

--- 

## O Pipeline de Machine Learning (ML)

O Pipeline de ML é um processo sistemático usado para construir, treinar e implantar modelos de machine learning. Garante que cada etapa, desde a identificação de objetivos de negócios até o monitoramento de modelos implantados, seja gerenciada e otimizada para desempenho. As etapas típicas no pipeline são as seguintes:

**Etapas:**
1. Identificar o Objetivo de Negócio
2. Estruturar o Problema de ML
3. Coletar Dados
4. Pré-processar Dados
5. Engenharia de Atributos
6. Treinar, Ajustar, Avaliar
7. Implantar
8. Monitorar

---

### 1. Identificar o Objetivo de Negócio
- **Descrição**: Definir critérios de sucesso e alinhar as partes interessadas para garantir que o projeto de ML atenda aos objetivos de negócios.
- **Atividades-chave**:
  - Estabelecer métricas de sucesso claras.
  - Alinhar com as partes interessadas em toda a organização.

### 2. Estruturar o Problema de ML
- **Descrição**: Definir o problema de ML, entradas, saídas e métricas, considerando viabilidade e análise de custo/benefício.
- **Atividades-chave**:
  - Identificar entradas, saídas, requisitos e métricas de desempenho.
  - Realizar análise de custo-benefício para avaliar a viabilidade.
  
- **Opções de Modelo**:
  - **Serviço de AI/ML Hospedado** (ex: AWS Comprehend, Forecast, Personalize): Nenhum treinamento necessário.
  - **Modelos Pré-treinados** (ex: Amazon Bedrock, SageMaker JumpStart): Ajuste fino com seus dados.
  - **Modelo Totalmente Personalizado**: Construir e treinar do zero.

### 3. Coletar Dados

- **Descrição**: Coletar e preparar os dados necessários para treinar o modelo.

- **Atividades-chave**:
  - Identificar fontes de dados (ex: bancos de dados, lagos de dados, APIs externas).
  - Ingestão e rotulagem de dados.

- **Onde os Dados são Armazenados**:  
  - Os dados coletados para machine learning são tipicamente armazenados no **Amazon S3**. Isso se aplica tanto a dados provenientes de sistemas internos quanto a conjuntos de dados de terceiros acessados via **AWS Data Exchange**.

- **Ferramentas**:
  - **AWS Glue**: Para processos de **ETL (Extração, Transformação, Carga)**, movendo e transformando dados em um formato utilizável antes do armazenamento no **Amazon S3**.
  - **SageMaker Ground Truth**: Para rotulagem humana de dados ambíguos, com dados rotulados armazenados no **Amazon S3**.
  - **AWS Data Exchange**: Permite acesso seguro a conjuntos de dados de terceiros. Esses conjuntos de dados podem ser usados como fontes adicionais de dados de treinamento, e os dados ingeridos são armazenados no **Amazon S3**.
  - **Amazon S3**: Serviço de armazenamento principal onde os dados coletados são armazenados com segurança antes de serem processados ou usados para treinamento.

### 4. Pré-processar Dados

- **Descrição**: Limpar e preparar os dados, garantindo que sejam adequados para o treinamento.

- **Atividades-chave**:
  - Realizar **Análise Exploratória de Dados (EDA)**.
  - Limpar os dados, removendo duplicatas, preenchendo valores ausentes e anonimizando **PII**.
  - Os dados são frequentemente divididos em proporções de **treinamento (80%)**, **validação (10%)** e **teste (10%)**.

- **Como Limpar os Dados**:
  - **Transformações do AWS Glue**: O Glue possui transformações integradas para tarefas como remoção de duplicatas ou preenchimento de valores ausentes, e permite transformações personalizadas usando Python ou Spark.
  - **Macie para PII**: O AWS Macie detecta e anonimiza dados de **PII**, trabalhando com o **Amazon S3** para escanear e mascarar informações sensíveis.
  - **AWS Glue DataBrew**: Permite a preparação e limpeza de dados por meio de uma interface visual. Você pode aplicar **regras de qualidade de dados**, como preenchimento de valores ausentes, e salvar essas transformações como **receitas** para reutilização.
  - **SageMaker Canvas**: Facilita a importação, transformação e visualização de dados sem exigir conhecimento técnico profundo. Usa transformações integradas que são adicionadas passo a passo para preparar os dados para treinamento, e cada passo pode ser rastreado visualmente no fluxo.

- **Ferramentas**:
  - **AWS Glue**: Um serviço de ETL com transformações integradas para limpeza de dados.
  - **AWS Glue DataBrew**: Uma ferramenta visual de preparação de dados onde você pode definir e aplicar regras de transformação (chamadas de **receitas**), com verificações de qualidade de dados integradas.
  - **SageMaker Canvas**: Uma ferramenta para importar, preparar e transformar dados com uma interface visual e sem código. Cada transformação é parte de um fluxo de trabalho claro, facilitando a preparação dos dados.

### 5. Engenharia de Atributos
- **Descrição**: Selecionar e criar atributos que melhorarão o desempenho do modelo.
- **Atividades-chave**:
  - Seleção de Atributos: Identificar os atributos mais relevantes do conjunto de dados com base no conhecimento do domínio, reduzindo a dimensionalidade e melhorando a eficiência do modelo.
  - Criação de Atributos: Transformar dados brutos em novos atributos (ex: escalonamento, codificação de variáveis categóricas e derivação de novas métricas a partir das existentes).
  - Transformação de Atributos: Aplicar transformações matemáticas ou estatísticas (ex: normalização, padronização) para melhorar a convergência e o desempenho do modelo.
- Engenharia de Atributos Automatizada: Considere usar o SageMaker Autopilot, que pode gerar e classificar automaticamente atributos que podem melhorar o desempenho do modelo.
- Redução de Dimensionalidade: Técnicas como Análise de Componentes Principais (PCA) podem ser aplicadas para reduzir o número de atributos, mantendo as informações mais importantes.
- Escalonamento de Atributos: Ferramentas como AWS Glue ou SageMaker DataBrew podem ser usadas para aplicar técnicas de escalonamento (ex: normalização ou padronização), garantindo que os atributos contribuam igualmente para o treinamento do modelo.
- Codificação Categórica: Converter variáveis categóricas em valores numéricos usando técnicas como codificação one-hot ou codificação de alvo usando SageMaker Data Wrangler ou AWS Glue.
  
- **Ferramentas**:
  - **SageMaker Feature Store**: Armazenar e gerenciar atributos como uma única fonte da verdade.

### 6. Treinar, Ajustar e Avaliar o Modelo
- **Descrição**: Treinar o modelo, ajustá-lo e avaliar seu desempenho.
- **Atividades-chave**:
  - Treinar o modelo iterativamente e ajustar parâmetros.
  - Ajustar hiperparâmetros (ex: época, tamanho do lote, taxa de aprendizado) e executar experimentos.
  - Avaliar o modelo usando métricas e comparar desempenho.

- **Parâmetros**:

  - **Parâmetros de Inferência** (suportados pelo Amazon Bedrock):
    - **Aleatoriedade e Diversidade**:
      - Temperatura:
        - Controla a aleatoriedade — valores mais altos levam a saídas mais diversas e criativas; valores mais baixos produzem resultados mais previsíveis e determinísticos.
      - Top K:
        - Limita o modelo a selecionar entre os K tokens mais prováveis; valores menores de K resultam em escolhas mais seguras e previsíveis.
        - Top K não é um parâmetro muito útil - use Temperatura ou Top-P em vez disso. 
      - Top P:
        - Usa probabilidade cumulativa para escolher tokens, focando no menor conjunto de tokens com uma probabilidade combinada de P, equilibrando aleatoriedade e diversidade.
        - Valores mais altos de Top P (mais próximos de 1) reduzem a aleatoriedade restringindo o conjunto de tokens apenas às escolhas mais prováveis. 
      - Top-K vs Top-P: Top K fixa o número de tokens considerados, enquanto Top P usa um número variável de tokens com base em sua probabilidade combinada, tornando o Top P mais adaptável e flexível no equilíbrio entre aleatoriedade e precisão.
      - Temperatura vs. Top P: Temperatura ajusta a aleatoriedade geral escalonando probabilidades, permitindo mais ou menos aleatoriedade em todos os tokens possíveis. Top P estreita as escolhas de tokens para aqueles que coletivamente atingem um determinado limiar de probabilidade, equilibrando aleatoriedade com precisão.
      - Casos de Uso:
        - Use Top-P quando quiser diversidade adaptativa, mas deseja permanecer mais próximo dos resultados mais prováveis.
        - Use Temperatura quando precisar de controle consistente sobre a aleatoriedade em geral.  
    - Comprimento da resposta:
      - Especifica o comprimento máximo da saída gerada, afetando quão verbosa ou concisa é a resposta.
    - Penalidades:
      - Aplica penalidades a tokens ou sequências repetidas para incentivar a variedade no texto gerado.
    - Sequências de parada:
      - Define sequências específicas onde o modelo parará de gerar texto, garantindo um comprimento ou formato de saída controlado.
  - **Parâmetros de Treinamento do Modelo** (Hiperparâmetros):
    - **Época**: O número de iterações por todo o conjunto de dados.
      - Aumentar as épocas geralmente melhora o aprendizado do modelo, mas pode levar ao overfitting se muito alto. Mais épocas ajudam o modelo a aprender melhor, mas também podem resultar em retornos decrescentes após um certo ponto.
    - **Tamanho do Lote**: Número de amostras antes de atualizar os parâmetros do modelo.
      - Tamanhos de lote menores fornecem atualizações mais frequentes, o que pode ajudar na convergência rápida, mas pode introduzir mais ruído. Tamanhos de lote maiores são mais estáveis, mas podem exigir mais computação e memória.
    - **Taxa de Aprendizado**: Controla a rapidez com que o modelo aprende.
      - Uma taxa de aprendizado alta acelera o treinamento, mas pode pular soluções ótimas, enquanto uma taxa de aprendizado baixa leva a uma convergência mais lenta, mas mais precisa, embora corra o risco de ficar preso em mínimos locais.
        
- **Métricas de Erro**:

  - **MSE (Erro Quadrático Médio)**: Durante a avaliação do modelo, o MSE calcula a média das diferenças ao quadrado entre os valores previstos e os valores reais, dando mais peso a erros maiores. Um MSE mais baixo indica melhor desempenho, sendo útil para comparar diferentes modelos ou ajustar hiperparâmetros.
    - **Caso de Uso**: Útil em problemas de regressão como previsão de preços de casas ou valores de ações.
    - **Regra Geral**: Quanto mais baixo, melhor, pois significa que as previsões do modelo estão mais próximas dos valores reais.
    
  - **RMSE (Raiz do Erro Quadrático Médio)**: RMSE é a raiz quadrada do MSE e fornece uma medida de erro na mesma unidade que os valores previstos, tornando-a mais interpretável. O RMSE é usado para ver quão grande erro é esperado por previsão.
    - **Caso de Uso**: Frequentemente usado ao lado do MSE em problemas de regressão para uma interpretabilidade mais fácil.
    - **Regra Geral**: RMSE mais baixo significa melhor desempenho do modelo.
  
  - **Perplexidade**: A perplexidade mede quão bem um modelo prevê uma sequência de tokens (ex: palavras). Uma perplexidade mais baixa indica melhor desempenho, pois significa que o modelo é melhor em prever a próxima palavra em uma sequência.
    - **Caso de Uso**: Comumente usada para modelos de linguagem, como avaliar quão bem um modelo prevê a próxima palavra em uma frase.
    - **Regra Geral**: Perplexidade mais baixa significa melhor desempenho preditivo.
  
  - **Precisão**: A precisão é a razão entre verdadeiros positivos e o número total de previsões positivas (verdadeiros positivos + falsos positivos). É usada quando minimizar falsos positivos é importante.
    - **Caso de Uso**: Frequentemente usada em tarefas de classificação como detecção de spam, onde evitar falsos positivos é crítico.
    - **Regra Geral**: Maior precisão é melhor quando o custo de falsos positivos é alto.
  
  - **Recall (TPR)**: Recall (Taxa de Verdadeiros Positivos) é a razão entre verdadeiros positivos e o total de positivos reais (verdadeiros positivos + falsos negativos). É usada quando minimizar falsos negativos é crucial.
    - **Caso de Uso**: Comumente usada em testes médicos (ex: triagens de doenças) para evitar perder casos positivos.
    - **Regra Geral**: Maior recall é melhor quando perder casos positivos é custoso.
  
  - **Taxa de Falsos Positivos (FPR)**: FPR é a razão entre falsos positivos e o número total de negativos (falsos positivos + verdadeiros negativos). É usada para medir com que frequência previsões positivas incorretas são feitas.
    - **Caso de Uso**: Frequentemente usada em aplicações de segurança, como detecção de fraudes ou alarmes, onde falsos positivos devem ser minimizados.
    - **Regra Geral**: FPR mais baixo é melhor, pois significa menos falsos alarmes.
  
  - **Especificidade (TNR)**: Especificidade (Taxa de Verdadeiros Negativos) é a razão entre verdadeiros negativos e o total de negativos reais (verdadeiros negativos + falsos positivos). Mede quão bem o modelo identifica instâncias negativas.
    - **Caso de Uso**: Usada em testes médicos para identificar corretamente pacientes não doentes.
    - **Regra Geral**: Maior especificidade é melhor quando identificar verdadeiros negativos é importante.
  
  - **Acurácia**: A acurácia é a razão entre previsões corretas (tanto verdadeiros positivos quanto verdadeiros negativos) e o número total de previsões. É usada quando previsões positivas e negativas são igualmente importantes.
    - **Caso de Uso**: Tipicamente usada em tarefas de classificação balanceadas como classificação de imagens.
    - **Regra Geral**: Acurácia mais alta é melhor para correção geral.
  
  - **F1 Score**: O F1 Score é a média harmônica da precisão e recall, usada quando há necessidade de um equilíbrio entre precisão e recall.
    - **Caso de Uso**: Usado em classificação de documentos ou tarefas onde tanto falsos positivos quanto falsos negativos são importantes.
    - **Regra Geral**: F1 score mais alto significa melhor equilíbrio entre precisão e recall.
  
  - **Curva ROC**: A curva ROC (Receiver Operating Characteristic) plota a taxa de verdadeiros positivos (recall) contra a taxa de falsos positivos em vários níveis de limiar. É usada para avaliar a troca entre sensibilidade e especificidade.
    - **Caso de Uso**: Comumente usada em problemas de classificação binária para visualizar o desempenho do modelo em diferentes limiares.
    - **Regra Geral**: Uma área maior sob a curva ROC (AUC) indica melhor desempenho do modelo.
  
- **Problemas de Treinamento do Modelo**:
  - **Overfitting**: Treinamento excessivo nos mesmos dados, fazendo com que o modelo se torne excessivamente específico.
    - Solução: Usar dados mais diversos durante o treinamento.
  - **Underfitting**: O modelo não aprende padrões suficientes dos dados.
    - Solução: Treinar o modelo por mais épocas ou com mais dados.
  - **Viés e Justiça**: Falta de diversidade nos dados de treinamento levando a previsões tendenciosas.
    - Solução: Garantir dados de treinamento diversos e representativos; incluir restrições de justiça.

- **Ajuste Fino** (BedRock e SageMaker):
  - Ajustar os pesos de um modelo pré-treinado com seus dados específicos e _rotulados_ para adaptá-lo a novas tarefas. 
  - Esteja ciente de que, se você fornecer apenas instruções para uma única tarefa, o modelo pode perder sua capacidade de propósito mais geral e experimentar _esquecimento catastrófico_.
  - **Ajuste fino de adaptação de domínio** (SageMaker): Ajusta um modelo de fundação pré-treinado para um domínio específico (ex: jurídico, médico) usando uma pequena quantidade de dados específicos do domínio. Isso ajuda o modelo a ter um desempenho melhor em tarefas relacionadas àquele domínio específico.
  - **Ajuste fino baseado em instruções** (SageMaker): Envolve fornecer exemplos rotulados de tarefas específicas (ex: sumarização, classificação) para melhorar o desempenho de um modelo naquela tarefa específica. Esse tipo de ajuste fino é útil para tornar o modelo melhor em tarefas onde saídas precisas são necessárias.
 
- **Continued-Pretraining** (BedRock):
  - Usando dados _não rotulados_ para expandir o conhecimento geral do modelo sem restringir seu escopo a uma tarefa específica.
 
- **Transfer Learning**:
  - Ajustar um modelo existente que aprendeu características gerais e aplicá-lo a um novo problema, acelerando o treinamento e melhorando a precisão.
     
- **Ferramentas**:
  - **SageMaker Training Jobs**: Gerenciar processos de treinamento, especificar dados de treinamento, hiperparâmetros e recursos computacionais.
  - **SageMaker Experiments**: Rastrear execuções de modelos e ajuste de hiperparâmetros.
  - **Automatic Model Tuning (AMT)**: Ajustar automaticamente hiperparâmetros usando a métrica especificada.

### 7. Implantar o Modelo
- **Descrição**: Implantar o modelo treinado para fazer previsões.
    
- Opções de Implantação do SageMaker:
  - **Inferência em Tempo Real**: Para previsões de baixa latência e tráfego sustentado com capacidades de autoescalonamento.
  - **Transformação em Lote**: Para processamento de grandes lotes de dados de forma assíncrona.
  - **Inferência Assíncrona**: Para solicitações de inferência de longa duração com grandes cargas úteis, tratadas sem respostas imediatas.
  - **Inferência Sem Servidor**: Para tráfego intermitente, onde o modelo escala automaticamente sem gerenciamento de infraestrutura.
- Mecanismos de Implantação do Bedrock:
  - **Inferência Sob Demanda**: Pagamento por uso com base no número de tokens de entrada/saída. Ideal para uso baixo ou esporádico.
  - **Throughput Provisionado**: Necessário para modelos personalizados ou ajustados, fornecendo capacidade garantida para inferência consistente e de alto rendimento.
  - **Agentes do BedRock**: Implantar agentes para fluxos de trabalho de múltiplas etapas, integrando modelos com ferramentas como Amazon Kendra e AWS Lambda para lidar com tarefas complexas.
  
- **Ferramentas**:
  - **AWS API Gateway**: Expor o modelo como um endpoint de API para integração com aplicações.

- **Ferramentas**:
  - **AWS API Gateway (Opcional)**: Usado para expor modelos como APIs RESTful, permitindo integração perfeita com outras aplicações ou microsserviços. É opcional e tipicamente usado quando se deseja que aplicações externas interajam com seu endpoint de modelo.
  - Implantação do SageMaker: Os modelos são implantados via imagens Docker armazenadas no Amazon ECR e implantadas no Lambda (para Inferência Sem Servidor), EC2, EKS (Elastic Kubernetes Service) ou ECS (Elastic Container Service), dependendo dos casos de uso.
  - Tipos de Instância:
    - Inf1: Otimizado para inferência de deep learning de alto desempenho e custo efetivo usando chips AWS Inferentia.
    - P4: Alimentado por GPUs NVIDIA A100, ideal para inferência em larga escala e alto desempenho com baixa latência.
    - G5: Projetado para cargas de trabalho baseadas em GPU, otimizado para gráficos e inferência de machine learning com GPUs NVIDIA.
    - Graviton2 (C6g, M6g): Instâncias baseadas em ARM, energeticamente eficientes, para tarefas gerais de inferência de machine learning.
  - Endpoints do SageMaker: Após a implantação, os modelos são servidos via Endpoints do SageMaker para inferência em tempo real ou trabalhos de transformação em lote.
  - Implantação do Bedrock:
    - AWS Lambda: Frequentemente integrado com o Bedrock para Agentes do Bedrock para permitir automação em fluxos de trabalho de múltiplas etapas.
    - Amazon Kendra: Ao implantar Agentes do Bedrock, o Amazon Kendra é frequentemente usado para busca de documentos e tarefas baseadas em conhecimento.
    - Ferramentas de Throughput Provisionado: Provisionamento de capacidade de inferência para aplicações de alto rendimento via Console de Gerenciamento da AWS ou API do Bedrock.

### 8. Monitorar o Modelo
- **Descrição**: Monitorar continuamente o desempenho do modelo e detectar qualquer desvio de dados ou conceito.
- **Atividades-chave**:
  - Monitorar o modelo em tempo real para desvio de dados e conceito.
  - Definir alertas e automatizar ações corretivas se o desempenho diminuir.

- **Tipos de Desvio**:
  - Desvio de Dados: As entradas mudam, mas a relação entre entradas e saídas permanece a mesma (ex: um novo demográfico).
  - Desvio de Conceito: A relação entre entradas e saídas muda, significando que os padrões aprendidos pelo modelo não se aplicam mais (ex: novos padrões de fraude que o modelo não foi treinado).

- **Ferramentas**:
  - **SageMaker Model Monitor**: Agendar e monitorar desvio de dados, enviar resultados para o CloudWatch e automatizar medidas corretivas.

---

### MLOps e Automação
- **Descrição**: Aplicar princípios de DevOps para gerenciar modelos de machine learning ao longo de seu ciclo de vida, com foco em automação, controle de versão e monitoramento.
- **Atividades-chave**:
  - Automatizar a implantação, monitoramento e re-treinamento de modelos.
  - Garantir integração e entrega contínuas (CI/CD) para atualizações de modelos.
  - Implementar controle de versão para gerenciar várias versões de modelos.
- **Ferramentas**:
  - **SageMaker Pipelines**: Automatizar e gerenciar o fluxo de trabalho de ML de ponta a ponta.
  - **AWS CodePipeline**: Automatizar as fases de construção, teste e implantação para modelos.
  - **SageMaker Model Registry**: Gerenciar e rastrear versões de modelos e metadados.
  - **Amazon S3**: Usado para armazenar artefatos de modelo treinados após o treinamento tanto para SageMaker quanto para Bedrock. As saídas do modelo, incluindo pesos e artefatos, são exportadas para o S3 para fácil acesso durante a implantação e avaliação.

---

### Governança e Explicabilidade de Modelos
- **Descrição**: Garantir transparência, responsabilidade e conformidade regulatória para modelos de ML, ao mesmo tempo em que torna seu comportamento interpretável para as partes interessadas.
- **Atividades-chave**:
  - Implementar estruturas de governança para rastrear o uso e a linhagem do modelo.
  - Usar ferramentas para detectar e mitigar viés, garantir justiça e explicar previsões.
  - Fornecer documentação clara da história e desempenho do modelo para auditorias.
- **Ferramentas**:
  - **SageMaker Clarify**: _Detectar viés_, explicar previsões do modelo e aumentar a transparência.
  - **SageMaker Model Cards**: Documenta os riscos e classificações dos modelos, além de fornecer informações personalizadas, promovendo transparência e responsabilidade no uso de modelos de aprendizado de máquina.
  - **ML Governance from SageMaker**: Fornece ferramentas para controle e visibilidade mais rigorosos sobre modelos de ML, ajudando a rastrear informações do modelo e monitorar comportamentos como viés.
  - **SageMaker ML Lineage Tracking**: Capturar todo o fluxo de trabalho, rastreando a linhagem do modelo para reprodutibilidade e governança.
  - **Glue DataBrew**: Simplificar a governança de dados com preparação visual de dados e regras de qualidade.
  - **AWS Audit Manager**: Automatiza a auditoria de serviços da AWS, garantindo conformidade contínua e prontidão para auditorias em relação a regulamentos do setor.
  - **AWS Artifact**: Fornece acesso sob demanda a relatórios de conformidade e acordos, ajudando organizações a atender aos requisitos de conformidade.
  - **AWS AI Service Cards**: Aumentar a transparência, fornecendo informações sobre casos de uso, limitações, práticas responsáveis de IA e melhores práticas de desempenho para serviços e modelos de IA.
  
---

### Otimização de Custo e Desempenho
- **Descrição**: Otimizar o uso de recursos e o desempenho do modelo sem inflacionar custos.
- **Atividades-chave**:
  - Usar treinamento gerenciado por spot para trabalhos de treinamento de menor custo.
  - Selecionar tipos de instância apropriados para o trabalho e aproveitar as capacidades de autoescalonamento.
  - Usar monitoramento de recursos para detectar ineficiências na utilização de recursos.
- **Ferramentas**:
  - **AWS Trusted Advisor**: Fornece recomendações para melhorias de custo e desempenho.
  - **SageMaker Managed Spot Training**: Reduz os custos de treinamento utilizando capacidade ociosa da AWS EC2.
  - **SageMaker Profiler**: Identifica o uso ineficiente de recursos durante o treinamento do modelo.
  - **Amazon Inspector**: Automação de avaliações de segurança de aplicações de ML, identificando vulnerabilidades que podem levar a degradação de desempenho ou problemas de segurança.

---

### Aprendizado Contínuo e Re-treinamento
- **Descrição**: Re-treinar continuamente os modelos para levar em conta novos dados e condições em mudança, prevenindo degradação de desempenho.
- **Atividades-chave**:
  - Agendar re-treinamento regular do modelo com base em novos dados.
  - Usar ferramentas para detectar quedas de desempenho e iniciar automaticamente fluxos de trabalho de re-treinamento.
  - Lidar com a deriva do modelo monitorando a deriva de conceito e dados.
- **Ferramentas**:
  - **SageMaker Model Monitor**: Detectar desvio de dados e acionar fluxos de trabalho de re-treinamento.
  - **SageMaker Pipelines**: Automatizar processos de re-treinamento de ponta a ponta.

---

### Segurança
- **Descrição**: Implementar as melhores práticas de segurança para proteger modelos de machine learning, dados e infraestrutura relacionada.
  
- **Atividades-chave**:
  - **Princípio do Menor Privilégio**: Garantir que funções e políticas IAM concedam apenas as permissões necessárias para trabalhos ou funções específicas.
  - **PrivateLink e VPC Endpoints**: Restringir o acesso ao **SageMaker** para evitar exposição à internet. Usar **PrivateLink** e **VPC endpoints** para acessar recursos de forma segura dentro da sua rede privada.
  - **Criptografia em Repouso e em Trânsito**: Por padrão, o **SageMaker** criptografa dados em repouso e em trânsito usando o **KMS** (Serviço de Gerenciamento de Chaves).
  - **Funções e Políticas IAM**: Criar e gerenciar funções e políticas IAM para garantir acesso seguro aos dados e recursos do modelo.
  - **S3 Block Public Access**: Evitar a exposição dos dados do modelo garantindo que as configurações de **S3 Block Public Access** substituam qualquer acesso público potencial.
  - **AWS IAM Identity Center**: Centralizar o gerenciamento de identidade, permitindo acesso a várias contas da AWS, e integrar com o Active Directory para gerenciamento de identidade.
  
- **Ferramentas**:
  - **AWS Config**: Monitora e registra continuamente mudanças de configuração em recursos da AWS para garantir conformidade e segurança.
  - **AWS CloudTrail**: Registra chamadas de API e rastreia atividades de usuários para auditoria e conformidade.
  - **Amazon Inspector**: Escaneamentos automáticos de vulnerabilidades em ambientes de machine learning para garantir que os modelos implantados sejam seguros.
  - **AWS Audit Manager**: Auditoria automatizada e garantia de conformidade com regulamentos do setor através da geração de relatórios de auditoria para validação.
  - **AWS Artifact**: Fornece acesso a documentos de conformidade e relatórios de segurança para garantir que seus ambientes de ML atendam aos padrões de segurança e regulatórios.
  - **SageMaker Role Manager**: Simplifica o gerenciamento de permissões e funções para recursos e serviços do SageMaker.

---

## Serviços 

### AWS Managed AI Services

AWS oferece uma gama de serviços gerenciados de IA projetados para serem facilmente integrados a aplicações, fornecendo poderosas capacidades de IA sem a necessidade de profunda experiência em machine learning. Aqui está uma visão geral dos principais serviços:

#### Visão Computacional
- **AWS Rekognition**
  - Análise e comparação facial, detecção de objetos e texto, moderação de conteúdo. Bom para _filtragem de conteúdo_ como identificação de material violento ou inadequado.

#### Análise de Texto e Documentos
- **AWS Textract** (OCR)
  - Converte imagens digitalizadas em texto, permitindo gerenciamento digital de conteúdo.
- **Amazon Comprehend** (NLP)
  - Extrai frases-chave, entidades e sentimentos do texto. Útil para analisar _sentimento de feedback_ e detectar _dados PII_.
- **AWS Intelligent Document Processing** (IDP)
  - Um conjunto de serviços da AWS que automatiza a extração, classificação e processamento de dados de vários tipos de documentos. Aproveita tecnologias de IA como Reconhecimento Óptico de Caracteres (OCR), Processamento de Linguagem Natural (NLP) e Aprendizado de Máquina (ML) para lidar com dados não estruturados encontrados em documentos como PDFs, faturas e contratos legais.

#### IA de Linguagem
- **Amazon Lex**
  - Constrói interfaces de conversação para voz e texto, ideal para criar _chatbots_.
- **Amazon Transcribe**
  - Serviço de fala para texto, perfeito para criar _legendas para áudio_.
- **Amazon Polly**
  - Converte texto em fala realista, aumentando o engajamento do usuário por meio da voz.

#### Experiência do Cliente
- **Amazon Kendra**
  - Fornece capacidades inteligentes de busca em documentos.
- **Amazon Personalize**
  - Oferece recomendações de produtos personalizadas, semelhante a recursos de "você também pode gostar".
- **Amazon Translate**
  - Facilita a tradução de idiomas, apoiando a interação global com usuários.

#### Métricas de Negócios
- **Amazon Forecast**
  - Prevê pontos futuros em dados de séries temporais, como _níveis de estoque_.
- **Amazon Fraud Detection**
  - Detecta fraudes potenciais em vários cenários, incluindo transações online e criações de novas contas.

#### Amazon Q

- **Amazon Q Business**
  - Um assistente alimentado por IA generativa que ajuda em tarefas como responder perguntas, gerar conteúdo e automatizar fluxos de trabalho acessando fontes de dados empresariais como S3, SharePoint e Salesforce.
- **Amazon Q Developer**
  - Uma ferramenta para desenvolvedores que inclui recursos como geração de código e verificação de segurança para ajudar a automatizar tarefas relacionadas ao desenvolvimento e teste.
- **Amazon Q in QuickSight**
  - Integrado ao Amazon QuickSight para consultas em linguagem natural, permitindo que os usuários façam perguntas relacionadas a inteligência de negócios e gerem insights a partir de seus dados do QuickSight com IA.
- **Amazon Q in Connect**
  - Integrado ao Amazon Connect, o Amazon Q ajuda a melhorar o atendimento ao cliente respondendo a perguntas dos clientes, automatizando respostas e gerenciando tickets usando IA de linguagem natural.
- **Amazon Q in AWS Supply Chain**
  - Integrado ao AWS Supply Chain, o Amazon Q ajuda a otimizar e automatizar a gestão da cadeia de suprimentos gerando insights a partir dos dados da cadeia de suprimentos, agilizando a gestão de estoque e prevendo a demanda.

---

### Amazon SageMaker

Amazon SageMaker é um serviço integrado de machine learning que permite que desenvolvedores e cientistas de dados construam, treinem e implantem modelos de machine learning em escala. Os usuários podem criar modelos personalizados do zero ou usar e ajustar modelos existentes por meio do SageMaker JumpStart. Esta plataforma oferece mais controle do que serviços de IA de alto nível como o AWS Rekognition, permitindo uma personalização e otimização detalhadas para atender a requisitos específicos do projeto.

#### SageMaker Studio

SageMaker Studio é um ambiente de desenvolvimento integrado (IDE) para machine learning, fornecendo uma única interface para preparar dados, construir modelos, treinar, ajustar e implantá-los. Oferece recursos como notebooks Jupyter para desenvolvimento de código, ferramentas de depuração integradas e gerenciamento de experimentos, tudo dentro de um ambiente colaborativo baseado em nuvem. O Studio também suporta colaboração em tempo real e fácil acesso a várias capacidades do SageMaker, incluindo monitoramento de modelos e preparação de dados.

####  Processo de Treinamento

O processo típico de treinamento do SageMaker inclui vários elementos-chave que ajudam a configurar e gerenciar os trabalhos de treinamento:

- **Locais dos Dados de Treinamento**: Os dados são tipicamente armazenados no Amazon S3 e acessados via URLs do S3.
- **Instâncias de Computação ML**: O SageMaker aproveita as instâncias EC2 (instâncias ECR) para poder computacional escalável.
- **Imagens de Treinamento**: O processo de treinamento é executado usando imagens de contêiner Docker especificamente projetadas para machine learning.
- **Hiperparâmetros**: Parâmetros que guiam o processo de aprendizado (ex: taxa de aprendizado, tamanho do lote).
- **Bucket de Saída S3**: Os artefatos do modelo treinado são armazenados em um bucket S3 para uso posterior.

#### Recursos
- **SageMaker Feature Store**  
  - Repositório central para armazenar, recuperar e compartilhar recursos de machine learning.
- **SageMaker Model Registry**  
  - Gerencia diferentes versões de modelos e seus metadados.
- **SageMaker Pipelines**  
  - Fornece um serviço de orquestração de fluxo de trabalho para construir, treinar e implantar modelos com fluxos de trabalho repetíveis.
- **SageMaker Model Monitor**  
  - Utiliza regras integradas para detectar desvio de dados ou criar regras personalizadas, os resultados do monitoramento podem ser enviados para o CloudWatch e automatizar medidas corretivas.
- **SageMaker Ground Truth**  
  - Aproveita humanos reais para rotular dados, garantindo conjuntos de dados de treinamento de alta qualidade.
- **SageMaker Canvas**  
  - Uma ferramenta visual e sem código que permite aos usuários construir modelos com base em seus dados com menos conhecimento técnico.
- **SageMaker JumpStart**  
  - Acesso a Modelos Pré-Treinados e um hub para implantar facilmente soluções de machine learning.
- **SageMaker Clarify**  
  - Ferramentas para ajudar a detectar viés e explicar previsões para aumentar a transparência.
- **SageMaker Role Manager**  
  - Gerencia permissões para recursos e serviços do SageMaker.
- **SageMaker Model Cards**  
  - Documenta os riscos e classificações dos modelos, além de fornecer informações personalizadas, promovendo transparência e responsabilidade no uso de modelos de aprendizado de máquina. 
- **SageMaker ML Lineage Tracking**  
  - Rastreia a linhagem dos modelos de ML para estabelecer governança, reproduzir fluxos de trabalho e manter o histórico de trabalho.
- **SageMaker Model Dashboard**  
  - Fornece uma interface unificada para gerenciar e monitorar todas as atividades relacionadas a modelos.
- **SageMaker Data Wrangler**  
  - Simplifica o processo de preparação de dados para machine learning, permitindo limpeza, transformação e visualização de dados de forma rápida e fácil.
- **SageMaker Experiments (Agora chamado MLflow com Amazon SageMaker)**
  - Rastreia, organiza, visualiza, analisa e compara a experimentação iterativa de ML.
- **SageMaker Autopilot**
  - Constrói, treina e ajusta automaticamente modelos de machine learning, enquanto oferece total visibilidade e controle sobre o processo.
- **Amazon Augmented AI (A2I)**
  - Permite adicionar revisão humana para previsões de baixa confiança ou amostras aleatórias, garantindo resultados mais precisos.
- **SageMaker Managed Spot Training**
  - Reduz o custo de treinamento de modelos usando capacidade ociosa da AWS.
- **SageMaker Profiler**
  - Identifica ineficiências de recursos em trabalhos de treinamento para minimizar custos sem sacrificar velocidade ou precisão.

---

### Amazon Bedrock

Amazon Bedrock é um serviço totalmente gerenciado e sem servidor que fornece acesso a modelos de fundação de alto desempenho (FMs) de empresas líderes em IA por meio de uma única API. É projetado para facilitar a criação de aplicações de IA generativa, priorizando segurança, privacidade e IA responsável.

#### Preços
- **Pagamento conforme o uso**: O Amazon Bedrock cobra com base no número de **tokens de entrada e saída** usados durante a inferência. Isso significa que você paga apenas pelos tokens processados ao usar os modelos de fundação.
- **Modelos ajustados**: Se você estiver usando um **modelo personalizado ou ajustado**, cobranças adicionais se aplicam ao **Throughput Provisionado**, que garante desempenho consistente e capacidade reservada para inferência.

#### Recursos
- **Escolha do Modelo**  
  - Acesso a uma variedade de modelos de fundação da AI21 Labs, Anthropic, Cohere, Meta, Mistral AI, Stability AI e Amazon, permitindo a seleção ideal do modelo com base nas necessidades específicas da aplicação.
  - Modelos Amazon Titan
    - Exclusivos do Amazon Bedrock, os modelos Amazon Titan são modelos de fundação pré-treinados e de alto desempenho criados pela AWS, projetados para uma ampla gama de casos de uso com práticas responsáveis de IA.
- **Personalização**  
  - Personalize modelos de fundação de forma privada com seus dados usando técnicas como ajuste fino e Geração Aumentada por Recuperação (RAG), melhorando a relevância e precisão do modelo.
- **Avaliação de Modelos de Fundação**
  - A Avaliação de Modelos no Amazon Bedrock permite avaliar, comparar e selecionar os melhores modelos de fundação para seu caso de uso específico. Você pode avaliar modelos com base em métricas personalizadas, como precisão, robustez e toxicidade, garantindo que atendam aos seus requisitos de desempenho. A integração com o Amazon SageMaker Clarify e o fmeval suporta ainda mais a avaliação do modelo, verificando viés e explicabilidade.
- **Bases de Conhecimento do Bedrock**
  - Usa Geração Aumentada por Recuperação (RAG) para buscar dados de fontes privadas, fornecendo respostas mais relevantes e precisas com suporte total para o fluxo de trabalho RAG — lidando com ingestão de dados, recuperação e aumento de prompt.
  - Melhora as saídas integrando processos de recuperação que puxam conhecimento externo relevante para o modelo generativo.
- **Agentes do Bedrock**  
  - Crie agentes capazes de planejar e executar tarefas de múltiplas etapas usando sistemas e fontes de dados da empresa — agilizando tarefas complexas como consultas de clientes e processamento de pedidos.
- **Serverless**  
  - Elimina a necessidade de gerenciamento de infraestrutura, simplificando a implantação e escalonamento de capacidades de IA.
- **Privacidade e Segurança**  
  - Recursos robustos para restringir saídas de IA, prevenindo a geração de conteúdo inadequado e restringindo conselhos sensíveis como recomendações financeiras, garantindo uso ético e conforme da IA.
- **PartyRock**
  - Um playground prático para construção de aplicativos de IA alimentado pelo Amazon Bedrock, onde os usuários podem rapidamente construir aplicativos de IA generativa e experimentar com modelos sem escrever código.

---

### AWS Glue 

AWS Glue é um serviço ETL (Extração, Transformação, Carga) totalmente gerenciado e otimizado para a nuvem que ajuda a preparar e carregar dados para análises e modelos de IA.

#### Recursos

- **Serviço ETL do AWS Glue**
  - Serviço ETL baseado em nuvem para preparação de dados com transformações integradas como remoção de duplicatas e preenchimento de valores ausentes.
  - Exemplo de Fluxo de Trabalho: AWS Kinesis Data Streams -> Trabalho ETL do AWS Glue -> CSV para Parquet -> Lago de Dados S3.
- **Catálogo de Dados do AWS Glue**
  - Repositório centralizado para gerenciamento e monitoramento de trabalhos ETL, armazenando metadados (esquemas, não dados) com classificadores integrados.
- **AWS Glue Databrew**
  - Ferramenta visual para preparação de dados, definição de regras de qualidade de dados e salvamento de transformações como "receitas".
- **Qualidade de Dados do AWS Glue**
  - Detecta anomalias e recomenda regras de qualidade de dados para garantir dados limpos e de alta qualidade para modelos de IA.
---

## Tabelas

### ML Tradicional vs Deep Learning

| Categoria          | ML Tradicional                                      | Deep Learning                                 |
|-------------------|-----------------------------------------------------|-----------------------------------------------|
| **Complexidade da Tarefa** | Tarefas bem definidas                                  | Tarefas complexas                                 |
| **Tipo de Dado**      | Estruturado / Dados Rotulados                           | Dados Não Estruturados (Imagens, Vídeo, Texto)       |
| **Metodologia**    | Resolve problemas por meio de estatísticas e matemática  | Utiliza redes neurais                      |
| **Tratamento de Atributos** | Seleção e extração de atributos manuais                | Atributos são aprendidos automaticamente pelo modelo |
| **Custo**           | Menos custoso                                         | Custos mais altos devido às demandas computacionais     |


### Tipos de Machine Learning

| Tipo de Aprendizado         | Descrição                                          | Desafios                            | Ferramentas AWS              | Casos de Uso Comuns                   |
|-----------------------|------------------------------------------------------|---------------------------------------|------------------------|------------------------------------|
| **Aprendizado Supervisionado** | Usa dados pré-rotulados para treinar modelos.               | Rotular os dados pode ser desafiador. | SageMaker Ground Truth | Classificação de imagens, detecção de spam |
| **Aprendizado Não Supervisionado** | Trabalha com dados não rotulados para encontrar padrões.         | Requer métodos para interpretar padrões.| Nenhum específico          | Agrupamento, detecção de anomalias, LLMs para fases iniciais de treinamento |
| **Aprendizado por Reforço** | Aprende por tentativa e erro para maximizar recompensas. | Requer ambiente para interação do agente. | AWS DeepRacer      | IA em jogos, robótica, decisões em tempo real |


### Tipos de Modelos de Difusão

| Tipo de Modelo de Difusão | Descrição                                          | Quando Usar                                  | Notas                 |
|----------------------|------------------------------------------------------|----------------------------------------------|--------------------------|
| **Difusão Direta**| Adiciona ruído aos dados progressivamente.                    | Não é frequentemente usado (adiciona ruído)    |   |
| **Difusão Reversa**| Reconstrói dados originais a partir do ruído.               | Criando imagens detalhadas a partir de entradas distorcidas. | Ferramentas de restauração de imagem |
| **Difusão Estável** | Funciona em espaço latente reduzido, não diretamente em pixels. | Melhor que a Difusão Reversa | Midjourney, DALL-E       |


### Métodos de Inferência do Amazon SageMaker

| Tipo de Inferência     | Implantado Em         | Características                                                         |
|--------------------|---------------------|-------------------------------------------------------------------------|
| **Lote**          | EC2                 | Custo-efetivo para trabalhos grandes e infrequentes                               |
| **Assíncrona**   | EC2                 | Adequado para aplicações não sensíveis ao tempo e grandes cargas úteis          |
| **Serverless**     | Lambda              | Tráfego intermitente, períodos sem tráfego, autoescalonamento automático|
| **Tempo Real**      | EC2                 | Previsões ao vivo, tráfego sustentado, baixa latência, desempenho consistente|


### Tipos de Dados de Treinamento para Machine Learning/IA

| Tipo de Dado       | Exemplo de Fonte de Dados AWS                | Exemplo Real                           |
|-----------------|----------------------------------------|------------------------------------------|
| **Estruturado**  | Dados SQL armazenados em RDS e depois movidos para S3| Informações de clientes em tabelas relacionais|
| **Semi-Estruturado** | Dados em DynamoDB ou DocumentDB e depois movidos para S3 | Logs JSON de atividade do usuário           |
| **Não Estruturado**| Objetos e arquivos armazenados diretamente no S3| Imagens, vídeos e documentos PDF        |
| **Séries Temporais** | Dados com carimbo de tempo armazenados no S3         | Dados de dispositivos IoT, dados do mercado de ações       |

### Métricas de desempenho de IA generativa
| Nome da Métrica                                         | Explicação                                                             |
|-----------------------------------------------------|-------------------------------------------------------------------------|
| **Recall Oriented Understudy for Gisting Evaluation (ROUGE)** | Mede a sobreposição entre o texto gerado e o de referência, bom para resumos. |
| **Bilingual Evaluation Understudy (BLEU)**           | Avalia a precisão da tradução comparando n-grams entre saídas e referências. |
| **General Language Understanding Evaluation (GLUE)** | Avalia o desempenho do modelo em várias tarefas de compreensão de linguagem natural. |
| **Holistic Evaluation of Language Models (HELM)**    | Fornece avaliação ampla e específica de tarefas das capacidades do modelo de linguagem.  |
| **Massive Multitask Language Understanding (MMLU)**  | Testa o conhecimento do modelo em uma variedade de domínios e tópicos.            |
| **Beyond the Imitation Game Benchmark (BIG-bench)**  | Avalia modelos em tarefas criativas e difíceis não cobertas por benchmarks padrão. |
| **Perplexidade**                                       | Mede quão bem um modelo prevê a probabilidade do próximo token ou palavra. |

### Modelos de IA Generativa

| Modelo de IA Generativa                            | Exemplos                               | Caso de Uso/Para o que é Bom                              |
|------------------------------------------------|----------------------------------------|----------------------------------------------------------|
| **Redes Adversariais Generativas (GANs)**     | StyleGAN, CycleGAN, ProGAN             | Geração de imagem, síntese de rostos, criação de vídeos          |
| **Autoencoders Variacionais (VAEs)**            | VAE de Kingma & Welling, Beta-VAE         | Remoção de ruído de imagem, detecção de anomalias, compressão de imagem     |
| **Transformers**                               | GPT-4, BERT, T5                        | Geração de texto, tradução de linguagem, geração de conteúdo |
| **Redes Neurais Recorrentes (RNNs)**           | LSTMs, GRUs                            | Dados sequenciais, previsão de séries temporais, modelos de linguagem |
| **Aprendizado por Reforço para Tarefas Generativas** | AlphaGo, DQN, OpenAI Five              | IA em jogos, controle autônomo, otimização de tarefas generativas  |
| **Difusão**                                  | Difusão Estável, DALL·E 2, Imagen     | Geração de imagem e texto para imagem                        |
| **Modelos Baseados em Fluxo**                          | Glow, RealNVP                          | Geração de imagem de alta qualidade, estimativa de densidade         |

### Folhas de Estudo

| **Termo/Conceito**                    | **Descrição**                                                                                                                                                      |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Top-P**                           | Valor de 0 a 1 — probabilidade cumulativa, equilibra aleatoriedade e precisão, 1 é menos aleatório.                                                                          |
| **Temperatura**                     | Controla a aleatoriedade—valores mais altos levam a saídas diversas e criativas; valores mais baixos tornam os resultados mais determinísticos.                                                    |
| **Épocas**                          | Número de iterações no treinamento de um modelo — mais geralmente é melhor, mas muitas podem levar ao overfitting.                                                             |
| **AWS Rekognition**                 | Visão computacional/reconhecimento de imagem, usado para detecção de objetos, análise facial e moderação de conteúdo.                                                               |
| **AWS Textract**                    | Serviço de **OCR** — converte imagens digitalizadas em texto, extração estruturada de dados de documentos.                                                                           |
| **Amazon Comprehend**               | Extrai frases-chave, entidades, sentimento e dados de **PII** do texto.                                                                                                   |
| **AWS Intelligent Document Processing (IDP)** | Automatiza o processamento de documentos não estruturados (ex: PDFs, faturas) usando Textract, Comprehend e A2I.                                                  |
| **Amazon Lex**                      | Serviço para **construir chatbots** com interfaces de conversação natural em texto ou voz.                                                                                  |
| **Amazon Transcribe**               | Serviço de **fala para texto**, incluindo legendagem de áudio.                                                                                                                  |
| **Amazon Polly**                    | Serviço de **texto para fala** para converter texto escrito em palavras faladas.                                                                                                |
| **Amazon Kendra**                   | Motor de busca inteligente para documentos com compreensão semântica.                                                                                                      |
| **Amazon Personalize**              | Serviço para **recomendações de produtos personalizadas**.                                                                                                                    |
| **Amazon Translate**                | Serviço de **tradução de idiomas**.                                                                                                                                       |
| **Amazon Forecast**                 | Fornece **previsões de séries temporais**, ex: previsão de níveis de estoque.                                                                                                |
| **Amazon Fraud Detection**          | Detecta atividades fraudulentas, incluindo transações online e tomadas de conta.                                                                                    |
| **Amazon Q Business**               | Assistente alimentado por IA generativa para processamento de dados empresariais e tarefas.                                                                                            |
| **Amazon Macie**                    | Detecção e anonimização de **PII** para segurança de dados.                                                                                                      |
| **SageMaker Clarify**               | Detecção de **viés** e explicabilidade para modelos de machine learning.                                                                                                       |
| **SageMaker Ground Truth**          | Fornece **rotulagem humana** para conjuntos de dados de **treinamento de modelos**.                                                                                                                 |
| **Amazon Augmented AI (A2I)**       | Revisão humana para previsões de baixa confiança durante a **inferência**.                                                                                                        |
| **AWS Data Exchange**               | Acesso seguro a **conjuntos de dados de terceiros**.                                                                                                                                |
| **Transformações do AWS Glue**        | Transformações ETL como remoção de duplicatas e preenchimento de valores ausentes.                                                                                             |
| **Amazon SageMaker JumpStart**      | Hub com modelos pré-treinados e implantações com um clique.                                                                                                               |
| **Amazon SageMaker Canvas**         | Ferramenta sem código para construção e treinamento de modelos de machine learning.                                                                                                      |
| **Ajuste Fino**                     | **Ajuste de pesos do modelo** usando dados **rotulados** para melhorar o desempenho em tarefas específicas.                                                                                              |
| **Ajuste fino de adaptação de domínio**   | Ajusta um modelo para um **domínio específico** como jurídico ou médico usando pequenos conjuntos de dados.                                                                                      |
| **Ajuste fino baseado em instruções**   | Ajuste fino de um modelo para **melhorar em tarefas específicas**, ex: classificação.                                                                                       |
| **Continued-Pretraining**           | Usando dados **não rotulados** para **expandir a base de conhecimento do modelo**.                                                                                                            |
| **Automatic Model Tuning (AMT)**    | Ajuste automático de hiperparâmetros para melhorar o desempenho do modelo.                                                                                                    |
| **Desvio de Dados**                  | As entradas mudam, mas a relação entre entradas e saídas permanece a mesma (ex: novo demográfico).                                                          |
| **Desvio de Conceito**               | A relação entre entradas e saídas muda, significando que os padrões aprendidos pelo modelo não se aplicam mais (ex: novos padrões de fraude que o modelo não foi treinado).                                |
| **AWS Trusted Advisor**             | Fornece recomendações para melhorias de custo, desempenho e segurança.                                                                                           |
| **Amazon Inspector**                | Avaliações automáticas de segurança para cargas de trabalho de aplicações.                                                                                                            |

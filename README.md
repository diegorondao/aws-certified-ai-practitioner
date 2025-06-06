# AWS Certified AI Practitioner (AIF-C01) - Anotações de Estudo

## Links Úteis
- [Guia Oficial do Exame](https://d1.awsstatic.com/training-and-certification/docs-ai-practitioner/AWS-Certified-AI-Practitioner_Exam-Guide.pdf)
- [Preparação Oficial para o Exame - Amazon Skill Builder](https://explore.skillbuilder.aws/learn/course/internal/view/elearning/19554/exam-prep-standard-course-aws-certified-ai-practitioner-aif-c01) - recomendo assistir em 1.5x
- [Questões Oficiais de Prática](https://explore.skillbuilder.aws/learn/course/internal/view/elearning/19790/exam-prep-official-practice-question-set-aws-certified-ai-practitioner-aif-c01-english) - No nível do exame real.

## Visão Geral

### IA Geral
- **Definição**: Refere-se ao conceito mais amplo de inteligência artificial, com o objetivo de construir sistemas capazes de realizar qualquer tarefa intelectual que um humano possa. É frequentemente usada para descrever objetivos de longo prazo de criar sistemas de IA altamente autônomos e flexíveis.
- **Conceito-chave**: IA com capacidade ampla para executar múltiplas tarefas em diferentes domínios, ao contrário de sistemas de IA especializados.
- **Exemplos**: **Sistemas Especialistas**, **Motores de Regras** (ex: MYCIN), que usam lógica e regras pré-definidas para tomar decisões.

### Aprendizado de Máquina (ML)
- **Definição**: Um subconjunto da IA que permite que sistemas aprendam a partir de dados e façam previsões ou decisões sem programação explícita ou regras fixas.
- **Conceito-chave**: IA que opera por meio de padrões de dados e treinamento, em vez de instruções codificadas explicitamente.
- **Exemplos**: **Regressão Linear**, **Árvores de Decisão**, **Máquinas de Vetores de Suporte** — algoritmos de aprendizado supervisionado usados para tarefas preditivas.

### Aprendizado Profundo (Deep Learning)
- **Definição**: Subconjunto do aprendizado de máquina que utiliza redes neurais com múltiplas camadas (por isso "profundo") para modelar padrões complexos em dados.
- **Conceito-chave**: Eficaz para tarefas como reconhecimento de imagens, processamento de linguagem natural e sistemas autônomos.
- **Exemplos**: **Redes Neurais Convolucionais (CNNs)** para processamento de imagens, **Redes Neurais Recorrentes (RNNs)** para dados sequenciais como séries temporais ou modelos de linguagem.

### IA Generativa
- **Definição**: Subconjunto do aprendizado profundo focado em criar novos conteúdos (como texto, imagens ou música) a partir de dados aprendidos. Modelos generativos geralmente são baseados em **modelos de fundação**, que são grandes modelos pré-treinados adaptáveis a várias tarefas.
- **Conceito-chave**: Sistemas de IA que geram saídas inéditas com base em padrões aprendidos durante o treinamento. Modelos de fundação fornecem versatilidade para ajuste fino em tarefas específicas.
- **Exemplos**: **ChatGPT** para geração de texto, **DALL·E** para geração de imagens, **DeepDream** para geração artística visual.

### Grandes Modelos de Linguagem (LLMs)
- **Definição**: Um tipo de **IA Generativa** focada em compreender e gerar texto semelhante ao humano. LLMs são treinados com grandes volumes de dados textuais para aprender padrões de linguagem, gramática e contexto.
- **Conceito-chave**: LLMs geram textos coerentes e de alta qualidade a partir de prompts e são capazes de realizar tarefas como sumarização, tradução e resposta a perguntas.
- **Exemplos**: **GPT-4**, **BERT**, **T5**, **Claude 2** — usados para geração de texto, análise de sentimento, sumarização e compreensão de linguagem natural.

---

## Conceitos

### Aprendizado em Contexto (In-Context Learning)
- **Definição**: Método de aprimorar modelos generativos adicionando dados e exemplos ao prompt, ajudando o modelo a resolver tarefas de forma mais eficaz.

### Tipos de Prompt
- **Prompt Few-Shot**: Fornece alguns exemplos no prompt para guiar o comportamento do modelo.
- **Prompt Zero-Shot**: Não fornece exemplos, pedindo ao modelo para realizar a tarefa sem orientação.
- **Prompt One-Shot**: Fornece exatamente um exemplo para guiar o modelo.
- **Template de Prompt**: Formato ou estrutura pré-definida para padronizar e melhorar a interação com modelos de IA.
- **Prompt Chain-of-Thought**: O prompt incentiva o modelo a dividir o raciocínio em etapas.
- **Ajuste de Prompt (Prompt Tuning)**: Processo de ajustar prompts para melhorar o desempenho do modelo em tarefas específicas.

### Espaço Latente
- **Definição**: Conhecimento ou padrões codificados capturados por grandes modelos de linguagem (LLMs) que armazenam relações entre dados.
- **Uso**: Representa o entendimento interno de linguagem ou dados que os modelos de IA usam para gerar saídas.

### Embeddings
- **Definição**: Representações numéricas vetorizadas de tokens (palavras, frases, etc.) que capturam seu significado semântico.
- **Uso**: Utilizados em tarefas como busca semântica, onde o significado é importante.
- **Armazenamento**: Podem ser armazenados em bancos de dados vetoriais para busca eficiente.

### Tokens
- **Definição**: Unidades básicas de texto (palavras, subpalavras ou caracteres) processadas por modelos de linguagem. Em LLMs, tokens representam tanto entradas quanto saídas.

### Janela de Contexto (Context-Window)
- **Definição**: Quantidade máxima de tokens que um modelo LLM pode processar de uma vez, incluindo prompt e saída. Se exceder, partes anteriores do texto podem ser truncadas.
- **Uso**: A janela de contexto determina quanto de informação pode ser fornecida ao modelo de uma vez, afetando tarefas como geração de texto longo, análise de documentos ou conversas multi-turno.

### Alucinações
- **Definição**: Ocorrem quando um modelo de linguagem gera informações incorretas ou sem sentido que podem parecer plausíveis, mas não são baseadas em dados reais ou no input fornecido.
- **Mitigações**:
  - Geração Aumentada por Recuperação (RAG): Recupera dados externos relevantes durante a geração, garantindo respostas baseadas em informações corretas.
  - Fine-Tuning: Treinar o modelo com dados mais relevantes e precisos pode reduzir alucinações.
  - Humano no Loop (HITL): Revisão humana em áreas de baixa confiança pode evitar saídas alucinadas em aplicações críticas.

### Modelos Multimodais
- **Definição**: Modelos que trabalham com múltiplos tipos de dados, incorporando texto, imagens ou áudio em um espaço compartilhado. Usados para tarefas como criar legendas para imagens ou gerar visuais a partir de descrições textuais, aproveitando diferentes tipos de entrada para produzir saídas mais ricas e contextuais.

---

### Métodos de Busca
- **Busca por Palavra-chave**: Busca termos exatos na consulta.
- **Busca Semântica**: Usa embeddings para entender o significado da consulta, permitindo resultados mais precisos e relevantes.

---

### Bancos de Dados Vetoriais
- **Definição**: Banco de dados projetado para armazenar e consultar vetores (embeddings), útil para tarefas como busca semântica.

#### Opções de Banco Vetorial na AWS
- **Amazon OpenSearch Service**: Suporta busca k-nearest neighbor (k-NN) para bancos vetoriais. Útil para análise de logs, monitoramento em tempo real e busca.
- **Amazon Aurora PostgreSQL-Compatible Edition & Amazon RDS for PostgreSQL**: Suporta a extensão __pgvector__, permitindo armazenamento eficiente de embeddings e buscas por similaridade.
- **Amazon Neptune ML**: Usa Graph Neural Networks (GNNs) para previsões baseadas em dados de grafos, suportando dados vetorizados em bancos de grafos.
- **Amazon MemoryDB**: Suporta armazenamento e recuperação vetorial de alta velocidade, com tempos de consulta em milissegundos e dezenas de milhares de QPS.
- **Amazon DocumentDB**: Suporta busca vetorial com compatibilidade MongoDB, permitindo armazenamento, indexação e busca de milhões de vetores com resposta em milissegundos.

--- 

## O Pipeline de Machine Learning (ML)

O Pipeline de ML é um processo sistemático para construir, treinar e implantar modelos de machine learning. Garante que cada etapa, desde a definição dos objetivos de negócio até o monitoramento dos modelos implantados, seja gerenciada e otimizada para desempenho. As etapas típicas são:

**Etapas:**
1. Identificar o Objetivo de Negócio
2. Formular o Problema de ML
3. Coletar Dados
4. Pré-processar Dados
5. Engenharia de Features
6. Treinar, Ajustar e Avaliar
7. Implantar
8. Monitorar

---

### 1. Identificar o Objetivo de Negócio
- **Descrição**: Definir critérios de sucesso e alinhar stakeholders para garantir que o projeto de ML atenda aos objetivos do negócio.
- **Atividades-chave**:
  - Estabelecer métricas de sucesso claras.
  - Alinhar com stakeholders da organização.

### 2. Formular o Problema de ML
- **Descrição**: Definir o problema de ML, entradas, saídas e métricas, considerando viabilidade e análise de custo/benefício.
- **Atividades-chave**:
  - Identificar entradas, saídas, requisitos e métricas de desempenho.
  - Realizar análise de custo-benefício para avaliar viabilidade.
  
- **Opções de Modelo**:
  - **Serviço AI/ML Gerenciado** (ex: AWS Comprehend, Forecast, Personalize): Não requer treinamento.
  - **Modelos Pré-treinados** (ex: Amazon Bedrock, SageMaker JumpStart): Ajuste fino com seus dados.
  - **Modelo Totalmente Personalizado**: Construir e treinar do zero.

### 3. Coletar Dados

- **Descrição**: Coletar e preparar os dados necessários para treinar o modelo.

- **Atividades-chave**:
  - Identificar fontes de dados (bancos de dados, data lakes, APIs externas).
  - Ingerir e rotular dados.

- **Onde os Dados São Armazenados**:
  - Dados coletados para ML geralmente são armazenados no **Amazon S3**. Isso vale tanto para dados internos quanto para conjuntos de terceiros acessados via **AWS Data Exchange**.

- **Ferramentas**:
  - **AWS Glue**: Para processos **ETL (Extract, Transform, Load)**, movendo e transformando dados antes do armazenamento no **Amazon S3**.
  - **SageMaker Ground Truth**: Para rotulagem humana de dados ambíguos, com dados rotulados armazenados no **Amazon S3**.
  - **AWS Data Exchange**: Permite acesso seguro a conjuntos de dados de terceiros, armazenando-os no **Amazon S3**.
  - **Amazon S3**: Serviço principal de armazenamento para dados coletados antes do processamento ou treinamento.

### 4. Pré-processar Dados

- **Descrição**: Limpar e preparar os dados, garantindo que estejam adequados para o treinamento.

- **Atividades-chave**:
  - Realizar **Análise Exploratória de Dados (EDA)**.
  - Limpar dados, removendo duplicatas, preenchendo valores ausentes e anonimizar **PII**.
  - Dividir dados em proporções de **treinamento (80%)**, **validação (10%)** e **teste (10%)**.

- **Como Limpar Dados**:
  - **Transformações AWS Glue**: Transformações embutidas para tarefas como remoção de duplicatas ou preenchimento de valores ausentes, além de permitir transformações customizadas em Python ou Spark.
  - **Macie para PII**: AWS Macie detecta e anonimiza dados **PII**, trabalhando com o **Amazon S3** para mascarar informações sensíveis.
  - **AWS Glue DataBrew**: Permite preparação e limpeza visual dos dados, aplicando **regras de qualidade** e salvando transformações como **receitas** reutilizáveis.
  - **SageMaker Canvas**: Facilita importação, transformação e visualização de dados sem necessidade de conhecimento técnico profundo, com transformações visuais rastreáveis no fluxo.

- **Ferramentas**:
  - **AWS Glue**: Serviço ETL com transformações embutidas para limpeza de dados.
  - **AWS Glue DataBrew**: Ferramenta visual para preparação de dados, definindo regras de transformação ("receitas") e verificações de qualidade.
  - **SageMaker Canvas**: Ferramenta visual, sem código, para importar, preparar e transformar dados, com workflow claro.

### 5. Engenharia de Features
- **Descrição**: Selecionar e criar features que melhorem o desempenho do modelo.
- **Atividades-chave**:
  - Seleção de Features: Identificar as mais relevantes com base no conhecimento do domínio, reduzindo dimensionalidade e melhorando eficiência.
  - Criação de Features: Transformar dados brutos em novas features (ex: escalonamento, codificação de variáveis categóricas, derivação de métricas).
  - Transformação de Features: Aplicar transformações matemáticas ou estatísticas (ex: normalização, padronização) para melhorar convergência e desempenho.
- Engenharia Automatizada: Use SageMaker Autopilot para gerar e ranquear features automaticamente.
- Redução de Dimensionalidade: Técnicas como PCA podem ser aplicadas para reduzir o número de features mantendo as mais importantes.
- Escalonamento de Features: Ferramentas como AWS Glue ou SageMaker DataBrew aplicam técnicas de escalonamento, garantindo contribuição igual das features.
- Codificação Categórica: Converter variáveis categóricas em valores numéricos (one-hot, target encoding) usando SageMaker Data Wrangler ou AWS Glue.
  
- **Ferramentas**:
  - **SageMaker Feature Store**: Armazene e gerencie features como fonte única de verdade.

### 6. Treinar, Ajustar e Avaliar o Modelo
- **Descrição**: Treinar o modelo, ajustá-lo e avaliar o desempenho.
- **Atividades-chave**:
  - Treinar o modelo iterativamente e ajustar parâmetros.
  - Ajustar hiperparâmetros (ex: época, batch size, learning rate) e rodar experimentos.
  - Avaliar o modelo usando métricas e comparar desempenho.

- **Parâmetros**:
  - **Parâmetros de Inferência** (Amazon Bedrock):
    - **Aleatoriedade e Diversidade**:
      - Temperatura:
        - Controls randomness—higher values lead to more diverse, creative outputs; lower values produce more predictable, deterministic results.
      - Top K:
        - Limits the model to selecting from the top K most probable tokens; smaller K values result in safer, more predictable choices.
        - Top K is not a terribly useful parameter - use Temperature or Top-P instead. 
      - Top P:
        - Uses cumulative probability to choose tokens, focusing on the smallest set of tokens with a combined probability of P, balancing randomness and diversity.
        - Higher Top P values (closer to 1) reduce randomness by restricting the token pool to only the most probable choices. 
      - Top-K vs Top-P: Top K fixes the number of tokens considered, while Top P uses a variable number of tokens based on their combined probability, making Top P more adaptive and flexible in balancing randomness.
      - Temperature vs. Top P: Temperature adjusts the overall randomness by scaling probabilities, allowing more or less randomness across all possible tokens. Top P narrows the token choices to those that collectively add up to a certain probability threshold, balancing randomness with accuracy.
      - Use Cases:
        - Use Top-P when you want adaptive diversity but want to stay closer to more likely outcomes.
        - Use Temperature when you need consistent randomness control across the board.  
    - Response length:
      - Specifies the maximum length of generated output, affecting how verbose or concise the response is.
    - Penalties:
      - Applies penalties to repeated tokens or sequences to encourage variety in the generated text.
    - Stop sequences:
      - Defines specific sequences where the model will stop generating text, ensuring controlled output length or format.
  - **Parâmetros de Treinamento** (Hiperparâmetros):
    - **Época**: O número de iterações através de todo o conjunto de dados.
      - Increasing epochs generally improves the model's learning but can lead to overfitting if too high. More epochs help the model learn better but might also result in diminishing returns after a certain point.
    - **Batch Size**: Número de amostras antes de atualizar os parâmetros do modelo.
      - Smaller batch sizes provide more frequent updates, which can help in converging quickly but can introduce more noise. Larger batch sizes are more stable but may require more computation and memory.
    - **Learning Rate**: Controls how fast the model learns.
      - A high learning rate speeds up training but may skip optimal solutions, while a low learning rate leads to slower but more precise convergence, though it risks getting stuck in local minima.
        
- **Métricas de Erro**:

  - **MSE (Erro Quadrático Médio)**: Calcula a média dos quadrados das diferenças entre valores previstos e reais, dando mais peso a erros maiores. Quanto menor, melhor.
    - **Uso**: Problemas de regressão como previsão de preços de casas.
    - **Regra**: Quanto menor, melhor.
    
  - **RMSE (Raiz do Erro Quadrático Médio)**: Raiz quadrada do MSE, fornece erro na mesma unidade dos valores previstos, facilitando interpretação.
    - **Uso**: Usado junto com MSE em regressão.
    - **Regra**: Quanto menor, melhor.
  
  - **Perplexidade**: Mede quão bem um modelo prevê uma sequência de tokens. Quanto menor, melhor.
    - **Uso**: Avaliação de modelos de linguagem.
    - **Regra**: Quanto menor, melhor.
  
  - **Precisão**: Razão entre verdadeiros positivos e o total de positivos previstos. Importante quando minimizar falsos positivos é crucial.
    - **Uso**: Classificação de spam.
    - **Regra**: Quanto maior, melhor.
  
  - **Recall (TPR)**: Razão entre verdadeiros positivos e o total de positivos reais. Importante quando minimizar falsos negativos é crucial.
    - **Uso**: Testes médicos.
    - **Regra**: Quanto maior, melhor.
  
  - **Taxa de Falsos Positivos (FPR)**: Razão entre falsos positivos e o total de negativos. Mede frequência de alarmes falsos.
    - **Uso**: Segurança, detecção de fraudes.
    - **Regra**: Quanto menor, melhor.
  
  - **Especificidade (TNR)**: Razão entre verdadeiros negativos e o total de negativos reais. Mede identificação correta de negativos.
    - **Uso**: Testes médicos para identificar não-doentes.
    - **Regra**: Quanto maior, melhor.
  
  - **Acurácia**: Razão entre previsões corretas e o total de previsões. Usada quando positivos e negativos são igualmente importantes.
    - **Uso**: Classificação de imagens.
    - **Regra**: Quanto maior, melhor.
  
  - **F1 Score**: A pontuação F1 é a média harmônica entre precisão e recall, usada quando é preciso equilibrar ambos.
    - **Uso**: Classificação de documentos.
    - **Regra**: Quanto maior, melhor.
  
  
- **Problemas de Treinamento**:
  - **Overfitting**: Treinamento excessivo, tornando o modelo muito específico.
    - Solução: Usar dados mais diversos durante o treinamento.
  - **Underfitting**: O modelo não aprende padrões suficientes dos dados.
    - Solução: Treinar o modelo por mais épocas ou com mais dados.
  - **Viés e Justiça**: Falta de diversidade nos dados de treinamento levando a previsões tendenciosas.
    - Solução: Garantir dados de treinamento diversos e representativos; incluir restrições de justiça.

- **Fine-Tuning** (BedRock e SageMaker):
  - Ajusta os pesos de um modelo pré-treinado com seus dados _rotulados_ para adaptá-lo a novas tarefas. 
  - Be aware that if you only provide instructions for a single task, the model may lose its more general purpose capability and experience _catastrophic forgetting_.
  - **Fine-tuning baseado em domínio** (SageMaker): Tailora um modelo de fundação pré-treinado para um domínio específico (ex: legal, médico) usando uma pequena quantidade de dados específicos do domínio. Isso ajuda o modelo a ter um desempenho melhor em tarefas relacionadas àquele domínio específico.
  - **Fine-tuning baseado em instrução** (SageMaker): Envolve fornecer exemplos rotulados de tarefas específicas (ex: sumarização, classificação) para melhorar o desempenho de um modelo naquela tarefa específica. Esse tipo de ajuste fino é útil para tornar o modelo melhor em tarefas onde saídas precisas são necessárias.
 
- **Continued-Pretraining** (BedRock):
  - Using _unlabeled_ data to expand the model's overall knowledge without narrowing its scope to a specific task.
 
- **Transfer Learning**:
  - Fine-tuning an existing model that has learned general features and applying it to a new problem, speeding up training and improving accuracy.
     
- **Ferramentas**:
  - **SageMaker Training Jobs**: Gerencia processos de treinamento, especificando dados, hiperparâmetros e recursos computacionais.
  - **SageMaker Experiments**: Rastreia execuções de modelos e ajuste de hiperparâmetros.
  - **Automatic Model Tuning (AMT)**: Ajusta hiperparâmetros automaticamente usando a métrica especificada.

### 7. Implantar o Modelo
- **Descrição**: Implantar o modelo treinado para fazer previsões.
    
- Opções de Implantação SageMaker:
  - **Inferência em Tempo Real**: Para previsões de baixa latência e tráfego sustentado, com autoescalonamento.
  - **Batch Transform**: Para processamento de grandes lotes de dados de forma assíncrona.
  - **Inferência Assíncrona**: Para solicitações de inferência de longa duração com grandes payloads.
  - **Inferência Serverless**: Para tráfego intermitente, onde o modelo escala automaticamente.
- Mecanismos de Implantação Bedrock:
  - **Inferência Sob Demanda**: Pagamento por uso, ideal para uso esporádico.
  - **Throughput Provisionado**: Necessário para modelos customizados, garantindo capacidade consistente.
  - **Agentes BedRock**: Implantação de agentes para fluxos de trabalho multi-etapas, integrando modelos com Amazon Kendra e AWS Lambda.
  
- **Ferramentas**:
  - **AWS API Gateway**: Expõe o modelo como endpoint de API para integração com aplicações.

- **Ferramentas**:
  - **AWS API Gateway (Opcional)**: Usado para expor modelos como APIs REST, permitindo integração com outros sistemas ou microsserviços. É opcional e tipicamente usado quando se deseja que aplicações externas interajam com o endpoint do modelo.
  - SageMaker Deployment: Modelos são implantados via imagens Docker armazenadas no Amazon ECR e implantadas no Lambda (para Inferência Serverless), EC2, EKS (Elastic Kubernetes Service) ou ECS (Elastic Container Service), dependendo dos casos de uso.
  - Tipos de Instância:
    - Inf1: Otimizado para inferência de deep learning de alto desempenho e custo-efetivo usando chips AWS Inferentia.
    - P4: Alimentado por GPUs NVIDIA A100, ideal para inferência em larga escala e alto desempenho com baixa latência.
    - G5: Projetado para cargas de trabalho baseadas em GPU, otimizado para gráficos e inferência de machine learning com GPUs NVIDIA.
    - Graviton2 (C6g, M6g): Instâncias baseadas em ARM, eficientes em energia, para tarefas gerais de inferência de machine learning.
  - Endpoints SageMaker: Após a implantação, os modelos são servidos via Endpoints SageMaker para inferência em tempo real ou jobs de transformação em lote.
  - Implantação Bedrock:
    - AWS Lambda: Frequentemente integrado com Bedrock para Agentes Bedrock, permitindo automação em fluxos de trabalho multi-etapas.
    - Amazon Kendra: Ao implantar Agentes Bedrock, o Amazon Kendra é frequentemente usado para busca de documentos e tarefas baseadas em conhecimento.
    - Ferramentas de Throughput Provisionado: Provisionamento de capacidade de inferência para aplicações de alto throughput via Console de Gerenciamento da AWS ou API do Bedrock.

### 8. Monitorar o Modelo
- **Descrição**: Monitorar continuamente o desempenho do modelo e detectar drift de dados ou conceito.
- **Atividades-chave**:
  - Monitorar em tempo real para drift de dados e conceito.
  - Configurar alertas e automatizar ações corretivas se o desempenho degradar.

- **Tipos de Drift**:
  - Drift de Dados: Mudança nos dados de entrada, mas relação entre entrada e saída permanece a mesma (ex: um novo demográfico).
  - Drift de Conceito: A relação entre entrada e saída muda, significando que os padrões aprendidos pelo modelo não se aplicam mais (ex: novos padrões de fraude que o modelo não foi treinado).

- **Ferramentas**:
  - **SageMaker Model Monitor**: Agenda e monitora drift de dados, envia resultados ao CloudWatch e automatiza correções.

---

### MLOps e Automação
- **Descrição**: Aplicar princípios DevOps para gerenciar modelos de ML durante todo o ciclo de vida, focando em automação, versionamento e monitoramento.
- **Atividades-chave**:
  - Automatizar implantação, monitoramento e re-treinamento.
  - Garantir integração e entrega contínuas (CI/CD) para atualizações de modelos.
  - Implementar versionamento para gerenciar múltiplas versões de modelos.
- **Ferramentas**:
  - **SageMaker Pipelines**: Automatiza e gerencia o workflow de ML de ponta a ponta.
  - **AWS CodePipeline**: Automate the build, test, and deploy phases for models.
  - **SageMaker Model Registry**: Manage and track model versions and metadata.
  - **Amazon S3**: Used to store trained model artifacts after training for both SageMaker and Bedrock. Model outputs, including weights and artifacts, are exported to S3 for easy access during deployment and evaluation.

---

### Governança e Explicabilidade de Modelos
- **Descrição**: Garantir transparência, responsabilidade e conformidade regulatória, tornando o comportamento dos modelos interpretável para as partes interessadas.
- **Atividades-chave**:
  - Implementar frameworks de governança para rastrear uso e linhagem dos modelos.
  - Usar ferramentas para detectar e mitigar viés, garantir justiça e explicar previsões.
  - Fornecer documentação clara do histórico e desempenho do modelo para auditorias.
- **Ferramentas**:
  - **SageMaker Clarify**: _Detecta viés_, explica previsões e aumenta transparência.
  - **SageMaker Model Cards**: Cria documentação para modelos treinados, incluindo métricas de desempenho e uso pretendido.
  - **ML Governance from SageMaker**: Provides tools for tighter control and visibility over ML models, helping track model information and monitor behavior like bias.
  - **SageMaker ML Lineage Tracking**: Capture the entire workflow, tracking model lineage for reproducibility and governance.
  - **Glue DataBrew**: Simplify data governance with visual data preparation and quality rules.
  - **AWS Audit Manager**: Automates the auditing of AWS services, ensuring continuous compliance and audit readiness for industry regulations.
  - **AWS Artifact**: Provides on-demand access to compliance reports and agreements, helping organizations meet compliance requirements.
  - **AWS AI Service Cards**: Enhance transparency by providing information on use cases, limitations, responsible AI practices, and performance best practices for AI services and models.
  
---

### Otimização de Custo e Desempenho
- **Descrição**: Otimizar uso de recursos e desempenho sem aumentar custos.
- **Atividades-chave**:
  - Usar treinamento gerenciado com spot para reduzir custos.
  - Selecionar tipos de instância apropriados e aproveitar capacidades de autoescalonamento.
  - Usar monitoramento de recursos para detectar ineficiências.
- **Ferramentas**:
  - **AWS Trusted Advisor**: Recomendações para custo e desempenho.
  - **SageMaker Managed Spot Training**: Reduz custo de treinamento usando capacidade EC2 ociosa.
  - **SageMaker Profiler**: Identifica ineficiências de recursos durante o treinamento.
  - **Amazon Inspector**: Automates security assessments of ML applications, identifying vulnerabilities that can lead to performance degradation or security issues.

---

### Aprendizado Contínuo e Re-treinamento
- **Descrição**: Re-treinar modelos continuamente para novos dados e condições, evitando degradação de desempenho.
- **Atividades-chave**:
  - Agendar re-treinamento regular com novos dados.
  - Usar ferramentas para detectar quedas de desempenho e iniciar automaticamente fluxos de trabalho de re-treinamento.
  - Lidar com drift monitorando conceito e dados.
- **Ferramentas**:
  - **SageMaker Model Monitor**: Detecta drift e aciona re-treinamento.
  - **SageMaker Pipelines**: Automatiza processos de re-treinamento.

---

### Segurança
- **Descrição**: Implementar melhores práticas para proteger modelos, dados e infraestrutura de ML.
  
- **Atividades-chave**:
  - **Princípio do Menor Privilégio**: IAM concede apenas permissões necessárias.
  - **AWS IAM Identity Center**: Centraliza gestão de identidade e integra com Active Directory.
  
- **Ferramentas**:
  - **AWS Config**: Monitora e registra mudanças de configuração para conformidade.
  - **AWS CloudTrail**: Registra chamadas de API e rastreia atividade do usuário para auditoria e conformidade.
  - **Amazon Inspector**: Escaneia automaticamente vulnerabilidades em ambientes de machine learning.
  - **AWS Audit Manager**: Automatiza auditorias e garante conformidade com regulamentos da indústria.
  - **AWS Artifact**: Fornece acesso a documentos de conformidade e relatórios de segurança.
  - **SageMaker Role Manager**: Simplifica a gestão de permissões e papéis para recursos SageMaker.

---

## Serviços 

### Serviços de IA Gerenciados AWS

A AWS oferece uma variedade de serviços de IA gerenciados, facilmente integráveis em aplicações, fornecendo capacidades avançadas sem necessidade de expertise profunda em ML. Veja os principais:

#### Visão Computacional
- **AWS Rekognition**
  - Comparação e análise facial, detecção de objetos e texto, moderação de conteúdo. Bom para _triagem de conteúdo_ como identificação de material violento ou impróprio.

#### Análise de Texto e Documentos
- **AWS Textract** (OCR)
  - Converte imagens digitalizadas em texto, facilitando a gestão de conteúdo digital.
- **Amazon Comprehend** (NLP)
  - Extrai frases-chave, entidades e sentimento de textos. Útil para analisar _sentimento de feedback_ e detectar _PII_.
- **AWS Intelligent Document Processing** (IDP)
  - Conjunto de serviços AWS que automatizam extração, classificação e processamento de dados de documentos variados, usando OCR, NLP e ML.

#### IA de Linguagem
- **Amazon Lex**
  - Cria interfaces conversacionais para voz e texto, ideal para _chatbots_.
- **Amazon Transcribe**
  - Serviço de transcrição de fala para texto, ideal para _legendas de áudio_.
- **Amazon Polly**
  - Converte texto em fala realista, melhorando engajamento por voz.

#### Experiência do Cliente
- **Amazon Kendra**
  - Busca inteligente de documentos.
- **Amazon Personalize**
  - Recomendações personalizadas de produtos.
- **Amazon Translate**
  - Tradução automática de idiomas.

#### Métricas de Negócio
- **Amazon Forecast**
  - Previsão de séries temporais, como _níveis de estoque_.
- **Amazon Fraud Detection**
  - Detecta fraudes em transações online e criação de contas.

#### Amazon Q

- **Amazon Q Business**
  - Assistente de IA generativa para tarefas como responder perguntas, gerar conteúdo e automatizar fluxos de trabalho acessando dados empresariais.
- **Amazon Q Developer**
  - Ferramenta para desenvolvedores com geração de código e análise de segurança.
- **Amazon Q in QuickSight**
  - Consultas em linguagem natural para BI no QuickSight.
- **Amazon Q in Connect**
  - Melhora atendimento ao cliente no Amazon Connect com IA conversacional.
- **Amazon Q in AWS Supply Chain**
  - Otimiza e automatiza gestão de cadeia de suprimentos com insights de IA.

---

### Amazon SageMaker

Amazon SageMaker é um serviço integrado de ML que permite criar, treinar e implantar modelos em escala. Usuários podem criar modelos do zero ou usar/ajustar modelos existentes via JumpStart. Oferece mais controle que serviços de IA de alto nível como o Rekognition.

#### SageMaker Studio

IDE para ML, com interface única para preparar dados, construir, treinar, ajustar e implantar modelos. Suporta colaboração em tempo real, notebooks Jupyter, ferramentas de depuração e gerenciamento de experimentos.

#### Processo de Treinamento

Inclui:
- **Local dos Dados de Treinamento**: Normalmente no Amazon S3.
- **Instâncias de Computação ML**: Usa instâncias EC2 para escalabilidade.
- **Imagens de Treinamento**: Usa imagens Docker específicas para ML.
- **Hiperparâmetros**: Parâmetros que guiam o aprendizado (ex: learning rate, batch size).
- **Bucket de Saída S3**: Artefatos do modelo treinado são armazenados no S3.

#### Funcionalidades
- **SageMaker Feature Store**  
  - Repositório central de features.
- **SageMaker Model Registry**  
  - Gerencia versões e metadados de modelos.
- **SageMaker Pipelines**  
  - Orquestração de workflows de ML.
- **SageMaker Model Monitor**  
  - Detecta drift de dados, envia resultados ao CloudWatch e automatiza correções.
- **SageMaker Ground Truth**  
  - Rotulagem humana de dados.
- **SageMaker Canvas**  
  - Ferramenta visual, sem código, para construção de modelos.
- **SageMaker JumpStart**  
  - Modelos pré-treinados e implantação fácil.
- **SageMaker Clarify**  
  - Detecção de viés e explicabilidade.
- **SageMaker Role Manager**  
  - Gerencia permissões.
- **SageMaker Model Cards**  
  - Documentação transparente de modelos.
- **SageMaker ML Lineage Tracking**  
  - Rastreia linhagem dos modelos.
- **SageMaker Model Dashboard**  
  - Interface unificada para monitoramento.
- **SageMaker Data Wrangler**  
  - Prepara, limpa e visualiza dados rapidamente.
- **SageMaker Experiments (agora MLflow com SageMaker)**
  - Organiza e compara experimentos de ML.
- **SageMaker Autopilot**
  - Automatiza construção, treinamento e ajuste de modelos.
- **Amazon Augmented AI (A2I)**
  - Revisão humana para previsões de baixa confiança.
- **SageMaker Managed Spot Training**
  - Reduz custo usando capacidade EC2 ociosa.
- **SageMaker Profiler**
  - Identifica ineficiências de recursos em treinamentos.

---

### Amazon Bedrock

Serviço totalmente gerenciado e serverless que fornece acesso a modelos de fundação de IA de empresas líderes via API única. Foco em segurança, privacidade e IA responsável.

#### Preços
- **Pay-as-you-go**: Cobrança por **tokens de entrada e saída** usados na inferência.
- **Modelos Fine-tuned**: Cobrança adicional por **Provisioned Throughput** para modelos customizados.

#### Funcionalidades
- **Escolha de Modelos**  
  - Acesso a modelos de AI21 Labs, Anthropic, Cohere, Meta, Mistral AI, Stability AI e Amazon.
- **Customização**  
  - Personalize modelos com seus dados via fine-tuning e RAG.
- **Avaliação de Modelos**
  - Avalie e compare modelos com métricas customizadas, integração com SageMaker Clarify e fmeval.
- **Knowledge Bases**
  - Usa RAG para buscar dados privados, entregando respostas mais relevantes.
- **Bedrock Agents**  
  - Crie agentes para tarefas multi-etapas integrando sistemas e dados.
- **Serverless**  
  - Sem necessidade de gerenciar infraestrutura.
- **Guardrails de Segurança e Privacidade**  
  - Restringe saídas inadequadas e conselhos sensíveis.
- **PartyRock**
  - Playground para construir apps de IA generativa sem código.

---

### AWS Glue

Serviço ETL totalmente gerenciado e otimizado para nuvem, preparando e carregando dados para analytics e IA.

#### Funcionalidades

- **AWS Glue ETL Service**
  - ETL na nuvem com transformações embutidas (remover duplicatas, preencher valores ausentes).
  - Exemplo: Kinesis Data Streams -> Glue ETL -> CSV para Parquet -> S3 Data Lake.
- **AWS Glue Data Catalog**
  - Repositório central de metadados (esquemas, não dados).
- **AWS Glue Databrew**
  - Ferramenta visual para preparação de dados, definindo regras de qualidade e salvando "receitas".
- **AWS Glue Data Quality**
  - Detecta anomalias e recomenda regras de qualidade.
---

## Tabelas

### ML Tradicional vs Deep Learning

| Categoria          | ML Tradicional                                   | Deep Learning                                 |
|-------------------|--------------------------------------------------|-----------------------------------------------|
| **Complexidade**  | Tarefas bem definidas                            | Tarefas complexas                             |
| **Tipo de Dados** | Estruturados / Rotulados                         | Não estruturados (imagens, vídeo, texto)      |
| **Metodologia**   | Estatística e matemática                         | Redes neurais                                 |
| **Features**      | Seleção manual                                   | Aprendidas automaticamente pelo modelo        |
| **Custo**         | Menor                                            | Maior devido à demanda computacional          |


### Tipos de Aprendizado de Máquina

| Tipo de Aprendizado         | Descrição                                         | Desafios                            | Ferramentas AWS         | Casos de Uso Comuns                   |
|----------------------------|---------------------------------------------------|-------------------------------------|-------------------------|---------------------------------------|
| **Supervisionado**         | Usa dados pré-rotulados para treinar modelos.     | Rotulagem pode ser desafiadora.     | SageMaker Ground Truth  | Classificação de imagens, spam        |
| **Não Supervisionado**     | Trabalha com dados não rotulados para achar padrões.| Interpretação dos padrões.         | Nenhuma específica      | Clustering, detecção de anomalias, LLM|
| **Reforço**                | Aprende por tentativa e erro para maximizar recompensas.| Requer ambiente de interação. | AWS DeepRacer           | Jogos, robótica, decisões em tempo real|


### Tipos de Modelos de Difusão

| Tipo de Difusão    | Descrição                                         | Quando Usar                                  | Observações                 |
|--------------------|---------------------------------------------------|----------------------------------------------|-----------------------------|
| **Forward**        | Adiciona ruído progressivamente.                  | Raramente usado (adiciona ruído)             |                             |
| **Reverse**        | Reconstrói dados originais a partir do ruído.     | Restauração de imagens distorcidas           | Ferramentas de restauração  |
| **Stable Diffusion**| Trabalha em espaço latente reduzido.              | Melhor que Reverse Diffusion                  | Midjourney, DALL-E          |


### Métodos de Inferência SageMaker

| Tipo de Inferência | Implantado em         | Características                                                         |
|--------------------|----------------------|------------------------------------------------------------------------|
| **Batch**          | EC2                  | Econômico para grandes jobs esporádicos                                 |
| **Assíncrono**     | EC2                  | Para aplicações não sensíveis ao tempo e payloads grandes               |
| **Serverless**     | Lambda               | Tráfego intermitente, autoescalonamento                                |
| **Tempo Real**     | EC2                  | Previsões ao vivo, baixa latência, desempenho consistente               |


### Tipos de Dados para ML/IA

| Tipo de Dado      | Exemplo AWS           | Exemplo Real                              |
|-------------------|----------------------|-------------------------------------------|
| **Estruturado**   | SQL no RDS, depois S3| Info de clientes em tabelas relacionais   |
| **Semiestruturado**| DynamoDB/DocumentDB, depois S3| Logs JSON de atividade de usuário   |
| **Não estruturado**| S3                   | Imagens, vídeos, PDFs                     |
| **Séries Temporais**| S3                  | Dados de IoT, mercado de ações            |

### Métricas de desempenho em IA Generativa
| Nome da Métrica                                    | Explicação                                                             |
|----------------------------------------------------|------------------------------------------------------------------------|
| **ROUGE**                                         | Mede sobreposição entre texto gerado e referência, bom para resumos.   |
| **BLEU**                                          | Avalia tradução comparando n-gramas entre saída e referência.          |
| **GLUE**                                          | Avalia desempenho em múltiplas tarefas de compreensão de linguagem.     |
| **HELM**                                          | Avaliação ampla e específica de tarefas para modelos de linguagem.      |
| **MMLU**                                          | Testa conhecimento do modelo em vários domínios.                        |
| **BIG-bench**                                     | Avalia modelos em tarefas criativas e difíceis.                         |
| **Perplexidade**                                  | Mede quão bem o modelo prevê o próximo token ou palavra.                |

### Modelos de IA Generativa

| Modelo                                   | Exemplos                               | Casos de Uso                                    |
|-------------------------------------------|----------------------------------------|-------------------------------------------------|
| **GANs**                                 | StyleGAN, CycleGAN, ProGAN             | Geração de imagens, faces, vídeos               |
| **VAEs**                                 | Kingma & Welling VAE, Beta-VAE         | Denoising, detecção de anomalias, compressão    |
| **Transformers**                         | GPT-4, BERT, T5                        | Geração de texto, tradução, conteúdo            |
| **RNNs**                                 | LSTMs, GRUs                            | Dados sequenciais, séries temporais, linguagem   |
| **Reforço para Geração**                  | AlphaGo, DQN, OpenAI Five              | IA para jogos, controle autônomo, otimização    |
| **Difusão**                              | Stable Diffusion, DALL·E 2, Imagen     | Geração de imagens e texto-para-imagem          |
| **Flow-Based**                           | Glow, RealNVP                          | Geração de imagens de alta qualidade            |

### Resumo de Conceitos

| **Termo/Conceito**                    | **Descrição**                                                                                 |
|---------------------------------------|---------------------------------------------------------------------------------------------|
| **Top-P**                             | Valor de 0 a 1 — probabilidade cumulativa, equilibra aleatoriedade e precisão, 1 é menos aleatório. |
| **Temperatura**                       | Controla aleatoriedade — valores altos geram saídas criativas, baixos tornam determinístico. |
| **Épocas**                            | Número de iterações no treinamento — mais é melhor, mas excesso causa overfitting.           |
| **AWS Rekognition**                   | Visão computacional, detecção de objetos, faces e moderação de conteúdo.                     |
| **AWS Textract**                      | **OCR** — converte imagens digitalizadas em texto, extração estruturada de documentos.       |
| **Amazon Comprehend**                 | Extrai frases-chave, entidades, sentimento e PII de textos.                                  |
| **AWS Intelligent Document Processing (IDP)** | Automatiza processamento de documentos não estruturados usando Textract, Comprehend e A2I. |
| **Amazon Lex**                        | **Chatbots** com interfaces de texto ou voz.                                                 |
| **Amazon Transcribe**                 | **Fala para texto**, incluindo legendas de áudio.                                            |
| **Amazon Polly**                      | **Texto para fala** realista.                                                                |
| **Amazon Kendra**                     | Busca inteligente de documentos com compreensão semântica.                                   |
| **Amazon Personalize**                | **Recomendações personalizadas** de produtos.                                                |
| **Amazon Translate**                  | **Tradução automática** de idiomas.                                                          |
| **Amazon Forecast**                   | **Previsão de séries temporais**, ex: estoque.                                               |
| **Amazon Fraud Detection**            | Detecta fraudes em transações e contas.                                                      |
| **Amazon Q Business**                 | Assistente de IA generativa para dados empresariais.                                         |
| **Amazon Macie**                      | Detecção e anonimização de **PII** para segurança de dados.                                  |
| **SageMaker Clarify**                 | **Detecção de viés** e explicabilidade em modelos de ML.                                     |
| **SageMaker Ground Truth**            | **Rotulagem humana** para conjuntos de treinamento.                                          |
| **Amazon Augmented AI (A2I)**         | **Revisão humana** para previsões de baixa confiança durante **inferência**.                  |
| **AWS Data Exchange**                 | Acesso seguro a **dados de terceiros**.                                                      |
| **AWS Glue Transformations**          | ETL: remover duplicatas, preencher valores ausentes.                                         |
| **Amazon SageMaker JumpStart**        | Modelos pré-treinados e implantação fácil.                                                   |
| **Amazon SageMaker Canvas**           | Ferramenta sem código para construir e treinar modelos.                                      |
| **Fine-Tuning**                       | **Ajuste de pesos** com **dados rotulados** para melhorar desempenho.                        |
| **Fine-tuning por domínio**           | Adaptar modelo para **domínio específico** com poucos dados.                                 |
| **Fine-tuning baseado em instrução**  | Melhorar desempenho em tarefas específicas, ex: classificação.                               |
| **Continued-Pretraining**             | Usar **dados não rotulados** para expandir conhecimento do modelo.                            |
| **Automatic Model Tuning (AMT)**      | Ajuste automático de hiperparâmetros.                                                        |
| **Data-Drift**                        | Mudança nos dados de entrada, relação entrada-saída igual.                                   |
| **Concept-Drift**                     | Relação entre entrada e saída muda, padrões aprendidos não se aplicam.                       |
| **AWS Trusted Advisor**               | Recomendações para custo, desempenho e segurança.                                            |
| **Amazon Inspector**                  | Avaliações automáticas de segurança.                                                         |
| **AWS PrivateLink**                   | Conexões privadas seguras entre VPCs e serviços AWS.                                         |
| **AWS Config**                        | Monitora e registra mudanças de configuração.                                                |
| **AWS CloudTrail**                    | Logs de chamadas de API AWS para auditoria.                                                  |
| **BedRock GuardRails**                | Restringe saídas inadequadas de modelos de fundação.                                         |
| **Postgres (Aurora ou RDS)**          | Banco SQL com suporte vetorial para busca por similaridade.                                  |
| **Amazon DocumentDB**                 | Armazenamento JSON, compatível com MongoDB e busca vetorial.                                 |
| **Amazon Neptune**                    | Banco de grafos com busca vetorial.                                                          |
| **Amazon Neptune ML**                 | GNNs para prever resultados em dados de grafos.                                              |
| **Amazon MemoryDB**                   | Banco em memória com busca vetorial rápida.                                                  |
| **Amazon OpenSearch Service**         | Serviço de busca com suporte vetorial.                                                       |
| **MSE (Erro Quadrático Médio)**       | Diferença quadrática média entre previsto e real, menor é melhor.                            |
| **RMSE (Raiz do Erro Quadrático Médio)**| Raiz do MSE, mais interpretable; menor RMSE é melhor.                                        |
| **Perplexidade**                      | Mede quão bem o modelo prevê a próxima palavra ou token.                                      |

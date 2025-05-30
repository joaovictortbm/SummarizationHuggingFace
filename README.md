# Summarization Hugging Face
Este projeto consiste no fine-tuning de modelos Transformer para a tarefa de **resumo automático de diálogos** utilizando o **SAMSum Dataset**.
O objetivo principal é ajustar modelos pré-treinados, como T5 ou BART, para gerar automaticamente resumos coerentes e informativos a partir de conversas do cotidiano. 

O fluxo do projeto inclui:

- Carregamento e análise do dataset.
- Pré-processamento e tokenização dos textos.
- Configuração do DataCollator para tarefas de Seq2Seq.
- Definição de parâmetros de treinamento.
- Fine-tuning utilizando a API Trainer da Hugging Face.
- Previsões usando o modelo treinado

---

## Tecnologias Utilizadas

- **Hugging Face Transformers**: para modelos e tokenização.
- **Hugging Face Datasets**: para carregamento e manipulação eficiente do SAMSum.
- **Pandas**: para tratamento dos dados.

---

## Dataset Utilizado

**SAMSum Dataset**  
Contém mais de 16 mil exemplos de conversas reais com resumos humanamente anotados, ideal para treinar e avaliar modelos de resumo automático.

---

## Como funciona o pipeline

1. Carrego o SAMSum com `datasets.load_dataset`.
2. Aplico tokenização e pré-processamento para adequar os textos ao modelo.
3. Utilizo o `DataCollatorForSeq2Seq` para lidar com o padding dinâmico.
4. Defino `TrainingArguments` com parâmetros como taxa de aprendizado, batch size, e estratégias de avaliação e salvamento.
5. Faço o fine-tuning com `Trainer`, ajustando o modelo à tarefa de summarization.
6. Faço predições utilizando o modelo treinado


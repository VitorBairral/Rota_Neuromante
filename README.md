# Rota da Neuromante
Repositório virtual para a tarefa "Rota da Neuromante" da disciplina de Redes Neurais da Ilum Escola de Ciência
## Objetivo:
Para esta tarefa, foi demandado o teste de ao menos 100 arquiteturas de redes neurais diferentes para resolução de um problema de classificação ou regressão. O problema a ser resolvido é a identificação de indivíduos portadores de Alzheimer ou não com base na base de dados provida por [1]. Para fazer isso, foram abordadas duas estratégias: a Classificação por Support Vector Machine (SVC) e por um classificador Multilayer Perceptron.

## Estrutura do Projeto
### Dataset: 
A base de dados é o arquivo Dataset_Alzheimers.csv. A base de dados possui 131 colunas, sendo duas de dados categóricos e o restante de dados numéricos, e 333 linhas, representando cada paciente analisado. As duas colunas de dados categóricos são "Genotype", que pertence aos atributos a serem analisados e a coluna "Class" que representa a classe de indivíduos ("Impaired" ou "Control", sendo os indivíduos afetados ou saudáveis respectivamente) que queremos prever.

### Classificador SVC (Base):
O arquivo SVC.ipynb realiza a classificação por meio de Supported Vector Machine. Possui todos os processos de tratamento de dados, split train-test e processamento necessários.

### Rede Neural:
O arquivo Rede Neural.ipynb realiza a classificação por meio de Multilayer Perceptron. Possui todos os processos de tratamento de dados, split train-test e processamento necessários.

### Outros arquivos:
Os arquivos svc-alzheimer4.db e MLPfinal_agora_vai_mesmo2 são arquivos de saída de objetos de estudo do optuna. Estão presentes para economizar o tempo do leitor com uma rodada de otimizações de hiperparâmentros.

## Resultados:
O modelo SVC apresentou grande viés muito grande para os dados "Control", não prevendo nenhum indivíduo doente.

A rede neural apresentou overfit severo na sua curva de aprendizado, o que torna os resultados pouco confiáveis. Apresentou métricas elevadas, com macro-média e média ponderada das métricas altas. A matriz de confusão demonstra poucos erros, acertando a maior parte de ambos os tipos de indivíduos.


## Referências
[1] CRAIG-SCHAPIRO, R.; KUHN, M.; XIONG, C.; et al. Multiplexed immunoassay panel identifies novel CSF biomarkers for Alzheimer’s disease diagnosis and prognosis. PLoS ONE, v. 6, n. 4, e18850, 2011. DOI: 10.1371/journal.pone.0018850
### Uso de IA:
Para resolver eventuais problemas que apareceram durante o desenvolvimento do código, foram utilizados recursos de inteligência artificial. A conversa está disponível em: https://claude.ai/chat/b21e125d-3831-4050-90bf-2831e227177c

###  A proposta para prever os valores da coluna 'failure_type' da sheet 'desafio_manutencao_preditiva_teste.csv' consiste basicamente em um modelo de machine learn do tipo Arvore de Decisão Classificatória (DecisionTreeClassifier) treinando um modelo e em seguida aplicado dos dados de Teste.

###  Por se tratar de um problema do tipo Classificação,decido usar o modelo que mais se aproxima dos dados,  chamado DecisionTreeClassifier da biblioteca Sklearn. 
  
###  Os pros são : poder utilizar uma variavel string a ser prevista 

###  Os contras são: que ja nos Features (Variaveis de treino x) não posso utilizar string, por isso me levou a retirar a coluna type do dataframe.
  
  
###  Para medir a Performace (eficácia) do modelo, é utilizado a função Accuracy_score do pacote sklearn.metrics.

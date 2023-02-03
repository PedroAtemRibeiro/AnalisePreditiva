#                                                   Desafio Análise Preditiva
 
 ## Desafio

Olá candidato, o objetivo deste desafio é testar os seus conhecimentos sobre a resolução de problemas de análise de dados e aplicação de modelos preditivos. Queremos testar seus conhecimentos dos conceitos estatísticos de modelos preditivos, criatividade na resolução de problemas e aplicação de modelos básicos de machine learning.  É importante deixar claro que não existe resposta certa e que o que nos interessa é sua capacidade de descrever e justificar os passos utilizados na resolução do problema. 

Seu objetivo é identificar quais máquinas apresentam potencial de falha tendo como base dados extraídos através de sensores durante o processo de manufatura.  Para isso são fornecidos dois datasets: um dataset chamado desafio_manutencao_preditiva_treino composto por 6667 linhas, 9 colunas de informação (features) e a variável a ser prevista (“failure_type”). 

O segundo dataset chamado de desafio_manutencao_preditiva_teste possui 3333 linhas e 8 colunas e não possui a coluna “failure_type”. Seu objetivo é prever essa coluna a partir dos dados enviados e nos enviar para avaliação dos resultados.


## Resolução ->

### Para prever os valores da coluna 'failure_type' da sheet 'desafio_manutencao_preditiva_teste.csv', eu aplicaria um modelo de machine learn do tipo Arvore de Decisão.


1 - Primeiro eu começo importando o arquivo de treino 'desafio_manutencao_preditiva_treino.csv'para a variavel 'Dados' e transformando-o em um dataFrame utilizando a biblioteca Pandas


2- Faço o mesmo para os dados de Teste, vinculando à variavel DadosTeste.

### 3- Escolho somente as colunas(Variaveis) necessárias para DadosTeste : 'air_temperature_k'	'process_temperature_k'	'rotational_speed_rpm'	'torque_nm'	'tool_wear_min'.

4- Para aplicar o aprendizado de maquina importamos a biblioteca Train_test_split do pacote sklearn

5- Divido os dados de teste em x(Features) e y(Predict)

6- Aplico a função de aprendizado de maquina 'Train_test_split' utilizando as variaveis x e y, e determinando a porcentagem de teste para '0.2'
 
### 7- Por se tratar de um problema do tipo Classificação,decido usar o modelo que mais se aproxima dos dados,  chamado DecisionTreeClassifier da biblioteca Sklearn. Os pros são : poder utilizar uma variavel string a ser prevista 
os contras são: que ja nos Features (Variaveis de treino x) não posso utilizar string, por isso me levou a retirar a coluna type do dataframe.

8- Chamo a função DecisionTreeClassifier utilizando os parâmetros de x_treino e y_treino .

9- Agora com nosso modelo ja treinado, chamo esta função utilizando os dados de x e o transformo em um dataframe vinculando à variavel 'FullPredictedSheetTrain'para testarmos a eficácia do modelo.

### 10- Para medir a Performace (eficácia) do modelo, é utilizado a função Accuracy_score do pacote sklearn.metrics.

### 11- Ao aplicar a função Accuracy_score para a comparação dos dataframes 'FullPredictedSheetTrain' e 'Y', é obtido um percentual de 99.4% de acerto .

### 12- Agora podemos aplicar o modelo 'DecisionTreeClassifier' para os dados de  'desafio_manutencao_preditiva_teste.csv' 




![1](https://user-images.githubusercontent.com/114637779/216668172-f5831793-af6e-4e99-a0ee-073869113a7d.png)






### 13- Agora é só concatenar com a tabela de Teste deixando só a coluna exigida no desafio .




![2](https://user-images.githubusercontent.com/114637779/216668662-3ee608d9-29c9-4f60-a0a8-c5856e105f48.png)




### 14- Por fim eu exporto a tabela concatenada em formato csv para a sheet 'Predicted' conforme o solicitado.


### OBS : A criação do arquivo FeedBack é para tirar a teima de que o aprendizado de maquina estaria funcionando .
----------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Como Rodar o Projeto : 

### É necessário ter a sheet onde deseja salvar os resultados dentro do mesmo Folder do projeto, e na linha  "TableTest.to_csv('NomeDoArquivo.formato', index =False)"  adicionar o nome desse arquivo seguido de '.' e o tipo do arquivo.


## Video de Execução 'Predicted' : 


https://user-images.githubusercontent.com/114637779/216673700-465c96d7-55b0-4570-942d-1a5c2dc1cc06.mp4




## Video de Execução 'Feedback' : 



https://user-images.githubusercontent.com/114637779/216673739-1b309304-4114-4b3c-b917-8c7b30e185c9.mp4



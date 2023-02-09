#                                                   Desafio Análise Preditiva
 
[Desafio](PedroAtemRibeiro/AnalisePreditiva/blob/main/Desafio.md)

[Proposta]() 

[Importando Dados](https://github.com/PedroAtemRibeiro/AnalisePreditiva/blob/main/ImportandoDados.md)

[Dividindo e Treinando Modelo](https://github.com/PedroAtemRibeiro/AnalisePreditiva/blob/main/dividindoTreinando.md)

[Aplicando Modelo](https://github.com/PedroAtemRibeiro/AnalisePreditiva/blob/main/usandoModelo.md)

[Concatenando e Exportando](https://github.com/PedroAtemRibeiro/AnalisePreditiva/blob/main/ConcatenandoeExportando.md)

[Como Rodar o Projeto]()

Para prever os valores da coluna 'failure_type' da sheet 'desafio_manutencao_preditiva_teste.csv', eu aplicaria um modelo de machine learn do tipo Arvore de Decisão.


1 - Primeiro eu começo importando o arquivo de treino 'desafio_manutencao_preditiva_treino.csv'para a variavel 'Dados' e transformando-o em um dataFrame utilizando a biblioteca Pandas


2- Faço o mesmo para os dados de Teste, vinculando à variavel DadosTeste.

### 3- Escolho somente as colunas(Variaveis) necessárias para DadosTeste : 'air_temperature_k'	'process_temperature_k'	'rotational_speed_rpm'	'torque_nm'	'tool_wear_min'.

4- Para aplicar o aprendizado de maquina importamos a biblioteca Train_test_split do pacote sklearn

5- Divido os dados de teste em x(Features) e y(Predict)

6- Aplico a função de aprendizado de maquina 'Train_test_split' utilizando as variaveis x e y, e determinando a porcentagem de teste para '0.2'
 
### 7- Por se tratar de um problema do tipo Classificação,decido usar o modelo que mais se aproxima dos dados,  chamado DecisionTreeClassifier da biblioteca Sklearn. 
### Os pros são : poder utilizar uma variavel string a ser prevista 
### Os contras são: que ja nos Features (Variaveis de treino x) não posso utilizar string, por isso me levou a retirar a coluna type do dataframe.

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



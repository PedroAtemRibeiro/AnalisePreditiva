### 1- Para aplicar o aprendizado de maquina importamos a biblioteca Train_test_split do pacote sklearn

### 2- Escolho somente as colunas(Variaveis) necessárias para DadosTeste : 'air_temperature_k' 'process_temperature_k' 'rotational_speed_rpm' 'torque_nm' 'tool_wear_min'.

### 3- Para aplicar o aprendizado de maquina importamos a biblioteca Train_test_split do pacote sklearn

### 4- Divido os dados de teste em x(Features) e y(Predict)

### 5- Aplico a função de aprendizado de maquina 'Train_test_split' utilizando as variaveis x e y, e determinando a porcentagem de teste para '0.2'

### 6- Chamo a função DecisionTreeClassifier utilizando os parâmetros de x_treino e y_treino .

### 7- Agora com nosso modelo ja treinado, chamo esta função utilizando os dados de x e o transformo em um dataframe vinculando à variavel 'FullPredictedSheetTrain'para testarmos a eficácia do modelo.

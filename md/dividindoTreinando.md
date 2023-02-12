 Para aplicar o aprendizado de maquina importamos a biblioteca Train_test_split e DecisionTreeClassifier do pacote sklearn
![ImportandoTreino](https://user-images.githubusercontent.com/114637779/217748985-717681d4-885b-48d2-b5e3-19ddf7e69939.png)

  Escolho somente as colunas(Variaveis) necessárias para DadosTeste : 'air_temperature_k' 'process_temperature_k' 'rotational_speed_rpm' 'torque_nm' 'tool_wear_min'.

  Divido os dados de teste em x(Features) e y(Predict).

  Aplico a função de aprendizado de maquina 'Train_test_split' utilizando as variaveis x e y, e determinando a porcentagem de teste para '0.2'

![TrainTestSplit](https://user-images.githubusercontent.com/114637779/217749706-b1bd7f0d-dcc6-4f6d-aa8e-545a142a6508.png)



  Chamo a função DecisionTreeClassifier utilizando os parâmetros de x_treino e y_treino.

![DecisionTreetrein](https://user-images.githubusercontent.com/114637779/217749886-b751f25d-3fba-494d-a504-b16567fa140a.png)

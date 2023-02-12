## Importando Dados

Primeiro eu começo importando o arquivo de treino 'desafio_manutencao_preditiva_treino.csv'para a variavel 'Dados' e transformando-o em um dataFrame utilizando a biblioteca Pandas

![Importando Panda](https://user-images.githubusercontent.com/114637779/217747892-74ef176e-a592-4ca4-a9c5-e5077c0d4bbd.png)
![ImportandoDadosTreino](https://user-images.githubusercontent.com/114637779/217748650-35946941-e969-4566-8167-dacf32fbc702.png)



Faço o mesmo para os dados de Teste, vinculando à variavel DadosTeste.

![ImportandoDAdosTeste](https://user-images.githubusercontent.com/114637779/217748313-fcb9b26c-fd4e-441b-a3b5-dbbe6b413100.png)

 Escolho somente as colunas(Variaveis) necessárias para DadosTeste : 'air_temperature_k' 'process_temperature_k' 'rotational_speed_rpm' 'torque_nm' 'tool_wear_min'.

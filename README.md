# Introdução
![Proposta](https://github.com/user-attachments/assets/6bdffd3f-9f46-451d-a724-d14994df85fa)
## Desenvolvimento
![image](https://github.com/user-attachments/assets/d72c47ff-d40b-41d6-b1fc-f42bdf58ca23)
Resultados
---
1. Busca de Redes Wi-Fi: O dispositivo escaneia redes Wi-Fi disponíveis e verifica se os pontos de acesso (APs) de interesse são encontrados com base em seus SSIDs.
2. Cálculo de Distâncias: Para cada AP encontrado, o código utiliza a intensidade do sinal (RSSI) para estimar a distância entre o dispositivo e o AP, com base em uma fórmula de propagação de sinal.
3. Triangulação: Se as distâncias para três APs forem determinadas, o código calcula a posição do dispositivo resolvendo um sistema de equações.
4. Exibição dos Resultados: Quando bem-sucedido, a posição estimada (coordenadas x e y) é exibida. Caso contrário, o código informa que a trilateração falhou ou que nem todos os APs foram encontrados.
---
O código realiza uma estimativa da posição de um dispositivo no espaço 2D utilizando redes Wi-Fi próximas, calculando distâncias com base no RSSI e aplicando trilateração para obter as coordenadas.

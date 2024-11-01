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
O código realiza uma estimativa da posição de um dispositivo no espaço 2D utilizando redes Wi-Fi próximas, calculando distâncias com base no RSSI e aplicando trilateração para obter as coordenadas.


# Funcionamento da ESP32:
---
### Criando o efeito Bouncing:
O efeito de ''bouncing'' surge com frequência em circuitos que utilizam botões, pois é a forma mais acessível de interação entre pessoas e máquinas. No entanto, botões mecânicos causam um fenômeno indesejado: ao serem pressionados, podem gerar sinais rápidos devido à vibração interna do contato.

Sem Controle de Estado: O código não alterna entre estados; ele simplesmente acende e apaga o LED sempre que o botão está pressionado.

Bouncing: Se você pressionar e soltar o botão, o LED pode piscar rapidamente devido ao efeito de bouncing, pois ele não lida com múltiplas leituras rápidas.

Intervalo: O LED acende e apaga em um intervalo definido por blink_interval, mas o comportamento pode ser irregular se o botão gerar múltiplas leituras.

Efeito de Bouncing: Ao usar este código, você deve notar que o LED pode piscar rapidamente, especialmente se você pressionar e soltar o botão rapidamente.

Link do experimento: https://wokwi.com/projects/413130701876292609

![image](https://github.com/user-attachments/assets/653c6445-9479-4292-a67d-7bf12c1fc43b)



# Solução
---
O debouncing por meio de software é realizado utilizando um pequeno atraso no código (o conhecido delay), que seria o tempo suficiente para que a etapa do efeito bouncing passasse, e desta forma minimizar esse problema.

Debouncing: Um atraso é introduzido após detectar que o botão está pressionado. Isso ajuda a evitar múltiplas leituras rápidas.

Alternância de Estado: O estado do LED (led_on) é alternado toda vez que o botão é pressionado e o LED é atualizado com o novo estado.

Aguardar Botão Solto: Após alternar o estado do LED, o código aguarda até que o botão seja solto antes de continuar, evitando que a mesma ação seja registrada várias vezes.

Comportamento
Ao pressionar o botão, o LED acende ou apaga dependendo do estado anterior.
Pressionar o botão novamente alterna o estado do LED.
Esse código deve proporcionar um controle eficaz do LED sem o efeito de bouncing. 

https://wokwi.com/projects/413130611969250305
![image](https://github.com/user-attachments/assets/6143a238-8fa4-4cd7-bf82-65d63c8eaefe)


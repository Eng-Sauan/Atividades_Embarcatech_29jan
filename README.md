ATIVIDADE 1:

Este código implementa a simulação de um semáforo utilizando a placa BitDogLab com arquitetura Pi Pico W. Ele controla três LEDs representando as cores do semáforo (vermelho, amarelo e verde) e exibe mensagens no terminal indicando a contagem regressiva para a troca de estado.

A lógica funciona com dois temporizadores:

1- Temporizador dos LEDs (3 segundos por estado): Alterna os LEDs entre verde, amarelo e vermelho seguindo a sequência do semáforo.

2- Temporizador das mensagens (1 segundo por estado): Exibe uma contagem regressiva correspondente à cor do semáforo, garantindo sincronização com os LEDs.

A função verifica_estado() muda os LEDs conforme o estado atual, enquanto temp_semaforo() imprime os avisos no terminal. O loop principal apenas mantém o programa em execução, pois os temporizadores gerenciam a alternância dos estados automaticamente.



ATIVIDADE 2:


Este código implementa um sistema de controle de LEDs utilizando um botão na placa BitDogLab com arquitetura Pi Pico W. O funcionamento é baseado na ativação de um ciclo de estados dos LEDs após o pressionamento do botão.

Funcionamento:

1- Inicialização: Configura os pinos dos LEDs e do botão. O botão utiliza um resistor pull-up interno.

2- Pressionamento do Botão: Quando pressionado, inicia um ciclo de LEDs e impede novas ativações até o ciclo terminar.

3- Ciclo dos LEDs: Alterna entre quatro estados em intervalos de 3 segundos:

* Todos os LEDs acesos.
* Apenas vermelho e verde acesos.
* Apenas verde aceso.
* Todos apagados.

4- Temporizador: Um alarme gerencia a troca de estados até que todos os LEDs se apaguem, permitindo uma nova ativação do botão.

O loop principal verifica constantemente o estado do botão e evita repetições indesejadas usando um atraso de debounce.


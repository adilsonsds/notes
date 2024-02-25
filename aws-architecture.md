
# SQS

## Tipos

* Standard
  * Sem limite de mensagens por segundo.
* FIFO
  * Limite de 3000 mensagens por segundo.
  * Garantia de ordem (primeiro que chega é o primeira que sai).

## Visibility timeout

Quando uma mensagem for processada, ela ficará "oculta" para outros *consumers* por determinado tempo.
Valor aceito: 0 segundos até 12 horas.

## Message retention

Tempo em que a mensagem ficará na fila até desaparecer. Valor aceito: 1 minuto até 14 dias.

## Delivered delay

Tempo que a mensagem entre ter sido inserida até começar a ser consumida.


# AWS Fargate
Recomendado usar quando tem um worker consumindo uma fila

# Amazon EC2 Instances
Recomendado usar em casos onde é necessário ter uma disponibilidade contínua como, por exemplo, aplicações web, API.
Aluna: Mirian Ajiki Molicawa
Instrutor: Jefferson Stachelski - Engenheiro de software
Conceitos de arquitetura em aplicações para internet.
19/10/2021

# Exercício Final

Com base no Exercício 2, desligue um dos serviços criados e tente utilizar o sistema, faça isso para as duas versões e compare o resultado.

Se desligado o sistema 2 - usuários não receberão notificações do sistema de biblioteca.

Sem as notificações, usuário além de não receber as últimas novidades sobre livros, matérias e reportagens, ficará sem saber das datas agendadas para entrega de livros.

Na versão Microserviços #2, adicione uma ferramente de fila (como o RabbitMQ) e adicione na fila Dead letter queue a mensagem que teve durante sua tentativa de processar, para isso provoque um erro manualmente.

As mensagens de uma fila podem ser "devolvidas", ou seja, republicada quando qualquer um dos seguintes eventos ocorrer:

- A mensagem é confirmada negativamente por um consumidor usando basic.reject ou basic.nack com o parâmetro requeue definido como false.
- A mensagem expira devido ao TTL por mensagem;
- A mensagem é descartada porque a fila excedeu o limite de comprimento

Adição de ferramenta
rabbitmqctl on Windows
rabbitmqctl.bat set_policy my-pol "^one-meg$" ^
"{""max-length-bytes"":1048576}" ^
--apply-to queues

      The message is dropped because its queue exceeded a length limit

Define Max Queue Length Using x-arguments During Declaration

This example in Java declares a queue with a maximum length of 10 messages:
Map<String, Object> args = new HashMap<String, Object>();
args.put("x-max-length", 10);
channel.queueDeclare("myqueue", false, false, false, args);

Fonte: https://www.rabbitmq.com/maxlength.html
https://www.rabbitmq.com/dlx.html

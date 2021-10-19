Aluna: Mirian Ajiki Molicawaa
Instrutor Jefferson Stachelski - Engenheiro de software
Conceitos de arquitetura em aplicações para internet.
19/10/2021

# Exercício 2

Com base no sistema escrito no Exercício 1, crie uma cópia do sistema criado com o objetivo de ter uma versão na arquitetura Microserviços #1 e outro na arquitetura Microserviços #2

Use como message broker a ferramenta de sua preferência.

Microserviços #1
Visão:
O sistema de biblioteca virtual. Poderá ser acessado de forma web, através de aplicativos instalados em dispositivos móveis com tecnologia android ou IOS, assim como aplicativos para desktops nas diferentes plataformas operacionais.

Um message broker é um software que possibilita que aplicativos, sistemas e serviços se comuniquem e troquem informações entrem sistema, com o objetivo de fazer integração de serviços permitindo que os remetentes emitam mensagens sem saber onde estão os destinatários, se eles estão ativos ou não ou quantos deles existem.

RabbitMQ é ideal para entrega de mensagens de baixa latência, garantias por mensagem e roteamento complexo.

Sistema de mensagens ponto a ponto: esse é o padrão de distribuição utilizado em filas de mensagens com um relacionamento de um a um entre o remetente e o destinatário da mensagem. Cada mensagem na fila é enviada somente a um destinatário e é consumida somente uma vez. O sistema de mensagens ponto a ponto é chamado quando uma mensagem deve receber uma ação somente uma vez. Exemplos de casos de uso adequados para esse estilo de sistema de mensagens incluem folha de pagamento e processamento de transações financeiras. Nesses sistemas, tanto os remetentes quanto os destinatários precisam de uma garantia de que cada pagamento será enviado uma vez e uma única vez.

No caso, como exemplo: como regra o usuário que realizar empréstimo de livro e não devolver em tempo agendado pagará multa financeira.

Microserviços #2

Os message brokers também tem:

Sistemas de mensagens de publicação/assinatura: nesse padrão de distribuição de mensagens, também chamado de "pub/sub", o produtor publica cada mensagem em um tópico e diversos consumidores de mensagens assinam os tópicos para receber as mensagens. Todas as mensagens publicadas em um tópico são distribuídas para todos os aplicativos inscritos. Trata-se de um método de distribuição de estilo de transmissão, no qual há um relacionamento de um para muitos entre o publicador da mensagem e os consumidores. Se, por exemplo, uma companhia aérea fosse disseminar atualizações sobre os horários de pouso ou o status de atraso de seus voos, diversas partes poderiam fazer uso das informações: tripulações de solo realizando manutenção e reabastecimento de aeronaves, responsáveis por bagagens, comissários de bordo e pilotos se preparando para a próxima viagem do avião e operadores de monitores visuais notificando o público. Um estilo de sistema de mensagens pub/sub seria apropriado para uso nesse cenário

Então deste modo os message brokers podem validar, armazenar, rotear e entregar mensagens aos destinos apropriados.

Então, caso o usuário inscreva-se para receber notificações da biblioteca receberá as atualizações de livros, matérias,reportagens, vídeos pertinentes aos sistema de bibliotecas.

RabbitMQ é ideal para entrega de mensagens de baixa latência, garantias por mensagem e roteamento complexo.

Fonte:
https://en.wikipedia.org/wiki/Message_broker
https://www.ibm.com/br-pt/cloud/learn/message-brokers

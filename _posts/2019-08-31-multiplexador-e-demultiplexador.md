---
layout: post
title: Multiplexador e Demultiplexador
subtitle: >-
  Para se obter uma saída nos circuitos combinacionais é preciso colocar os
  valores exclusivamente e unicamente nas entradas do circuito, ao contrário dos
  circuitos sequenciais mais conhecidos como flip-flops ...
categories: acadêmico
---
Para se obter uma saída nos circuitos combinacionais é preciso colocar os valores exclusivamente e unicamente nas entradas do circuito, ao contrário dos circuitos sequenciais mais conhecidos como flip-flops, que para obter um resultado final é preciso enviar valores para entradas e também para suas saídas. Eu sei pode parecer esquisito mas é assim que os flip-flops funcionam, e isso acontece porque suas saídas são conectadas com entradas de outras portas dos circuitos.

![ Um exemplo de circuitos combinacionais ](/img/uploads/combinacional.png " Um exemplo de circuitos combinacionais ")





![Um exemplo de Flip-Flop](/img/uploads/flipflop.gif "Um exemplo de Flip-Flop")

Você pode achar que estar no texto errado porque começamos com os conceitos de circuitos combinacionais e sequenciais ao invés de começamos com o multiplex e demultiplex.



Isso aconteceu porque tanto multiplex e o demuliplex são circuitos combinacionais cujo o objetivo é o envio de informações. Mas você dever estar se perguntado qual a principal diference entre os dois?



O multiplex serve para enviar a informação para vários canais de informação para um canal e o demultiplex possui a função inversa ou seja envia informações de um canal para vários canais.



Agora que você sabe o conceitos de ambos os circuitos, vamos aprender a esquematizar os dois, mas para isso é preciso entender o conceito de gerador de produtos canônicos.



Quando se trabalha com circuitos digitais só é possível se trabalhar com duas saídas que são 0 e 1, então através da fórmula 2 elevado a n é possível obter o números de combinações possíveis usando esses valores com um determinado número de variáveis, então as possiblidades com duas variáveis são:

![Tabela do gerador de produtos canônicos](/img/uploads/tabelamultiplex-1-.png "Tabela do gerador de produtos canônicos")

Se você desenhar os circuitos lógicos dessa tabela, você automaticamente estar criando um gerador de produtos canônicos, então significa dizer que esse circuito consiste em possibilidades de combinações de 1 e 0 então se você quiser fazer um gerador de produtos canônicos de 3 variáveis, só é preciso criar uma tabela verdade e depois gerar o desenho.

![Exemplo do desenho do gerador de produtos canônicos](/img/uploads/canonicos.png "Exemplo do desenho do gerador de produtos canônicos")

Agora finalmente vamos entender como criar um circuito multiplex, que basicamente consiste em um gerador de produtos de canônicos sendo que cada uma das suas portas representam um canal de comunicação e que são interligadas em uma porta ou.

![Exemplo de um multiplexador de 4 canais](/img/uploads/multiplexador.png "Exemplo de um multiplexador de 4 canais")

A diferença do desenho do demultiplexador para o do multiplexador é que não possui uma porta ou e sim uma entrada que representa o canal de comunicação que envia a informação para os outros canais.

![Exemplo de um demultiplexador de 4 variáveis](/img/uploads/demultiplexador.jpg "Exemplo de um demultiplexador de 4 variáveis")

Espero que você tenha aprendido um pouco sobre multiplex e demultiplex, no final tem 5 questões para vocês praticarem, bons estudos.



MULTIPLEX E DEMULTIPLEX



1- Faça um multiplex de 16 canais



2- Diferencie multiplex do demultiplex



3- Explique o funcionamento do gerador de produtos canônicos.



4- Porque na estrutura do multiplex e do demultiplex existe o gerador de produtos canônicos

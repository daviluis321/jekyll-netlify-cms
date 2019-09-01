---
layout: post
title: Conhecendo o Wireshark
subtitle: >-
  Se você precisa de um programa para análise de pacotes que trafegam em uma
  determinada rede, o wireshark é o programa certo, tanto que ele pode ser usado
  para solucionar problemas de rede, examinar problemas de segurança e até
  mesmo, ajudar a entender um pouco sobre o funcionamento dos protocolos de
  redes.
categories: redes
---
Se você precisa de um programa para análise de pacotes que trafegam em uma determinada rede, o wireshark é o programa certo, tanto que ele pode ser usado para solucionar problemas de rede, examinar problemas de segurança e até mesmo, ajudar a entender um pouco sobre o funcionamento dos protocolos de redes.



Para instalar o mesmo no Windows, só é preciso baixar o instalador no site oficial, já no linux (Distribuições Baseadas no Debian), é preciso utilizar os comandos abaixo:



sudo add-apt-repository ppa:wireshark-dev/stable

sudo apt-get update

sudo apt-get install wireshark

Eu vou utilizar o Windows 10, talvez a interface mude no seu sistema operacional.

![Tela Inicial do Wireshark.](/img/uploads/interface.jpg "Tela Inicial do Wireshark.")

A Tela inicial do wireshark mostra as interfaces de rede disponíveis para a análise, além mostrar as que estão com um maior tráfego de dados. No meu caso, vou clicar no Wi-Fi, para explorar as funcionalidades do wireshark. Obs: No Linux depois que você instalar o software, algumas interfaces de rede não estejam disponíveis, porque o wireshark precisa da permissão do administrador.

![Interface Wi-Fi.](/img/uploads/wifi.jpg "Interface Wi-Fi.")

A próxima tela vai mostrar todos pacotes trafegando na rede, em tempo real, tanto que a rolagem do software é automática e isso é bom mas também pode ser ruim se o tráfego for muito grande mas é possível configurar essa rolagem, além do recurso de filtragem de pacotes. Também é possível observar diversas colunas que serão explicadas abaixo:



1. Time: Mostra o tempo que pacote foi capturado;
2. No: Mostrar a ordem de captura dos pacotes;
3. Source: Destino: Contém o endereço do ponto de partida do pacote;
4. Destination: Endereço do ponto de chegada do pacote;
5. Protocol: O nome do Protocolo, como UDP por exemplo;
6. Length: Tamanho do Pacote;
7. Info: Detalhes Adicionais

Agora vamos para o recurso que vc vai utilizar bastante que são os filtros, como você pode observar nas imagens existe um campo de texto com “Apply a display filter”, lá vai ser aonde vai acontecer a mágica você digitar http e vai aparecer todos protocolos relacionados a esse protocolo. Mas muitas vezes vamos precisar ser mais específicos, para isso podemos utilizar strings específicas como http.request.method == "GET", que vai me dá o seguinte resultado:

![Filtrando Requisições Get.](/img/uploads/get.jpg "Filtrando Requisições Get.")

Para facilitar na hora de criar sua string, você clicar no no “expression” ao lado do "mais".

![Montando Strings de Busca.](/img/uploads/string.jpg "Montando Strings de Busca.")

Você vai perceber também que cada pacote de dados possui cores específicas, elas servem como regras para entender melhor as mesmas, você pode ir na opção view do menu principal e depois clicar em coloring rules.

![Color Rules](/img/uploads/colorules.jpg "Color Rules")

O Wireshark também fornece o recurso statistics que fornece uma análise detalhada dos dados e até mesmo geração de gráficos:

![Statistics](/img/uploads/statiscs.jpg "Statistics")

![Gráficos](/img/uploads/graficos.jpg "Gráficos")

Caso você queira trabalhar com estatística em outro software como minitab ou excel por exemplo, você pode exportar o arquivo para, csv, txt, xml e json.

![Exportanto Dados](/img/uploads/dados.jpg "Exportanto Dados")

Por último o wireshark é open source, além de possui diversos projetos para integração caso seja necessário, aumentando as possibilidades de uso desse software. Espero que vocês tenham gostado desse artigo, vou está sempre melhorando ele, até mais.

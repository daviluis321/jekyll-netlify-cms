---
layout: post
title: Entendendo o Css Display
subtitle: >-
  Quando eu comecei estudar css, acabava quebrando diversos layouts, por não
  conhecer bem as características, por isso estou fazendo esse texto sobre box
  model, que vai ser parte de uma série de posts relacionados ao css ...
categories: css
---
Quando eu comecei estudar css, acabava quebrando diversos layouts, por não conhecer bem as características, por isso estou fazendo esse texto sobre box model, que vai ser parte de uma série de posts relacionados ao css.

Bem  cada elemento dentro do seu site possui é uma caixa retangular formada por diversas propriedades e denominada de box model, como na figura abaixo.

![Box Model](/img/uploads/box-model.svg "Box Model")

 Descomplicando cada parte da figura:

\-Content : O conteúdo da caixa, onde o texto e as imagens aparecem

\-Padding : Espaço dentro do Container 

\-Border : Uma borda em volta do elemento

\-Margin :  Espaço fora do Container

Agora que entendemos a teoria, abaixo vou deixar um exemplo na prática onde você pode fazer uma cópia e começa a testar essas propriedades do box model.

<br>

<div>

<p class="codepen" data-height="265" data-theme-id="0" data-default-tab="html,result" data-user="daviluis321" data-slug-hash="pozrqKw" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="Box Model">

  <span>See the Pen <a href="https://codepen.io/daviluis321/pen/pozrqKw/">

  Box Model</a> by Davi Luis de Oliveira (<a href="https://codepen.io/daviluis321">@daviluis321</a>)

  on <a href="https://codepen.io">CodePen</a>.</span>

</p>

</div>



No código acima definimos a largura de 250px  através da propriedade width, mas graças a box model temos 370px do nosso elemento e também temos o margin de 20px cada lado, dando 410px, que o elemento tá ocupando. 



Para entender isso melhor vamos analisar o cálculo incluindo todos os elementos do box model  abaixo:



250px (width)

+ 50px + 50px (left + right padding)

+ 10px + 10px  (left + right border)

+ 2px (left + right margin)

\= 410px  

Então olha o problema que isso pode gerar, porque muitas vezes  eu queria um elemento de 300px por exemplo e não sabia o cálculo do box model então acabava que eu sempre quebrava os layouts. 

Mas se você não gostar do comportamento do box model, o css tem um recurso onde você pode alterar o mesmo, porque padrão nosso elemento está definido content-box, que possui essa característica de adicionar mais pixels ao elemento e pode resolvido definindo o box-sizing = border box; igual no código abaixo:

<br>

<p class="codepen" data-height="265" data-theme-id="0" data-default-tab="html,result" data-user="daviluis321" data-slug-hash="zYOdQXO" style="height: 265px; box-sizing: border-box; display: flex; align-items: center; justify-content: center; border: 2px solid; margin: 1em 0; padding: 1em;" data-pen-title="Box Model 2">

  <span>See the Pen <a href="https://codepen.io/daviluis321/pen/zYOdQXO/">

  Box Model 2</a> by Davi Luis de Oliveira (<a href="https://codepen.io/daviluis321">@daviluis321</a>)

  on <a href="https://codepen.io">CodePen</a>.</span>

</p>

Agora agora o nosso elemento, mesmo com border e padding vai ter 250px, é claro ainda vai precisa com margin que a gente colocou de 20px.

Para finalizar espero que você entendido como funciona o box model e que isso a fazer os seus layouts, além disso recomendo você sempre utilizar ferramentas como pager rule e o brackets por exemplo, para verificar o tamanho real dos seus elementos

**Referências**

****[**https://developer.mozilla.org/pt-BR/docs/Web/CSS/box_model**](https://developer.mozilla.org/pt-BR/docs/Web/CSS/box_model)****

****[**https://www.w3.org/TR/CSS2/box.html**](https://www.w3.org/TR/CSS2/box.html)****

<https://tableless.github.io/iniciantes/manual/css/box-model.html>

<https://pt-br.learnlayout.com/box-model.html>

<https://www.w3schools.com/css/css_boxmodel.asp>

<https://www.geeksforgeeks.org/css-box-model/>

<https://hackernoon.com/the-box-model-44fc2c04a935>

<https://internetingishard.com/html-and-css/css-box-model/>

<https://medium.com/@silascaimi/o-modelo-caixa-do-css-box-model-384d05d9817d>

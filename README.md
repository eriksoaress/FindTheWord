# FindTheWord

## Introdução 
O projeto FINDTHEWORD tem como objetivo criar um algoritmo que jogue o jogo da forca, com o máximo 5 tentativas. 

## Explicação da ideia por trás do algoritmo
O algoritmo de jogar o jogo da forca tem por base acertar uma palavra com no máximo 5 chances de errar. O projeto tem por base aplicar os conhecimentos obtidos de álgebra linear em sala de aula. Fizemos uma implementação que utiliza o conceito de frequência das letras nas palavras. Isso traz uma leve ideia de uma arvore de decisão binária, no qual a letra que será chutada será aquela que aparece mais vezes em palavras distintas. Decidimos por optar chutar na letra que mais aparece nas palavras, em vez de chutar naquela que mais aparece no geral( por exemplo, nas palavras mamao e abacate, usando o método escolhido, temos que a letra a aparece nas duas palavras, logo a gente considerou como 2 a frequência dessa letra, ao invés de contar como 5). O método que a gente escolheu  reduz a probabilidade de errar a letra em comparação com o outro método. Nesse projeto, utilizamos probabilidades, que foi usado para selecionar a letra mais recorrente no espaço amostral de palavras.

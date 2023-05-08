# FindTheWord

## Introdução 
O projeto FINDTHEWORD tem como objetivo criar um algoritmo que jogue o jogo da forca, com o máximo 5 tentativas. 

## Explicação da ideia por trás do algoritmo
Em um jogo da forca, onde se conhece todas as palavras disponíveis, é interessante a ideia de chutar a letra que possui uma frequência maior nas 
palavras. A ideia central do nosso algoritmo foi baseado nas frequências das letras que aparecem nas palavras. As frequências das letras são 
baseado no princípio de verificar qual a letra que mais aparece nas palavras. Como por exemplo, considere as palavras abacate e mamao, a letra a aparece nas duas palavras, por isso sua frequência é tida como duas, a letra m só aparece em mamao, por isso sua frequência é uma. Perceba que não consideramos a quantidade de letras em sí, mas apenas a quantidade de palavras que ela aparece. Isso é uma estratégia que visa minimizar a chance de errar a letra, pois conseguimos aumentar a probabilidade de acertar aquela letra pois temos uma quantidade máxima de palavras que a possue no espaço amostral. Essa técnica é 
boa pois no jogo da forca não perdemos uma chance se acertamos a letra. Assim, conseguimos reduzir cada vez mais o número de palavras no espaço  amostral de possibilidades de palavras, mesmo que de forma menos eficiente do que o método que conta o total bruto de letras nas palavras(por exemplo, em abacate e mamao, a contagem seria de que há 5 letras a e duas letras m). A gente pensou nesse método, mas vimos que existe um risco maior de errar a letra. Isso pode ser demonstrado da seguinte forma: suponha que tenhamos um conjunto de n palavras no nosso espaço amostral S, vamos supor que a letra mais frequente (considerando a frequência das palavras contando apenas uma vez mesmo se a letra aparecer mais de uma vez na mesma palavra. Vamos chamar de método 1) seja a letra a, desse modo dentro do espaço amostral S, teremos um conjunto de k palavras, com k <= n. Suponha agora que estamos usando o método 2(o que conta a letra mais de uma vez mesmo se ela aparece na mesma palavra) e que a letra mais frequente seja a letra b com uma quantidade q de letra b, temos que q <= k. Vamos provar pelo método da prova por absurdo que q <= k. Dado que 
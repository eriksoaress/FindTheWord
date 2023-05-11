# FindTheWord

## Introdução 
O projeto FINDTHEWORD tem como objetivo criar um algoritmo que jogue o jogo da forca, com o máximo 5 tentativas. 

## Como instalar
Para utilizar o programa basta clonar esse repositório em algum local de sua máquina. Para fazer isso, clique no botão verde "Code" logo acima, escolha um modo de baixar o repositório, podendo ser baixando o zip e descompactando ou clonando através de https ou ssh. Após seguir essas etapas, será preciso instalar as bibliotecas necessárias. Isso pode ser feito, estando na raiz do projeto, rodando no terminal o seguinte comando: pip install -r requirements.txt , com isso, as bibliotecas necessárias serão instaladas. No projeto já existe um demo.ipynb que é a solucão já implementada e rodada.

## Explicação da ideia por trás do algoritmo
O algoritmo do jogo da forca tem por base acertar uma palavra com no máximo 5 chances através de conhecimentos de álgebra linear.\
Fizemos uma implementação que utiliza a frequência das letras nas palavras, isso traz e aplica ideia de uma arvore de decisão binária, no qual a letra que será chutada será aquela que aparece mais vezes em palavras distintas.

Decidimos por optar chutar na letra que mais aparece nas palavras, em vez de chutar naquela que mais aparece no geral( por exemplo, nas palavras mamao e abacate, usando o método escolhido, temos que a letra a aparece nas duas palavras, logo a gente considerou como 2 a frequência dessa letra, ao invés de contar como 5). O método que a gente escolheu  reduz a probabilidade de errar a letra em comparação com o outro método.

Nesse projeto, utilizamos probabilidades para selecionar a letra mais recorrente no espaço amostral de palavras. Como o algoritmo se baseia em chutar a letra que aparece em mais palavras, para fazer ele falhar, basta que haja no mínimo 6 palavras (incluindo a certa) nas quais todas as letras não testadas dessas palavras devem possuir a mesma frequência que as não testadas das outras palavras. Dessa forma, o nosso algoritmo começa a encontrar casos em que ele não tem certeza da resposta correta, haja vista que não consegue reduzir o espaço amostral tanto quanto o necessário.
# Conjuntos

## Definir conjuntos

$\newcommand{\N}{\mathbb N}$

Conjuntos são objetos básicos na matemática. A teoria dos conjuntos foi desenvolvido a partir do final do século XIX por matemáticos tais como Cantor, Hilbert, Zorn, Zermelo e Fraenkel. A teoria rigorosa dos conjuntos é um assunto avançado que nós não vamos abordar nesta disciplina. O que nós vamos estudar neste semestre é chamado "Teoria Ingênua dos Conjuntos". Para estudar matemática moderna e avançada, esta teoria não é suficiente, mas ela serve para introduzir os conceitos básicos e fundamentar os estudos nas disciplinas da graduação.

Um *conjunto* $A$ é uma coleção de objetos. Se $x$ é um objeto que pertence ao conjunto $A$, então escrevemos que $x\in A$. Se $x$ não pertence a $A$, então escreve-se que $x\not\in A$. Para um conjunto ser bem definido, é necessário que para qualquer objeto $x$ seja possível decidir se $x\in A$ ou $x\not\in A$. Nós vamos considerar apenas conjuntos de objetos de matemática (tais como números, funções, etc). Muitos textos gostam de citar exemplos de conjuntos de objetos cotadianos, mas estes conjuntos normalmente não satisfazem o critério de ser bem definido. Por exemplo, se queremos considerar o conjunto $X$ de alunos da UFMG, não é claro se o mesmo inclui os alunos que estão em trancamento, os pesquisadores de pós-doutorado, os alunos que não frequentam disciplinas, etc. Para evitar estas ambiguidades, vamos considerar apenas conjuntos que contêm objetos matemáticos.

Exemplos $\label{ex:conjuntos}$

:   - Podemos considerar por exemplo o conjunto $X=\{1,2,3,4,5\}$. Neste caso $1\in X$, mas $-1\not\in X$. 
- Pode-se também considerar o conjunto $\mathbb N$ dos números naturais. Temos que $\N=\{1,2,3,\ldots\}$. Em particular, $2\in\N$, mas $-1\not\in\N$. Nós também não vamos considerar zero como natural, então $0\not\in \N$. 
  
Note que o uso do símbolo $\ldots$ está usado no segundo exemplo. Normalmente, este símbolo deve ser evitado, pois pode introduzir  ambiguidade desnecessária. Por exemplo, se escrevemos que $X=\{2,5,8,12,\ldots\}$, então não se sabe se $15\in X$ ou $15\not\in X$. No entanto, em alguns casos quando o significado está absolutamente claro, permitimos o uso de $\ldots$.

Conjuntos podem ser definidos também como uma coleção de elementos em um conjunto maior. Por exemplo, seja
$$
    X=\{n\in\N\mid \mbox{$n$ é múltipo de $2$}\}.
$$
Em outras palávras, $X$ é o conjunto dos números naturais pares. Note que a definição de $X$ tem duas partes. Na primeira parte ``$n\in\N$'', nós indicamos que os elementos de $X$ serão elementos de $\N$, enquanto na segunda parte, especificamos quais elementos de $\N$ serão elementos de $X$. Neste caso, os elementos de $X$ são os elementos de $\N$ qua são múltiplos de $2$.  

## Subconjuntos
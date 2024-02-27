# Proposições ou sentenças

\newcommand{\lxor}{\dot\lor}
\newcommand{\cond}{\Rightarrow}
\newcommand{\bicond}{\Leftrightarrow}


### Proposições simples

Entender o significado de afirmações na matemática exige o conhecimento dos elementos da lógica básica que vamos estudar nesta página. Além disso, a compreensão deste conteúdo é importante também no trabalho com expressões lógicas (booleanas) nas [linguagens de programação](https://panda.ime.usp.br/aulasPython/static/aulasPython/aula05.html).

Na matemática, uma *proposição* (ou *sentença*) é uma afirmação que afirma um fato. Por exemplo, as seguintes afirmações são proposições:

- $1\neq 2$;
- $\pi < \sqrt{10}$;
- $1+2=3$.

Cada proposição deve ser ou *verdadeira* ou *falsa*, mas não pode ser verdadeira *e* falsa no mesmo tempo. A veracidade ou falsidade de uma proposição chama-se *valor lógico* ou *valor de verdade*. Cada proposição tem exatamente um dos dois valores lógicos: *verdadeiro* ou *falso*. É importante notar que uma proposição não precisa ser verdadeira. Por exemplo, a terceira proposição na lista anterior é falsa, mas ela é ainda uma proposição (com valor lógico *falso*).

Nesta disciplina, nós lidamos com proposições sobre objetos de matemática, como nos exemplos anteriores, pois as proposições cotadianas, tais como "O Pedro é estudante" são frequentamente demasiado polémicas para terem um valor lógico bem definido. (Pode ser que o Pedro não está matriculado no momento, ou pode ser que mesmo sendo matriculado não frequenta as aulas. Nestes casos, pode ser questionável se o Pedro é de fato um estudante.) 

As seguintes não são proposições. 

- $x = 3$.
- O número $10$ é interessante. 
- Você deve estudar mais.


No primeiro caso, o valor lógico depende do valor de $x$ que não está definido. Nos dois outros casos, a afirmação é subjetiva, pode ser verdadeira para uma pessoa e falsa para uma outra.


:::{.exe}
**Exemplo.** A propisição que "2 é um número par" é verdadeira, enquanto a proposição "3 é um número negativo" é falsa. Similarmente, a proposição "$2+3=5$" é verdadeira, enquanto a proposição "$2+3<5$" é falsa.
:::

As proposições no exemplo anterior e na lista em cima são *proposições simples*.

### Proposições compostas

Usando as operações lógicas, pode-se formar proposições compostas a partir das proposições simples (ou atómicas). As principais operações lógicas (ou conectivos) são **conjunção** (e), **disjunção** (ou) e a **negação** (não). 

Sejam $A$ e $B$ proposições. 


**A conjunção ($\land$)**: 
A conjunção das proposições $A$ e $B$ é a proposição $A\land B$ (leia-se "$A$ e $B$"). A proposição $A\land B$ é verdadeira se e somente se $A$ é verdadeira e $B$ é verdadeira. Caso contrário, $A\land B$ é falsa.

**A disjunção ($\lor$)**: 
A disjunção das proposições $A$ e $B$ é a proposição $A\lor B$ (leia-se "$A$ ou $B$"). A proposição $A\lor B$  é verdadeira se e somente se $A$ é verdadeira ou $B$ é verdadeira. Em particular, se ambas de $A$ e $B$ são verdadeiras, então $A\lor B$ é verdadeira. Caso contrário, $A\lor B$ é falsa.

**A negação ($\neg$)**: 
A negação da proposição $A$ é $\neg A$ (leia-se "não $A$"). A proposição  $\neg A$ é verdadeira se e somente se $A$ é falsa. Caso contrário $\neg A$ é falsa

:::{.exe}
**Exemplo:** Considere por exemplo as seguintes duas proposições $A$ e $B$.
\begin{align*}
A&:2+4=3;\\
B&:\mbox{$9$ é múltiplo de $3$}.
\end{align*}
Os valores lógicos das proposições que podemos formar com as operações $\land$, $\lor$, $\neg$ são os seguintes:
\begin{align*}
A&:\mbox{falsa}\\
B&:\mbox{verdadeira}\\
\neg A&:\mbox{verdadeira}\\
\neg B&:\mbox{falsa}\\
A\land B&:\mbox{falsa}\\
A\lor B&:\mbox{verdadeira}\\
\neg A\land B&:\mbox{verdadeira}\\
A\land \neg B&:\mbox{falsa}\\
\neg A\land \neg B&:\mbox{falsa}\\
\neg(A\land B)&:\mbox{verdadeira}\\
\neg A\lor B&:\mbox{verdadeira}\\
A\lor \neg B&:\mbox{falsa}\\
\neg A\lor \neg B&:\mbox{verdadeira}\\
\neg(A\lor B)&:\mbox{falsa}\\
\end{align*}
:::

As operações $\neg$, $\lor$ e $\land$ podem ser combinadas para obter afirmações mais complexas. Por exemplo a afirmação
$$
[\neg(A\land B)]\lor [\neg(A\lor B)]
$$
é verdadeira, pois ela é a disjunção de duas afirmações, a primeira sendo verdadeira, enquanto a segunda sendo falsa.

Note que nós usamos parênteses para indicar a ordem das operações. A última expressão poderia ser escrita também como 
$$
\neg(A\land B)\lor \neg(A\lor B)
$$
sem nenhuma ambiguidade. Em caso de dúvida, é melhor adicionar os parênteses que omitir. Às vezes, os parênteses são necessários para a interpretação da expressão. Por exemplo, a expressão 
$$
A\lor B \land C
$$
está ambígua, pois pode denotar $(A\lor B)\land C$ ou 
$A\lor(B\land C)$. Se $A$ é verdadeira e $C$ é falsa, então $(A\lor B)\land C$ é falsa, mas $A\lor (B\land C)$ é verdadeira (independentemente do valor lógico de $B$). Nestes casos, as operações são feitas da esquerda para a direita, e a proposição deve ser interpretada como $(A\lor B)\land C$. Tendo dito isso, é melhor colocar as parénteses. 

Outras operações lógicas que são frequentamente usadas são a disjunção exclusiva $\lxor$, a condicional $\cond$ e bicondicional $\bicond$.

**Disjunção exclusiva ($\lxor$)**: 
A disjunção exclusiva (XOR ou XOU) das proposições $A$ e $B$ é a proposição $A\lxor B$ (ou $A$ ou $B$ mas não ambos). A proposição $A\lxor B$ é verdadeira se e somente se $A$ é verdadeira ou $B$ é verdadeira, mas não quando $A$ e $B$ são ambas verdadeiras. Caso contrário $A\lxor B$ é falsa.

**Condicional ($\cond$)**: 
A condicional das proposições $A$ e $B$ é a proposição $A\cond B$ (leia-se "$A$ implica $B$"). A proposição $A\cond B$ é verdadeira se e somente se $A$ é falsa, ou $A$ e $B$ são ambas verdadeiras. 

**Bicondicional ($\bicond$)**: A bicondicional das proposições $A$ e $B$ é a proposição $A\bicond B$ (leia-se "$A$ é equivalente a $B$"). A proposição $A\bicond B$ é verdadeira se e somente se $A$ é $B$ têm o mesmo valor lógico; ou seja, $A$ e $B$ são ambas verdadeiras ou $A$ e $B$ são ambas falsas.


Note que a disjunção exclusiva $\lxor$ está mais próxima ao  significado cotadiano da palavra "ou". Nas expressões de matemática "ou" normalmente significa disjunção inclusiva e quando queremos disjunção exclusiva, isso deve ser claramente indicada. Por exemplo a proposição 
$$
\mbox{($6$ é par)}\lor \mbox{($6$ é um múltiplo de $3$)}
$$
é considerada verdadeira, mas 
$$
\mbox{($6$ é par)}\lxor \mbox{($6$ é um múltiplo de $3$)}
$$
é falsa.

Note também que a condicional $A\cond B$ é verdadeira sempre quando $A$ é falsa. Em outras palavras, a implicação é considerada verdadeira sempre quando a premissa $A$ é falsa. Por exemplo, a proposição 
$$
\mbox{($5$ é par)}\cond\mbox{($10$ é um múltiplo de $3$)}
$$
é considerada verdadeira. É importante notar que isso não quer dizer de forma nenhuma que $10$ é um múltiplo de $3$! Quer dizer apenas que a afirmação que "$5$ é par" implica que "$10$ é múltiplo de $3$". Ou seja, uma afirmação falsa implica qualquer outra afirmação. Nós vamos ver situações ainda nesta disciplina que vão explicar melhor o porquê desta regra.

### A tabela-verdade

A veracidade de proposições compostas pode ser estudada usando tabelas-verdade. Sejam $P$ e $Q$ proposições simples. A tabela verdade da proposição $P\land Q$ é a seguinte. 


| $P$ | $Q$ | $P\land Q$ |
|---|---|---------|
| V | V | V       |
| V | F | F       |
| F | V | F       |
| F | F | F       |

Considere a seguinte expressão.
$$
(P \land \neg Q) \lor (\neg P \land Q). 
$$
A sua tabela-verdade pode ser escrita como 




| $P$ | $Q$ | $\neg P$ | $\neg Q$ | $P \land \neg Q$ | $\neg P \land Q$ | $(P \land \neg Q) \lor (\neg P \land Q)$ |
|---|---|---|---|---|---|---|
| V | V | F | F | F | F | F |
| V | F | F | V | V | F | V |
| F | V | V | F | F | V | V |
| F | F | V | V | F | F | F |

Note que a expressão $(P \land \neg Q) \lor (\neg P \land Q)$ é verdadeira se e somente se $P$ é verdadeira ou $Q$ é verdadeira, mas elas não são verdadeiras no mesmo tempo. Logo, pode se concluir que 
$$
(P \land \neg Q) \lor (\neg P \land Q) \bicond P \lxor Q
$$
para qualquer proposição $P$ e $Q$

:::{.exercise}
Exercício.
Usando tabelas-verdade, verifique, para proposições $P$ e $Q$, que 
$$
P\cond Q \bicond (\neg P) \lor Q
$$
e 
$$
P\bicond Q \bicond (P \land Q) \lor (\neg P \land \neg Q).
$$
:::

:::{.exercise}
Exercício.
Demonstre as seguintes afirmações usando tabelas-verdade.
$$
\neg(P\lor Q)\bicond \neg P \land \neg Q
$$
e 
$$
\neg(P\land Q) \bicond \neg P \lor \neg Q
$$
:::

As afirmações no exercício anterior são conhecidas como as *identidades de de Morgan*. Elas são importantes quando formamos negações de proposições compostas. Por exemplo, se 
$$
P:\ \mbox{$2$ é primo}, \quad Q:\ \mbox{$3$ divide $7$}
$$
então 
\begin{align*}
P\land Q&:\ \mbox{$2$ é primo e $3$ divide $7$}\\
P\lor Q&:\ \mbox{$2$ é primo ou $3$ divide $7$}\\
\neg(P\land Q)&:\ \mbox{$2$ não é primo ou  $3$ não divide $7$}\\
\neg(P\lor Q)&:\ \mbox{$2$ não é primo e $3$ não divide $7$}\\
\end{align*}



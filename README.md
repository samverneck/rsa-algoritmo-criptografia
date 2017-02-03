# RSA algoritmo [criptografia]

Geração das chaves
No RSA as chaves são geradas desta maneira:

1 - Escolha de forma aleatória dois números primos grandes {\displaystyle p\,}  e {\displaystyle q\,} , da ordem de {\displaystyle 10^{100}}  no mínimo.
2 - Compute {\displaystyle n=pq\,} 
3 - Compute a função totiente em {\displaystyle n\,} : {\displaystyle \phi (n)=(p-1)(q-1)\,} .
4 - Escolha um inteiro {\displaystyle e\,}  tal que 1 < {\displaystyle e\,}  < {\displaystyle \phi (n)\,} , de forma que {\displaystyle e\,}  e {\displaystyle \phi (n)\,}  sejam primos entre si.
5 - Compute {\displaystyle d\,}  de forma que {\displaystyle de\equiv 1{\pmod {\phi (n)}}\,} , ou seja, {\displaystyle d\,}  seja o inverso multiplicativo de {\displaystyle e\,}  em {\displaystyle {\pmod {\phi (n)}}\,} .

* No passo 1 os números podem ser testados probabilisticamente para primalidade
* No passo 5 é usado o algoritmo de Euclides estendido, e o conceito de inverso multiplicativo que vem da aritmética modular
Por final temos:

A chave pública: o par {\displaystyle (n,e)} .

A chave privada: a tripla {\displaystyle (p,q,d)} . (De fato, para desencriptar, basta guardar {\displaystyle d}  como chave privada, mas os primos {\displaystyle p}  e {\displaystyle q}  são usados para acelerar os cálculos)


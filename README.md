# Testes-Lumni
Testes técnicos realizados para empresa Lumni 

**1 - Parênteses Balanceados**
##
Uma string que consiste em parênteses esquerdo e direito, "(" e ")", é dada e pede-se que você equilibre os parênteses inserindo parênteses conforme necessário. Determine o número mínimo de caracteres que devem ser inseridos.


Descrição do formato da função solução
1) Recebe como parâmetro uma string com parênteses.
2) Retorne um número inteiro que deve ser o número mínimo de caracteres a serem adicionados na string.


Exemplos
Exemplo 1:
Entrada: palavra="()))"
Saída: 2

Exemplo 2:
Entrada: palavra="()()"
Saída: 0

Exemplo 3:
Entrada: palavra="())("
Saída: 2

## SOLUÇÃO

/* A solução utiliza uma pilha para manter os parênteses abertos que ainda não foram fechados. Para cada parêntese na string, verificamos se ele é de abertura ou fechamento.

Se o parêntese for de abertura, o adicionamos na pilha. Caso contrário, verificamos se a pilha está vazia (o que significa que não há nenhum parêntese aberto que possa ser fechado) e, caso esteja, incrementamos o número de adições necessárias. Se a pilha não estiver vazia, removemos o último parêntese aberto da pilha.

Ao final do loop, somamos o número de adições necessárias com o tamanho da pilha (que indica quantos parênteses abertos ainda não foram fechados) para obter o número mínimo de caracteres a serem adicionados. */

##

**2 - Possivelmente Palíndromas**

Observe as seguintes strings abaixo:

"arara"
"osso"
"socorram-me, subi no onibus em marrocos"

Agora leia essas strings de trás para frente. Você pode ler elas independentemente do sentido da leitura!

Palavras e frases assim são chamadas de palíndromas.

Agora observe as seguintes strings:
"parar"
"temem"
"technation"

"parar" e "temem" são chamadas de palavras potencialmente palíndromas
Isso ocorre porque você pode rearranjar/permutar as letras dessas palavras de forma que elas se tornem palíndromas

"parar" -> "rapar"
"temem" -> "metem"

Enquanto isso, "technation" nunca será uma palavra palíndroma, independentemente de como você reorganizar as letras dela (se duvida de mim, pode tentar!)

Observações adicionais:
1) Não é necessário que as strings sejam palavras que existem na vida real
2) Considere a string vazia como potencialmente palíndroma


Descrição do formato da função solução
1) Recebe como parâmetro uma string
2) Retorne True, caso a palavra seja potencialmente palíndroma. Retorne False, caso contrário


Exemplos
Exemplo 1:
Entrada: palavra = "abbac"
Saída: True

Exemplo 2:
Entrada: palavra = "abba"
Saída: True

Exemplo 3:
Entrada: palavra = "abbacd"
Saída: False

## SOLUÇÃO

/* 
A solução utiliza um Map para armazenar a frequência de cada letra na palavra. Em seguida, percorremos os valores do Map para contar quantas letras aparecem um número ímpar de vezes.

Se o número de letras com frequência ímpar for maior do que 1, a palavra não é potencialmente palíndroma e retornamos false. Caso contrário, a palavra é potencialmente palíndroma e retornamos true.

Note que utilizamos o operador || para inicializar a frequência de cada letra com zero caso ela ainda não tenha sido adicionada ao Map.
*/

## 

**3 - Problema da soma de dois números**


Um vetor com números chamado numeros é dado e pede-se que você encontre os dois elementos desse vetor que somados são iguais ao número objetivo.

Considere que existe somente uma solução possível e que você não poderá usar o mesmo elemento mais de uma vez.

Retorne os valores em ordem crescente de indice no vetor.

## SOLUÇÃO

/*Explicando a solução:

A solução utiliza um Map (uma estrutura de dados que permite armazenar pares chave-valor) para armazenar os elementos do vetor que já foram visitados. A chave do Map é o elemento do vetor e o valor é o índice desse elemento no vetor.

Em cada iteração do loop, calculamos o complemento do elemento atual (isto é, a diferença entre o objetivo e o elemento atual). Verificamos se o complemento já foi visitado, o que significa que encontramos uma solução. Caso contrário, adicionamos o elemento atual ao Map.

Se chegarmos ao final do loop e não encontrarmos uma solução, retornamos um vetor vazio.

Por fim, retornamos um vetor com os índices dos elementos que somados resultam no objetivo, em ordem crescente. Note que utilizamos a função Math.min e Math.max para garantir que o índice menor é retornado primeiro.*/

##

**4 - Problema do Zelador Eficiente**
O zelador de uma faculdade é extremamente eficiente. Ao final de cada dia, todo o lixo da escola está em sacos plásticos com peso entre 1,01 e 3,00 quilos. Então, todas as sacolas plásticas são levadas para as lixeiras do lado de fora. Uma viagem é descrita como selecionar um número de sacolas que juntas não pesam mais de 3,00 quilos, despejá-las na lixeira externa e retornar à faculdade. Dado o número de sacolas plásticas n e o peso de cada sacola, determine o número mínimo de viagens que o zelador deve fazer.


Descrição do formato da função solução
1) Recebe como parâmetro um vetor com o peso das sacolas a serem levadas.
2) Retorne a quantidade de viagens que o zelador deve fazer.


Exemplos
Exemplo 1:
Entrada: pesos = [1.01, 1.99, 2.5, 1.5, 1.01]
Saída: 3
Explicação: O zelador consegue levar todas as sacolas plásticas em 3 viagens: [1,01 + 1,99 , 2,5, 1,5 + 1,01].

Exemplo 2:
Entrada: pesos = [1.01, 1.01, 1.01, 1.4]
Saída: 2

Exemplo 3:
Entrada: pesos = [1.01, 1.993, 1.32, 1.7, 1.8]
Saída: 4

## SOLUÇÃO

// ordena os pesos em ordem crescente
// inicializa a quantidade de viagens como 0
// inicializa o índice do primeiro elemento como 0
// inicializa o índice do último elemento como o tamanho do vetor menos 1
// se a soma dos pesos for menor ou igual a 3.0
// incrementa o índice do primeiro elemento
// decrementa o índice do último elemento
// incrementa a quantidade de viagens
// retorna a quantidade de viagens


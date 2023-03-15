# Trabalho de Compiladores
Este é um repositório do trabalho realizado para a disciplina de Construção de Compiladores na Universidade Federal de Uberlândia. Nosso objetivo é desenvolver um compilador que possa realizar as funções básicas da linguagem de programação definida em nossa gramática.


# GLC Inicial


programa ::= declaracoes comandos

declaracoes ::= declaracao | declaracoes declaracao

declaracao ::= tipo identificador ;

tipo ::= int | float | char

identificador ::= [a-zA-Z][a-zA-Z0-9]*

comandos ::= comando | comandos comando

comando ::= atribuicao | condicional | repeticao

atribuicao ::= identificador = expressao ;

expressao ::= termo | expressao operador termo | ( expressao )

termo ::= fator | termo operador fator

fator ::= identificador | numero | ( expressao )

numero ::= inteiro | flutuante | char

inteiro ::= [0-9]* | - [0-9]*

flutuante ::= [0-9].[0-9]+(E[-+]?[0-9]+)? | -[0-9].[0-9]+(E[-+]?[0-9]+)?

char ::= '[a-z| A-Z | 0-9]*'

operador ::= + | - | * | /

condicional ::= if ( expressao ) comando | if ( expressao ) comando else comando

repeticao ::= enquanto ( expressao ) comando | faça comando enquanto ( expressao ) | repita comando até ( expressao )


==============

# Tabela de tokens

| Token           | Atributo                           | Tipo        |
|----------------|-----------------------------------|-------------|
| int            | -                                 | palavra reservada     |
| float          | -                                 | palavra reservada     |
| char           | -                                 | palavra reservada     |
| se             | -                                 | palavra reservada     |
| enquanto          | -                                 | palavra reservada     |
| faça             | -                                 | palavra reservada     |
| repita         | -                                 | palavra reservada     |
| até          | -                                 | palavra reservada     |
| identificador  | nome do identificador              | cadeia      |
| inteiro        | valor do número inteiro            | inteiro     |
| flutuante      | valor do número de ponto flutuante | flutuante   |
| caractere      | valor do caractere                 | caractere   |
| +              | -                                 | operador    |
| -              | -                                 | operador    |
| *              | -                                 | operador    |
| /              | -                                 | operador    |
| =              | -                                 | operador    |
| ==             | -                                 | operador    |
| <              | -                                 | operador    |
| >              | -                                 | operador    |
| <=             | -                                 | operador    |
| >=             | -                                 | operador    |
| (              | -                                 | delimitador |
| )              | -                                 | delimitador |
| {              | -                                 | delimitador |
| }              | -                                 | delimitador |
| ;              | -                                 | delimitador |
| /.../              | comentario                                 | string |

# Trabalho de Compiladores
Trabalho para a disciplina de construção de compiladores


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
| int            | -                                 | palavra     |
| float          | -                                 | palavra     |
| char           | -                                 | palavra     |
| if             | -                                 | palavra     |
| while          | -                                 | palavra     |
| do             | -                                 | palavra     |
| repeat         | -                                 | palavra     |
| until          | -                                 | palavra     |
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
| ;              | -                                 | delimitador |
| /.../              | comentario                                 | string |

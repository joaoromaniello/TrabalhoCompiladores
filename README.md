# Trabalho de Compiladores
Trabalho para a disciplina de construção de compiladores


# GLC Inicial

GLC para aritmética básica: 


<programa> ::= <declaracoes> <comandos>

<declaracoes> ::= <declaracao> | <declaracoes> <declaracao>

<declaracao> ::= <tipo> <identificador> ;

<tipo> ::= int | float | char

<identificador> ::= [a-zA-Z][a-zA-Z0-9]*

<comandos> ::= <comando> | <comandos> <comando>

<comando> ::= <atribuicao> | <condicional>

<atribuicao> ::= <identificador> = <expressao> ;

<expressao> ::= <termo> | <expressao> <operador> <termo> | ( <expressao> )

<termo> ::= <fator> | <termo> <operador> <fator>

<fator> ::= <identificador> | <numero> | ( <expressao> )

<numero> ::= <inteiro> | <flutuante> | <char>

<inteiro> ::= [0-9]* | - [0-9]*  (Permite tanto positivo quanto negativo)

<flutuante> ::= [0-9]* +.[0-9]+(E[-+] + [0-9]) | - [0-9]* +.[0-9]+(E[-+] + [0-9]) 

<char> ::= '[a-z| A-Z | 0-9]*'

<operador> ::= + | - | * | /

<condicional> ::= if ( <expressao> ) <comando>


# Tabela de tokens

| Token         | Nome              | Tipo de Atributo |
|---------------|-------------------|------------------|
| ;             | Ponto e vírgula   | Nenhum           |
| int           | Palavra reservada | Tipo de dado     |
| float         | Palavra reservada | Tipo de dado     |
| char          | Palavra reservada | Tipo de dado     |
| [a-zA-Z]      | Identificador     | String           |
| [0-9]+        | Inteiro           | Inteiro          |
| - [0-9]+      | Inteiro           | Inteiro          |
| [0-9]*\.[0-9]+ | Flutuante         | Flutuante        |
| [0-9]+E[-+]?[0-9]+ | Flutuante      | Flutuante        |
| '[a-zA-Z0-9]' | Char              | Char             |
| +             | Operador          | Nenhum           |
| -             | Operador          | Nenhum           |
| *             | Operador          | Nenhum           |
| /             | Operador          | Nenhum           |
| if            | Palavra reservada | Nenhum           |
| (             | Parêntese         | Nenhum           |
| )             | Parêntese         | Nenhum           |

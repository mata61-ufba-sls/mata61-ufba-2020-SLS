# Projeto de um Compilador

## Parte I: Análise Léxica

Nesta parte do projeto, você irá implementar um analisador léxico para a linguagem C-. 
O analisador léxico ou _scanner_ deve ler um programa fonte e produzir uma lista de _tokens_, sequencialmente, um _token_ de cada vez, anotado com as seguintes informações: tipo do _token_ (identificador, constante inteira, etc) e sua localização no código fonte.
Se uma entrada inválida for encontrada, ele deve parar e informar _error_, anotado com o lexema incorreto.

Antes de iniciar a sua implementação, recomendamos que leia com atenção o [capítulo 3](../resources/20-chapter3.pdf) do livro "Introduction to Compilers and Language Design" de Douglas Thain. Apesar da sintaxe de C- ser um pouco diferente da usada nesse livro, os exemplos de código e o material podem ser extremamente úteis.

Para conhecer Flex, pode utilizar texto [Flex in a Nutshell](../resources/21-FlexInANutshell.pdf).

## Classes de _tokens_ 

In your lexer implementation, consider the following classes of tokens in the language:

```
__ID__      Identifier
__NUM__     Literal decimal (integer)
__KEY__     Keyword
__SYM__     Lexical Symbol
__ERROR__   Lexeme of the first error found
 ``` 
  
* Exemplo de arquivo de entrada (main.c)

```
void main(void)
{
  int a;
  a = 4 + 5;
}
```

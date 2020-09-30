# Projeto de um Compilador

## Parte I: Análise Léxica

Nesta parte do projeto, você irá implementar um analisador léxico para a [linguagem C-](../../language/README.md). 
O analisador léxico ou _scanner_ deve ler um programa fonte e produzir uma lista de _tokens_, sequencialmente, um _token_ de cada vez, anotado com as seguintes informações: tipo do _token_ (identificador, constante inteira, etc) e sua localização no código fonte.
Se uma entrada inválida for encontrada, ele deve parar e informar _error_, anotado com o lexema incorreto.

Antes de iniciar a sua implementação, recomendamos que leia com atenção o [capítulo 3](../../resources/20-chapter3.pdf) do livro "Introduction to Compilers and Language Design" de Douglas Thain. Apesar da sintaxe de C- ser um pouco diferente da usada nesse livro, os exemplos de código e o material podem ser extremamente úteis.

Para conhecer Flex, pode utilizar texto [Flex in a Nutshell](../../resources/21-FlexInANutshell.pdf).

## Classes de _tokens_ 

Em sua implementação do analisador léxico, considere as seguintes classes de _tokens_ da linguagem:

__ID__      Identifier  
__NUM__     Literal decimal (integer)  
__KEY__     Keyword  
__SYM__     Lexical Symbol  
__ERROR__   Lexeme of the first error found  

Comentários e caracteres de espacejamento (_white space_) devem ser descartados durante a fase de análise léxica do compilador. Você deve imprimir o número da linha na qual o _token_ foi encontrado, inclusive no caso de erro. O analisador léxico deve parar após encontrar o primeiro erro léxico.
No caso de erro por um comentário não fechado (_unfinished comment error_), o lexema ```'/*' ``` deve ser o _token_ __ERROR__. 
O formato de saída é: 

``` (line_num,token_class,"lexeme") ```
  
## Exemplo de arquivo de entrada (main.c)
```
void main(void)
{
  int a;
  a = 4 + 5;
}
```

## Como executar (dois argumentos: entrada e saída)
O programa deve ler a entrada a partir de um arquivo (_source_) e escrever a saída em outro arquivo (_target_):
```
$ ./lexer main.c main.lex
```

## Exemplo de arquivo de saída gerado pelo analisador léxico (main.lex)
```
(1,KEY,"void")
(1,ID,"main")
(1,SYM,"(")
(1,KEY,"void")
(1,SYM,")")
(2,SYM,"{")
(3,KEY,"int")
(3,ID,"a")
(3,SYM,";")
(4,ID,"a")
(4,SYM,"=")
(4,NUM,"4")
(4,SYM,"+")
(4,NUM,"5")
(4,SYM,";")
(5,SYM,"}")
```

## Scripts
Não se esqueça de criar dois arquivos em sua pasta de submissão: __compile.sh__ e __run.sh__ para compilar e executar o seu código:

+ __compile.sh__ (se estiver usando a ferramenta Flex)
```
flex lexer.lex
gcc -o lexer lex.yy.c -ll
```

+ __run.sh__ (recebe dois argumentos que deverão ser nomes de arquivos)
```
./lexer $1 $2
```

__Observação Importante sobre__ ___Line Endings___: Arquivos de texto criados com DOS/Windows machines usam _carriage return_ _line feed_ ("\r\n") para terminar uma linha, enquando que os criados com Unix usam apenas o _line feed_ ("\n").

-----
Material cedido pelo Prof. Vinicius.

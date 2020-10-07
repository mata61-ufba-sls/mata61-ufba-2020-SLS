# A Linguagem C-

## Aspectos Léxicos

1. Palavras-chave (_keywords_)

```
else  if  int  return  void  while
```

As palavras-chave são reservadas e devem ser escritam em letras minúsculas.

2. Símbolos especiais

```
  +  -  *  /  <  <=  >  >=  ==  !=  =  ;  ,  (  )  [  ]  {  }  //
```

 3. ID (identificadores) e NUM (números inteiros)

```
  ID = letter (letter | digit)*

  NUM = digit digit*

  letter = a | .. | z | A | .. | Z

  digit = 0 | .. | 9
```

Carateres minúsculos e maiúsculos são diferenciados.

4. Caracteres de espacejamento (_white space_) incluem _blanks_ (' '), _newlines_ ('\n'), e _tabs_ ('\t'). Tais caracteres devem ser ignorados exceto quando separam  ID, NUM e palavras-chave.

5. Comentários de uma linha apenas

Comentários de uma linha (_single-line comments_) são iniciados por "//".
Comentários podem ser colocados em qualquer local do programa, mas a ocorrência "//" indica que o resto da linha será considerado como comentário.
Comentários não podem se estender por mais de uma linha e não podem ser aninhados.
Outros tipos de comentários não são suportados.

-----
Adaptação com base no material cedido pelo Prof. Vinicius.

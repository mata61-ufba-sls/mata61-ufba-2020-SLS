# A Linguagem C-

A especificação da linguagem Cminus ou C- foi extraída e adaptada a partir do livro  "Compiler Construction Principles And Practice" de Kenneth Louden. 
A linguagem inclui variáveis inteiras, funções e arrays. Ela possui declarações locais e globais e suporta comandos condicionais (_if-statement_) e comandos de repetição (_while-statement_), bem como chamadas de função recursivas. A linguagem C- tem esse nome porque é um pequeno subconjunto da linguagem C.

## Convenções Léxicas

1. Palavras-chave (_keywords_)

```
else  if  int  return  void  while
```

As palavras-chave são reservadas e devem ser escritam em letras minúsculas.

2. Símbolos especiais

```
  +  -  *  /  <  <=  >  >=  ==  !=  =  ;  ,  (  )  [  ]  {  }  /*  */
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

5. Comentários são  utilizam a notação  ``` /* … */```. 
Comentários podem ser colocados em qualquer local em que caracteres de espacejamento (_white spaces_) podem aparecer (isto é, comentários não podem ser colocados dentro de _tokens_), podem ser estender por mais de uma linha e não podem ser aninhados.
Comentários de uma linha (_single-line comments_) que utilizam "//" não são suportados.

## Sintaxe

## Semântica

## Programas em C-

### Programa 1

O programa a seguir recebe dois valores inteiros, calcula o máximo divisor comum entre eles e imprime o resultado na saída.

```
/* A program to perform Euclid's
   Algorithm to compute gcd. */

int gcd (int u, int v) {
    if (v == 0) 
      return u ;
    else 
      return gcd(v,u-u/v*v);

    /* u-u/v*v == u mod v */
}

void main(void) { 
   int x; int y;
   x = input(); 
   y = input();

   output(gcd(x, y)) ;
}
```

### Programa 2
O programa abaixo recebe como entrada uma lista de 10 valores inteiros, ordena usando _selection sort_, e imprime a lista ordenada na saída.

```
/* A program to perform selection sort on a 10 element array */

int x[10];

int minloc(int a[], int low, int high) {
    int i; int x; int k;
    k = low;
    x = a[low];
    i = low + 1;

    while (i < high) {
        if (a[i] < x) {
            x = a[i];
            k = i;
        }
        i = i + 1;
    }
    return k;

}

void sort(int a[], int low, int high) {
    int i;
    int k;
    i = low;

    while (i < high - 1) {
        int t;
        k = minloc(a, i, high);
        t = a[k];
        a[k] = a[i];
        a[i] = t;
        i = i + 1;
    }
}

void main(void) {
    int i;
    i = 0;

    while (i < 10) {
        x[i] = input();
        i = i + 1;
    }

    sort(x, 0, 10);
    
    i = 0;
    while (i < 10) {
        output(x[i]);
        i = i + 1;
    }
}
```

-----
Material cedido pelo Prof. Vinicius.

A primeira coisa que o shell faz ao executar algum comando é interpretar as coisas que foram passadas a ele.


## Quoting 

O quoting serve para proteger/evitar que o shell interprete as variaveis.

```console
$ echo *
Desktop Documents Downloads Music Pictures Public Templates Videos
$ echo "*"
*
```

## \

A barra invertida protege apenas o proximo caracter de ser interpretado.

```console
$ echo \* $SHELL
* /bin/bash
```

## ""

As aspas duplas protegem os caracteres de serem interpretados com a exceção dos seguintes: $, `, \

```console
$ HE4RT="melhor comunidade dev BR"
$ echo "$HE4RT"
melhor comunidade dev BR
```

## ''

As aspas simples tem a mesma função dos demais porém ela protege todos os caracteres de serem interpretados pelo shell.

```console
$ echo '$HE4RT'
$HE4RT
```
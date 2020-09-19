# Exercicios

## 1 - Encontre as seguintes informações sobre a sua instalação Linux:

### O caminho completo do arquivo .bash_history para o seu usuário.

```console
$ echo $HISTFILE
/home/lucas/.bash_history

$ set | grep HISTFILE
HISTFILE=/home/lucas/.bash_history
```

### A release do kernel instalado.

```console
$ uname -r
5.8.8-arch1-1
```

### Os diretórios incluidos em seu PATH.

```console
$ echo $PATH
/home/lucas/.config/composer/vendor/bin:/usr/local/bin:/usr/local/sbin:/usr/bin:/usr/lib/jvm/default/bin:/usr/bin/site_perl:/usr/bin/vendor_perl:/usr/bin/core_perl

$ env | grep "$PATH"
PATH=/home/lucas/.config/composer/vendor/bin:/usr/local/bin:/usr/local/sbin:/usr/bin:/usr/lib/jvm/default/bin:/usr/bin/site_perl:/usr/bin/vendor_perl:/usr/bin/core_perl
```

### O hostname da máquina.

```console
$ echo $HOSTNAME
he4rt

$ uname -n 
he4rt

$ hostname
he4rt
```

### O PID da sua sessão do shell atual

```console
$ echo $$
3768

$ ps | grep bash
3768
```

### A localização do comando tar

```console
$ which tar
/usr/bin/tar
```

## 2 - Crie e exporte uma variável chamada "NOME" que contenha o seu nome completo.

```console
$ export NOME="Lucas Silva"
```

## 3 - Crie um comando que escreva na tela a seguinte frase: "O Conteúdo da Variável $NOME é: <Valor da Variável NOME>"

```console
$ echo 'O conteudo da variavel $NOME é:' $NOME
O conteudo da variavel $NOME é: Lucas Silva
```
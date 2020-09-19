# Shell

O shell é a interface que fica entre o usuário e o linux, é por ele onde conseguimos ter acesso aos recursos que o sistema nos oferece, como ler o conteúdo de um arquivo, desligar o computador, etc.

Existem varios tipos de shell, shell flavors, por exemplo o bash, sh, csh, ksh, zsh entre outros.

### Comandos do shell

Os comandos do shell podem ser classificados em três tipos.

* __Internos:__ são os comandos que fazem parte do shell, embutidos dentro do shell.
* __Externos:__ são os comandos que são instalados.
* __Scripts:__ são sequencias lógicas de passos a serem seguidos dentro do shell.

É possivel identificar qual o tipo do comando utilizando o type.

```console
$ type echo
echo is a shell builtin

$ type tar
tar is /bin/bash
```

Ao utilizar o comando type podemos nos deparar com um retorno como este: 

```console
$ type clear
clear is hashed (/usr/bin/clear)
```

Isso acontece pois ao usarmos comandos externos o linux faz um cache do comando.

### PATH

PATH é uma variavel de ambiente que armazena os diretórios onde o shell irá consultar para encontrar os comandos externos. Os diretórios são separados por dois pontos, ":", e consultados respectivamente, da esquerda para direita.

```console
$ echo $PATH
/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/games:/usr/local/games:/snap/bin
```

### Caminhos

Existem dois tipos de caminhos:

#### Absolutos:

São aqueles indicados desde o inicio, no caso o diretório "/".
    
```console 
$ cd /home/lucas/Desktop    
```

#### Relativos: 

São aqueles indicados com base no diretório atual.

```console
$ cd Desktop/
```

### Execução de scripts

Para executarmos scripts é necessario referencia-los ou move-los para algum diretório contido na variavel de ambiente PATH.

```console
$ ./script.sh
$ ./home/lucas/script.sh 
```

Caso o arquivo esteja em algum diretório da variavel PATH basta digitar somente o comando sem referencia-lo.

```console
$ script.sh
```

## Alguns comandos

### echo

Este comando mostra na tela o que o usuário digitar na frente.

```console
$ echo Linux
Linux
$ echo "He4rt Devs"
He4rt Devs
```

Também podemos imprimir variaveis com este comando, como visto anteriormente.

```console
$ echo $SHELL
/bin/bash
```

### pwd

Este comando mostra o diretório atual completo.

```console
$ pwd
/home/lucas
```

### cd

Este comando é utilizado para a navegação entre os diretórios.

```console
$ cd Desktop/
```

### ls

Lista o conteúdo dos diretórios.

```console
$ ls
Desktop Documents Downloads Music Pictures Public Templates Videos
```
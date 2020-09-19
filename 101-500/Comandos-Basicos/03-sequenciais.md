# Comandos sequênciais

É possivel executar comandos de forma sequencial no shell utilizando alguns operadores.

## Operadores

### ;

Executa os comandos em sequência, não importando se algum retornou erro.

```console
$ cd Desktop/ ; ls ; clear
```

### &&

Executa o primeiro comando, caso tenha sucesso, executa o próximo.

```console
$ ls /tmp/teste && echo Linux
ls: cannot acess '/tmp/teste': No such file or directory
$ ls && echo Linux
Desktop Documents Downloads Music Pictures Templates Videos
Linux
```
### ||

Executa o comando somente se o primeiro comando não funcionar.

```console
$ ls /tmp/teste || echo Linux
Linux
```

# Histórico

Ao digitarmos comandos no bash eles são gravados no arquivo de histórico, podemos navegar pelo histórico usando as setas para cima e para baixo, consultando o arquivo ou usando o comando history. Cada usuário tem seu próprio arquivo de histórico. O arquivo history é gravado ao final de cada sessão do bash.

### history

Mostra os comandos digitados daquela sessão.

### history -c

A flag -c limpa o arquivo de histórico.

### !!

Executa o ultimo comando digitado.

```console
$ echo Linux
Linux
$ !!
echo Linux
Linux
```

### !<numero_do_comando>

Os comandos do arquivo de histórico tem um número proprio, então podemos
utilizar o !&lt;numero&gt; para executá-lo novamente.

```console
$ !14
$ echo Linux
Linux
```

### !<string>

Utilizando o ! desta maneira, ele irá buscar no arquivo de histórico o último comando que a string passada foi usada e executa-lo novamente.

```console
$ !ls
$ ls && echo Linux
Desktop Documents Downloads Music Pictures Templates Videos                         
Linux
```

### CTRL + R

Com essa combinação de teclas é possível pesquisar comandos já digitados que ja estão armazenados no arquivo de histórico.

```console
(revverse-i-search)`clear': cd Desktop/ ; ls ; clear
```

### TAB

Nós podemos autocompletar comandos, arquivos e diretórios utilizando a tecla TAB. Se a tecla tab for pressionada duas vezes ao digitar ele nos mostra as općões que podem ser utilizadas.

```console
$ ls
ls  lsblk   lscpu   lshw    lsipc   lslogins    lsof    lspcmcia    lsusb   lsattr  lsb_release lsdiff  lsinitramfs lslocks lsmod   lspci   lspgot
```

## Comando de ajuda

Praticamente todos os comandos, arquivos de configuração tem um manual de referência que pode ser acessado através do man.

### man

Abre o manual de referência do comando, somente comandos externos, passado como parametro.

```console
$ man ls
```

Para consultar comandos internos é necessario consultar o manual do bash.

```console
$ man bash
```

### man -k "string"

A flag -k traz a referencia de todos os comandos que tem aquele string passada como parametro.

```console
$ man -k "system information"
dumpe2fs (8)         - dump ext2/ext3/ext4 filesystem information
uname (1)            - print system information
```

### info

O info também é um arquivo de informação, porém ele é um pouco mais enxuto.

```console
$ info ls
```

### whatis

Este comando faz uma busca se encontrar retorna a descrição do comando passado por parametro.

```console
$ whatis uname
uname (1)            - print system information
```

### apropos

Este comando faz uma busca baseado na descrição, igual ao man -k.

```console
$ apropos "system information"
dumpe2fs (8)         - dump ext2/ext3/ext4 filesystem information
uname (1)            - print system information
```
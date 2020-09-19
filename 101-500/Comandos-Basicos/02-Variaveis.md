# Variaveis de ambiente

Quando o shell é carregado, uma série de variaveis de ambiente também são carregadas, essas variaveis são utilizadas pelos processos do shell comandos, interfaces graficas, etc.

## Declaração

Variaveis de ambiente declaradas localmente somente são visiveis na sessão do shell que elas foram declaradas, processos já iniciados pelo shell não conseguem acessa-las.

```console
$ NOME_VAR=valor
$ echo $NOME_VAR
valor
```

Para que processos ja iniciados possam ter acesso a essas variaveis é necessario exportá-las.

```console
export NOME_VAR
```

_Somente os processos gerados a partir do shell que a variavel foi exportada podem ter acesso a ela._

---

## Algumas das principais variaveis de ambiente

#### DISPLAY

Indica às aplicações gráficas onde as janelas deverão ser exibidas.

#### HISTFILE

Arquivo do histórico de comandos.

#### HISTFILESIZE

Quantidades de linhas/comandos armazenados suportados no arquivo de histórico.

#### HOME

Indica o diretório home do usuário atual.

#### LOGNAME e USER

Nome do usuário atual.

#### PATH

Diretórios onde o Linux irá procurar por arquivos executaveis.

#### PS1

Aparência do prompt do shell.

#### PWD 

Diretório atual.

#### OLDPWD

Diretório anterior.

#### $$

Mostra o PID do processo atual.

#### $!

Mostra o PID do ultimo processo que foi executado em background.

#### $?

Mostra o exit code do ultimo processo executado.

_Sempre que o exit code for 0 significa que não ocorreu nenhum erro na execução._

#### ~

Contém a home do usuário atual, porém se passarmos outro usuário em seguida recebemos a home do usuário passado como parametro.

```console
$ echo ~
/home/lucas
$ echo ~root
/root
```

---

## Alguns comandos

### cat

Este comando mostra o conteúdo de um arquivo de texto

```console
$ cat arquivo.txt
Linux é top!!!
```

### set

Este comando nos mostra todas as variaveis de ambiente, locais e exportadas, declaradas no shell.

```console
$ set
```

### env

Este comando mostra somente as variaveis de ambiente exportadas e globais.

```console
$ env
```

Também é possivel alterar uma variavel de ambiente somente para a execução de um processo com o comando env.

```console
$ env NOME_VAR="valor trocado" ./script
valor trocado
```

### unset

Este comando remove a declaração de uma variavel de ambiente.

```console
$ unset NOME_VAR
```
# Aplicando filtros a textos e arquivos

## cat

Le um arquivo de texto e exibe na saída padrão.

* `-n`: Mostra as linhas enumeradas.
* `-b`: Mostra as linhas não brancas enumeradas.
* `-s`: Se houver mais de uma linha branca em sequencia exibe somente uma.
* `-A`: Exibe os caracteres especiais.

## tac

Imprime o arquivo de baixo para cima.

## head

Exibe as primeiras linhas do arquivo, por padrão são 5 ou 10 linhas.

* `-n<numero>`: Mostra o numero de linhas que foram passados por parametro do arquivo.
    
    ```console
    $ head -n2 arquivo.txt
    ```

* `-c<numero>`: Mostra os primeiros bytes passados por parametro do arquivo.

    ```console
    $ head -c10 arquivo.txt
    ```

## tail

Exibe as ultimas linhas do arquivo, por padrão 5 ou 10. As flags são as mesmas do comando head.

* `-f`: Le as ultimas linhas do arquivo e aguarda alguma alteração em tempo real.

## less

Mostra o arquivo de forma paginada assim podemos ler arquivos longos e navegar por ele através deste comando.

### Navegação

* Seta cima/baixo e enter: navegam entre as linhas.
* Barra de espaço: muda de página.
* /string: busca pela próxima palavra que foi passada por parametro, podendo continuar a busca
apertando a tecla N para o próximo match ou SHIFT+N para o match anterior.

## wc

Exibe a quantidade de linhas, quantidade de caracteres e a quantidade de bytes respectivamente.

* `-l`: Exibe somente a quantidade de linhas.
* `-w`: Exibe somente a quantidade de palavras.
* `-c`: Exibe somente a quantidade de bytes.

## nl

Igual ao `cat -b`, enumera as linhas de um arquivo desconsiderando as linhas em branco.

## sort

Exibe o arquivo em ordem alfabetica. Linhas em branco, números e letras respectivamente.

* `-r`: Inverte a ordenação.
# Comandos básicos do Linux 5
## tail, tac e wc

### Comando tail
Usado para ver as últimas linhas de um arquivo.
`tail arq1`Mostra as 10 últimas linhas de arq1.
`tail -n 20 arq1` Mostra as 20 últimas linhas de arq1.
`tail -f /var/log/messages` Mostra as 10 últimas linhas dinâmicamente enquanto são geradas.

### Comando tac
Inverso do comando cat: envia os arquivos de texto para a saída padrão, com as linhas em ordem reversa.  
`tac [arquivo]`

### Comando wc (word count)
Exibe contagem de caracteres, palavras e linhas em arquivos.
`wc [opções] [arquivos]`  
`-c` Contagem de caracteres  
`-l` Contagem de linhas  
`-w` Contagem de palavras  
Exemplo:  
`wc -l /etc/group` Mostra o número de grupos do sitema.
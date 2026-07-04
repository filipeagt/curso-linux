# Comandos básicos do Linux 3
## head, sort, combinação de comandos

### head
Mostra as primeiras linhas de um ou mais arquivos.  
`head [opções] arquivo` 

`head arq2` mostra as 10 primeiras linhas de arq2.  
`head -c50` Exibe os primeiros 50 bytes de um arquivo (k para kilobytes, m para megabytes).  
`head -n15 arq2` Mostra as 15 primeiras linhas de arq2.  
`head -n8 /etc/group` Mostra os 8 primeiros grupos

### Combinando head com cut
`cut -d' ' -f2 arq1 | head -n5` Mostra somente os nomes das 5 primeiras frutas do arquivo arq1.

### Comando sort
Organiza os dados de acordo com a nessecidade dos usuários (de acordo com a primeira coluna de caracteres).  
`sort [opções] arq1`  
`sort [opções] arq1 > arq_sorted`  
Opções:  
`-f` Ignora o case  
`-n` Numericamente  
`-r` Ordem reversa  
`cut -c3-5 arq4 | sort > arq5` seleciona as colunas de 3 a 5 do arq4 ordena e cria arq5 com o resultado.
`cut -d' ' -f2 arq1 | sort > frutas` Cria um arquivo chamado frutas contendo apenas os nomes das frutas do arq1, em ordem alfabética.
`sort -n arq1` ordena de forma numérica, sem -n alfabética.
# Comandos básicos do Linux 06
## uniq (eliminar linhas repetidas adjacentes)

### Comando uniq
Escreve em stdout uma entrada, eliminando linhas duplicadas adjacentes.  
Para eliminar linhas duplicada não adjacentes, primeiro organize o arquivo com `sort`.  
`uniq [opções] [entrad[saída]]`  
`-d` Processa apenas as linhas que se repetem.  
`-u` Processa apenas as linhas que não se repetem.  
`uniq arquivo`  
`uniq -d arquivo`  
`iniq -u arquivo`  
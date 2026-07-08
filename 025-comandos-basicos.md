# Comados básicos do Linux 08
## mv (mover arquivos), cp e rm (outras opções)

### Mais exemplos do comando cp
`cp /home/filipe/arq2 .` Copia o arquivo arq2 do diretório /home/filipe para o diretório atual.  
`cp /root/a* /home` Copia todos os arquivos que se iniciam com a letra **a** do diretório /root para o diretório /home  

### Comando mv
`mv [opções] origem destino` move o arquivo ou diretório para o destino especificado.  
Opções:  
`-i` Consultra o usuário antes de mover arquivos.  
Exemplo:  
`mv /root/arq1 /home/` Move o arquivo arq1 de /root para /home  

### Comado mv - outros usos
`mv /home/fabio/arq1 /home/fabio/arq2` Renomeia o arquivo arq1 para arq2. Para isso, deve-se mover o arquivo de um diretório para o próprio diretório onde ele se encontra, trocando o nome do arquivo no final do comando.
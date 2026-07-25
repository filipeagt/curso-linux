# Redirecionamentos e pipes no Linux 01
## stdin, stdout, stderr

### Arquivos de Dispositivos  

Tudo são arquivos  
Mapeado para o sistema de arquivos  
Os dispositiovs podem ser acessados por meio de mapeamentos denominados arquivos de Dispositivos.  
Ex.: /dev/sda  
Um Arquivo de Dispositivo é um objeto do sistema que oferece uma interface para o dispositivo em si.  
O Kernel associa os drivers de dispositivos aos arquivos de dispositivos.  

### Descritores de Arquivos
Abstração de uma identificação para acessar um arquivo.  
Três descritores:  
Entrada Padrão (stdin)  
Saída padrão (stdout)  
Erro Padrão (stderr)  

### Entrada Padrão
Stream (fluxo) para entrada de texto. Vinculada ao teclado.  
Descritor de Arquivos 0.  

### Saída Padrão
Stream para saída normal dos programas. Vinculada ao terminal ou em uma janela de terminal.  
Descritor de Arquivos 1.  

### Erro Padrão
Stream de sáida de texto, usado para exibir mensagens de erro. Vinculada ao terminal.  
Descritor de Arquivos 2.  

### Pipes
| - Permite juntar dois ou mais comandos.  
`ls -l | less`  
Se forem usados mais de dois comandos com redirecionamentos, damos o nome de pipeline a operação resultante.  
`ls /etc | sort -r | less`  

### Redirecionamentos
Operador de redirecionamento >  
`ls -i > inodes.txt`  

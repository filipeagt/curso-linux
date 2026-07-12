# Comandos básicos do Linux 09
## mkdir, rmdir, rm -r, Manipulação de diretórios

### Comando mkdir
Criar um ou mais diretórios  
`mkdir [opções] nome_diretórios`  
Opções:  
`-m modo` Define direitos de acesso no modo octal.  
`-p` Cria subdiretórios recursivamente.  

### Comando rmdir
Remover um diretório (tem que estar vazio)  
`rmdir nome_diretório`  

### Comando rm
Este comando pode ser usado para excluir tanto arquivos quanto diretórios.  
`rm [opções] arquivo_diretório`  

Para excluir um diretório ocupado:  
`rm -r nome_diretório`  

### Comando rm -Rf /
Este comando remove recursivamente todos os arquivos e diretório do seu sistema Linux até a raiz. Nuca execute!
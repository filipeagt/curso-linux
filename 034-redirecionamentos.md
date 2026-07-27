# Redirecionamentos e pipes 02

As sáidas redirecionadas para um arquivo não são exibidas na sáida padrão (terminal), exceto os erros padrão.  
O operdor `>` cria arquivos; para não sobrescrever o conteúdo de um arquivo já existente, use o operador `>>`  

`cat < /etc/group > /tmp/grupos`  

`ls -zz 2> erro.txt`

## Comando tee
Permite enviar a saída de um comando para um arquivo e para a tela ao mesmo tempo.  

Sintaxe:  
`tee [opções] arquivos`  
`-a` Anexa aos arquivos, em vez de sobrescrevê-los.  

Exemplo:  
`ls -l | tee arquivo1`  

Exemplo 2:  
`ls -i | tee arquivo1 | less`  
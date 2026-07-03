# Comandos básicos do Linux 02
## touch, cut, timestamp

### touch
- Permite alterar o registro de data e hora de modificação e acesso de um arquivo; Cria um arquivo de texto vazio se utilizado sem opções.
- Sintaxe: `touch [opções] nome arquivo <enter>`  
-a Altera a hora de cesso  
-m Altera a hora de modificação  
-t YYYYMMDDhhmmss - Configura a hora digitada  
Ex.: touch -m -t 201012211400 arquivo

### cut
- "Cortar" campos ou colunas selecionados de cada linha de um arquivo; Imprime colunas ou campos delimitados por espaços ou outros caracteres especificados pelo usuário.  
`cut [opções] arquivo` 
- Opções:  
`-c` Posição de caractere ou coluna  
`-f[n]` Campos  
`-d[d]` Delimitador  
- Exemplos:  
`cut -c1-6 arq1` Imprime as colunas de 1 a 6.
`cut -c4,8 arq1` Imprime colunas 4 e 8. 
`cut -d: -f3 arq1` Imprime o campo 3 usando o caractere : comodelimitador. Para usar o espaço como delimitador use ' ' (espaço entre aspas simples).  
`cut -d: -f1 /etc/passwd` Lista os usuários do sistema.  
`cut -d: -f1,6 /etc/passwd` Lista os usuários e seus diretórios padrão.
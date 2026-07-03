# Comandos básicos do Linux 01
## bash, ls, cd, pwd, encadeamento, clear

### bash
Shel padrão Debian, Bourne-again shell

Sintaxe básica em quatro partes:  
|comando|-opção|argumento|enter|
|-------|------|---------|-----|
|ls     |-l    |/home    |\<enter\>|

### ls
Pode ser usado sem opções ou argumentos para mostrar o conteúdo da pasta atual. Se utilizado com a opção -l mostra detalhes dos arquivos e diretórios, com a opção -a exibe arquivos ocultos, -i mostra o inode do arquivo, -o formato longo sem coluna de grupo, -r lista reversa. As opções podem ser combinadas.

### clear
Limpa a tela.

### pwd 
Mostra o caminho do diretório atual.

### cd
Muda de diretório. Sintaxe: `cd [caminho]` se utilizar ~ como argumento, muda para diretŕio do usuário atual, - muda diretório anterior, .. diretório pai.

### encadeamento
Para encadear comandos utiliza-se `;` como separador. Exemplo: `cd /home; ls -l`



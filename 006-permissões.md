# Permissões de acesso para arquivos e pastas

- Atalho 'ctrl + alt + t' abre terminal.
- O comando `ls -l` mostra as permissões.

    |Permissões|Links|Proprietário|Grupo |Tamanho|Data e Hora |Nome   |
    | -------- | --- | ---------- | ---- | ----- | ---------- | ----- |
    |drwxrwxr-x| 14  |filipe      |filipe|4096   |mar  2 19:35|Arduino|

- Primeiro caractere:
    - d = diretório
    - &minus; = arquivo comum de usuário
    - c = arquivo de caractere
    - b = arquivo de bloco
    - l = link

- Demais caracteres

    |Proprietário|Grupo|Outros|
    | ---------- | --- | ---- |
    |rwx         |rwx  |r-x   |

    - r = Read (Leitura)
    - w = Write (Escrita)
    - x = Execution (Execução ou abrir diretório)
    - &minus; = Sem permissão
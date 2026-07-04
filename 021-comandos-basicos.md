# Comandos básicos do Linux 4
## split (dividir arquivos), cat (concatenação)

### Comando split
Divide um arquivo em várias partes em uma sucessão de arquivos com final aa, ab, ac, etc..  
`split [opções] arq_entrada arq_saídaX`  
Opções:  
`--lines=n`, `-l=n` n linhas por arquivo  
`--bytes=n`, `-b=n` n bytes por arquivo

### Exemplo do comando split
`split -b 120 arq.conf arq-` Divide o arquivo arq.conf em várias partes com 120 bytes cada, com os nomes arq-aa, arq-ab, arq-ac, etc...
Para unir novamente as partes use o comando cat: `cat arq-aa arq-ab arq-ac > arq.conf`

### Comando split na prática
    cp /etc/passwd /home/filipe
    cd /home/filipe
    ls
    split -b 200 passwd pass-
    ls -l
---
    cat pass-* > passwd-2
    ls
    cat passwd-2


# Gerenciamento de usuários egrupos 01
## Arquivo /etc/passwd

### Arquivos de cinfiguração  
/etc/passwd  
/etc/group  
/etc/shadow  
/etc/gshadow  

### /etc/passwd
Lista dos usuários do sistema.  
Antigamente -> arquivo de senhas (uso original).  
Legível por qualquer um no sitema.  
Pode ser editado com editores de textos; porém é recomndado que sejam feitas operações com o comando `usermod` (/usr/sbin/usermod).  

    filipe:x:1000:1000:Filipe,,,:/home/filipe:/bin/bash  
       1   2   3    4     5            6          7  

1 - Nome de usuário (1 - 32 caracteres)  
2 - senha (senhas shadow)  
3 - UID (ID do Usuário) (0 - 65535)  
4 - GID (ID do Grupo) (primário)  
5 - Comantários - informações extras sobre o usuário (Nome completo / número do telefone); também conhecido como campo GECOS  
6 - Diretório home (padrão)  
7 - Shell padrão  

usuário root  
root:x:0:0:root:/root:/bin/bash
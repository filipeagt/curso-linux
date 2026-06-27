# Atualizar distribuição Debian

***FAÇA BACKUP DOS SEUS ARQUIVOS ANTES***

- `lsb_release -a`: Mostra a versão atual do sistema.

### Passos para atualização

1. Editar o arquivo *sources.list* para apontar para os repositórios da nova versão.
    Utilize o comando `nano /etc/apt/sources.list` para visualizar o conteúdo do arquivo, ctrl+x para sair.  
    Altere o nome da versão antiga para a nova em todas as ocorrências dela no arquivo, poder ser feito manualmente com o *nano* mas tem um jeito mais fácil com o comando *sed*.  

    `sed -i 's/[versão_antiga]/[versão_nova]/g' /etc/apt/sources.list`

    Podemos abrir novamente com *nano* para verificar se o arquivo foi editado corretamente.

2. Atualizar as listas de pacotes: `apt update`

3. Atulizar os pacotes: `apt upgrade`

4. Atualização da Distribuição: `apt full-upgrade`

5. Reiniciar o sitema: `shutdown -r now`

6. Verificar a versão da Distibuição: `lsb_release -a`

7. Verificar a versão do Kernel: `uname -r`
# Varáveis de ambiente e comandos echo, env e export

- As variáveis de ambiente permitem mudar o shell de várias formas para adptá-lo às nessecidades do usuário.
- Exemplos de varáveis de ambiente:  
    - `PS1`: Prompt da linha de comandos
    - `HOME`: Diretório /home de um usuário
    - `PATH`: Lista de diretórios vasculhados quando um comando é executado.
- Comandos para verificar conteúdo de varáveis de ambiente 
    - `env`: todas as variáveis.
    - `echo $VARIAVEL`: variável específica.
- Adicionar um camoinho à variável PATH: `PATH=$PATH:/novo_caminho`
- Criar uma variável de ambiente: `MINHAVAR=meuconteúdo`  

As variáveis assim criadas possuem escopo local, são válidas apenas no shell atual. Para tornar seu escopo global, exporte-as com o comando `export MINHAVAR`.  

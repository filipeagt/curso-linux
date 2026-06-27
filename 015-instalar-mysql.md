# Instalação do MySql no Debian

`apt install default-mysql-server`: Instala MariaDB na verdade

`/etc/init.d/mariadb restart`: Para e reinicia o "MySql" 

### Arquivos de configuração:  
`vi /etc/mysql/my.cnf`: Esse foi mostrado na aula, para sair pressione Esc, digite `:q!` (descarta alterações) e Enter.  
O MariaDB por padrão pode ser acessado diretamente no terminal apenas pelo usuário root do sistema, não precisa de senha. Para permitir acesso externo altere o IP de `bind-address = 0.0.0.0` no arquivo de configuração com `nano /etc/mysql/mariadb.conf.d/50-server.cnf` e reinicie o MariaDB.
Use o comando `CREATE USER 'novo_usuario'@'%' IDENTIFIED BY 'sua_senha_forte';` para criar um novo usuário. Altere as permissões:
`GRANT ALL PRIVILEGES ON nome_do_banco.* TO 'novo_usuario'@'%'; FLUSH PRIVILEGES;`  

### Comandos SQL utilizados na aula:

    CREATE DATABASE teste;
    SHOW DATABASES;
    USE teste;
    CREATE TABLE tbl_teste (id SMALLINT, nome VARCHAR(30));  
    INSERT INTO tabela (id, nome) VALUES (100, 'Filipe');
    SELECT * FROM tabela;
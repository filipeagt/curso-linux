# ldd, ldconfig, ld.so

**Gerenciamento de bibliotecas compartilhadas no Linux**

- `ldd`: Exibe as **bibliotecas compartilhadas** requeridas por cada um dos programas listados na sua linha de comando, trazendo o nome da biblioteca e local  onde se espera encontrá-la.

    - `ldd [programas]`: Imprime a dependências de bibliotecas compartilhadas.
    - `ldd --version`: Mostra a versão do ldd.
    - `ldd -v [programa]`: Modo verboso para o pprograma especificado.  

    `ldd -v /bin/ls`  

- Vinculando as bibliotecas compartilhadas: `ld.so`

    - Os programas executavei dinamicamente vinculados são examinados, no momento da execução, pelo vinculador dinâmico de objetos compartilhados `ld.so`.
    - Ele procura por ***dependências*** no executável que está sendo carregado e tenta satisfazer vínculos a bibliotecas compartilhadas de sistema que não estejam resolvidos. Se ele não encontrar uma biblioteca, o programa não poderá rodar.
    - `ld.so` pode procurar pelos diretórios que contém bibliotecas na variável `LD_LIBRARY_PATH` ou as bibliotecas são procuradas em um índice de nomes e localizações de bibliotecas (binário) chamado `/etc/ld.so.cache`.
    - Adicionar novas entradas ao cache: adicione o diretório que contém as bibliotecas ao arquivo `/etc/ld.so.conf` e atualize o cache com o comando `ldconfig`.  
      
    `cat /etc/ld.so.conf`  

- `ldconfig`: Configura ligações em tempo de execução do ligador dinâmico `ld.so`.

    - Cria links e cache necessários para as bibliotecas compartilhadas mais recentes encontradas nos diretórios especificados na CLI, no arquivo `/etc/ld.so.conf` e nos diretórios `/lib` e `/usr/lib`.
    - **Deve ser executado após a instalação de uma nova biblioteca compartilhada.**
    - `ldconfig -p`: Examina o conteúdo do cache de bibliotecas ld.so.cache.
    - `ldconfig`: Reconstrói o cache incluindo as atualizações realizadas em /etc/ld.so.conf.

- Variável de ambiente `LD_LIBRARY_PATH`

    - Contém uma lista de diretórios separadas por **:** onde o sistema irá procurar por determinada biblioteca dinâmica `*.so`.
    - Quando um programa precisa de uma biblioteca, o sistema procura nos diretórios listados em `LD_LIBRARY_PATH`, depois no arquivo de cache `/etc/ld.so.cache` e então nos diretórios `/lib` e `/usr/lib`.
    - Para visualizar o conteúdo da variável de ambiente LD_LIBRARY_PATH, use o seguinte comando: `echo $LD_LIBRARY_PATH`.

- `/etc/ld.so.conf`: Arquivo que contém uma lista de diretórios nos quais pode se procurar por bibliotecas; configurável pelo usuário.

- `/etc/ld.so.cache`: Arquivo que contém uma lista ordenada de bibliotecas encontradas nos diretórios especificados em /etc/ld.so.conf. Não é legível por humanos e não deve ser editado, pois é binário.

#### Outros comandos utilizados na aula 

- `cat`: Visualizar conteúdo de arqivos de texto.
- `echo`: Exibe mensagens, imprime valores de variáveis e direciona texto para arquivos.
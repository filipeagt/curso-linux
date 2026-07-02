# init, runlevels, init.d, inittab e telinit - Debian

**Inicialização do Sistema**
- Ao se iniciar o Linux, são usados diversos scripts presentes no diretório /etc para configurar o sistema e mudar um nível de execução a outro.
- Esse processo varia um pouco entre as distribuições.

**Processo init**
- Init: Inicialização do controle de processos, criado a partir de um script armazenado em /etc/inittab. (primeiro processo criado)
- PID: 1

**Runlevels - Níveis de execução**
- O conceito de runlevels especifica as diferentes formas pelas quais um sistema pode ser utilizado e controle sob os quais serviços rodarão.
- Os níveis de execução são especificados pelos número inteiros de 0 a 6.
- O processo init é responsável por levar o sistema ao nível de execução padrão.

**Inicialização do sistema - Runlevels**
- 0: Sistema desligado.
- 1, S, s: Modo monousuário.
- 2: Multiusuário; Padrão no Debian.
- 3: Multiusuário. Padrão no Red Hat, sem GUI.
- 4: Não usado.
- 5: Multiusuário completo com login gráfico (Red Hat)
- 6: Reinicialização do sitema.

**/etc/init.d**
- Diretório que comtém scripts de inicialização/encerramento para cada serviço do sistema.
- Exemplo: /etc/init.d/sshd
- Esses scripts aceitam argumentos como start, stop, restart, status e reload.
- Esses scripts não são executados diretamente pelo processo init. Em vez disso, os diretórios /etc/rc0.d a /etc/rc6.d possuem links simbólicos para esses scripts.

**/etc/rc0.d a /etc/rc6.d**
- Os links são nomeados nos formatos KNNnome e SNNnome
- K = Kill ("finalizar") Serviços que não deverão rodar no runlevel; Executados primeiro.
- S = Start ("Iniciar") Serviços que deverão rodar no runlevel.
- NN = Número de sequência (ordem de execução dos scripts).
- Nome = Identificação dos scripts.

**Nível de execução padrão**
- Podia ser configurado no arquivo: /etc/inittab Mas em sistemas Debian modernos, o arquivo /etc/inittab e o antigo sistema SysVinit foram substituídos pelo gerenciador de serviços systemd. A inicialização e o gerenciamento do sistema são agora configurados através de alvos (targets) em vez de runlevels tradicionais.Para gerenciar sua inicialização, utilize o comando `systemctl`.  
- Em sistemas antigos, o nível de execução padrão podia ser alterado substituindo o número presente na linha junto da palavra initdefault, exemplo: `id:2:initdefault`

**Comando telinit**
- Use o comando `telinit[nº_runlevel]` para mudar o runlevel em tempo de execução. Exemplo `telinit 0` desliga o sistema.

**Mais opções**
- `init [num]`: Muda runlevel
- `telinit q`: Aplicava mudanças realizadas em /etc/inittab
- `runlevel`: Mostra o runlevel prévio e o atual.

**Outros comandos utilizados na aula**  
`ls /etc/rc* | less`  
`head /etc/inittab`
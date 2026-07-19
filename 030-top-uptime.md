# Comandos to e uptime
## Monitoramento e performance de sistemas Linux

### Comando top
Fornece uma visão em tempo real do sistema em execução.  
`top [opções]`  

`-d atraso` Especifica o atraso em segundos entre as atualizações de tela. O padrão é 5 segundos.  
`-i` Ignora processos ociosos.  
`-n num` Exibe num iterações e depois termina.  
`-b` Roda em modo batch. Útil para mandar a saída de top para outros programas ou um arquivo.  

### Comando top - opções interativas (sem parâmetros)
`h` Gera uma tela de ajuda  
`k` Termina um processo (será pedido seu PID)  
`q` Sai do programa
`r` Modifica a prioridade de um processo (renice); Serão pedidos seu PID e valor nice (valores positivos tem menor prioridade)  
`s` Modifica o atraso em segundos entre as atualizações. Será pedido o tempo em segundos. 

### Descrição dos campos de top
`PID` o PID de cada processo  
`USER` Usuário proprietário do processo  
`PR` Prioridade da tarefa  
`NI` Valor NICE da tarefa  
`VIRT` Memória virtual usada peo processo  
`RES` Memória física usada pelo processo  
`SHR` Memória compartilhada usada pelo processo  
`S` Estado da tarefa (S = sleeping, R = running, T = stopped, Z = zombie, etc)  
`%CPU` % de tempo de CPU usada pelatarefa  
`%MEM` % de memória física usada pelo processo  
`TIME+` Tempo total de atividade da tarefa desde que ela foi iniciada  
`COMMAND` Nome do processo  

### Comando uptime
Mostra o tempo atual, a quanto tempo o sistema está rodando, quantos usuários estão logados atualmente e as médias de carga do sistema nos últimos 1, 5, e 15 minutos.  
`uptime` 

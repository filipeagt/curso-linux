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

### Descrição dos comandos de top

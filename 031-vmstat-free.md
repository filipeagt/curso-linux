# Comandos vmstat e free
## Monitoramento e performance do sistema Linux 02

### Comando vmstat
Este comando reporta informações sobre processos, memória, paginação, blocos de I/O, *traps* e atividade de *CPU*.  
Sintaxe:  
`vmstat [opções]`  

`-S M` Usa a unidade *MB* em vez do padrão *KB*  
`-a` Mostrar memória ativa e inativa  
`-d` Mostrar estatísticas de discos  
`-p partição` Mostra informações de R/W na partição especificada  
`-s` Mostra estatísticas em formato de tabela   

### Comado vmstat - campos
1. **procs**  
`r`: Nº de processos esperando par rodar  
`b`: Nº  de processos em dormência initerrupta  

2. **memory**  
`swpd`: Memória virtual usada  
`free`: Memória livre  
`buff`: Memória usada como buffer  
`cache`: Memória usada com cache  

3. **swap**  
`si`: Memória trocada a partir do disco  
`so`: Memória trocada para o disco  

4. **io**  
`bi`: Blocos recebidos de um dispositivo de blocos (blocos/s)  
`bo`: Blocoxs enviados a um dispositivo de blocos (blocos/s)  

5. **system**  
`in`: nº de interrupções por segundo, incluindo clock  
`cs`: nº de mudanças de contexto por segundo  

6. **cpu**  
`us`: Tempo gasto rodando código que não pe kernel  
`sy`: Tempo gasto rodando código do kernel  
`id`: Tempo gasto em ociosidade  
`wa`: Tempo gasto esperando por I/O 
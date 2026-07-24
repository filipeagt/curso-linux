# Comandos iostat e dstat
## Monitoramento e performance do sitema linux

### Comando iostat
Mostra informações sobre o uso da CPU e várias estatísticas sobre E/S do sitema.  
Sintaxe:  
`iostat [opções]`  
`-c` Mostra apenas estatísticas da CPU  
`-d` Mostra apenas estatísticas de I/O de disco  
`-p sda` Mostra apenas estisticas para sda  

### Comando dstat
Permite monitoramento e verificar performance do sistema Linux, possindo características dos comando top, vmstat, free, iostat combinadas.  

Intale-o com:  
`apt install dstat`  

Sintaxe:  
`dstat [opções]`  

`dstat n` Permite ajustar o intervalo de atualização para n segundos  
`-m` Estatísticas de uso de memória  
`-c` Estatísticas de CPU  
`-d` Estatísticas de disco  
`-i` Interrupções  
`-n` Estatísticas de uso de rede  
`--fs` Estatísticas do sitema de arquivos  
`--ntp` Mostra a hora a partir de um servidor NTP  

### gnome-system-monitor
Ferramenta gráfica que pode ser usada para monitorar processos e desempenho do sistema  

`apt install gnome-system-monitor`  
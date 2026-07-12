# Como criar array RAID por software no Linux
## Comando mdadm

### RAID - Redundant Array of Independent Disks
RAID 0 - Striping  
RAID 1 - Mirroring  

Comando mdadm - administrar conjuntos de multi-dispositivos  

`apt install mdadm`  

### Sintáxe básica do mdadm
`mdadm [modo] [nome_array] [opções] [componentes_do_array]`  
`fdisk -l` Listagem dos discos do sistema.  

Discos usados no exemplo:  
/dev/sdb  
/dev/sdc  

1. Criar partições nos discos  
fdisk /dev/sdb  
fdisk /dev/sdc 
Tipo de partição: fd (detecção automática de RAID Linux)  

2. Criar o array RAID:  
`mdadm --create /dev/md0 --verbose --level=1 --raid-devices=2 /dev/sdb1 /dev/sdc1`  
`cat /proc/mdstat` Verificar o status do array.  
`mdadm --detail /dev/md0`  Mostra informações detalhadas.  

3. Adicionar o array ao arquivo de configuração do mdadm: /etc/mdadm/mdadm.conf  
`mdadm -Es | grep md >> /etc/mdadm/mdadm.conf`  

4. Formatar o array:  
`mkfs.ext4 /dev/md0`  

5. Montar o array:  
/raid  
`mount -t ext4 /dev/md0 /raid`  
6. Verificar o ponto de montagem  
`df -h`   

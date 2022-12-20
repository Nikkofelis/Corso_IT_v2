# Introduzione

- **Shell**: interfaccia utente, sia grafica (Graphic User Interface, GUI) che a linea di comando (CLI)
- **Kernel**: micro linguaggio per la comunicazione tra hardware e software

# Configurazione

## Switch Configuration

1. Attach the PC through the console cable (RS 232 - Console) -> Switch
2. `switch> enable`: activate privileged EXEC
3. `switch# configure terminal`: activate global configuration
4. `switch(config)# hostname WORD`: name device
5. `switch(config)# banner motd CHAR BANNER CHAR`: set banner
6. `switch(config)# enable secret PASSWORD`: set encrypted password for privileged EXEC
7. `switch(config)# service password-encryption`: encrypt past and future passwords
8. `switch(config)# line console 0`: enter console configuration
9. `switch(config-line)# password PASSWORD`: set password for console connection
10. `switch(config-line)# login`: abilitate password request for console link
11. `switch(config-line)# exit`: return to global configuration
12. `switch(config)# line vty 0 15`: enter virtual terminal configuration
13. `switch(config-line)# password PASSWORD`: set password for vty connection
14. `switch(config-line)# login`: abilitate password request for vty link
15. `switch(config-line)# exit`: return to global configuration
16. `switch(config)# interface vlan 1`: enter virtual interface configuration
17. `switch(config-if)# ip address ADDRESS MASK`: set the IP address and subnet mask
18. `switch(config-if)# no shutdown`: enable the virtual interface
19. `switch(config-if)# exit`: return to global configuration
20. `switch(config)# ip default-gateway ADDRESS`: set the default gateway
21. `switch(config)# ip defaul-name`: enable DNS
22. `switch(config)# exit`: return to privileged EXEC
23. `switch# show running-config`: display the running configuration
24. `switch# copy running-config startup-config`: save the running configuration file

### Configuration Script

```terminal
enable
configure terminal
hostname NAME
banner motd BANNER
enable secret PASSWORD
service password-encryption
line console 0
password PASSWORD
login
exit
line vty 0 15
password PASSWORD
login
exit
interface vlan 1
ip address ADDRESS MASK
no shutdown
exit
ip default-gateway ADDRESS
exit
exit
show running-config
```

```ad-warning
Ricorda di assegnare un IP anche al PC
```  

## Router Configuration

Diversamente dallo Switch, nel Router la running-config va configurato manualmente.

1. Attach the PC through the console cable (RS 232 - Console) -> Switch
2. `router> enable`: activate privileged EXEC
3. `router# configure terminal`: activate global configuration
4. `router(config)# hostname WORD`: name device
5. `router(config)# banner motd CHAR BANNER CHAR`: set banner
6. `router(config)# enable secret PASSWORD`: set encrypted password for privileged EXEC
7. `router(config)# service password-encryption`: encrypt past and future passwords
8. `router(config)# line console 0`: enter console configuration
9. `router(config-line)# password PASSWORD`: set password for console connection
10. `router(config-line)# login`: abilitate password request for console link
11. `router(config-line)# exit`: return to global configuration
12. `router(config)# line vty 0 15`: enter virtual terminal configuration
13. `router(config-line)# password PASSWORD`: set password for vty connection
14. `router(config-line)# login`: abilitate password request for vty link
15. `router(config-line)# exit`: return to global configuration
16. `router(config)# interface gigabitEthernet 0/0`: enter physical interface configuration
17.  `router(config-if)# ip address ADDRESS MASK`: assign an IPv4 to the interface, repeat for every other port
18. `router(config-if)# no shutdown`: enable the physical interface
19. `router(config-if)# exit`: return to global configuration
20. `router(config)# exit`: return to privileged EXEC
21. `router# show running-config`: display the running configuration
22. `router# copy running-config startup-config`: save the running configuration file

```ad-warning
Per il Router, la singola porta ha un IP, non il dispositivo in sé
```

### Configuration Scripts

#### IPv4

```terminal
enable
configure terminal
hostname NAME
banner motd BANNER
enable secret PASSWORD
service password-encryption
line console 0
password PASSWORD
login
exit
line vty 0 15
password PASSWORD
login
exit
interface g 0/0
ip address ADDRESS MASK
no shutdown
exit
exit
show running-config
```

#### IPv6

```terminal
enable
configure terminal
hostname NAME
banner motd BANNER
enable secret PASSWORD
service password-encryption
line console 0
password PASSWORD
login
exit
line vty 0 15
password PASSWORD
login
exit
ipv6 unicast-routing
interface g 0/0
ip address ADDRESS MASK
no shutdown
ipv6 enable
ipv6 address ADDRESS/PREFIX
ipv6 address ADDRESS link-local
exit
exit
show running-config
```

# Note

**Linee virtuali**: virtual teletype (vty), permettono la configurazione da remoto.

Inserire `no` davanti alle linee di comando cancella la configurazione di quel comando

**interfaccia**: collegamento logico anche a lunga distanza (Router)
**porta**: collegamento fisico, usato per link a breve distanza (Switch)

Cambiando i parametri di speed e duplex vanno cambiati su entrambi i dispositivi connessi ad un cavo.

# [Lista di Comandi per Terminal Switch](Lista%20di%20Comandi%20per%20Terminal%20Switch.md)

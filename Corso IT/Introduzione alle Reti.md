# Tipi di Rete

**LAN**: Rete locale (Local Area Network)
**WAN**: Rete ampia (Wide Area Network)
**Internet**: Interconnessione tra LAN e WAN

**Client-server**: gerarchia tra client e server, i server fornisce solo risposte, i client solo domande.
**Peer-to-peer**: una rete di dispositivi che fungono sia da client che da server a seconda del bisogno che condividono accesso a dispositivi e informazioni.

# Componenti di una Rete

**End device**: mittenti e destinatari in una rete. Vengono chiamati anche host se dispongono di un IP (Internet Protocol). Si dividono in:

- **Client**: dispongono di software per la richiesta e la visualizzazione delle informazioni.
- **Server**: mettono a disposizione le informazioni richieste dal client.

**Intermediate device**: permettono la comunicazione tra mittente e destinatario. Fungono da ripetitori in connessioni WAN.

- **[Switch](Switch%20and%20Router%20Configuration.md)**: struttura che collega device attraverso cavi
- **Access point**: struttura che collega i device da switch e wireless
- **Modem**: collegamento e comunicazione tra WAN e LAN

# [Metodi di connessione](Physical%20Layer.md)

- [Cavo di rame](Copper%20Cabling.md)
- [Cavo di fibra](Fibre%20Cabling.md)
- [Wireless](Wireless%20Media.md)

# Diagrammi Topologici

Devices are connected though different methods:

- **Network Interface Card (NIC)** - A NIC physically connects the end device to the network.
- **Physical Port** - A connector or outlet on a networking device where the media connects to an end device or another networking device.
- **Interface** - Specialized ports on a networking device that connect to individual networks. Because routers connect networks, the ports on a router are referred to as network interfaces.

```ad-abstract
title: Diagrammi Fisici

I diagrammi di topologia fisica illustrano la posizione fisica dei dispositivi intermedi e l'installazione dei cavi. È possibile vedere che le stanze in cui si trovano questi dispositivi sono etichettate in questa topologia fisica.
```

```ad-abstract
title: Diagrammi Logici

I diagrammi della topologia logica illustrano i dispositivi, le porte e lo schema di indirizzamento della rete. Puoi vedere quali dispositivi finali sono collegati a quali dispositivi intermedi e quali supporti vengono utilizzati.
```

# Network Size

## Internet Domestico o Piccole Aziende

- **Cellulare**: L'accesso a internet tramite cellulare utilizza una rete del telefono cellulare per la connessione. Ovunque sia possibile ottenere un segnale cellulare, è possibile ottenere l'accesso a internet tramite cellulare.
- **Satellite**: La disponibilità di accesso a Internet tramite satellite è un vantaggio notevole nelle aree in cui non sarebbe altrimenti disponibile la connettività a internet.
- **Cavo**: Offerto in genere dai provider di servizi di TV via cavo, il segnale di dati Internet viene trasmesso sullo stesso cavo dedicato alla TV via cavo.
- **DSL**: forniscono una connessione a internet a elevata larghezza di banda, sempre attiva. DSL funziona su una linea telefonica.
- **Telefono dial-up**: Un'opzione economica che utilizza qualsiasi linea telefonica e un modem. La bassa larghezza di banda fornita da una connessione modem dial-up non è sufficiente per il trasferimento di dati di grandi dimensioni, sebbene sia utile per l'accesso mobile durante i viaggi.

## Internet Aziendali

- **Linea affittata dedicata** - Le linee dedicate sono circuiti riservati all'interno della rete del provider di servizi, che collegano uffici geograficamente separati per realizzare reti private per dati e/o voce.
- **Metro Ethernet** - Questo a volte è noto come Ethernet WAN. Estendono la tecnologia di accesso LAN alla WAN.
- **DSL aziendale** - La DSL aziendale è disponibile in diversi formati.
- **Satellite** - Il servizio via satellite può fornire una connessione quando non è disponibile una soluzione cablata.

# [Architettura della Rete](Network%20Architecture.md)

- [Tolleranza ai Guasti](Network%20Architecture.md#Tolleranza%20ai%20Guasti)
- [Scalabilità](Network%20Architecture.md#Scalabilità)
- [Quality of Service](Network%20Architecture.md#Quality%20of%20Service)
- [Sicurezza](Network%20Architecture.md#Sicurezza)

# Passaggi

1. Invio richiesta: DNS
	1. Traduzione richiesta server a IP
	2. Default gateway (router) -> analisi richiesta
	3. (modem) -> server DNS che trova l’IP del device che contiene la risposta cercata
	4. Invio della risposta al primo mittente
	5. Il primo mittente invia di nuovo la richiesta al gateway
	6. Il gateway cerca l’IP interessato e comunica la prima richiesta al server ricercato

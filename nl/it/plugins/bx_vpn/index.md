---



copyright:

  years: 2015，2018

lastupdated: "2018-06-21"


---

{:codeblock: .codeblock}
{:shortdesc: .shortdesc}
{:new_window: target="_blank"}

# Plug-in VPN per la CLI {{site.data.keyword.Bluemix_notm}}

*Versione:* 1.4.0

Puoi utilizzare la CLI (command line interface) per configurare e gestire il tuo servizio {{site.data.keyword.vpn_full}}. Il plug-in della CLI VPN è disponibile in due versioni: una da utilizzare con il plug-in della CLI Cloud Foundry e l'altra da utilizzare con il plug-in della CLI {{site.data.keyword.Bluemix}}. Entrambe le versioni del plug-in forniscono la stessa funzionalità.
{:shortdesc}

Il plug-in VPN è disponibile per i sistemi operativi Windows, MAC e Linux. Assicurati di utilizzare il plug-in adatto a te.

Le seguenti istruzioni servono a gestire il plug-in della CLI {{site.data.keyword.Bluemix_notm}}. Per utilizzare il plug-in con il plug-in della CLI Cloud Foundry (cf), vedi [VPN CLI plug-in for cf CLI](../vpn/index.html).


Le informazioni che seguono elencano tutti i comandi supportati dal plug-in VPN per la CLI {{site.data.keyword.Bluemix_notm}} e comprendono i relativi nomi, opzioni, utilizzo, prerequisiti, descrizioni ed esempi. Vedi [Estendi la tua interfaccia riga di comando IBM Cloud](../../index.html#cli_bluemix_ext) per informazioni su come installare il plug-in VPN.

**Nota:** i *Prerequisiti* elencano quali azioni sono richieste prima di utilizzare il comando. I prerequisiti possono includere una o più delle seguenti azioni:
<dl>
<dt>**Endpoint**</dt>
<dd>Un endpoint API deve essere impostato mediante `ibmcloud api` prima di utilizzare il comando.</dd>
<dt>**Accesso**</dt>
<dd>È necessario accedere mediante il comando `ibmcloud login` prima di utilizzare questo comando.</dd>
<dt>**Destinazione**</dt>
<dd>È necessario utilizzare il comando `ibmcloud target` per impostare un'organizzazione e uno spazio prima di utilizzare questo comando.</dd>
</dl>


## ibmcloud vpn connection-create
Crea una connessione VPN.

```
ibmcloud vpn connection-create NOME_CONNESSIONE -g NOME_GATEWAY -k CHIAVE_PRECONDIVISA -subnets "SOTTORETE/MASCHERA" -cip INDIRIZZO_IP_GATEWAY_CLIENTE [-d DESCRIZIONE] [-peer_id ID_PEER] [-admin_state STATO_AMMINISTRAZIONE] [-dpd-action AZIONE] [-gateway_ip INDIRIZZO_IP] [-i STATO_INIZIATORE] [-dpd-timeout VALORE] [-dpd-interval VALORE] [-ike NOME] [-ipsec NOME]
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_CONNESSIONE*  (obbligatorio):  il nome della connessione.

-g *NOME_GATEWAY*  (obbligatorio):  il nome del gateway.

-k *CHIAVE_PRECONDIVISA*  (obbligatorio): la chiave precondivisa.

-subnets "*SOTTORETE*/*MASCHERA*"  (obbligatorio):  l'indirizzo di sottorete remota in formato CIDR.

-cip *INDIRIZZO_IP_GATEWAY_CLIENTE*  (obbligatorio):  l'indirizzo IP dell'endpoint remoto del tunnel VPN.

-d *DESCRIZIONE*  (facoltativo): la descrizione dei parametri specificati.

-peer_id *ID_PEER*  (facoltativo): l'ID del peer remoto. Altro endpoint del tunnel VPN.

-admin_state *STATO_AMMINISTRAZIONE*  (facoltativo): lo stato della connessione VPN. I valori validi sono `UP` o `DOWN`.

-dpd-action *AZIONE*  (facoltativo): l'azione da eseguire quando viene rilevato che il peer è inattivo. I valori validi sono `hold`, `clear`, `disabled`, `restart` o `restart-by-peer`. Il valore predefinito è `hold`.

-gateway_ip *INDIRIZZO_IP*  (facoltativo): l'indirizzo IP dell'endpoint del tunnel VPN locale.

-i *STATO_INIZIATORE*  (facoltativo):  lo stato dell'iniziatore. Il valore predefinito è `bi-directional`.

-dpd-timeout *VALORE*  (facoltativo):  il valore di timeout, espresso in secondi, dopo il quale la sessione viene terminata. Intervallo: 6 - 86400 secondi. Il valore predefinito è `120` secondi.

-dpd-interval *VALORE*  (facoltativo): l'intervallo keepalive, in secondi. Invia dei messaggi keepalive all'intervallo configurato per verificare lo stato di attività del peer. Intervallo: 5-86399 secondi. Il valore predefinito è `15` secondi.

-ike *NOME*  (facoltativo): il nome della politica IKE.

-ipsec *NOME*  (facoltativo): il nome della politica IPSec.

**Esempi**:

Crea una nuova connessione vpn con il nome `my_connection`:
```
ibmcloud vpn connection-create my_connection -g my_gateway -k 123456 -subnets "192.168.10.0/24" -cip 162.135.1.1
```


## ibmcloud vpn ike-create
Crea una politica IKE.

```
ibmcloud vpn ike-create NOME_POLITICA -g NOME_GATEWAY [-d DESCRIZIONE] [-pfs GRUPPO] [-e ALGORITMO_DI_CRITTOGRAFIA] [-lv VALORE_DURATA]
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_POLITICA*  (obbligatorio): il nome della politica IKE.

-g *NOME_GATEWAY*  (obbligatorio):  il nome del gateway.

-d *DESCRIZIONE*  (facoltativo): la descrizione dei parametri specificati.

-pfs *GRUPPO*  (facoltativo): l'identificativo del gruppo DH (Diffie-Hellman). I valori validi sono `Group2`, `Group5` o `Group14`. Il valore predefinito è `Group2`.

-e *ALGORITMO_DI_CRITTOGRAFIA*  (facoltativo): l'algoritmo di crittografia. I valori validi sono `aes-128`, `aes-192`, `aes-256` o `3des`. Il valore predefinito è `aes-128`.

-lv *VALORE_DURATA*  (facoltativo): il valore di durata dell'associazione di sicurezza IKE. Intervallo: 60 - 86400 secondi. Il valore predefinito è `86400` secondi.

**Esempi**:

Crea una nuova politica IKE con il nome `my_ike`:
```
ibmcloud vpn ike-create my_ike -g my_gateway
```


## ibmcloud vpn ipsec-create
Crea una politica IPSec.

```
ibmcloud vpn ipsec-create NOME_POLITICA -g NOME_GATEWAY [-d DESCRIZIONE] [-pfs GRUPPO] [-e ALGORITMO_DI_CRITTOGRAFIA] [-lv VALORE_DURATA]
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_POLITICA*  (obbligatorio): il nome della politica IPSec.

-g *NOME_GATEWAY*  (obbligatorio):  il nome del gateway.

-d *DESCRIZIONE*  (facoltativo): la descrizione dei parametri specificati.

-pfs *GRUPPO*  (facoltativo): l'identificativo del gruppo DH (Diffie-Hellman). I valori validi sono `Group2`, `Group5` o `Group14`. Il valore predefinito è `Group2`.

-e *ALGORITMO_DI_CRITTOGRAFIA*  (facoltativo): l'algoritmo di crittografia. I valori validi sono `aes-128`, `aes-192`, `aes-256` o `3des`. Il valore predefinito è `aes-128`.

-lv *VALORE_DURATA*  (facoltativo): il valore di durata dell'associazione di sicurezza. Intervallo: 60 - 86400 secondi. Il valore predefinito è `3600` secondi.

**Esempi**:

Crea una politica IPSec con il nome `my_policy`:
```
ibmcloud vpn ipsec-create my_policy -g my_gateway
```


## ibmcloud vpn gateway-create
Crea un gateway VPN.

```
ibmcloud vpn gateway-create NOME_GATEWAY -t TIPO [-gateway_ip INDIRIZZO_IP] [-subnets INDIRIZZO_SOTTORETE]
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_GATEWAY* (obbligatorio): il nome del gateway.

-t *TIPO*  (obbligatorio): contenitori per i quali vuoi abilitare il servizio. I valori validi sono `allSingleContainers`, `allContainerGroups` o `allContainers`. Nessun valore predefinito; devi specificare un tipo.

-gateway_ip *INDIRIZZO_IP*  (facoltativo); l'indirizzo IP del gateway.

-subnets *INDIRIZZO_SOTTORETE*  (facoltativo): l'indirizzo di sottorete in formato CIDR.

**Esempi**:

Crea un gateway con il nome `my_gateway` e il tipo `allContainerGroups`:
```
ibmcloud vpn gateway-create my_gateway -t allContainerGroups
```


## ibmcloud vpn connections
Visualizza le informazioni su tutte le connessioni correnti.

```
ibmcloud vpn connections
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione


## ibmcloud vpn ikes
Visualizza le informazioni sulle connessioni IKE correnti.

```
ibmcloud vpn ikes
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione


## ibmcloud vpn ipsecs
Visualizza le informazioni sulle connessioni IPSec correnti.

```
ibmcloud vpn ipsecs
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione


## ibmcloud vpn gateways
Visualizza le informazioni sui gateway correnti.

```
ibmcloud vpn gateways
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione


## ibmcloud vpn connection
Visualizza tutte le informazioni su una specifica connessione.

```
ibmcloud vpn connection NOME_CONNESSIONE
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_CONNESSIONE*  (obbligatorio): il nome della connessione da visualizzare.


## ibmcloud vpn ike
Visualizza le informazioni su una connessione IKE.

```
ibmcloud vpn ike NOME_POLITICA
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_POLITICA* (obbligatorio): il nome della politica IKE da visualizzare.


## ibmcloud vpn ipsec
Visualizza le informazioni su una connessione IPSec.

```
ibmcloud vpn ipsec NOME_POLITICA
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_POLITICA* (obbligatorio): il nome della politica IPSec da visualizzare.


## ibmcloud vpn gateway
Visualizza le informazioni di connessione relative a un gateway.

```
ibmcloud vpn gateway NOME_GATEWAY
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_GATEWAY*  (obbligatorio): il nome del gateway da visualizzare.


## ibmcloud vpn connection-delete
Elimina una connessione esistente.

```
ibmcloud vpn connection-delete NOME_CONNESSIONE
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_CONNESSIONE*  (obbligatorio): il nome della connessione da eliminare.


## ibmcloud vpn ike-delete
Elimina una politica IKE esistente.

```
ibmcloud vpn ike-delete NOME_POLITICA
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_POLITICA* (obbligatorio): il nome della politica IKE da eliminare.


## ibmcloud vpn ipsec-delete
Elimina una politica IPSec esistente.

```
ibmcloud vpn ipsec-delete NOME_POLITICA
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_POLITICA* (obbligatorio): il nome della politica IPSec da eliminare.


## ibmcloud vpn gateway-delete
Elimina un gateway esistente.

```
ibmcloud vpn gateway-delete NOME_GATEWAY
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_GATEWAY*  (obbligatorio): il nome del gateway da eliminare.


## ibmcloud vpn connection-update
Aggiorna una connessione VPN esistente.

```
ibmcloud vpn connection-update NOME_CONNESSIONE [-g NOME_GATEWAY] [-k CHIAVE_PRECONDIVISA] [-subnets "SOTTORETE/MASCHERA"] [-cip INDIRIZZO_IP_GATEWAY_CLIENTE] [-d DESCRIZIONE] [-peer_id ID_PEER] [-admin_state STATO_AMMINISTRAZIONE] [-dpd-action ACTION] [-gateway_ip INDIRIZZO_IP] [-i STATO_INIZIATORE] [-dpd-timeout VALORE] [-dpd-interval VALORE] [-ike NOME] [-ipsec NOME]
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_CONNESSIONE*  (obbligatorio):  il nome della connessione.

-g *NOME_GATEWAY*  (facoltativo):  il nome del gateway.

-k *CHIAVE_PRECONDIVISA*  (facoltativo): la chiave precondivisa.

-subnets "*SOTTORETE*/*MASCHERA*"  (facoltativo):  l'indirizzo di sottorete in formato CIDR.

-cip *INDIRIZZO_IP_GATEWAY_CLIENTE*  (facoltativo):  l'indirizzo IP dell'endpoint remoto del tunnel VPN.

-d *DESCRIZIONE*  (facoltativo): la descrizione dei parametri specificati.

-peer_id *ID_PEER*  (facoltativo): l'ID del peer remoto. Altro endpoint del tunnel VPN.

-admin_state *STATO_AMMINISTRAZIONE*  (facoltativo): lo stato della connessione VPN. I valori validi sono `UP` o `DOWN`.

-dpd-action *AZIONE*  (facoltativo): l'azione da eseguire quando viene rilevato che il peer è inattivo. I valori validi sono `hold`, `clear`, `disabled`, `restart` o `restart-by-peer`.

-gateway_ip *INDIRIZZO_IP*  (facoltativo): l'indirizzo IP dell'endpoint del tunnel VPN locale.

-i *STATO_INIZIATORE*  (facoltativo):  lo stato dell'iniziatore.

-dpd-timeout *VALORE*  (facoltativo):  il valore di timeout, espresso in secondi, dopo il quale la sessione viene terminata. Intervallo: 6 - 86400 secondi.

-dpd-interval *VALORE*  (facoltativo): l'intervallo keepalive, in secondi. Invia dei messaggi keepalive all'intervallo configurato per verificare lo stato di attività del peer. Intervallo: 5-86399 secondi.

-ike *NOME*  (facoltativo): il nome della politica IKE.

-ipsec *NOME*  (facoltativo): il nome della politica IPSec.


## ibmcloud vpn ike-update
Aggiorna una politica IKE.

```
ibmcloud vpn ike-update NOME_POLITICA [-g NOME_GATEWAY] [-d DESCRIZIONE] [-pfs GRUPPO] [-e ALGORITMO_DI_CRITTOGRAFIA] [-lv VALORE_DURATA]
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_POLITICA*  (obbligatorio): il nome della politica IKE.

-g *NOME_GATEWAY*  (facoltativo):  il nome del gateway.

-d *DESCRIZIONE*  (facoltativo): la descrizione dei parametri specificati.

-pfs *GRUPPO*  (facoltativo): l'identificativo del gruppo DH (Diffie-Hellman). I valori validi sono `Group2`, `Group5` o `Group14`.

-e *ALGORITMO_DI_CRITTOGRAFIA*  (facoltativo): l'algoritmo di crittografia. I valori validi sono `aes-128`, `aes-192`, `aes-256` o `3des`.

-lv *VALORE_DURATA*  (facoltativo): il valore di durata dell'associazione di sicurezza IKE. Intervallo: 60 - 86400 secondi.


## ibmcloud vpn ipsec-update
Aggiorna una politica IPSec.

```
ibmcloud vpn ipsec-update NOME_POLITICA [-g NOME_GATEWAY] [-d DESCRIZIONE] [-pfs GRUPPO] [-e ALGORITMO_DI_CRITTOGRAFIA] [-lv VALORE_DURATA]
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_POLITICA*  (obbligatorio): il nome della politica IPSec.

-g *NOME_GATEWAY*  (facoltativo):  il nome del gateway.

-d *DESCRIZIONE*  (facoltativo): la descrizione dei parametri specificati.

-pfs *GRUPPO*  (facoltativo): l'identificativo del gruppo DH (Diffie-Hellman). I valori validi sono `Group2`, `Group5` o `Group14`.

-e *ALGORITMO_DI_CRITTOGRAFIA*  (facoltativo): l'algoritmo di crittografia. I valori validi sono `aes-128`, `aes-192`, `aes-256` o `3des`.

-lv *VALORE_DURATA*  (facoltativo): il valore di durata dell'associazione di sicurezza. Intervallo: 60 - 86400 secondi.


## ibmcloud vpn gateway-update
Aggiorna un gateway VPN esistente.

```
ibmcloud vpn gateway-update NOME_GATEWAY [-t TIPO] [-gateway_ip INDIRIZZO_IP] [-subnets INDIRIZZO_SOTTORETE]
```

**Prerequisiti**:  Endpoint, Accesso, Destinazione

**Opzioni comando**:

*NOME_GATEWAY* (obbligatorio): il nome del gateway.

-t *TIPO*  (facoltativo): contenitori per i quali vuoi abilitare il servizio. I valori validi sono `allSingleContainers`, `allContainerGroups` o `allContainers`.

-gateway_ip *INDIRIZZO_IP*  (facoltativo); l'indirizzo IP del gateway.

-subnets *INDIRIZZO_SOTTORETE*  (facoltativo): l'indirizzo di sottorete in formato CIDR.

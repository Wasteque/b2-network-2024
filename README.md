# b2-network-2024

## I. Basics

☀️ Carte réseau WiFi

Carte réseau sans fil Wi-Fi :

```Suffixe DNS propre à la connexion. . . :
   Description. . . . . . . . . . . . . . : Intel(R) Wi-Fi 6E AX211 160MHz
   Adresse physique . . . . . . . . . . . : 70-D8-23-5E-1B-C2
   DHCP activé. . . . . . . . . . . . . . : Oui
   Configuration automatique activée. . . : Oui
   Adresse IPv6 de liaison locale. . . . .: fe80::bcb3:710f:3811:6eb4%16(préféré)
   Adresse IPv4. . . . . . . . . . . . . .: 10.33.73.75(préféré)
   Masque de sous-réseau. . . . . . . . . : 255.255.240.0 /20
```

☀️ Déso pas déso

```
Adresse de réseau : 10.33.64.0
Adresse de broadcast : 10.33.79.255
Nombre d'adresses IP disponibles : 4094
```

☀️ Hostname

```
PS C:\Users\Wasteque> hostname
DESKTOP-0SI12JN
```

☀️ Passerelle du réseau

 ```
 Passerelle par défaut. . . . . . . . . : 10.33.79.254

7c-5a-1c-d3-d8-76
```

☀️ Serveur DHCP et DNS

```
Adresse IP du serveur DHCP : 10.33.79.254
Adresses IP des serveurs DNS : 8.8.8.8, 1.1.1.1
```

☀️ Table de routage
Déterminer...

```
 0.0.0.0          0.0.0.0     10.33.79.254      10.33.73.75     30
```

## II. Go further

☀️ Hosts ?
```
PS C:\Users\Wasteque> ping b2.hello.vous

Envoi d’une requête 'ping' sur b2.hello.vous [1.1.1.1] avec 32 octets de données :
Réponse de 1.1.1.1 : octets=32 temps=18 ms TTL=55
Réponse de 1.1.1.1 : octets=32 temps=19 ms TTL=55

```

☀️ Go mater une vidéo youtube et déterminer, pendant qu'elle tourne...

```
 [chrome.exe]
  TCP    10.33.73.75:51377      172.65.251.78:443      ESTABLISHED
  ```

  ☀️ Requêtes DNS

```
  S C:\Windows\system32> nslookup www.thinkerview.com
Serveur :   dns.google
Address:  8.8.8.8

Réponse ne faisant pas autorité :
Nom :    www.thinkerview.com
Addresses:  2a06:98c1:3121::7
          2a06:98c1:3120::7
          188.114.96.7
          188.114.97.7



          PS C:\Windows\system32> nslookup 143.90.88.12
Serveur :   dns.google
Address:  8.8.8.8

Nom :    EAOcf-140p12.ppp15.odn.ne.jp
Address:  143.90.88.12
 ```

 ☀️ IP publique

 ```
 195.7.117.146
 ```

 ## III. Le requin
 
 ☀️ Capture ARP

 


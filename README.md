# Tracker analysis

Progetto realizzato per il corso di Gestione di reti. Lo scopo del progetto è analizzare il traffico di una rete per visualizzare i collegamenti ai
domini che effettuano attività di tracking, mostrando statistiche che aiutano a comprendere la portata del fenomeno. Ho scelto la libreria open source di deep packet inspection nDPI, aggiungendo la funzionalità a ndpiReader.

L’argomento -a <nomefile> (o –tracking <nomefile>) accetta in input una lista di domini, uno per riga, che viene utilizzata per il riconoscimento del traffico. Il file script.sh genera una lista adatta allo scopo.

## Esempio di esecuzione
```
./script.sh list
./ndpiReader --tracking list -i eth0
```
Segue il risultato dell’esecuzione durante una visita alla home page del sito d’informazione repubblica.it
```
Tracking and Advertising Stats: 
       accounts.us1.gigya.com                   packets: 26            bytes: 8900          flows: 2             
       ad.doubleclick.net                       packets: 373           bytes: 260894        flows: 2             
       ade.googlesyndication.com                packets: 26            bytes: 7029          flows: 2             
       ads.rubiconproject.com                   packets: 25            bytes: 10006         flows: 2             
       adx.g.doubleclick.net                    packets: 70            bytes: 19088         flows: 2             
       b.scorecardresearch.com                  packets: 24            bytes: 6820          flows: 2             
       beacon-eu-ams3.rubiconproject.com        packets: 4             bytes: 956           flows: 1             
       cdn-gl.imrworldwide.com                  packets: 120           bytes: 69236         flows: 3             
       cdns.gigya.com                           packets: 97            bytes: 67549         flows: 2             
       cdns.us1.gigya.com                       packets: 53            bytes: 29664         flows: 2             
       ds-aksb-a.akamaihd.net                   packets: 25            bytes: 7762          flows: 2             
       geo.moatads.com                          packets: 27            bytes: 7730          flows: 2             
       googleads.g.doubleclick.net              packets: 50            bytes: 13122         flows: 3             
       googleads4.g.doubleclick.net             packets: 44            bytes: 9967          flows: 2             
       gruppoespresso01.webtrekk.net            packets: 19            bytes: 4713          flows: 2             
       gscounters.us1.gigya.com                 packets: 25            bytes: 9452          flows: 2             
       it-gmtdmp.mookie1.com                    packets: 15            bytes: 2650          flows: 2             
       optimized-by.rubiconproject.com          packets: 16            bytes: 4328          flows: 2             
       pagead2.googlesyndication.com            packets: 157           bytes: 87673         flows: 4             
       ping.chartbeat.net                       packets: 19            bytes: 5048          flows: 2             
       px.moatads.com                           packets: 22            bytes: 9068          flows: 2             
       s0.2mdn.net                              packets: 398           bytes: 282981        flows: 4             
       secure-assets.rubiconproject.com         packets: 47            bytes: 27665         flows: 2             
       secure-it.imrworldwide.com               packets: 106           bytes: 25117         flows: 10            
       securepubads.g.doubleclick.net           packets: 206           bytes: 125705        flows: 2             
       static.chartbeat.com                     packets: 35            bytes: 16417         flows: 2             
       tpc.googlesyndication.com                packets: 425           bytes: 283264        flows: 6             
       www.googletagservices.com                packets: 17            bytes: 4221          flows: 2             
       z.moatads.com                            packets: 106           bytes: 72849         flows: 2             
       TOTAL                                    packets: 2577          bytes: 1479874       flows: 75            

Protocols: (tracking flows/total flows) 
       DNS:     10 / 38    26.32% 
       HTTP:     9 / 36    25.00% 
       SSL:     14 / 14    100.00%
```

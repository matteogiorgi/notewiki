# Algoritmi per la gestione di funzioni virtuali di rete
##### FEDERICA PAGANELLI - Friday, 4 March 2022, 09:41


## Contesto

Nelle reti di telecomunicazione tradizionali, i servizi di rete sono forniti da funzioni (es. firewall, NAT, DPI, load balancer, ecc.) che sono eseguite su hardware dedicato alla specifica funzione da eseguire. Un tale approccio però è poco flessibile rispetto ai requisiti emergenti degli operatori di rete, che hanno bisogno di adattare i servizi alla domanda di traffico, contenendo i costi. Nelle reti moderne (reti fisse e mobili 5G e oltre), il paradigma Network Function Virtualization mira a risolvere questo problema sostituendo i dispositivi dedicati con funzioni implementate tramite componenti software che vengono eseguite su server generici usando tecnologie di virtualizzazione (es. VM, container). 

Uno dei problemi chiave nella Network Function Virtualization è il posizionamento delle funzioni virtualizzate (VNF) sui nodi della rete al fine di contenere i costi e rispettare i requisiti di Qualità del Servizio (VNF Placement Problem).


## Obiettivo

Nel dettaglio, il lavoro consiste nell’estendere un lavoro esistente che propone una formulazione basata su Programmazione Lineare Intera del problema di VNF Placement, formulando un approccio di risoluzione più efficiente e scalabile, come un’euristica o una meta-euristica (ad es. algoritmi genetici) . Il lavoro comprenderà infine la valutazione comparativa dell’euristica e del modello esatto già disponibile tramite simulazione.


## Referenti

- Federica Paganelli: `federica.paganelli@unipi.it`
- Antonio Brogi

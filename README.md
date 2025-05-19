
# librerie python open source per la logistica

> panoramica aggiornata al 2025-05-19

Di seguito una rassegna di quindici librerie open source, sviluppate interamente in Python, utili a risolvere diversi problemi di logistica: gestione del magazzino, ottimizzazione del trasporto, allocazione di veicoli, instradamento e consolidamento di imballi.

---

## pulp
**problemi risolti**  
modeling di problemi lineari e misti interi (lp/mip) per allocazione prodotti, dimensionamento magazzini, instradamento veicoli.

**completezza e robustezza**  
libreria matura (coin-or, mit) con sintassi semplice; affida la risoluzione ai solver open‑source (cbc incluso).

**documentazione e community**  
manuale dettagliato, numerosi tutorial; ampia community su coin‑or e stackoverflow.

**prestazioni**  
overhead minimo; performance dipendono dal solver (cbc buono per istanze medio‑piccole).

**licenza:** mit  
**competenze matematiche:** intermedio (programmazione lineare)  
**specificità vs generalità:** generale per qualsiasi problema lp/mip  
**supporto e aggiornamenti:** aggiornamenti occasionali ma costanti  
**scalabilità:** buona fino a qualche migliaio di variabili/vincoli  
**link:** <https://github.com/coin-or/pulp> – <https://coin-or.github.io/pulp/>

---

## pyomo
**problemi risolti**  
modellazione avanzata (lp, mip, nlp, stocastici) per rete logistica, scorte, trasporti multimodali.

**completezza e robustezza**  
supporta vasta gamma di classi di problemi, inclusi non lineari; curva di apprendimento più ripida.

**documentazione e community**  
manuale, libro dedicato, community accademica attiva (sandia labs).

**prestazioni**  
setup modello più lento di pulp; risoluzione demandata ai solver (cbc, glpk, ipopt).

**licenza:** bsd‑3  
**competenze matematiche:** avanzato  
**specificità vs generalità:** molto generale  
**supporto e aggiornamenti:** attivo, rilasci annuali  
**scalabilità:** ottima con tecniche di decomposizione  
**link:** <https://github.com/pyomo/pyomo> – <https://pyomo.readthedocs.io/>

---

## python‑mip
**problemi risolti**  
risoluzione efficiente di problemi mip per vrp, assegnamento e flussi.

**completezza e robustezza**  
interfaccia in stile pulp ma con binding nativi a cbc per maggiore velocità.

**documentazione e community**  
readthedocs + esempi; community coin‑or in crescita.

**prestazioni**  
setup rapido, risoluzione tramite cbc integrato; ottimo per istanze medio‑grandi.

**licenza:** epl‑2  
**competenze matematiche:** intermedio  
**specificità vs generalità:** generale mip  
**supporto e aggiornamenti:** attivo fino al 2024  
**scalabilità:** limitata dal solver ma buona fino a migliaia di variabili  
**link:** <https://github.com/coin-or/python-mip> – <https://python-mip.readthedocs.io/>

---

## networkx
**problemi risolti**  
analisi di reti: cammini minimi, flussi a costo minimo, matching per allocazione veicoli.

**completezza e robustezza**  
ampia collezione di algoritmi su grafi, testata dal 2005.

**documentazione e community**  
doc eccellente e grande community scientifica.

**prestazioni**  
python puro: ok per reti fino a decine di migliaia di nodi.

**licenza:** bsd‑3  
**competenze matematiche:** base‑intermedio (teoria dei grafi)  
**specificità vs generalità:** generale per grafi  
**supporto e aggiornamenti:** molto attivo  
**scalabilità:** buona su reti medio‑grandi  
**link:** <https://github.com/networkx/networkx> – <https://networkx.org>

---

## simpy
**problemi risolti**  
simulazione di processi di magazzino, centri distributivi, flotta veicoli a eventi discreti.

**completezza e robustezza**  
motore semplice basato su generatori; stabile da anni.

**documentazione e community**  
tutorial chiaro; community accademica discreta.

**prestazioni**  
gestisce milioni di eventi; esecuzione veloce senza animazione.

**licenza:** mit  
**competenze matematiche:** base (code, probabilità)  
**specificità vs generalità:** generale per simulazione discreta  
**supporto e aggiornamenti:** maturo, pochi bug  
**scalabilità:** elevata sugli eventi  
**link:** <https://github.com/simpy/simpy> – <https://simpy.readthedocs.io/>

---

## salabim
...
## salabim
**problemi risolti**  
simulazione a eventi discreti con animazione 2d/3d per layout di magazzini e cicli di trasporto.

**completezza e robustezza**  
basato su simpy, aggiunge risorse, queue e monitor con animazione integrata.

**documentazione e community**  
manuale dettagliato; piccola community ma autore molto presente.

**prestazioni**  
veloce senza animazione; animazione opzionale può rallentare ma utile per demo.

**licenza:** mit  
**competenze matematiche:** base  
**specificità vs generalità:** generale ma con focus logistico pratico  
**supporto e aggiornamenti:** aggiornamenti regolari  
**scalabilità:** buona (animazione potrebbe limitare)  
**link:** <https://github.com/salabim/salabim> – <https://www.salabim.org>

---

## openclsim
**problemi risolti**  
simulazione di cicli logistici complessi (carico‑trasporto‑scarico) tipici di operazioni portuali e hub‑and‑spoke.

**completezza e robustezza**  
componenti high‑level su simpy per attività ricorrenti e scheduler a regole.

**documentazione e community**  
readthedocs + esempi; community ristretta accademica (tu delft).

**prestazioni**  
buone grazie a simpy; adatto a scenari what‑if.

**licenza:** mit  
**competenze matematiche:** intermedio (modellazione processi)  
**specificità vs generalità:** molto specifico per cicli ripetitivi  
**supporto e aggiornamenti:** commit periodici fino al 2023  
**scalabilità:** sufficiente per decine di risorse  
**link:** <https://github.com/TUDelft-CITG/OpenCLSim> – <https://openclsim.readthedocs.io>

---

## supplychainpy
**problemi risolti**  
analisi domanda, politiche di scorta, simulazione monte carlo per rischio stock‑out.

**completezza e robustezza**  
moduli per eoq, rop, abc‑xyz, reportistica; progetto 0.x con sviluppo limitato.

**documentazione e community**  
readthedocs con quickstart; community minima.

**prestazioni**  
calcoli statistici leggeri; veloci su dataset piccoli‑medi.

**licenza:** bsd‑3  
**competenze matematiche:** intermedio (statistica base)  
**specificità vs generalità:** specifica per inventory management  
**supporto e aggiornamenti:** poco attivo  
**scalabilità:** buona su centinaia di sku  
**link:** <https://github.com/KevinFasusi/supplychainpy> – <https://supplychainpy.readthedocs.io>

---

## vrpy
**problemi risolti**  
vrp capacitario, con finestre temporali, pickup & delivery via column generation.

**completezza e robustezza**  
algoritmo esatto/euristico basato su networkx+cspy; supporta vari vincoli realistici.

**documentazione e community**  
readthedocs con esempi; community piccola ma reattiva.

**prestazioni**  
ottime per problemi fino a ~100 clienti; esatto per istanze medio‑piccole.

**licenza:** mit  
**competenze matematiche:** intermedio  
**specificità vs generalità:** specializzato su vrp  
**supporto e aggiornamenti:** ultimo rilascio 2021, stabile  
**scalabilità:** limitata oltre alcune centinaia di nodi  
**link:** <https://github.com/Kuifje02/vrpy> – <https://vrpy.readthedocs.io>

---

## verypy
**problemi risolti**  
15 euristiche classiche per cvrp/tsp (clarke‑wright, sweep, tabu, ecc.).

**completezza e robustezza**  
toolbox didattico per confrontare heuristic; implementazioni fedeli alla letteratura.

**documentazione e community**  
documentazione nel readme; community ridotta accademica.

**prestazioni**  
rapide su istanze <200 nodi; python puro può rallentare su 1000+.

**licenza:** mit  
**competenze matematiche:** base‑intermedio  
**specificità vs generalità:** molto focalizzato su cvrp  
**supporto e aggiornamenti:** poco attivo ma stabile  
**scalabilità:** buona su problemi medio‑piccoli  
**link:** <https://github.com/yorak/VeRyPy>

---

## aequilibrae
**problemi risolti**  
assegnazione traffico merci/passeggeri, analisi reti e skimming, modelli gravitazionali.

**completezza e robustezza**  
suite completa per modelling transport planning; include plugin qgis.

**documentazione e community**  
manuali, tutorial, forum google; community professionale attiva.

**prestazioni**  
algoritmi frank‑wolfe e bfw efficienti per reti urbane e regionali.

**licenza:** mit  
**competenze matematiche:** avanzato (equilibrio utenti)  
**specificità vs generalità:** specialistico pianificazione trasporti  
**supporto e aggiornamenti:** molto attivo (release 1.0 nel 2023)  
**scalabilità:** elevata su reti con decine di migliaia di archi  
**link:** <https://github.com/AequilibraE/aequilibrae> – <https://aequilibrae.com>

---

## spopt
**problemi risolti**  
location‑allocation (p‑median, max‑cover) e ottimizzazione spaziale.

**completezza e robustezza**  
integrazione con pysal; usa pulp per risoluzione mip.

**documentazione e community**  
notebook demo, manuale pysal; community gis attiva.

**prestazioni**  
buone su problemi con centinaia di siti; limitate da mip.

**licenza:** bsd‑3  
**competenze matematiche:** intermedio  
**specificità vs generalità:** specializzato in facility location  
**supporto e aggiornamenti:** rilasci regolari  
**scalabilità:** discreta (dipende da solver)  
**link:** <https://github.com/pysal/spopt> – <https://pysal.org/spopt>

---

## rectpack
**problemi risolti**  
bin packing 2d (rettangoli) per consolidamento imballi, taglio piani.

**completezza e robustezza**  
algoritmi skyline, maxrects, guillotine; progetto ancora in alpha.

**documentazione e community**  
doc minima; community quasi assente.

**prestazioni**  
ok per centinaia di rettangoli; python puro.

**licenza:** apache‑2  
**competenze matematiche:** base  
**specificità vs generalità:** specifico packing 2d  
**supporto e aggiornamenti:** sviluppo sporadico  
**scalabilità:** buona su input piccoli‑medi  
**link:** <https://github.com/secnot/rectpack>

---

## py3dbp
**problemi risolti**  
bin packing 3d per pianificazione carico container/pallet.

**completezza e robustezza**  
supporta rotazioni, pesi massimi; euristica deterministica.

**documentazione e community**  
readme con esempi; community ridotta.

**prestazioni**  
veloce su decine‑centinaia di oggetti.

**licenza:** mit  
**competenze matematiche:** base  
**specificità vs generalità:** specifico packing 3d  
**supporto e aggiornamenti:** fermo dal 2018 ma stabile  
**scalabilità:** ok fino a poche centinaia di scatole  
**link:** <https://github.com/enzoruiz/3dbinpacking>

---

## prtpy
**problemi risolti**  
partizionamento e bin packing 1d per bilanciare carichi e minimizzare numero di bin.

**completezza e robustezza**  
algoritmi esatti (ilp) e euristici; progetto coin‑or in forte sviluppo.

**documentazione e community**  
readme + notebook; autore attivo.

**prestazioni**  
euristiche molto veloci; ilp limitato da solver.

**licenza:** mit  
**competenze matematiche:** base‑intermedio  
**specificità vs generalità:** specializzato su packing 1d  
**supporto e aggiornamenti:** aggiornato 2024  
**scalabilità:** ottima con euristiche, limitata ilp  
**link:** <https://github.com/coin-or/prtpy>

---

### tabella comparativa

| libreria        | ambito principale                                    | valutazione (1‑5) |
|-----------------|-------------------------------------------------------|-------------------|
| pulp            | modellazione lp/mip                                   | **5** |
| pyomo           | modellazione avanzata di ottimizzazione               | **4** |
| python‑mip      | risoluzione mip efficiente                            | **4** |
| networkx        | algoritmi su grafi                                    | **5** |
| simpy           | simulazione eventi discreti                           | **5** |
| salabim         | simulazione + animazione                              | **4** |
| openclsim       | simulazione cicli logistici                           | **4** |
| supplychainpy   | analisi domanda e scorte                              | **3** |
| vrpy            | vehicle routing problem                               | **4** |
| verypy          | euristiche classiche cvrp                             | **4** |
| aequilibrae     | assegnazione traffico su rete                         | **5** |
| spopt           | facility location                                     | **4** |
| rectpack        | bin packing 2d                                        | **3** |
| py3dbp          | bin packing 3d                                        | **4** |
| prtpy           | bin packing / partizionamento 1d                      | **3** |


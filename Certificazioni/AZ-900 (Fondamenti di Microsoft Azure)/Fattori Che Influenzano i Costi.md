Più cose contribuiscono a far variare i costi nell’utilizzo delle risorse Azure. Con il Cloud, si passa dalla [[Capital expense (CapEx)]], tipica degli ambienti *on-premises*, alla [[Operational expense (OpEx)]]; è proprio il costo di quest’ultima a essere soggetto a cambiamenti. Di seguito, sono elencati i fattori che determinano il prezzo nell’utilizzo di una risorsa Azure.

## Tipologia di Risorsa

Quando si disloca una risorsa, Azure ne crea istanze a consumo. Contatori appositi ne tengono traccia dell’uso che se ne fa e generano un *record* di utilizzo usato per calcolare poi la bolletta. Le diverse impostazioni di una risorsa contribuiscono anch’esse a farne variare il prezzo di consumo.

## Consumo

[[Pay-as-you-go]] non è la sola modalità di fatturazione disponibile. Azure offre anche la possibilità di impegnarsi a utilizzare in anticipo una determinata quantità di risorse e di ricevere, per questo, sconti su tali risorse riservate. Molti servizi, inclusi *database*, strumenti di calcolo e di archiviazione, offrono la possibilità di impegnarsi su diversi  livelli di utilizzo e di ricevere uno sconto conseguente.

Quando si prenotano risorse, ci si impegna a usare e pagare una determinata quantità di risorse durante un preciso periodo (in genere, **uno** o **tre** anni). Con la sicurezza del *backup* del *pay-as-you-go*, se si nota un improvviso aumento della domanda che soverchia ciò che è stato prenotato in anticipo, si pagheranno solo le risorse aggiuntive in eccesso rispetto alla prenotazione originale. Questo modello consente di godere di risparmi, anche significativi, per carichi di lavoro affidabili e coerenti, sempre con la flessibilità di poter aumentare rapidamente il *footprint* del proprio ambiente Cloud in caso di necessità.

## Manutenzione

La flessibilità del Cloud consente di adattare rapidamente le risorse in base alla domanda. Per controllare i costi, è importante mantenere **ordinato** l’ambiente Cloud e l’uso dei [[Azure Resource Group]] aiuta in questo. Ad esempio, ogni volta che si disloca una [[Virtual Machine]], vengono dislocate anche **risorse aggiuntive**, come quelle per l’archiviazione e la rete. Con il *deprovisioning* della [[Virtual Machine]], è possibile che non venga eseguito anche il *deprovisioning* di tali risorse. Eliminare il [[Azure Resource Group]] contenitore di tutte le risorse ([[Virtual Machine]] e risorse aggiuntive) assicura di sbarazzarsi di tutto in un solo colpo. È importante tenere d’occhio le risorse e assicurarsi di non mantenere quello che non servono più, per controllare i costi del Cloud.

## Geografia

Quando si disloca la maggior parte delle risorse Azure, bisogna definire una [[Azure Region]] su cui distribuirle. L’infrastruttura Azure è presente a livello globale, permettendo così di spargere i servizi dove si vuole. Da questa distribuzione globale, però, derivano differenze di prezzo. Il costo di **energia**, **manodopera**, **tasse** e **commissioni**, infatti, varia a seconda della posizione.

Anche il traffico di rete è influenzato in base all’area geografica. Ad esempio, è meno costoso spostare le informazioni all’interno dell’Europa piuttosto che spostarle dall’Europa all’Asia, o al Sud America.

### Traffico di rete

Le *“billing zones”* sono un fattore nella determinazione del costo di alcuni servizi Azure.

La larghezza di banda si riferisce ai dati che entrano ed escono dai *data center* Azure. Alcuni trasferimenti in ingresso (nei *data center* Azure) sono **gratuiti**. Per i trasferimenti in uscita (dai *data center* Azure), i prezzi di trasferimento si basano su **zone**. Una zona è un raggruppamento geografico di [[Azure Region]] ai fini della fatturazione.

## Tipologia di Sottoscrizione

Alcuni tipi di sottoscrizione Azure includono **quote di utilizzo**. Ad esempio, una sottoscrizione di prova **gratuita** fornisce l’accesso a una serie di prodotti Azure gratuiti per **12 mesi**. Include anche **credito** da spendere entro i primi **30 giorni** dalla registrazione. Con tale sottoscrizione, si accede a più di 25 prodotti **sempre gratuiti** (in base alla disponibilità delle risorse e della [[Azure Region]]).

## Azure Marketplace

Azure Marketplace consente di acquistare soluzioni e servizi basati su Azure da fornitori di **terze parti**. Potrebbe trattarsi di un *server* con *software* preinstallato e configurato, dispositivi *firewall* di rete gestiti o connettori per servizi di *backup* di terze parti. Quando si comprano prodotti tramite Azure Marketplace, si potrebbe pagare non solo per i servizi Azure che si stanno usando, ma anche per i servizi o le competenze del fornitore di terze parti. Le “strutture” di fatturazione sono stabilite dal fornitore.

Tutte le soluzioni disponibili in Azure Marketplace sono **certificate** e **conformi** ai criteri e agli *standard* Azure. I criteri di certificazione possono variare in base al tipo di servizio o soluzione e al servizio Azure interessato.
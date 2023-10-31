Strumento di monitoraggio per:

1. Gestire la propria “posizione di sicurezza” e la protezione dalle minacce.
2. Rafforzare le risorse.
3. Semplificare la gestione della sicurezza.

Esso monitora ambienti *cloud*, *on-premise*, ibridi e *multicloud* così da fornire indicazioni e notifiche al fine di rafforzare il livello di sicurezza. *Deployare* Defender for Cloud è semplice; esso è già integrato in Azure, quindi molti servizi Azure sono monitorati e protetti nativamente. Tuttavia, se si dispone anche di un *data center* locale o si opera anche in un altro ambiente Cloud, controllare solo i servizi di Azure potrebbe non fornire un quadro completo della situazione. Defender for Cloud può *deployare* automaticamente un **Log Analytics *agent*** per raccogliere dati relativi alla sicurezza. Per le macchine Azure, tale distribuzione è gestita direttamente, mentre per gli ambienti ibridi e *multicloud*, i piani di Microsoft Defender sono estesi a macchine non Azure con l’aiuto di [[Azure Arc]]. Le funzionalità di [[Cloud Security Post Management (CSPM)]] sono invece estese anche alle macchine *multicloud* senza la necessità di alcun *agent*.

# Protezioni native di Azure

Defender for Cloud aiuta a rilevare minacce:

1. Nei **servizi PaaS di Azure**, rilevando le minacce rivolte ai servizi di Azure, tra cui Azure App Service, Azure SQL, Azure Storage Account e altri servizi dati. Puoi anche eseguire il rilevamento delle anomalie negli Azure *activity logs* mediante l’integrazione nativa con **Microsoft Defender for Cloud Apps** (precedentemente noto come **Microsoft Cloud App Security**).
2. Nei **servizi dati di Azure**, includendo funzionalità che consentono di classificare automaticamente i dati in Azure SQL. Puoi anche ottenere valutazioni per potenziali vulnerabilità in Azure SQL e nei servizi Storage, nonché consigli su come mitigarle.
3. Nelle **reti**, aiutando a limitare l’esposizione agli attacchi di forza bruta. Riducendo l’accesso alle porte delle [[Virtual Machine]] mediante l’accesso *just-in-time* alle [[Virtual Machine]] è possibile rafforzare la rete impedendo accessi non necessari. È possibile impostare criteri di accesso sicuro su porte selezionate, solo per utenti autorizzati, su intervalli di indirizzi IP di origine consentiti o singoli indirizzi IP e per un periodo di tempo limitato.

# Proteggere le risorse ibride

Come detto, è possibile aggiungere le funzionalità di Defender for Cloud a un ambiente Cloud **ibrido** per proteggere i *server* non appartenenti a Azure. Per aiutare a concentrarsi su ciò che conta di più, il servizio invia poi informazioni personalizzate sulle minacce e avvisi con priorità in base all’ambiente specifico.

Per estendere poi la protezione anche ai *computer* locali, é possibile *deployare* [[Azure Arc]] e abilitare le funzionalità di sicurezza avanzate di Defender for Cloud.

# Proteggere le Risorse su altri Cloud

Come detto, Defender for Cloud è in grado di proteggere le risorse dislocate in altri ecosistemi Cloud, come [[Amazon Web Services (AWS)]] e [[Google Cloud Platform (GCP)]]. Ad esempio, se un *account* Amazon Web Services (AWS) viene “connesso” a una sottoscrizione Azure, è possibile abilitare una delle seguenti protezioni:

1. Le funzionalità **Cloud Security Post Management (CSPM)** di Defender for Cloud si estendono alle risorse AWS. Questo piano senza *agent* stima le risorse AWS in base alle raccomandazioni di sicurezza specifiche di AWS e ne include i risultati nel punteggio di sicurezza. Le risorse sono inoltre vagliate per conformità agli *standard* specifici di AWS (**AWS CIS**, **AWS PCI DSS** e **AWS Foundational Security Best Practices**). La pagina dell’inventario delle risorse di Defender for Cloud è una funzionalità abilitata per il *multicloud* che aiuta a gestire le risorse AWS insieme alle risorse Azure.
2. Microsoft Defender per i ***container*** estende il rilevamento delle minacce dei *container* e le difese avanzate ai *cluster* **Amazon EKS Linux**.
3. Microsoft Defender per i ***server*** offre il rilevamento delle minacce e le difese avanzate alle istanze **EC2 Windows e Linux**.

# Valutare, proteggere e difendere

Defender for Cloud soddisfa tre esigenze vitali della gestione della sicurezza delle risorse e dei carichi di lavoro, sia nel Cloud che in locale. Esso, infatti:

1. Valuta costantemente, così da fornire la “posizione di sicurezza”, identificare e monitorare le vulnerabilità.
2. Protegge, “indurisce” le risorse e i servizi mediante Azure Security Benchmark.
3. Difende, rivela e risolve le minacce alle risorse, ai carichi di lavoro e ai servizi.

## Valutazione Continua

Defender for Cloud aiuta a valutare continuamente il proprio ambiente, includendo soluzioni di stima della vulnerabilità per le [[Virtual Machine]], i registri di *container* e i *server* SQL.

Microsoft Defender per i *server* include l’integrazione automatica e nativa con Microsoft Defender per gli **Endpoint**. Con questa integrazione abilitata, si ha accesso ai risultati delle vulnerabilità provenienti dalla gestione delle minacce e delle vulnerabilità di Microsoft.

Tra questi strumenti di valutazione ci sono scansioni di vulnerabilità regolari e dettagliate che coprono il *compute*, i dati e l’infrastruttura. È possibile rivedere e rispondere ai risultati di queste scansioni tutto da Defender for Cloud.

## Proteggere

Dai metodi di autenticazione, al controllo degli accessi fino al concetto di [[Zero Trust Model]], la sicurezza nel Cloud è una base essenziale che deve essere eseguita correttamente. Per essere sicuro nel Cloud, devi assicurarti che i tuoi carichi di lavoro siano protetti, mediante policy di sicurezza adeguate al tuo ambiente e alla tua situazione. Poiché i criteri in Defender per il cloud sono basati sui controlli dei criteri di Azure, ottieni la gamma completa e la flessibilità di una soluzione di criteri di livello mondiale. In Defender for Cloud, puoi impostare i tuoi criteri in modo che vengano eseguiti su gruppi di gestione, tra abbonamenti e persino per un intero tenant.

Uno dei vantaggi del passaggio al cloud è la possibilità di crescere e ridimensionarsi in base alle esigenze, aggiungendo nuovi servizi e risorse secondo necessità. Defender for Cloud monitora costantemente la distribuzione di nuove risorse nei tuoi carichi di lavoro. Defender for Cloud valuta se le nuove risorse sono configurate in base alle best practice di sicurezza. In caso contrario, vengono contrassegnati e ottieni un elenco di consigli in ordine di priorità per ciò che devi correggere. I consigli ti aiutano a ridurre la superficie di attacco su ciascuna delle tue risorse.

L'elenco delle raccomandazioni è abilitato e supportato dal benchmark di sicurezza di Azure. Questo benchmark creato da Microsoft, specifico per Azure, fornisce una serie di linee guida per le procedure consigliate di sicurezza e conformità basate su framework di conformità comuni.

In questo modo, Defender for Cloud ti consente non solo di impostare criteri di sicurezza, ma anche di applicare standard di configurazione sicuri a tutte le tue risorse.

Per aiutarti a capire quanto sia importante ogni raccomandazione per il tuo stato di sicurezza generale, Defender for Cloud raggruppa le raccomandazioni in controlli di sicurezza e aggiunge un valore di punteggio sicuro a ciascun controllo. Il punteggio di sicurezza fornisce un indicatore immediato dello stato di salute della posizione di sicurezza, mentre i controlli forniscono un elenco di cose da considerare per migliorare il punteggio di sicurezza e la posizione di sicurezza complessiva.

## Difendere

Le prime due aree erano incentrate sulla valutazione, il monitoraggio e la manutenzione dell'ambiente. Defender for Cloud ti aiuta anche a difendere il tuo ambiente fornendo avvisi di sicurezza e funzionalità avanzate di protezione dalle minacce.

### Security alerts

Quando Defender for Cloud rileva una minaccia in qualsiasi area del tuo ambiente, genera un avviso di sicurezza. Avvisi di sicurezza:

1. Descrivere i dettagli delle risorse interessate.
2. Suggerire passaggi correttivi.
3. Fornire, in alcuni casi, un'opzione per attivare un'app per la logica in risposta.

Se un avviso viene generato da Defender for Cloud o ricevuto da Defender for Cloud da un prodotto di sicurezza integrato, puoi esportarlo. La protezione dalle minacce di Defender for Cloud include l'analisi fusion kill-chain, che correla automaticamente gli avvisi nel tuo ambiente in base all'analisi cyber kill-chain, per aiutarti a comprendere meglio la storia completa di una campagna di attacco, dove è iniziata e che tipo di impatto ha avuto aveva sulle tue risorse.

### Advanced threat protection

Defender per il cloud offre funzionalità avanzate di protezione dalle minacce per molte delle tue risorse distribuite, tra cui macchine virtuali, database SQL, container, applicazioni web e la tua rete. Le protezioni includono la protezione delle porte di gestione delle tue macchine virtuali con accesso just-in-time e controlli adattivi delle applicazioni per creare liste consentite per le app che devono e non devono essere eseguite sui tuoi computer.
Servizio Azure che aiuta a gestirne la *governance*, perché consente di definire **regole** di conformità applicate automaticamente. Quando si crea una risorsa Azure, quest’ultimo:

1. Valida la **richiesta**, ossia capisce se è possibile creare quella risorsa così com’è stato chiesto.
2. Valida i **permessi** dell’utente che sta cercando di creare la risorsa.
3. Verifica se ci sono ***policy*** applicate.

[[Azure Policy]] valuta le risorse e consente di controllarne le proprietà, prendendo decisioni in base ai valori di tali proprietà. Per esempio, è possibile definire una regola che controlli che le risorse di un certo [[Azure Resource Group]] siano create in una [[Azure Region]] specifica. In questo caso, l’[[Azure Resource Group]] rappresenta lo ***scope*** della [[Azure Policy]], ossia l’ambito di applicazione. [[Azure Policy]] non controlla i permessi dell’utente che sta creando la risorsa, poiché ciò viene verificato al passaggio precedente, come elencato in alto. Per ***effect*** di [[Azure Policy]], invece, si intende il risultato del controllo, che può essere, nella forma più banale, di consentire la creazione della risorsa desiderata o di negare tale possibilità.

Ci sono due opzioni disponibili in [[Azure Policy]]:

1. ***Policy*** singola (come quella che controlla la [[Azure Region]] di appartenenza).
2. ***Initiative***, ossia gruppi di *policy* correlate tra loro.

Per entrambe le categorie, ne sono disponibili già molte di *default* in Azure, ma è possibile crearne di nuove. Si può scegliere come una [[Azure Policy]] deve comportarsi in caso di esito negativo del controllo, come, ad esempio, impedire la creazione della risorsa o inviare un *alert*.

[[Azure Policy]] valuta le risorse ed evidenzia quelle che non sono conformi alle *policy* definite.

Le *policy* possono essere impostate a ogni livello (specifica risorsa, [[Azure Resource Group]], [[Azure Subscription]], etc.). Inoltre, esse sono **ereditate**, quindi impostando una *policy* a un certo livello, essa verrà applicata automaticamente a tutti i raggruppamenti che rientrano nell’elemento padre (ad esempio, da un [[Azure Resource Group]] a tutte le singole risorse che vi appartengono).

[[Azure Policy]] è fornito con definizioni di *policy* e *initiative* per Storage, Networking, Compute, Security Center, and Monitoring. Ad esempio, definire una *policy* che consente di utilizzare solo una determinata dimensione per le [[Virtual Machine]] in un ambiente, tale *policy* viene richiamata quando si crea una nuova [[Virtual Machine]] e ogni volta che si ridimensionano le [[Virtual Machine]] esistenti. [[Azure Policy]] valuta e monitora anche tutte le [[Virtual Machine]] già presenti nell’ambiente, incluse le [[Virtual Machine]] create prima della *policy*.

In alcuni casi, [[Azure Policy]] può correggere automaticamente le risorse e le configurazioni non conformi per garantire l’integrità dello stato delle risorse. Ad esempio, se tutte le risorse in un determinato [[Azure Resource Group]] devono essere contrassegnate con il *tag* AppName e il valore “SpecialOrders”, [[Azure Policy]] applicherà automaticamente tale *tag* se manca. Tuttavia, si mantiene comunque il pieno controllo del proprio ambiente. Se si dispone di una risorsa specifica che non si vuole sia “sistemata” da [[Azure Policy]], si può contrassegnare tale risorsa come eccezione.

[[Azure Policy]] si integra anche con [[Azure DevOps]] applicando eventuali *policy* di [[Continuous Integration (CI)]] e *delivery pipeline* che riguardano le fasi di pre-distribuzione e post-distribuzione delle proprie applicazioni.

## Azure Policy initiatives

La definizione di una *initiative* contiene tutte le definizioni delle *policy* per tenere traccia dello stato di conformità per un obiettivo più ampio. Ad esempio, [[Azure Policy]] include una *initiative* denominata **Enable Monitoring in Azure Security Center**. Il suo obiettivo è monitorare tutte le raccomandazioni di sicurezza disponibili per tutti i tipi di risorse Azure in [[Azure Security Center]].

Nell’ambito di questa *initiative*, sono incluse le seguenti definizioni di *policy*:

1. **Monitor unencrypted SQL Database in Security Center**: esegue il monitoraggio dei *database* e dei *server* SQL non crittografati.
2. **Monitor OS vulnerabilities in Security Center**: monitora i *server* che non soddisfano la *baseline* di vulnerabilità del sistema operativo configurato.
3. **Monitor missing Endpoint Protection in Security Center**: esegue il monitoraggio dei *server* che non dispongono di un *agent* di protezione degli *endpoint* installato.

In effetti, la *initiative* **Enable Monitoring in Azure Security Center** contiene oltre cento definizioni di *policy* separate.
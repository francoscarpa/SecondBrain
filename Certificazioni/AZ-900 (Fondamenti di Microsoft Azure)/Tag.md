Con l’aumentare dell’uso del Cloud, è sempre più importante rimanere **organizzati**. Una buona strategia organizzativa aiuta a comprendere l’utilizzo che si fa del Cloud e a gestire i costi.

Non esistono solo le [[Azure Subscription]] e i [[Azure Resource Group]] per organizzare le risorse correlate, ma anche i [[Tag]], che forniscono informazioni aggiuntive, o “metadati”, sulle risorse. Questi metadati sono utili per:

1. Gestione delle risorse: i *tag* consentono di individuare e agire sulle risorse associate a carichi di lavoro, ambienti, unità aziendali e proprietari specifici.
2. Gestione e ottimizzazione dei costi: I tag consentono di raggruppare le risorse in modo da poter creare report sui costi, allocare centri di costo interni, tenere traccia dei budget e prevedere i costi stimati.
3. Gestione delle operazioni: I tag ti consentono di raggruppare le risorse in base all'importanza della loro disponibilità per la tua azienda. Questo raggruppamento consente di formulare accordi sul livello di servizio (SLA). Uno SLA è una garanzia di uptime o prestazioni tra te e i tuoi utenti.
4. Sicurezza: I tag consentono di classificare i dati in base al relativo livello di sicurezza, ad esempio pubblico o riservato.
5. Governance e compliance normativa: I tag ti consentono di identificare le risorse che si allineano con i requisiti di governance o conformità normativa, come ISO 27001. I tag possono anche far parte delle tue attività di applicazione degli standard. Ad esempio, potresti richiedere che tutte le risorse siano contrassegnate con un nome di proprietario o reparto.
6. Ottimizzazione e automazione di carichi di lavoro: I tag possono aiutarti a visualizzare tutte le risorse che partecipano a distribuzioni complesse. Ad esempio, potresti contrassegnare una risorsa con il carico di lavoro associato o il nome dell'applicazione e usare software come Azure DevOps per eseguire attività automatizzate su tali risorse.

È possibile aggiungere, modificare o eliminare i tag delle risorse tramite Windows PowerShell, l'interfaccia della riga di comando di Azure, i modelli di Azure Resource Manager, l'API REST o il portale di Azure.

È possibile usare Criteri di Azure per applicare regole e convenzioni di tagging. Ad esempio, puoi richiedere che determinati tag vengano aggiunti a nuove risorse durante il provisioning. Puoi anche definire regole che riapplicano i tag che sono stati rimossi. I tag non vengono ereditati, il che significa che puoi applicare i tag a un livello e non farli visualizzare automaticamente a un livello diverso, consentendoti di creare schemi di tagging personalizzati che cambiano a seconda del livello (risorsa, gruppo di risorse, abbonamento e così via su).

Un tag di risorsa è costituito da un nome e da un valore. È possibile assegnare uno o più tag a ogni risorsa di Azure.

Tieni presente che non è necessario imporre la presenza di un tag specifico su tutte le tue risorse. Ad esempio, potresti decidere che solo le risorse mission-critical abbiano il tag Impact. Tutte le risorse senza tag non sarebbero quindi considerate mission-critical.
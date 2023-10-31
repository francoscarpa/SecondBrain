Blocco sulle risorse, che ne impedisce la modifica o la cancellazione accidentale. Anche con le *policy* di [[Azure RBAC (Role-Based Access Control)]] in atto, persiste il rischio che le persone con il giusto livello di accesso possano compromettere le risorse Cloud. I [[Resource Lock]] possono essere applicati a singole risorse, ad [[Azure Resource Group]] o persino a un’intera [[Azure Subscription]]; sono inoltre ereditati: se si applica un [[Resource Lock]] su un [[Azure Resource Group]], a tutte le risorse al suo interno verrà applicato il [[Resource Lock]].

Esistono due tipi di [[Resource Lock]]:

1. ***Delete***: gli utenti autorizzati possono leggere e modificare una risorsa, ma non eliminarla.
2. ***Read-only***: gli utenti autorizzati possono leggere una risorsa, ma non eliminarla o aggiornarla. L’applicazione di questo blocco è simile al limitare tutti gli utenti autorizzati ai permessi concessi dal ruolo ***Reader***.

È possibile gestire i [[Resource Lock]] dal portale Azure (basta selezionare la voce “Locks”, presente nel menù verticale a sinistra sotto “Settings”, quando si entra nella pagina della risorsa stessa), da PowerShell, dalla Azure CLI o da un [[ARM template]].

Per modificare una risorsa bloccata, bisogna prima rimuovere il blocco. Fatto ciò, è possibile applicare qualsiasi azione che si è  autorizzati a eseguire. I [[Resource Lock]] si applicano **indipendentemente** dalle autorizzazioni di [[Azure RBAC (Role-Based Access Control)]]: anche se si è il proprietario di una risorsa, bisogna comunque rimuovere il blocco prima di poter eseguire l’attività sulla risorsa stessa.
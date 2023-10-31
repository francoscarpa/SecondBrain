La gestione stile Azure, dappertutto. Azure Arc consente di gestire le proprie risorse da un’unica “torre di controllo”, coerente e unificata, siano le risorse in ambienti locali, multi-*cloud* o *edge*, consentendo di usare gli strumenti e i servizi tipici che Azure offre  ovunque si trovino le risorse. Il suo funzionamento si basa sull’utilizzo di [[ARM template]]. Degli esempi di cosa Azure Arc consente di fare sono:

1. Gestire tutto il proprio ambiente insieme “proiettando” le risorse esistenti che non sono in Azure, in [[ARM template]].
2. Gestire [[Virtual Machine]] multi-*cloud* e ibride, *cluster* Kubernetes e *database* come se fossero in esecuzione in Azure (invece stanno magari girando *on-premises*).
3. Usare i servizi e le funzionalità di gestione tipici di Azure, indipendentemente da dove risiedono.

Attualmente, Azure Arc consente di gestire i seguenti tipi di risorse ospitati all’esterno di Azure:

1. Server.
2. Cluster Kubernetes.
3. Servizi dati di Azure
4. SQL Server.
5. Virtual Machine (in *preview*).
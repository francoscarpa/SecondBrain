Considerando il [[Principle of Least Privilege]], rappresenta il modo di gestire i **permessi** in Azure, senza impazzire assegnando tali permessi manualmente a ogni risorsa (cosa impraticabile considerando che si possono aggiungere sia nuove risorse che nuove persone).

Azure offre alcuni “livelli di accesso” di *default*, ma si possono naturalmente creare i propri. Ogni ruolo ha specifici insiemi di permessi d’accesso, che i membri inseriti in quel ruolo ereditano. Esempi di ruolo sono *owner* e *reader*.

Azure RBAC lavora per ***scope***, ossia gruppi di risorse che vanno dai [[Azure Management Group]] alle singole risorse. Un esempio grafico (da notare in alto i ruoli, a sinistra gli *scope*):

![[Azure RBAC.png]]

Le aree in azzurro rappresentano categorie di utenti.

Azure RBAC:
- È **gerarchico**, cioè i permessi vengono **ereditati** da tutti gli *scope* sottostanti.
- È applicato su qualsiasi azione sulle risorse Azure che passano tramite [[Azure Resource Manager (ARM)]].
- Non applica permessi di accesso ai livelli **applicazione** o **dati**. La sicurezza di un’applicazione dev’essere gestita dall’applicazione stessa.
- Usa un modello di **consenso**. Se un *role assignment* garantisce permessi di **lettura** a un *resource group* e un altro *role assignment* garantisce permessi di **scrittura** al medesimo *resource group*, si acquisiscono **entrambi** i permessi di lettura e scrittura su quel *resouce group*.
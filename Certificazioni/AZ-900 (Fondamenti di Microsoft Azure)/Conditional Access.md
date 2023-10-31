Strumento tramite cui [[Azure Active Directory (Azure AD)]] (non) consente a una persona di accedere a una risorsa.

Raccoglie ***identity signals*** (“segnali d’identità”), cioè informazioni del tipo:

- **Chi** è la persona?
- Quale **ruolo** ha?
- **Dove** si trova?
- Quale **dispositivo** sta usando?
- Quale **applicazione** sta usando?

Quindi, prende una **decisione** in merito, ad esempio:
- Dando uno specifico **livello di accesso** (completo, parziale o nullo) alla risorsa.
- Incalzando l’utente con un’ulteriore conferma di autenticità (MFA).

Questo strumento aiuta gli amministratori IT, perché gli consente di rendere produttivi gli utenti aziendali mantenendo al contempo sicuro l’accesso alle risorse. Si capisce che costituisce per natura un modo per modificare l’uso della [[Multi-factor authentication (MFA)]]. Due esempi:
- Visto che ti trovi nel posto X **conosciuto**, non c'è bisogno della MFA.
- Visto che ti trovi nel posto Y **sconosciuto**, ti verrà chiesto di usare la MFA.
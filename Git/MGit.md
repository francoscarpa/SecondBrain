Per le limitazione che Git ha su Android, devo agire.
Non uso Termux, valida alternativa. Cercavo un client GUI.
Ho scelto [MGit](https://f-droid.org/en/packages/com.manichord.mgit/), da F-Droid.
Su GitHub creare un personal access token (classic):

- In the left sidebar, click **Developer settings**.
- In the left sidebar, under **Personal access tokens**...

Impostare la scadenza. Copiarlo subito una volta creato, non verrà più mostrato.

Su Mgit, fare per clonare un repository: dirà errore: authentication is required but no credentialsprovider has been registered.

Dare OK, verrà mostrato il popup per mettere username e password. Come username mettere l'indirizzo email dell'account github, come password, invece, il personal access token appena creato.
Mgit clona il repository nella cartella in: /Android/data/com.manichord.mgit/files/repo.
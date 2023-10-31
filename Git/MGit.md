[MGit](https://github.com/maks/MGit) è un *client* Git per Android. Android presenta limitazioni nell’uso di Git. Una soluzione è [Termux](https://termux.dev/en/), ma non è GUI. [MGit](https://f-droid.org/en/packages/com.manichord.mgit/), invece, lo è.

MGit, per funzionare, necessita che sia impostato un ***personal access token (classic)*** su GitHub. Per crearne uno:

- Cliccare su <kbd>Developer settings</kbd>, nella barra laterale sinistra.
- Cliccare su <kbd>Personal access tokens</kbd>, nella barra laterale sinistra.

Impostarne **nome** e **scadenza**, quindi copiarlo subito, in quanto non verrà più mostrato.

Su MGit, clonare un *repository*. Il processo mostrerà un errore: *Authentication is required but no CredentialsProvider has been registered*. Dare l’OK e verrà così mostrato un *popup* per impostare *username* e *password*:

- Come *username*, mettere l’indirizzo *e-mail* dell’*account* GitHub.
- Come *password*, mettere il *personal access token* appena creato.

MGit clona i *repository* come sottocartelle della cartella `/Android/data/com.manichord.mgit/files/repo`.

A quanto sembra, su MGit, il *fetch* non ha effetto, non si vede nulla; fare il *pull*, però, mostra che vengono scaricate correttamente le modifiche.

Come *shortcut*, combinare tutti i comandi in uno (dopo il primo *commit*, che presumibilmente avrà un messaggio diverso, specifico, di inizio). Ad esempio, su MacOS:

```
cd /Users/francoscarpa/Desktop/SecondBrain && git add . && git commit -a -S -m "Edits." && git pull && git push -u origin Trunk
```

Sostituire `&&` con il comando di concatenazione appropriato per la piattaforma in uso.
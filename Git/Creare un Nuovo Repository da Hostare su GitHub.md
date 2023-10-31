La seguente procedura spiega come creare un nuovo _repository_ Git in locale da _hostare_ su GitHub:

1. Creare una cartella vuota in locale ovunque si desidera.
2. Entrare nella cartella appena creata mediante riga di comando (`cd ...`) e inizializzare la cartella come nuovo _repository_ Git mediante `git init --initial-branch=Trunk`. `--initial-branch` fa sì che il nuovo _branch_ creato di _default_ si chiamerà `Trunk`. Se a questo punto si esegue `git status` verrà indicato che in `Trunk` non c’è nulla di nuovo.
3. Creare il _file_ `.gitignore` a mano, popolato in base al contenuto del _repository_. Ad esempio, nel caso del _repository_ che contiene il _file_ che si sta leggendo proprio in questo momento (_repository_ che contiene _file_ generici), conviene popolarlo con [questo contenuto](https://www.toptal.com/developers/gitignore/api/osx,node,macos,linux,windows,visualstudiocode), che gestisce un po’ tutti i “casini” dei vari sistemi operativi, come i *file* `.DS_Store` di macOS.
4. (Opzionale) Aggiungere altri _file_.
5. Aggiungere tutti i _file_ all’area di _staging_ mediante `git add .` e fare il primo _commit_ in locale mediante `git commit -m "[Descrizione del commit]"`.
6. Creare il _repository_ su GitHub.
7. Da riga di comando, riposizionarsi sul _repository_ in locale e aggiungere la `origin` per farlo puntare al nuovo _repository_ GitHub mediante `git remote add origin [URL indicato su GitHub]`.
8. Eseguire il _push_ sulla `origin` in GitHub mediante `git push -u origin Trunk`. Questo farà sì che il _branch_ su GitHub si chiamerà anch’esso `Trunk`.
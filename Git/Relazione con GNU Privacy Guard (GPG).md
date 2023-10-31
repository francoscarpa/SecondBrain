Con GPG si possono firmare in maniera crittografata i file, per assicurare che una cosa provenga da qualcuno che è realmente chi dice di essere.

Concetti:
- chiave privata.
- chiave pubblica.
- passphrase.

In Git, con `git tag -s` si possono firmare i tag.

In more recent versions of Git (v1.7.9 and above), you can now also sign individual commits (https://git-scm.com/book/en/v2/Git-Tools-Signing-Your-Work), ma [Linus Torvalds dice che è sbagliato](https://www.reddit.com/r/programming/comments/af8i5q/comment/edxd7da/?utm_source=share&utm_medium=web2x&context=3), e che basta firmare i tag. (Vedi anche [questo](https://softwareengineering.stackexchange.com/questions/212192/what-are-the-advantages-and-disadvantages-of-cryptographically-signing-commits-a) e [questo]())

Comunque, anche per firmare i tag bisogna impostare GPG. Innanzitutto, renderne disponibile la CLI (https://www.gnupg.org/download/index.html). Quindi, bisogna creare le chiavi.

Affinché qualcuno possa verificare un tag firmato da qualcun altro, deve importare nel suo key pair la chiave pubblica di quest’ultimo (vedi [questo](https://stackoverflow.com/a/25074920/3918095) ).

Però la mia considerazione è: dipende sempre da quello che uno deve fare!!! Se su un repository ci laovor solo io, vale la pensa usare i commit, visto che non sto creando un progetto software ma, ad esempio, un diario personale.
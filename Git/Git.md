# Sistemi di Versioning: Git.

Git è un sistema di controllo versione distribuito che consente di tenere traccia delle modifiche nel codice sorgente durante lo sviluppo software. Di seguito sono riportati i comandi principali e le loro funzionalità, insieme a una spiegazione delle strategie di merging e gestione dei branch.

## Comandi Fondamentali di Git

- **File .git**: Questo file tiene traccia delle modifiche apportate al progetto e gestisce la cronologia delle versioni.
- **`git init`**: Crea un nuovo repository Git, generando il file `.git` nella directory corrente.
- **`git status`**: Mostra lo stato attuale del repository, inclusi i file modificati e quelli pronti per il commit.
- **`git add .`**: Aggiunge tutti i file modificati all'area di staging, preparandoli per il commit.
- **`git commit -m "messaggio"`**: Registra le modifiche nell'area di staging con un messaggio descrittivo. Utilizzando `-m`, il messaggio può essere specificato in una sola riga.
- **`git log`**: Visualizza la cronologia dei commit, mostrando gli ID identificativi di ciascun commit.
- **`git reset`**: Riporta il repository a uno stato precedente senza eliminare le modifiche nel working directory. Può essere utilizzato con diverse opzioni:
  - `--soft`: Mantiene le modifiche nell'area di staging.
  - `--mixed`: Rimuove le modifiche dall'area di staging ma le mantiene nel working directory.
  - `--hard`: Elimina tutte le modifiche non salvate.

## Gestione dei Branch

- **Branch**: Un branch è una ramificazione della storia del progetto. Creando un branch, si inizia una nuova linea di sviluppo mantenendo la storia del branch principale.
- **`git checkout -b nome_branch`**: Crea un nuovo branch e si sposta su di esso.
- **`git branch`**: Mostra l'elenco dei branch disponibili nel repository.
- **`git switch nome_branch`**: Permette di passare a un altro branch esistente.
- **`git branch -D nome_branch`**: Elimina un branch. È necessario non essere attualmente su quel branch per eliminarlo.

## Strategie di Merge

Le strategie di merging definiscono come combinare le modifiche da diversi branch:

- **Merge Commit**: Unisce le modifiche in un nuovo commit, mantenendo la cronologia dei commit originali. In caso di conflitti, Git crea un commit speciale per risolverli.
- **Squash**: Combina più commit in un singolo commit, semplificando la cronologia.
- **Rebase**: Sposta i commit su un altro branch, riscrivendo la cronologia in modo che i nuovi commit appaiano in cima. Questa operazione può alterare gli orari dei commit.

## Modifiche e Ripristino

- **`git diff nome_file`**: Mostra le differenze tra le versioni del file specificato rispetto all'ultima versione committata.
- **`git stash`**: Metti da parte temporaneamente le modifiche non committate, permettendo di ripristinarle in seguito con `git stash apply`.
- **`git cherry-pick hash_commit`**: Permette di applicare un singolo commit da un altro branch al branch corrente.

## Comandi Avanzati

- **Rebase Interattivo (`git rebase -i hash_commit`)**: Consente di riscrivere la storia dei commit precedenti, utile per combinare o modificare commit esistenti.
- **Amend (`git commit --amend`)**: Permette di aggiungere modifiche all'ultimo commit senza crearne uno nuovo.

## Conclusione

Git è uno strumento potente per gestire versioni e collaborazioni nel software. Comprendere i suoi comandi fondamentali e le strategie di merging è essenziale per una gestione efficace del codice sorgente. Utilizzando questi strumenti, gli sviluppatori possono mantenere una cronologia chiara e organizzata delle loro modifiche.

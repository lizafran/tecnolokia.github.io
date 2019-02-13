# Il sito di tecnolokia

Questo readme raccoglie alcune informazioni per gestire la pagina del progetto tecnolokia, e aggiornare i suoi contenuti.
Usiamo github pages e siamo una comunità di gente con background diversi, usiamo questa pagina come appunti per chi non è pratico di github/jekyll.

Se non vi interessa tecnolokia o non sapete cosa sia, probabilmente non vi interessa questa pagina.

### Chiariamo alcuni concetti: 

* sorgenti del sito: una serie di file in formato markdown (.md)
* repository: una cartella in cui manteniamo tutti i sorgenti del sito, pubblica. Le persone abilitate possono modificarne i file
* Jekyll: un applicativo che interpreta i sorgenti e genera HTML
* github: la piattaforma che ospita i sorgenti, ci esegue Jekyll quando li cambiamo e serve le pagine HTML.

### regole generali:

* un file .md che che viene aggiunto nella cartella principale diventa una pagina html del sito
* eccezione alla precedente regola: qualsiasi file inizia per '_' viene ignorato.

Esempio: se aggiungete un file test.md, e all'interno usate un formato documentato dopo, Jekyll produce una pagina /test sul vostro sito. Se il file si chiama _test.md Jekyll non fa niente.

* Il file _config.yml contiene la configurazione che Jekyll userà per generare le pagine HTML, non lo toccate
* nella cartella _posts ci sono dei file .md, ciascuno dei quali corrisponde ad un nuovo o vecchio evento. Questi sono i file che dovete creare/modificare per aggiungere eventi. 

Provate a visualizzarne uno, dalla cartella [_posts](https://github.com/tecnolokia/tecnolokia.github.io/tree/master/_posts). Cliccate su un file, vi viene mostrata una tabella con del testo sotto. Se avete i permessi di scrittura, cliccate sull'icona della penna accanto al cestino a destra. Dovreste vedere qualcosa di simile a quanto segue:

~~~
---
layout: post
title:  "Titolo della serata"
cover: "https://mateh.id.au/wp-content/uploads/2014/07/amazon-aws-logo.jpg"
date:   2016-01-05
start_time: "12:00"
end_time: "13:00"
organiser: "Jimmy Smith"
---

Just a quick introduction into AWS.

Please come along if your interested. Pizza will be provided.
~~~

Il testo contenuto tra i simboli "---" è intestazione. Potete cambiare tutti i campi **tranne il campo 'layout'**.
Gli altri sono intuitivi, il titolo, la data (rispettate il formato ANNO-MESE-GIORNO) l'ora di inizio e di fine, ed il nome di chi presentera' la serata. Ignorate il campo 'cover' per il momento.

Il testo sottostante è il corpo del nuovo evento e racchiude una breve spiegazione di quello che succederà. Il corpo è da scrivere in MarkDown, un linguaggio molto semplice per fare testo formattato (mini guida su [wikipedia](https://it.wikipedia.org/wiki/Markdown#Esempi)). 

Provate a creare un nuovo file nella cartella _posts:

1. andate nella cartella
2. cliccate su "crea nuovo file"
3. Date un nome al vostro file. ATTENZIONE: il nome è importante e deve essere del tipo ANNO-MESE-GIORNO-testo.md, tipo '2019-11-01-test.md'
4. copiate dentro l'intestazione che vi ho riportato sopra come esempio e modificate dei campi.
5. NB: se scegliete una data "nel futuro" il post apparirà nella lista degli "incontri futuri" o in quelli "passati" se fate altrimenti
6. Andate in fondo alla pagina e cliccate sul bottone verde "commit changes" (il mio browser è impostato in inglese, quindi il vostro bottone potrebbe essere diverso, sempre verde è). 
7. Andate su tecnolokia.github.io per vedere se il vostro evento è stato aggiunto. NB: cancellate la cache del browser (o chiudete e riapritelo, o usate un browser diverso) oppure potrebbe non ricaricare la pagina.



## Bonus: aggiungere un'immagine

È sempre meglio aggiungere un'immagine ad un evento. Per farlo, potete usare il campo 'cover' nell'intestazione. Li potete mettere un collegamento ad un'immagine qualsiasi su Internet, oppure ad un'Immagine che avete aggiunto voi al sito. Per convenzione le immagini stanno nella cartella [assets/images](https://github.com/tecnolokia/tecnolokia.github.io/tree/master/assets/images). Se volete aggiungerne una andate nella cartella, cliccate su "upload file" e aggiungete un'immagine, ad esempio "evento.png". 
Nel campo cover dovete poi aggiungere il link relativo a quell'immagine 

~~~
cover: "assets/images/evento.png"
~~~



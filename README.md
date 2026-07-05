# Colpo di Busta · Simulatore Strategico

Gioco originale ispirato ai classici giochi a premi basati sulla scelta tra
buste sigillate. Un solo file HTML, nessuna dipendenza esterna da
installare, pronto per essere pubblicato come sito statico.

Progetto amatoriale, non affiliato ad alcuna emittente o format televisivo.

![Anteprima del simulatore](./new-image.png)

Lo trovi online: `https://colpo-di-busta.pages.dev` 

## Caratteristiche

1. Tabellone originale a 20 buste.
2. Busta Nera, il cui contenuto viene sorteggiato in modo indipendente e resta segreto anche al Notaio finché non viene aperta.
3. Quattro varianti del Notaio: offerta classica, cambio diretto, "Cambio o Offerta" e "Le Carte".
4. Premio minimo garantito da 1 a 49 euro, portato automaticamente a 50 euro.
5. Minigioco "La Regione Vincente" nella finalissima, con due turni di indovinelli.
6. "Trova il Fortunello", con jackpot progressivo tra una partita e l'altra.
7. Tema chiaro e scuro, con contrasto calibrato su entrambi.
8. Effetti sonori generati in tempo reale con la Web Audio API, senza file audio esterni.

## Eseguirlo in locale

Basta aprire `index.html` direttamente nel browser. In alternativa, per
evitare eventuali limitazioni del browser sui file aperti da disco, un
piccolo server statico locale è sufficiente:

```bash
python3 -m http.server 8000
```

poi visita `http://localhost:8000`.

## Pubblicazione

Il progetto è pensato per Cloudflare Pages: nessun comando di build, nessuna
cartella di output da configurare, sono file statici pronti così come sono.
I passaggi completi (caricamento diretto oppure collegamento a questa
repository) sono in [`DEPLOY.md`](./DEPLOY.md).

In sintesi, collegando questa repository a un nuovo progetto Cloudflare
Pages, lascia vuoto il comando di build e imposta la radice del repository
come cartella di output. Da quel momento ogni push aggiorna il sito online.

## Struttura del repository

```
index.html            gioco completo (HTML, CSS e JavaScript)
favicon.svg            icona principale
favicon-32.png         icona di riserva per i browser meno recenti
apple-touch-icon.png    icona per la schermata Home su iOS
og-image.png            anteprima per social e chat
DEPLOY.md               istruzioni dettagliate per Cloudflare Pages
```

## Stack tecnico

HTML5, CSS3 (variabili personalizzate per il tema chiaro e scuro,
animazioni) e JavaScript, senza framework né librerie esterne. Web Audio API
per il motore sonoro, Canvas 2D per l'effetto coriandoli.

## Crediti

Ideato e sviluppato da **Alessandro Bagnuoli**.

## Licenza

Codice distribuito con licenza MIT, salvo diversa indicazione. "Colpo di
Busta" è un gioco originale e non rivendica alcun legame con format
televisivi esistenti.

## Segnalazioni

Un errore riscontrato o un suggerimento sono sempre benvenuti: apri una
issue su questa repository.

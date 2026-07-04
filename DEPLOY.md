# Pubblicare su Cloudflare Pages

Questa cartella contiene tutto il necessario: `index.html`, la favicon
(`favicon.svg`, `favicon-32.png`, `apple-touch-icon.png`) e l'immagine di
anteprima per social e chat (`og-image.png`). Nessun passaggio di build:
sono file statici pronti da servire.

## Percorso 1: caricamento diretto (più rapido, senza Git)

1. Vai su [pages.cloudflare.com](https://pages.cloudflare.com) e accedi (o crea un account gratuito).
2. Scegli "Upload assets" (o "Create a project" e poi "Direct Upload").
3. Trascina l'intera cartella con questi 5 file.
4. Conferma il nome del progetto: diventerà `<nome>.pages.dev`.
5. Il sito è online in pochi secondi, con HTTPS già attivo.

Ogni aggiornamento successivo richiede un nuovo caricamento manuale della cartella.

## Percorso 2: collegato a GitHub (aggiornamenti automatici)

1. Crea un repository su GitHub e carica questi 5 file (o l'intero progetto, se vuoi che il codice sia visibile).
2. Su Cloudflare Pages scegli "Create a project" poi "Connect to Git".
3. Seleziona il repository.
4. Nelle impostazioni di build lascia "Framework preset: None" e "Build command" vuoto: sono file statici, non serve compilare nulla.
5. "Build output directory": lascia la radice (`/`) se i file sono nella root del repository.
6. Da questo momento, ogni push aggiorna automaticamente il sito online.

## Dominio personalizzato (opzionale, gratuito)

Da "Custom domains" nel progetto Cloudflare Pages puoi collegare un dominio
tuo, se ne possiedi uno; altrimenti l'indirizzo `<nome>.pages.dev` fornito da
Cloudflare resta pienamente funzionante e stabile.

## Verifica dopo la pubblicazione

Una volta online, controlla che l'anteprima social funzioni davvero: incolla
l'URL su uno strumento come [opengraph.xyz](https://www.opengraph.xyz) per
vedere come appare la card con titolo, descrizione e immagine prima di
condividerlo.

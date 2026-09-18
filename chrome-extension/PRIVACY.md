# Informativa sulla privacy di Minimalista

**Ultimo aggiornamento: 18 settembre 2026** · Estensione: **Minimalista** (Chrome Web Store,
versione 1.0.2)

Questa informativa riguarda **solo l'estensione Chrome**. L'app Android Minimalista, che è un
prodotto separato, ha una **propria informativa**.

---

## In breve

- Minimalista **non raccoglie dati personali**: non ci sono account, non c'è telemetria, non
  c'è pubblicità, non c'è nessun server dello sviluppatore.
- Tutto quello che crei (siti da limitare, categorie, ToDo, preferiti, statistiche) resta
  **sul tuo dispositivo**, in `chrome.storage.local`, e **non viene mai inviato** da nessuna
  parte.
- L'unico collegamento verso l'esterno serve a **gestire il pagamento PRO e la prova
  gratuita** (ExtensionPay): l'estensione non trasmette contenuti personali.
- L'estensione **non legge il contenuto delle pagine web** e **non chiede permessi host**:
  vede solo l'URL delle schede che apri, per poter mostrare la pagina di blocco.
- L'estensione è **software proprietario** (il codice non è pubblico): il § 8 spiega cosa
  resta comunque verificabile dall'esterno e sul tuo dispositivo.

---

## 1. Titolare e contatti

Minimalista è sviluppata da **Istrot** (il publisher dell'estensione sul Chrome Web Store).
Per domande su questa informativa, o per esercitare i tuoi diritti, scrivi a
**danielescripter@gmail.com**.

## 2. Quali dati tratta l'estensione (solo sul tuo dispositivo)

| Dato | Contenuto | Dove | A cosa serve | Condiviso con |
|---|---|---|---|---|
| Impostazioni | siti e categorie da limitare, modalità (tieni premuto / blocca), limiti giornalieri, blocco ferreo, fasce orarie, tema, lingua, sfondo, collegamenti rapidi | `chrome.storage.local` | ricordare le tue scelte | nessuno |
| ToDo | il testo degli impegni che scrivi | `chrome.storage.local` | mostrarli nella nuova scheda | nessuno |
| Preferiti | nome e URL dei siti che aggiungi | `chrome.storage.local` | mostrarli nella nuova scheda | nessuno |
| Statistiche d'uso | tempo per dominio, tentativi di accesso bloccati, sblocchi (per giorno) | `chrome.storage.local` | i grafici della sezione Statistiche | nessuno |
| Stato PRO | un flag "PRO attivo" (pagamento oppure prova), la **data di fine della prova** e una chiave **anonima** di ExtensionPay | `chrome.storage.local` + `chrome.storage.sync` | sapere se le funzioni PRO sono attive (anche sui tuoi altri dispositivi) | ExtensionPay (solo stato di pagamento, vedi § 4) |

Note:

- gli URL delle schede e i tempi di utilizzo sono **calcolati localmente** e restano locali;
  l'estensione non usa la cronologia di Chrome e non conserva le pagine che visiti, solo il
  dominio e il tempo cumulato;
- se sei in **navigazione anonima**, l'estensione è attiva solo se la abiliti tu
  (l'opzione è disattivata per impostazione predefinita);
- le icone dei preferiti sono chieste alla **cache dei preferiti di Chrome** (`_favicon`):
  nessuna richiesta di rete parte dall'estensione.

## 3. Dati che non raccogliamo

Nessuno dei seguenti: dati anagrafici, indirizzo email, indirizzo IP, posizione, cronologia
di navigazione (non teniamo un elenco dei siti che visiti: vedi la nota al § 2), contenuto
delle pagine, ciò che digiti o clicchi, dati sanitari, dati finanziari, credenziali. Nessun
identificatore pubblicitario, nessuna telemetria, nessun report di errore, nessun
tracciamento, nessuna profilazione, nessuna vendita o cessione di dati a terzi.

### Conformità alla policy di Chrome (Limited Use)

**L'uso delle informazioni che l'estensione riceve aderisce alla Chrome Web Store User Data
Policy, compresi i requisiti di Limited Use.** In concreto:

- i dati servono **solo** a fornire la funzionalità dichiarata (bloccare i siti che scegli,
  mostrare la nuova scheda e le statistiche) e restano sul tuo dispositivo;
- non vengono **venduti** né trasferiti a terzi per pubblicità personalizzata o ri-targetizzata,
  né usati per valutare il merito creditizio o concedere prestiti;
- **nessuna persona** li legge: non esiste un server dello sviluppatore e niente lascia il tuo
  dispositivo, tranne ciò che serve al pagamento o alla prova PRO (§ 4), gestito da ExtensionPay
  su una pagina esterna in HTTPS.

## 4. Funzioni PRO: ExtensionPay e Stripe

Le funzioni PRO si sbloccano con un **acquisto una tantum** gestito da servizi esterni, non
dall'estensione:

- **Pagamento.** Cliccando "Sblocca PRO" l'estensione apre la pagina di pagamento di
  **ExtensionPay** (<https://extensionpay.com>) in una scheda; il pagamento è elaborato da
  **Stripe**. I dati che inserisci lì (ad esempio email e dati della carta) sono trattati da
  ExtensionPay e Stripe come titolari autonomi: le loro informative sono
  <https://extensionpay.com/privacy> e <https://stripe.com/privacy>. **Quei dati non passano
  mai dall'estensione**, che non li vede e non li conserva.
- **Verifica dello stato.** L'estensione contatta `extensionpay.com` per sapere se il
  pagamento risulta: all'avvio del browser, quando il servizio in background viene riattivato
  o l'estensione aggiornata, e quando apri la sezione Membership (per esempio subito dopo il
  pagamento, con un controllo ogni 4 secondi per un massimo di circa 5 minuti). La richiesta
  contiene **solo la chiave anonima** generata dall'estensione (nessun nome, nessuna email,
  nessun contenuto) e riceve in risposta lo stato "pagato / non pagato".
- **Prezzo dell'acquisto.** Quando apri la sezione Membership, l'estensione chiede a
  ExtensionPay anche la cifra del piano Lifetime, per mostrartela nell'interfaccia: la cifra
  non è scritta nell'estensione, arriva da lì, così quello che leggi è quello che viene
  addebitato. Anche questa richiesta **non contiene alcun dato tuo**: è una semplice lettura
  del listino del piano (nessuna chiave, nessun identificatore). La cifra letta resta in cache
  sul tuo dispositivo per mostrartela subito alla prossima apertura, senza nuove richieste.
- **Prova gratuita.** Se attivi la prova (pulsante nella sezione Membership), l'estensione
  apre in una finestra la pagina di prova di **ExtensionPay**: lì inserisci la tua **email**,
  che ExtensionPay usa per inviarti il link di conferma e per riconoscere la prova. Quell'email
  è trattata da ExtensionPay come titolare autonomo (informativa in
  <https://extensionpay.com/privacy>), **non passa dall'estensione** e non viene conservata:
  sul dispositivo resta solo la **data di fine della prova**. Alla scadenza la prova non si
  rinnova e non comporta nessun addebito.
- **Chiave anonima.** È una stringa casuale, salvata in `chrome.storage.sync`: serve a
  riconoscere l'acquisto su tutti i tuoi dispositivi. Non identifica te come persona.
- Se non usi le funzioni PRO e non apri la sezione Membership, non c'è nessun pagamento e
  nessuna comunicazione verso l'esterno.

## 5. Permessi richiesti e perché

| Permesso | Perché |
|---|---|
| `storage` | salvare impostazioni, ToDo, preferiti e statistiche solo sul dispositivo |
| `tabs` | riportare alla pagina di blocco una scheda **già aperta** quando il limite giornaliero viene superato mentre la stai usando |
| `webNavigation` | intercettare la navigazione verso i siti della tua lista **prima** che si aprano e mostrare la pagina di blocco |
| `alarms` | controlli periodici (~30 secondi) per far rispettare il limite, contare il tempo e recuperare i blocchi persi quando il servizio in background era spento |
| `favicon` | mostrare le icone dei preferiti prendendole dalla cache di Chrome |

**Nessun permesso host è dichiarato** e non vengono eseguiti script nelle pagine web:
l'estensione non può leggere ciò che le pagine contengono.

## 6. Conservazione e cancellazione

- I dati sul tuo dispositivo restano finché non li cancelli o non **disinstalli
  l'estensione**: disinstallandola Chrome elimina i suoi dati locali. Puoi anche azzerare
  statistiche e impostazioni dalle pagine dell'estensione.
- I dati relativi al pagamento sono conservati da **ExtensionPay** e **Stripe** secondo le
  loro informative; per cancellarli o accedervi rivolgiti a loro (indicando l'email usata al
  momento del pagamento). L'estensione non ne possiede copia: conserva solo un flag locale.

## 7. Minori

Minimalista non è destinata a minori di 13 anni (16 nell'Unione Europea) e non raccoglie
dati personali, quindi non ne raccoglie nemmeno dai minori.

## 8. Codice e licenza

Minimalista è **software proprietario** di **Istrot**: il codice sorgente non è pubblicato e
tutti i diritti sono riservati. Non è quindi possibile scaricarlo o ispezionarlo dall'esterno.

Resta comunque verificabile **dall'esterno e sul tuo dispositivo** tutto quello che conta per
la privacy: il pacchetto dichiara **nessun permesso host** e **nessun `content_script`** (la
scheda *Privacy* del Chrome Web Store lo attesta), quindi l'estensione non può leggere il
contenuto delle pagine; i dati descritti qui restano in `chrome.storage.local` e non esiste un
server dello sviluppatore; le uniche richieste di rete sono quelle verso `extensionpay.com`
per lo stato e il prezzo del piano PRO (§ 4), che puoi osservare tu stesso negli strumenti di
rete del browser.

L'estensione include la libreria di pagamento `ExtPay.js` di ExtensionPay, distribuita con
licenza **LGPL-3.0** e usata senza modifiche al codice: è l'**unico** componente di terze
parti con una licenza propria e la sua licenza **non** si estende al resto del progetto. Gli
avvisi e il testo della licenza sono nel file `LICENSE`, incluso nel pacchetto.

## 9. Modifiche a questa informativa

Questa informativa può essere aggiornata quando cambiano l'estensione o la legge. La data in
cima indica l'ultima revisione: la versione pubblicata su questa pagina è quella in vigore.

---
---

# Privacy Policy of Minimalista (English)

**Last updated: 18 September 2026** · Extension: **Minimalista** (Chrome Web Store, version
1.0.2)

This policy covers the **Chrome extension only**. The Minimalista Android app is a separate
product with its **own policy**.

## Summary

- Minimalista **collects no personal data**: no accounts, no telemetry, no ads, no developer
  server.
- Everything you create (blocked sites, categories, to-do items, favorites, statistics) stays
  **on your device** in `chrome.storage.local` and is **never sent anywhere**.
- The only outbound connection is the **PRO payment and free-trial handling** (ExtensionPay);
  the extension itself sends no personal content.
- The extension **cannot read web page content** and **requests no host permissions**: it
  only sees the URL of the tabs you open, so it can show the block page.
- The extension is **proprietary software** (the code is not public): § 8 explains what
  remains verifiable from the outside and on your device.

## 1. Controller and contact

Minimalista is developed by **Istrot** (the Chrome Web Store publisher). For questions about
this policy or to exercise your rights, write to **danielescripter@gmail.com**.

## 2. Data handled by the extension (on your device only)

| Data | Content | Where | Why | Shared with |
|---|---|---|---|---|
| Settings | sites and categories to limit, mode (hold / block), daily limits, cold turkey, time slots, theme, language, background, quick links | `chrome.storage.local` | remember your choices | nobody |
| To-do items | the text you type | `chrome.storage.local` | show them on the new tab | nobody |
| Favorites | name and URL you add | `chrome.storage.local` | show them on the new tab | nobody |
| Usage statistics | time per domain, blocked attempts, unlocks (per day) | `chrome.storage.local` | the Statistics charts | nobody |
| PRO status | a "PRO active" flag (payment or trial), the **trial end date** and an **anonymous** ExtensionPay key | `chrome.storage.local` + `chrome.storage.sync` | know whether PRO features are active (also on your other devices) | ExtensionPay (payment status only, see § 4) |

Tab URLs and usage time are computed locally and stay local: the extension does not use
Chrome's history and does not keep the pages you visit, only the domain and cumulative time.
In **incognito** it runs only if you enable it (off by default). Favorites icons are requested
from **Chrome's own favicon cache** (`_favicon`): no network request originates from the
extension.

## 3. Data we do not collect

No name, email, IP address, location, browsing history (we do not keep a list of the sites you
visit: see the note in § 2), page content, keystrokes, clicks, health data, financial data or
credentials. No advertising identifier, no telemetry, no crash reports, no tracking, no
profiling, no selling or sharing of data with third parties.

### Chrome policy compliance (Limited Use)

**Our use of the information the extension receives adheres to the Chrome Web Store User Data
Policy, including the Limited Use requirements.** Concretely:

- the data is used **only** to provide the declared functionality (blocking the sites you
  choose, showing the new tab and the statistics) and stays on your device;
- it is never **sold**, nor transferred to third parties for personalized or re-targeted
  advertising, nor used to determine credit-worthiness or for lending purposes;
- **no human reads it**: there is no developer server and nothing leaves your device except
  what the PRO payment or trial requires (§ 4), handled by ExtensionPay on an external HTTPS
  page.

## 4. PRO features: ExtensionPay and Stripe

PRO features are unlocked with a **one-time purchase** handled by external services, not by
the extension:

- **Payment.** Clicking "Unlock PRO" opens **ExtensionPay**'s payment page
  (<https://extensionpay.com>) in a tab; the payment is processed by **Stripe**. The details
  you enter there (e.g. email and card data) are processed by ExtensionPay and Stripe as
  independent controllers: see <https://extensionpay.com/privacy> and
  <https://stripe.com/privacy>. **Those details never reach the extension**, which neither
  sees nor stores them.
- **Status check.** The extension contacts `extensionpay.com` to check whether the purchase is
  registered: at browser start, whenever the background service worker is revived or the
  extension is updated, and when you open the Membership section (e.g. right after paying,
  polling every 4 seconds for up to ~5 minutes). The request contains **only the anonymous
  key** generated by the extension (no name, no email, no content) and receives back the
  "paid / not paid" status.
- **Purchase price.** When you open the Membership section, the extension also asks
  ExtensionPay for the Lifetime plan amount, to show it in the interface: the amount is not
  written in the extension, it comes from there, so what you read is what you are charged.
  This request too **carries no data of yours**: it is a simple read of the plan list (no key,
  no identifier). The amount it returns is cached on your device so it can be shown
  immediately next time you open it, with no new requests.
- **Free trial.** If you start the trial (button in the Membership section), the extension
  opens ExtensionPay's trial page in a small window: there you enter your **email address**,
  which ExtensionPay uses to send you the confirmation link and to recognize the trial. That
  email is processed by ExtensionPay as an independent controller (see
  <https://extensionpay.com/privacy>), **never passes through the extension** and is not
  stored locally: only the **trial end date** is kept on your device. When the trial ends it
  does not renew and no charge is made.
- **Anonymous key.** A random string stored in `chrome.storage.sync` so the purchase is
  recognized on all your devices. It does not identify you as a person.
- If you never use PRO features and never open the Membership section, there is no payment
  and no outbound communication.

## 5. Permissions and why they are needed

| Permission | Why |
|---|---|
| `storage` | keep settings, to-do items, favorites and statistics on the device only |
| `tabs` | send an **already open** tab to the block page when the daily limit is exceeded while you are using it |
| `webNavigation` | intercept navigation to sites on your list **before** they load and show the block page |
| `alarms` | periodic ticks (~30 seconds) to enforce limits, track usage time and recover blocks missed while the service worker was asleep |
| `favicon` | show favorites icons from Chrome's cache |

**No host permissions are declared** and no scripts run inside web pages: the extension cannot
read page content.

## 6. Retention and deletion

- On-device data stays until you delete it or **uninstall the extension**: uninstalling makes
  Chrome remove its local data. You can also reset statistics and settings from the
  extension's pages.
- Payment records are kept by **ExtensionPay** and **Stripe** under their own policies; contact
  them (quoting the email used at checkout) to delete or access them. The extension holds no
  copy of them, only a local flag.

## 7. Children

Minimalista is not intended for children under 13 (16 in the EU) and collects no personal data,
hence none from children.

## 8. Code and license

Minimalista is **proprietary software** by **Istrot**: the source code is not published and
all rights are reserved. It cannot be downloaded or inspected from the outside.

What remains verifiable **from the outside and on your device** is everything that matters for
privacy: the package declares **no host permissions** and **no `content_script`** (the Chrome
Web Store *Privacy* tab attests to it), so the extension cannot read page content; the data
described here stays in `chrome.storage.local` and there is no developer server; the only
network requests go to `extensionpay.com` for the PRO plan status and price (§ 4), which you
can watch yourself in the browser's network tools.

Minimalista bundles ExtensionPay's `ExtPay.js` payment library, released under the
**LGPL-3.0** license and used with no changes to its code: it is the **only** third-party
component with its own license, and that license does **not** extend to the rest of the
project. The notices and the license text are in the `LICENSE` file, included in the package.

## 9. Changes to this policy

This policy may be updated when the extension or the law changes. The date at the top marks the
latest revision: the version published on this page is the one in force.

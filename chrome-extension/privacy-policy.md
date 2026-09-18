# Informativa sulla privacy di Minimalista

**Ultimo aggiornamento: 18 settembre 2026** · Estensione: **Minimalista** (Chrome Web Store,
versione 1.0.2)

Questa informativa riguarda **solo l'estensione Chrome**; l'app Android Minimalista ha una
**propria informativa**.

---

## In breve

- Minimalista **non raccoglie dati personali**: nessun account, nessuna telemetria, nessuna
  pubblicità, nessun server dello sviluppatore.
- Tutto quello che crei (siti da limitare, categorie, ToDo, preferiti, statistiche) resta
  **sul tuo dispositivo** e non viene inviato da nessuna parte.
- L'unico collegamento verso l'esterno serve al **pagamento PRO e alla prova gratuita**
  (sezione 4).
- L'estensione **non legge il contenuto delle pagine web** e **non chiede permessi host**:
  vede solo l'URL delle schede che apri, per poter mostrare la pagina di blocco.

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
| Stato PRO | un flag "PRO attivo" (pagamento oppure prova), la **data di fine della prova** e una chiave **anonima** di ExtensionPay | `chrome.storage.local` + `chrome.storage.sync` | sapere se le funzioni PRO sono attive (anche sui tuoi altri dispositivi) | ExtensionPay (solo stato di pagamento: sezione 4) |

Note:

- gli URL delle schede e i tempi di utilizzo sono **calcolati localmente** e restano locali:
  l'estensione non usa la cronologia di Chrome e conserva solo il dominio e il tempo cumulato,
  non le pagine che visiti;
- in **navigazione anonima** è attiva solo se la abiliti tu (disattivata per impostazione
  predefinita);
- le icone dei preferiti arrivano dalla **cache dei preferiti di Chrome** (`_favicon`):
  nessuna richiesta di rete parte dall'estensione.

## 3. Dati che non raccogliamo

Nessuno dei seguenti: dati anagrafici, indirizzo email, indirizzo IP, posizione, cronologia di
navigazione (l'estensione vede solo il dominio, non le pagine: sezione 2), contenuto delle
pagine, ciò che digiti o clicchi, dati sanitari, dati finanziari, credenziali. Nessun
identificatore pubblicitario, nessuna telemetria, nessun report di errore, nessun tracciamento,
nessuna profilazione, nessuna vendita o cessione di dati a terzi.

### Conformità alla policy di Chrome (Limited Use)

**L'uso delle informazioni che l'estensione riceve aderisce alla Chrome Web Store User Data
Policy, compresi i requisiti di Limited Use.** In concreto:

- i dati servono **solo** a fornire la funzionalità dichiarata (bloccare i siti che scegli,
  mostrare la nuova scheda e le statistiche) e restano sul tuo dispositivo;
- non vengono **venduti** né trasferiti a terzi per pubblicità personalizzata o ri-targetizzata,
  né usati per valutare il merito creditizio o concedere prestiti;
- **nessuna persona** li legge: non esiste un server dello sviluppatore e niente lascia il tuo
  dispositivo, tranne ciò che serve al pagamento o alla prova PRO (sezione 4).

## 4. Funzioni PRO: ExtensionPay e Stripe

Le funzioni PRO si sbloccano con un **acquisto una tantum** gestito da servizi esterni, non
dall'estensione.

- **Pagamento.** Cliccando "Sblocca PRO" l'estensione apre la pagina di pagamento di
  **ExtensionPay** (<https://extensionpay.com>) in una scheda; il pagamento è elaborato da
  **Stripe**. I dati che inserisci lì (ad esempio email e dati della carta) sono trattati da
  ExtensionPay e Stripe come titolari autonomi (<https://extensionpay.com/privacy> e
  <https://stripe.com/privacy>) e **non passano mai dall'estensione**, che non li vede e non
  li conserva.
- **Verifica dello stato.** L'estensione contatta `extensionpay.com` per sapere se il
  pagamento risulta: all'avvio del browser, quando il servizio in background si riattiva o
  l'estensione si aggiorna, e quando apri la sezione Membership (anche in ripetizione subito
  dopo il pagamento). La richiesta contiene **solo la chiave anonima** generata
  dall'estensione — nessun nome, nessuna email, nessun contenuto — e riceve in risposta lo
  stato "pagato / non pagato".
- **Prezzo dell'acquisto.** Quando apri la sezione Membership, la cifra del piano Lifetime
  viene letta da ExtensionPay e mostrata nell'interfaccia: non è scritta nell'estensione, così
  quello che leggi è quello che viene addebitato. La richiesta **non contiene alcun dato tuo**
  e la cifra resta in cache sul dispositivo per mostrarla subito la volta successiva.
- **Prova gratuita.** Se attivi la prova (pulsante nella sezione Membership), l'estensione apre
  in una finestra la pagina di prova di **ExtensionPay**, dove inserisci la tua **email**: la
  usa ExtensionPay per inviarti il link di conferma e per riconoscere la prova, e la tratta
  come titolare autonomo. **L'email non passa dall'estensione** e non viene conservata: sul
  dispositivo resta solo la **data di fine della prova**. Alla scadenza la prova non si rinnova
  e non comporta nessun addebito.
- **Chiave anonima.** Una stringa casuale salvata in `chrome.storage.sync`, che serve a
  riconoscere l'acquisto su tutti i tuoi dispositivi: non identifica te come persona.
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
  momento del pagamento). L'estensione non ne possiede copia.

## 7. Minori

Minimalista non è destinata a minori di 13 anni (16 nell'Unione Europea) e non raccoglie dati
personali, quindi non ne raccoglie nemmeno dai minori.

## 8. Modifiche a questa informativa

Questa informativa può essere aggiornata quando cambiano l'estensione o la legge. La data in
cima indica l'ultima revisione: la versione pubblicata su questa pagina è quella in vigore.

---
---

# Privacy Policy of Minimalista (English)

**Last updated: 18 September 2026** · Extension: **Minimalista** (Chrome Web Store, version
1.0.2)

This policy covers the **Chrome extension only**; the Minimalista Android app has its **own
policy**.

## Summary

- Minimalista **collects no personal data**: no accounts, no telemetry, no ads, no developer
  server.
- Everything you create (blocked sites, categories, to-do items, favorites, statistics) stays
  **on your device** and is never sent anywhere.
- The only outbound connection is the **PRO payment and free-trial handling** (section 4).
- The extension **cannot read web page content** and **requests no host permissions**: it only
  sees the URL of the tabs you open, so it can show the block page.

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
| PRO status | a "PRO active" flag (payment or trial), the **trial end date** and an **anonymous** ExtensionPay key | `chrome.storage.local` + `chrome.storage.sync` | know whether PRO features are active (also on your other devices) | ExtensionPay (payment status only: section 4) |

Tab URLs and usage time are computed locally and stay local: the extension does not use
Chrome's history and keeps only the domain and the cumulative time, not the pages you visit.
In **incognito** it runs only if you enable it (off by default). Favorites icons come from
**Chrome's own favicon cache** (`_favicon`): no network request originates from the extension.

## 3. Data we do not collect

None of the following: name, email address, IP address, location, browsing history (the
extension sees only the domain, not the pages: section 2), page content, keystrokes, clicks,
health data, financial data or credentials. No advertising identifier, no telemetry, no crash
reports, no tracking, no profiling, no selling or sharing of data with third parties.

### Chrome policy compliance (Limited Use)

**Our use of the information the extension receives adheres to the Chrome Web Store User Data
Policy, including the Limited Use requirements.** Concretely:

- the data is used **only** to provide the declared functionality (blocking the sites you
  choose, showing the new tab and the statistics) and stays on your device;
- it is never **sold**, nor transferred to third parties for personalized or re-targeted
  advertising, nor used to determine credit-worthiness or for lending purposes;
- **no human reads it**: there is no developer server and nothing leaves your device except
  what the PRO payment or trial requires (section 4).

## 4. PRO features: ExtensionPay and Stripe

PRO features are unlocked with a **one-time purchase** handled by external services, not by
the extension.

- **Payment.** Clicking "Unlock PRO" opens **ExtensionPay**'s payment page
  (<https://extensionpay.com>) in a tab; the payment is processed by **Stripe**. The details
  you enter there (e.g. email and card data) are processed by ExtensionPay and Stripe as
  independent controllers (<https://extensionpay.com/privacy> and
  <https://stripe.com/privacy>) and **never reach the extension**, which neither sees nor
  stores them.
- **Status check.** The extension contacts `extensionpay.com` to check whether the purchase is
  registered: at browser start, whenever the background service worker is revived or the
  extension is updated, and when you open the Membership section (repeatedly, if you have just
  paid). The request contains **only the anonymous key** generated by the extension — no name,
  no email, no content — and receives back the "paid / not paid" status.
- **Purchase price.** When you open the Membership section, the Lifetime plan amount is read
  from ExtensionPay and shown in the interface: it is not written in the extension, so what you
  read is what you are charged. The request **carries no data of yours**, and the amount is
  cached on your device so it can be shown immediately next time.
- **Free trial.** If you start the trial (button in the Membership section), the extension opens
  ExtensionPay's trial page in a small window, where you enter your **email address**:
  ExtensionPay uses it to send you the confirmation link and to recognize the trial, and
  processes it as an independent controller. **The email never passes through the extension**
  and is not stored: only the **trial end date** is kept on your device. When the trial ends it
  does not renew and no charge is made.
- **Anonymous key.** A random string stored in `chrome.storage.sync` so the purchase is
  recognized on all your devices: it does not identify you as a person.
- If you never use PRO features and never open the Membership section, there is no payment and
  no outbound communication.

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
  copy of them.

## 7. Children

Minimalista is not intended for children under 13 (16 in the EU) and collects no personal data,
hence none from children.

## 8. Changes to this policy

This policy may be updated when the extension or the law changes. The date at the top marks the
latest revision: the version published on this page is the one in force.

# ach-officina

Lavori automatici di servizio delle guide di Ach. Qui non si conservano dati: i programmi e i risultati stanno
nel repository privato, che questi flussi leggono e aggiornano con una chiave (`PRIVATO_TOKEN`).

Regole: nei registri dei flussi (pubblici) si scrivono solo conteggi, mai indirizzi, nomi o siti; nessun file di
risultati resta in questo repository né come allegato dei giri.

## Flussi

| Flusso | Quando | Che cosa fa |
|---|---|---|
| `email-soggetti.yml` | ogni notte | email dai siti propri dei soggetti delle guide, e i link Facebook/Instagram che il sito stesso mostra |
| `email-siti.yml` | ogni giorno | raccolta dei siti dagli elenchi pubblici |
| `achrecipes-fonti.yml` | a richiesta | le fonti di AchRecipes (`achrecipes/strumenti/fonti.py`), come il flusso del privato ma gratis |
| `rilancia.yml` | quando un giro lungo va male | lo rifà partire una volta (email, siti, cerca siti, menu, domini) |
| `verifica-domini.yml` | ogni notte | domini dei destinatari delle lettere accese: i morti fra gli esclusi del privato |
| `caselle.yml` | ogni notte | affidabilità delle caselle: sito vivo o morto, indirizzo ancora sul sito, scheda OpenStreetMap; quanto tornano le lettere per ogni prova; caselle nuove per le lettere tornate indietro |
| `visite-lettere.yml` | ogni notte | visite portate da ogni lettera (GoatCounter, chiavi di sola lettura); senza chiavi non fa nulla |
| `leggi-pagine.yml` | a richiesta | legge le pagine web indicate (anche siti in JavaScript) e salva il testo pulito nel privato; da una chat: `python3 strumenti/leggi_online.py URL` |
| `menu-soggetti.yml` | ogni sera | link al menu e prezzo indicativo dei ristoranti di Dinners dal loro sito |
| `contatti-esteri.yml` | ogni tre mesi | contatti esteri da Overture, coda dei siti, elenchi esteri |
| `cerca-siti.yml` | la domenica | sito, email e profili social di chi non ha il sito, da OpenStreetMap, Overture e Wikidata |

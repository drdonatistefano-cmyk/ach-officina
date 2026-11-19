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
| `leggi-pagine.yml` | a richiesta | legge le pagine web indicate (anche siti in JavaScript) e salva il testo pulito nel privato; da una chat: `python3 strumenti/leggi_online.py URL` |
| `menu-soggetti.yml` | ogni sera | link al menu e prezzo indicativo dei ristoranti di Dinners dal loro sito |
| `contatti-esteri.yml` | ogni tre mesi | contatti esteri da Overture, coda dei siti, elenchi esteri |
| `cerca-siti.yml` | la domenica | sito, email e profili social di chi non ha il sito, da OpenStreetMap, Overture e Wikidata |

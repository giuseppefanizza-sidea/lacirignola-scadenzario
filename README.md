# lacirignola-scadenzario

Deck di presentazione, uso riservato.

## Il contenuto è cifrato

`index.html` non contiene il deck in chiaro: contiene una pagina di sblocco e il deck cifrato con
**AES-GCM 256 bit**, chiave derivata dalla password con **PBKDF2-SHA256 a 600.000 iterazioni**.
La decifratura avviene nel browser di chi conosce la password. Senza password la pagina contiene
solo dati illeggibili.

La password non è in questo repository e non va mai messa qui. Viaggia separata dal link.

La pagina è anche esclusa dai motori di ricerca con il meta tag `noindex`. Non collegare questo URL
da pagine pubbliche.

## Aggiornare il deck

Il sorgente in chiaro e lo script `cifra-deck.mjs` restano nel workspace di agenzia, mai qui.
Dopo ogni modifica:

    DECK_PW='<password>' node cifra-deck.mjs <cartella di questo repo>

poi commit e push di `index.html` su `main`. Non copiare mai qui il file HTML in chiaro: il
repository è pubblico e la cronologia resta visibile.

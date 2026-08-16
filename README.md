<div align="center">

# AtletAI

**Scrivi il tuo allenamento come lo racconteresti a un amico.**

[![Ultima versione](https://img.shields.io/github/v/release/DaviBlade05/atletai?label=ultima%20versione&color=cafd00&style=for-the-badge)](https://github.com/DaviBlade05/atletai/releases/latest)
[![Android](https://img.shields.io/badge/Android-8.0%2B-cafd00?style=for-the-badge&logo=android&logoColor=black)](https://github.com/DaviBlade05/atletai/releases/latest)
[![Gratis](https://img.shields.io/badge/gratis-senza%20pubblicit%C3%A0-cafd00?style=for-the-badge)](https://atletaii.netlify.app)

[**Scarica l'APK**](https://github.com/DaviBlade05/atletai/releases/latest) · [Sito](https://atletaii.netlify.app) · [Privacy](https://atletaii.netlify.app/privacy.html) · [Novità](https://github.com/DaviBlade05/atletai/releases)

</div>

---

Le altre app di allenamento ti fanno compilare moduli: scegli l'esercizio da una lista, imposta le serie, imposta le ripetizioni, imposta il carico, conferma. Fra una serie e l'altra, con una mano sola.

AtletAI no. Le scrivi, o le detti:

```
panca 4x8 80, lat machine 4x10 60
```

```
oggi push: panca 60 per 8, 8, 6 — poi alzate laterali 3x12 con 10
```

E lei capisce, riconosce gli esercizi che usi di solito, e registra. Se la frase è inequivocabile la legge **in locale**, senza nemmeno chiamare l'AI: la conferma appare all'istante.

---

## Cosa sa fare

| | |
|---|---|
| **Registri parlando** | Detti o scrivi in italiano. Riconosce top set, back off, warm-up, piramidali. |
| **Allenamento guidato** | Spunti le serie una a una, il timer di recupero parte da solo — e continua a contare anche a schermo spento, con il cronometro nella tendina delle notifiche. |
| **La tua scheda** | Creala parlando con l'assistente o a mano. La rotazione dei giorni avanza da sé quando concludi un allenamento. |
| **Progressi veri** | Record personali, volume settimana per settimana, calendario, storico completo senza limiti di giorni. |
| **I dati sono tuoi** | Esportazione in CSV con un tocco. Sincronizzazione con Health Connect, se la vuoi. |
| **Accesso senza attrito** | Passkey (impronta o volto), Google, oppure email e password. |

---

## Installazione

AtletAI **non è sul Play Store**: si installa direttamente dall'APK. Android chiederà una conferma in più — è normale per qualunque app distribuita fuori dallo store, e i passaggi sono questi:

1. Scarica l'APK dall'[ultima release](https://github.com/DaviBlade05/atletai/releases/latest).
2. Apri il file. Android dirà che questa origine non è consentita: tocca **Impostazioni**.
3. Attiva **Consenti da questa origine**, torna indietro e conferma l'installazione.
4. Dalla prossima versione non serve più: l'app avvisa da sola quando esce un aggiornamento.

Serve Android 8.0 o successivo. Health Connect richiede un blocco schermo attivo.

---

## Sotto il cofano

Costruita in solitaria, partendo da zero conoscenze di programmazione.

**React Native** ed **Expo** per l'app, con un modulo nativo in **Kotlin** scritto a mano per le cose che JavaScript non può fare: il timer di recupero che sopravvive allo schermo spento, il cronometro nella notifica, la scelta della suoneria dal telefono.

**Supabase** per dati e accesso. Row Level Security su ogni tabella, e ogni scrittura passa da una funzione transazionale: una sessione o entra tutta, o non entra niente. Niente stati a metà.

**Gemini** per l'assistente, dietro una funzione server che tiene la chiave lato suo — l'app non l'ha mai avuta — con tetti su lunghezza del prompt, token e tempo di risposta.

Aggiornamenti via **EAS Update**: le correzioni che non toccano il codice nativo arrivano senza reinstallare niente.

---

## Le versioni

Ogni rilascio ha le sue note, scritte in italiano e per intero: **[github.com/DaviBlade05/atletai/releases](https://github.com/DaviBlade05/atletai/releases)**

L'ultima è la **[1.8.0](https://github.com/DaviBlade05/atletai/releases/latest)**, e non contiene una sola funzione nuova. Una revisione del codice aveva trovato cinque strade per cui l'app poteva cancellare o perdere allenamenti *senza dirlo* — tutte raggiungibili parlando normalmente all'assistente o allenandosi in modo ordinario. Quella versione le chiude, e chiude anche la classe di difetti che le rendeva invisibili: il codice che dichiarava riuscito ciò che era fallito.

I test sono passati da 56 a 362.

---

## Dove sta andando

Il sito tiene una [roadmap onesta](https://atletaii.netlify.app/#roadmap), che separa quello che c'è davvero da quello su cui si sta lavorando — senza confondere le due cose.

In lavorazione: una nuova interfaccia (*Pulse*), e la strada verso il Play Store.

---

## Privacy

Gli allenamenti sono tuoi e restano tuoi. Nessuna pubblicità, nessuna profilazione, nessuna vendita di dati a nessuno. L'informativa completa è su **[atletaii.netlify.app/privacy.html](https://atletaii.netlify.app/privacy.html)**.

---

<div align="center">

Fatto in Italia · [Segnala un problema](https://github.com/DaviBlade05/atletai/issues) · [davi.marr5@gmail.com](mailto:davi.marr5@gmail.com)

</div>

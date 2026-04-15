---
name: contract-generator-italia
description: >
  Generatore di contratti e documenti legali per freelance e PMI italiane. Usa questa
  skill SEMPRE quando l'utente vuole: creare un contratto di prestazione di servizi,
  generare un preventivo professionale, scrivere termini e condizioni per un sito web,
  creare un contratto di collaborazione, generare un NDA (accordo di riservatezza),
  creare un contratto di agenzia, scrivere condizioni generali di vendita, creare un
  contratto SaaS o licenza software, generare una lettera di incarico professionale,
  creare un accordo di partnership, o quando menziona parole come "contratto",
  "preventivo", "termini e condizioni", "NDA", "accordo", "clausola", "penale",
  "risoluzione", "recesso", "prestazione servizi", "collaborazione", "freelance
  contratto", "foro competente", "legge applicabile", "clausola risolutiva". Questa
  skill conosce il Codice Civile italiano (Libro IV â Obbligazioni e Contratti),
  la normativa sui contratti a distanza (D.Lgs. 206/2005), le clausole vessatorie
  (artt. 1341-1342 c.c.), e le best practice contrattuali per il mercato italiano.
---

# Contract Generator Italia â Contratti Professionali in 5 Minuti

Skill professionale di AutomAI (info@lorenzonucci.com).
Genera contratti, preventivi e documenti legali personalizzati per freelance,
consulenti e PMI italiane â conformi al Codice Civile e alle normative vigenti.

**LINGUA:** Default italiano. I contratti per il mercato italiano DEVONO essere in italiano
(Ã¨ la lingua legale). Se l'utente richiede una versione bilingue per un contratto
internazionale, generare italiano + inglese con clausola "in caso di discrepanza
prevale la versione in lingua italiana".

---

## Cosa Fa Questa Skill

Genera 10 tipi di documenti legali personalizzati:
1. Contratto di prestazione di servizi
2. Preventivo professionale (vincolante o non vincolante)
3. NDA / Accordo di riservatezza
4. Termini e condizioni sito web
5. Condizioni generali di vendita
6. Contratto di collaborazione
7. Lettera di incarico professionale
8. Contratto SaaS / licenza software
9. Accordo di partnership
10. Liberatoria / cessione diritti d'autore

---

## Riferimenti Normativi Chiave

### Codice Civile â Libro IV (Obbligazioni e Contratti):
| Articoli | Contenuto |
|----------|-----------|
| 1321-1324 | Nozione e classificazione dei contratti |
| 1325 | Requisiti del contratto (accordo, causa, oggetto, forma) |
| 1326-1328 | Formazione del contratto (proposta e accettazione) |
| 1341-1342 | Clausole vessatorie (doppia firma obbligatoria) |
| 1362-1371 | Interpretazione del contratto |
| 1372-1375 | Effetti del contratto |
| 1382-1384 | Clausola penale |
| 1453-1462 | Risoluzione (inadempimento, impossibilitÃ , eccessiva onerositÃ ) |
| 1467-1469 | Eccessiva onerositÃ  sopravvenuta |
| 1559-1570 | Somministrazione |
| 1655-1677 | Appalto |
| 2222-2228 | Contratto d'opera |
| 2229-2238 | Prestazioni d'opera intellettuale |

### Clausole Vessatorie (Artt. 1341-1342 c.c.):
Queste clausole richiedono DOPPIA FIRMA separata per essere valide:
- Limitazione di responsabilitÃ 
- FacoltÃ  di recedere dal contratto
- Sospensione dell'esecuzione
- Decadenze a carico dell'altro contraente
- Limitazioni alla facoltÃ  di opporre eccezioni
- Clausole compromissorie (arbitrato)
- Deroghe alla competenza dell'autoritÃ  giudiziaria
- Tacito rinnovo
- Clausole penali

### Codice del Consumo (D.Lgs. 206/2005):
Si applica ai contratti B2C (business-to-consumer):
- Diritto di recesso 14 giorni (artt. 52-59)
- Informazioni precontrattuali obbligatorie (art. 49)
- Clausole abusive nei contratti con consumatori (artt. 33-38)
- Garanzia legale 2 anni (artt. 128-135)

### ProprietÃ  Intellettuale:
- L. 633/1941 (Legge diritto d'autore)
- D.Lgs. 30/2005 (Codice proprietÃ  industriale)
- Cessione diritti: deve essere specifica per tipo di utilizzo

---

## Input Richiesti dall'Utente

### Obbligatori:
1. **Tipo di contratto** â Quale documento serve?
2. **Parti coinvolte** â Chi sono le parti? (nomi, ragione sociale, P.IVA/CF, indirizzi)
3. **Oggetto** â Cosa viene prestato/venduto/accordato?
4. **Corrispettivo** â Quanto si paga? Come? Quando?
5. **Durata** â Quanto dura il contratto? Rinnovo tacito?

### Opzionali (con default intelligenti):
6. **Clausola penale** â Importo o percentuale in caso di inadempimento
7. **Recesso** â Preavviso, condizioni, penali di uscita
8. **Foro competente** â Default: foro del prestatore/venditore
9. **Riservatezza** â Clausola NDA integrata o separata
10. **ProprietÃ  intellettuale** â Chi detiene i diritti sugli output?
11. **ResponsabilitÃ ** â Limitazioni, esclusioni, massimali
12. **Pagamento** â ModalitÃ , tempistiche, penali ritardo (D.Lgs. 231/2002)

---

## Workflow Operativo

### Step 1 â Analisi e Scelta Template

Identifica il tipo contrattuale corretto:

```
ANALISI:
- Rapporto: [B2B / B2C / freelance-azienda]
- Tipo: [servizio / vendita / collaborazione / licenza]
- ComplessitÃ : [semplice / media / complessa]
- Normativa applicabile: [C.C. + eventuali normative speciali]
- Clausole vessatorie necessarie: [SÃ/NO â se sÃ¬, quali]
- Consumatore coinvolto: [SÃ/NO â se sÃ¬, applicare Codice Consumo]
```

### Step 2 â Generazione Contratto

Struttura standard per ogni contratto:

```
ââââââââââââââââââââââââââââââââââââââââââââ
CONTRATTO DI [TIPO]
ââââââââââââââââââââââââââââââââââââââââââââ

TRA

[PARTE A] â dati completi
(di seguito "il Committente" / "il Cliente" / "il Licenziante")

E

[PARTE B] â dati completi
(di seguito "il Prestatore" / "il Fornitore" / "il Licenziatario")

di seguito congiuntamente "le Parti"

PREMESSO CHE
- [contesto e motivazioni del contratto]
- [riferimenti a eventuali trattative precedenti]

SI CONVIENE E SI STIPULA QUANTO SEGUE

ââââââââââââââââââââââââââââââââââââââââââââ

ART. 1 â OGGETTO
[Descrizione precisa e dettagliata dell'oggetto del contratto.
PiÃ¹ Ã¨ specifico, meno ambiguitÃ  ci saranno.]

ART. 2 â DURATA
[Data inizio, data fine, condizioni di rinnovo.
Se rinnovo tacito: specificare preavviso per la disdetta.
NOTA: il rinnovo tacito Ã¨ clausola vessatoria â doppia firma.]

ART. 3 â CORRISPETTIVO E PAGAMENTO
[Importo, IVA, modalitÃ  pagamento, tempistiche.
Interessi di mora: D.Lgs. 231/2002 (tasso BCE + 8% per B2B).
Fatturazione: riferimento a fattura elettronica.]

ART. 4 â OBBLIGHI DELLE PARTI
4.1 Obblighi del Committente: [elenco]
4.2 Obblighi del Prestatore: [elenco]

ART. 5 â PROPRIETÃ INTELLETTUALE
[Chi detiene i diritti? Cessione totale, licenza, uso limitato?
Specificare per tipo: riproduzione, distribuzione, modifica.]

ART. 6 â RISERVATEZZA
[Definizione informazioni riservate, durata obbligo,
eccezioni, penali per violazione.]

ART. 7 â TRATTAMENTO DATI PERSONALI
[Riferimento GDPR, ruoli (titolare/responsabile),
rinvio a DPA separato se necessario.]

ART. 8 â RESPONSABILITÃ E LIMITAZIONI
[Massimale di responsabilitÃ , esclusioni.
NOTA: la limitazione di responsabilitÃ  Ã¨ clausola vessatoria â doppia firma.]

ART. 9 â CLAUSOLA PENALE
[Importo o percentuale per inadempimento.
NOTA: clausola penale Ã¨ vessatoria â doppia firma.]

ART. 10 â RISOLUZIONE E RECESSO
10.1 Risoluzione per inadempimento (art. 1453 c.c.): [condizioni]
10.2 Clausola risolutiva espressa (art. 1456 c.c.): [eventi specifici]
10.3 Recesso: [preavviso, modalitÃ , conseguenze economiche]
[NOTA: facoltÃ  di recesso Ã¨ clausola vessatoria â doppia firma.]

ART. 11 â FORZA MAGGIORE
[Definizione, effetti, termine sospensione, risoluzione automatica.]

ART. 12 â LEGGE APPLICABILE E FORO COMPETENTE
Il presente contratto Ã¨ regolato dalla legge italiana.
Per ogni controversia sarÃ  competente in via esclusiva il Foro di [CITTÃ].
[NOTA: deroga alla competenza Ã¨ clausola vessatoria â doppia firma.]

ART. 13 â DISPOSIZIONI FINALI
[Clausola di integritÃ , comunicazioni, modifiche solo per iscritto.]

ââââââââââââââââââââââââââââââââââââââââââââ

CLAUSOLE VESSATORIE ex artt. 1341-1342 c.c.
Ai sensi e per gli effetti degli artt. 1341 e 1342 del Codice Civile,
le Parti dichiarano di aver letto e di approvare specificamente le
seguenti clausole:
- Art. [N] â [Titolo clausola]
- Art. [N] â [Titolo clausola]
- Art. [N] â [Titolo clausola]

Firma Parte A: _________________________
Firma Parte B: _________________________

ââââââââââââââââââââââââââââââââââââââââââââ

Luogo e data: [CITTÃ], [DATA]

Firma Parte A: _________________________
Firma Parte B: _________________________
```

### Step 3 â Verifica Clausole Vessatorie

```
CHECKLIST CLAUSOLE VESSATORIE:
â Tutte le clausole vessatorie identificate?
â Elenco specifico in fondo al contratto?
â Doppia firma prevista per le clausole vessatorie?
â Se B2C: verificato anche artt. 33-38 Codice Consumo?
â Se B2C: diritto di recesso 14 giorni menzionato?
```

---

## Template per Tipo di Contratto

### 1. Preventivo Professionale:
```
Struttura:
- Intestazione professionale
- Destinatario
- Oggetto del preventivo
- Descrizione dettagliata dei servizi
- Tabella: Voce | Descrizione | QuantitÃ  | Prezzo unitario | Totale
- Subtotale, IVA, Totale
- Tempistiche di consegna
- ValiditÃ  del preventivo (30 giorni default)
- Condizioni di pagamento
- Esclusioni (cosa NON Ã¨ incluso)
- Firma per accettazione

Note: se il preventivo Ã¨ accettato diventa VINCOLANTE (art. 1326 c.c.)
```

### 2. NDA (Accordo di Riservatezza):
```
Elementi essenziali:
- Definizione "Informazioni Riservate" (ampia ma specifica)
- Durata obbligo (2-5 anni dalla cessazione del rapporto)
- Eccezioni: informazioni pubbliche, giÃ  note, ricevute da terzi
- Obblighi: non divulgare, proteggere, limitare accesso
- Restituzione/distruzione alla scadenza
- Penale per violazione
- Foro competente
```

### 3. Termini e Condizioni Sito Web:
```
Sezioni obbligatorie:
1. IdentitÃ  del titolare (ragione sociale, P.IVA, sede, contatti)
2. Oggetto del servizio
3. Condizioni di utilizzo
4. ProprietÃ  intellettuale dei contenuti
5. Limitazione di responsabilitÃ 
6. Modifiche ai T&C
7. Legge applicabile e foro
+ Se e-commerce: condizioni di vendita, reso, garanzia (Codice Consumo)
```

### 4. Contratto SaaS / Licenza Software:
```
Elementi specifici:
- Tipo di licenza (uso, non esclusiva, non trasferibile)
- SLA (Service Level Agreement) con uptime garantito
- Supporto tecnico: livelli e tempi di risposta
- Backup e sicurezza dati
- ProprietÃ  del codice vs. proprietÃ  dei dati dell'utente
- Condizioni di scaling (utenti, storage, API)
- Procedura di migrazione dati alla cessazione
```

---

## Regole e Vincoli

### COSA FARE:
1. SEMPRE identificare e segnalare le clausole vessatorie
2. SEMPRE prevedere la doppia firma per le clausole vessatorie
3. SEMPRE specificare legge applicabile e foro competente
4. SEMPRE includere la clausola sul trattamento dati (GDPR)
5. SEMPRE usare un linguaggio preciso ma comprensibile
6. SEMPRE numerare gli articoli in modo chiaro
7. Se B2C: SEMPRE includere riferimenti al Codice del Consumo
8. Specificare gli interessi di mora per i ritardi di pagamento
9. Indicare che le modifiche devono essere scritte

### COSA NON FARE:
1. MAI dimenticare le clausole vessatorie â puÃ² rendere nulle le clausole
2. MAI usare clausole abusive nei contratti B2C (artt. 33-38 Codice Consumo)
3. MAI omettere la doppia firma dove richiesta
4. MAI usare termini ambigui per l'oggetto del contratto
5. MAI indicare penali manifestamente eccessive (riducibili dal giudice, art. 1384 c.c.)
6. MAI dimenticare la clausola di forza maggiore (post-COVID Ã¨ essenziale)
7. MAI omettere le esclusioni (cosa NON Ã¨ incluso nel servizio)
8. MAI generare contratti per attivitÃ  illegali
9. MAI dare consulenza legale â specificare che Ã¨ un supporto operativo
10. NON usare un formato che sembri un copia-incolla generico

---

## Esempio Completo

### Input:
```
"Contratto di prestazione servizi per sviluppo sito web.
Prestatore: Marco Bianchi, P.IVA 01234567890, via Roma 10, Livorno.
Cliente: ABC Srl, P.IVA 09876543210, via Milano 5, Firenze.
Importo: â¬3000 + IVA, pagamento 50% anticipo e 50% alla consegna.
Durata: 60 giorni. ProprietÃ  intellettuale al cliente dopo il saldo."
```

### Output (estratto):

```
ââââââââââââââââââââââââââââââââââââââââââââ
CONTRATTO DI PRESTAZIONE DI SERVIZI

TRA
ABC Srl, P.IVA 09876543210, con sede in via Milano 5, 50100 Firenze (FI)
(di seguito "il Committente")

E
Marco Bianchi, P.IVA 01234567890, con sede in via Roma 10, 57100 Livorno (LI)
(di seguito "il Prestatore")

ART. 1 â OGGETTO
Il Prestatore si impegna a progettare e sviluppare un sito web per il
Committente, comprensivo di design, sviluppo frontend e backend, testing
e messa online.

ART. 3 â CORRISPETTIVO E PAGAMENTO
Il corrispettivo per la prestazione Ã¨ fissato in â¬3.000,00 (tremila/00)
oltre IVA 22%, per un totale di â¬3.660,00.
Il pagamento avverrÃ  come segue:
a) â¬1.830,00 alla firma del presente contratto (anticipo 50%)
b) â¬1.830,00 alla consegna e approvazione del lavoro (saldo 50%)
ModalitÃ : bonifico bancario. In caso di ritardo si applicano gli interessi
di mora ex D.Lgs. 231/2002.

ART. 5 â PROPRIETÃ INTELLETTUALE
La titolaritÃ  di tutti i diritti di proprietÃ  intellettuale relativi al
sito web sarÃ  trasferita al Committente al momento del pagamento del saldo.
[...]

CLAUSOLE VESSATORIE ex artt. 1341-1342 c.c.
Le Parti approvano specificamente:
- Art. 8 â Limitazione di responsabilitÃ 
- Art. 10 â FacoltÃ  di recesso
- Art. 12 â Deroga alla competenza del foro

Firma Committente: _________________________
Firma Prestatore: _________________________
```

---

## Disclaimer

I contratti generati da questa skill sono template personalizzati basati sulla normativa italiana vigente. Rappresentano un supporto operativo e NON sostituiscono la consulenza di un avvocato. Per contratti di valore elevato o situazioni complesse, si raccomanda sempre la revisione di un professionista legale.

---
name: fattura-facile-italia
description: >
  Generatore di fatture elettroniche italiane conformi alla normativa. Usa questa skill
  SEMPRE quando l'utente vuole: creare una fattura elettronica, generare XML FatturaPA,
  calcolare IVA italiana (aliquote 4%, 5%, 10%, 22%), gestire ritenuta d'acconto,
  creare fatture per regime forfettario, generare note di credito, calcolare bollo
  virtuale da â¬2, preparare fatture per la PA (Pubblica Amministrazione), verificare
  la conformitÃ  di una fattura al formato SDI, o quando menziona parole come "fattura",
  "fatturazione", "IVA", "SDI", "FatturaPA", "codice destinatario", "regime forfettario",
  "ritenuta d'acconto", "nota di credito", "bollo", "split payment", "reverse charge",
  "codice fiscale", "partita IVA", "XML fattura", "fattura elettronica". Questa skill
  conosce TUTTA la normativa italiana sulla fatturazione elettronica aggiornata al 2026,
  inclusi codici natura IVA (N1-N7), tipi documento (TD01-TD28), regimi fiscali, e
  formattazione XML conforme allo SDI.
---

# Fattura Facile Italia â Fatture Elettroniche in 30 Secondi

Skill professionale di AutomAI (info@lorenzonucci.com).
Genera fatture elettroniche italiane conformi al 100% alla normativa, in formato
XML FatturaPA pronto per lo SDI, oppure in formato leggibile (HTML/PDF).

---

## Cosa Fa Questa Skill

Trasforma un input naturale ("fattura per Mario Rossi, consulenza web â¬500") in:
- Fattura elettronica completa in formato XML FatturaPA 1.2.2
- Versione leggibile HTML con layout professionale
- Calcolo automatico IVA, ritenuta d'acconto, bollo, cassa previdenziale
- Numerazione progressiva automatica
- ConformitÃ  SDI al 100%

**LINGUA:** Sempre italiano (la fatturazione elettronica italiana Ã¨ per definizione in italiano).

---

## Normativa di Riferimento (Aggiornata 2026)

### Aliquote IVA Italia:
| Aliquota | Applicazione |
|----------|-------------|
| 22% | Aliquota ordinaria (default) |
| 10% | Ridotta â alimentari, turismo, ristrutturazioni |
| 5% | Super-ridotta â alcuni alimentari base |
| 4% | Minima â prima necessitÃ , editoria |
| 0% | Esente/non imponibile (con codice Natura) |

### Codici Natura IVA (quando aliquota = 0):
| Codice | Significato |
|--------|-------------|
| N1 | Escluse ex art. 15 |
| N2.1 | Non soggette â artt. 7-7septies (UE) |
| N2.2 | Non soggette â altri casi |
| N3.1 | Non imponibili â esportazioni |
| N3.2 | Non imponibili â cessioni intracomunitarie |
| N3.3 | Non imponibili â verso San Marino |
| N3.4 | Non imponibili â operazioni assimilate |
| N3.5 | Non imponibili â dichiarazione intento |
| N3.6 | Non imponibili â altre operazioni |
| N4 | Esenti |
| N5 | Regime del margine / IVA non esposta |
| N6.1 | Reverse charge â cessione rottami |
| N6.2 | Reverse charge â cessione oro/argento |
| N6.3 | Reverse charge â subappalto edilizia |
| N6.4 | Reverse charge â cessione fabbricati |
| N6.5 | Reverse charge â telefoni cellulari |
| N6.6 | Reverse charge â prodotti elettronici |
| N6.7 | Reverse charge â settore energetico |
| N6.8 | Reverse charge â settore energetico |
| N6.9 | Reverse charge â altri casi |
| N7 | IVA assolta in altro stato UE |

### Tipi Documento piÃ¹ comuni:
| Codice | Tipo |
|--------|------|
| TD01 | Fattura |
| TD02 | Acconto/anticipo su fattura |
| TD04 | Nota di credito |
| TD05 | Nota di debito |
| TD06 | Parcella (professionisti) |
| TD24 | Fattura differita |
| TD25 | Fattura differita (triangolazione) |
| TD26 | Cessione beni ammortizzabili |

### Regimi Fiscali:
| Codice | Regime |
|--------|--------|
| RF01 | Ordinario |
| RF02 | Contribuenti minimi |
| RF04 | Agricoltura |
| RF19 | Forfettario (regime agevolato) |

### Regole Bollo Virtuale:
- Obbligatorio se importo > â¬77,47 e operazione esente/fuori campo IVA
- Importo: â¬2,00
- Indicare in fattura: `<DatiBollo><BolloVirtuale>SI</BolloVirtuale><ImportoBollo>2.00</ImportoBollo></DatiBollo>`

### Ritenuta d'Acconto:
- Professionisti: 20% sull'imponibile (standard)
- Agenti: 23% sul 50% = 11,50% effettivo
- Tipo ritenuta: RT01 (persone fisiche), RT02 (persone giuridiche)
- Causale pagamento: A (lavoro autonomo), C (utili), ecc.

### Cassa Previdenziale:
| Codice | Cassa |
|--------|-------|
| TC01 | Cassa nazionale previdenza avvocati |
| TC02 | Cassa ingegneri e architetti (Inarcassa) |
| TC03 | Cassa geometri |
| TC04 | Cassa commercialisti (CNPADC) |
| TC07 | ENASARCO (agenti) |
| TC22 | INPS gestione separata |

---

## Input Richiesti dall'Utente

### Obbligatori:
1. **Dati emittente** â Ragione sociale/Nome, P.IVA, indirizzo, regime fiscale
2. **Dati cliente** â Ragione sociale/Nome, P.IVA o Codice Fiscale, indirizzo
3. **Codice destinatario** â 7 caratteri (o PEC per chi non ha codice SDI)
4. **Descrizione servizio/prodotto** â Cosa Ã¨ stato venduto/prestato
5. **Importo** â Prezzo unitario e quantitÃ 
6. **Aliquota IVA** â O indicazione del regime (forfettario, esente, ecc.)

### Opzionali (dedotti automaticamente se possibile):
7. **Tipo documento** â TD01 default, TD06 per professionisti, TD04 per note credito
8. **Ritenuta d'acconto** â Auto-calcolata se professionista con RF01
9. **Cassa previdenziale** â In base alla categoria professionale
10. **Bollo** â Auto-calcolato se operazione esente > â¬77,47
11. **Condizioni pagamento** â TP01 (rata), TP02 (completo), TP03 (anticipo)
12. **ModalitÃ  pagamento** â MP05 (bonifico), MP01 (contanti), MP08 (carta), ecc.
13. **Numero fattura** â Se non fornito, suggerisci formato progressivo
14. **Data fattura** â Default: oggi

### Dati salvati (per fatture ricorrenti):
Se l'utente ha giÃ  emesso fatture, ricorda i dati emittente e riutilizzali.

---

## Workflow Operativo

### Step 1 â Raccolta Dati e Validazione

Raccogli i dati e valida:

```
VALIDAZIONE:
â P.IVA emittente: formato corretto (11 cifre)
â P.IVA/CF cliente: formato corretto
â Codice destinatario: 7 caratteri alfanumerici (o "0000000" se PEC)
â Regime fiscale: coerente con l'operazione
â Aliquota IVA: coerente con la tipologia di operazione
â Se forfettario (RF19): IVA = 0, Natura = N2.2, no ritenuta
â Se esente: verificare codice Natura corretto
â Se importo esente > â¬77,47: bollo obbligatorio
â Se professionista: verificare ritenuta e cassa previdenziale
```

### Step 2 â Calcolo Importi

```
CALCOLO FATTURA:
âââââââââââââââââââââââââââââââââââââââââ
Descrizione: [dal brief]
QuantitÃ : [N]
Prezzo unitario: â¬ [X]
âââââââââââââââââââââââââââââââââââââââââ
Imponibile:                    â¬ [X * N]
+ Cassa previdenziale [X]%:   â¬ [se applicabile]
= Base imponibile:             â¬ [totale]
IVA [aliquota]%:               â¬ [calcolo]
- Ritenuta d'acconto [X]%:    â¬ [se applicabile]
+ Bollo:                       â¬ [2.00 se applicabile]
âââââââââââââââââââââââââââââââââââââââââ
TOTALE FATTURA:                â¬ [finale]
NETTO A PAGARE:                â¬ [totale - ritenuta]
âââââââââââââââââââââââââââââââââââââââââ
```

### Step 3 â Generazione XML FatturaPA

Genera il file XML completo e valido:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<p:FatturaElettronica versione="FPR12"
  xmlns:ds="http://www.w3.org/2000/09/xmldsig#"
  xmlns:p="http://ivaservizi.agenziaentrate.gov.it/docs/xsd/fatture/v1.2">

  <FatturaElettronicaHeader>
    <DatiTrasmissione>
      <IdTrasmittente>
        <IdPaese>IT</IdPaese>
        <IdCodice>[P.IVA EMITTENTE]</IdCodice>
      </IdTrasmittente>
      <ProgressivoInvio>[NUMERO]</ProgressivoInvio>
      <FormatoTrasmissione>FPR12</FormatoTrasmissione>
      <CodiceDestinatario>[CODICE 7 CHAR]</CodiceDestinatario>
    </DatiTrasmissione>

    <CedentePrestatore>
      <DatiAnagrafici>
        <IdFiscaleIVA>
          <IdPaese>IT</IdPaese>
          <IdCodice>[P.IVA]</IdCodice>
        </IdFiscaleIVA>
        <Anagrafica>
          <Denominazione>[RAGIONE SOCIALE]</Denominazione>
        </Anagrafica>
        <RegimeFiscale>[RF01/RF19/...]</RegimeFiscale>
      </DatiAnagrafici>
      <Sede>
        <Indirizzo>[VIA]</Indirizzo>
        <CAP>[CAP]</CAP>
        <Comune>[CITTA]</Comune>
        <Provincia>[PROV]</Provincia>
        <Nazione>IT</Nazione>
      </Sede>
    </CedentePrestatore>

    <CessionarioCommittente>
      <!-- [DATI CLIENTE - stessa struttura] -->
    </CessionarioCommittente>
  </FatturaElettronicaHeader>

  <FatturaElettronicaBody>
    <DatiGenerali>
      <DatiGeneraliDocumento>
        <TipoDocumento>[TD01/TD04/TD06]</TipoDocumento>
        <Divisa>EUR</Divisa>
        <Data>[YYYY-MM-DD]</Data>
        <Numero>[NUMERO FATTURA]</Numero>
        <!-- [DatiRitenuta se applicabile] -->
        <!-- [DatiBollo se applicabile] -->
        <!-- [DatiCassaPrevidenziale se applicabile] -->
      </DatiGeneraliDocumento>
    </DatiGenerali>

    <DatiBeniServizi>
      <DettaglioLinee>
        <NumeroLinea>1</NumeroLinea>
        <Descrizione>[DESCRIZIONE]</Descrizione>
        <Quantita>[QTA]</Quantita>
        <PrezzoUnitario>[PREZZO]</PrezzoUnitario>
        <PrezzoTotale>[TOTALE LINEA]</PrezzoTotale>
        <AliquotaIVA>[ALIQUOTA]</AliquotaIVA>
        <!-- <Natura>[N2.2 etc. se IVA=0]</Natura> -->
      </DettaglioLinee>
      <DatiRiepilogo>
        <AliquotaIVA>[ALIQUOTA]</AliquotaIVA>
        <ImponibileImporto>[IMPONIBILE]</ImponibileImporto>
        <Imposta>[IVA CALCOLATA]</Imposta>
        <EsigibilitaIVA>I</EsigibilitaIVA>
        <!-- <Natura>[se applicabile]</Natura> -->
      </DatiRiepilogo>
    </DatiBeniServizi>

    <DatiPagamento>
      <CondizioniPagamento>[TP02]</CondizioniPagamento>
      <DettaglioPagamento>
        <ModalitaPagamento>[MP05]</ModalitaPagamento>
        <ImportoPagamento>[NETTO A PAGARE]</ImportoPagamento>
      </DettaglioPagamento>
    </DatiPagamento>
  </FatturaElettronicaBody>
</p:FatturaElettronica>
```

### Step 4 â Generazione Versione Leggibile (HTML)

Genera anche una versione HTML professionale della fattura con:
- Logo e dati emittente in header
- Dati cliente
- Tabella dettaglio con righe, quantitÃ , prezzi
- Riepilogo IVA
- Totali
- Condizioni di pagamento
- Footer con dati fiscali

### Step 5 â Verifica Finale

```
CHECKLIST CONFORMITÃ SDI:
â Formato XML valido (well-formed)
â Versione FPR12 (privati) o FPA12 (PA)
â P.IVA emittente presente e valida
â P.IVA/CF cliente presente
â Codice destinatario corretto (7 char o "0000000")
â Tipo documento coerente
â Aliquota IVA o Natura compilata (MAI entrambi)
â Se Natura presente â aliquota = 0.00
â Totale documento calcolato correttamente
â Arrotondamenti a 2 decimali (centesimi)
â Bollo presente se dovuto
â Ritenuta calcolata se professionista ordinario
â Data formato YYYY-MM-DD
â Importi con punto decimale (non virgola) nell'XML
```

---

## Casi d'Uso Specifici

### Forfettario che fattura a un'azienda:
```
Input: "Fattura per consulenza web, â¬2000, sono forfettario"
â IVA: 0% con Natura N2.2
â Regime: RF19
â NO ritenuta d'acconto (i forfettari non la subiscono)
â Bollo: â¬2,00 (importo > â¬77,47 e operazione non soggetta IVA)
â Dicitura obbligatoria: "Operazione effettuata ai sensi dell'art. 1, 
  commi da 54 a 89, L. 190/2014 â Regime forfettario"
```

### Professionista ordinario (avvocato):
```
Input: "Parcella avvocato, â¬3000, cliente SpA"
â Tipo documento: TD06 (parcella)
â Cassa previdenziale: TC01 (4% Cassa Forense)
â Base imponibile: â¬3000 + â¬120 (cassa 4%) = â¬3120
â IVA 22%: â¬686,40
â Ritenuta: 20% su â¬3000 = â¬600
â Totale: â¬3806,40
â Netto a pagare: â¬3206,40
```

### Nota di credito:
```
Input: "Nota di credito per fattura n. 15 del 10/03/2026, errore importo"
â Tipo documento: TD04
â Riferimento fattura originale nei DatiGenerali
â Importi identici alla fattura ma come storno
```

### Fattura per la PA (Pubblica Amministrazione):
```
Input: "Fattura per consulenza al Comune di Livorno, â¬5000"
â FormatoTrasmissione: FPA12 (non FPR12)
â Codice destinatario: 6 caratteri (codice IPA/UFE, non 7)
â Campi obbligatori aggiuntivi:
  - CIG (Codice Identificativo Gara) se applicabile
  - CUP (Codice Unico Progetto) se applicabile
  - Riferimento amministrazione
â Split payment (scissione pagamenti) se previsto dalla PA
â EsigibilitÃ  IVA: S (split payment) invece di I (immediata)
```

### Fattura con piÃ¹ aliquote IVA:
```
Input: "Vendita: 10 libri a â¬20 (IVA 4%) + consulenza â¬500 (IVA 22%)"
â Due DettaglioLinee con aliquote diverse
â Due DatiRiepilogo separati
â Totale calcolato come somma dei singoli
```

---

## Regole e Vincoli

### COSA FARE:
1. SEMPRE validare P.IVA e Codice Fiscale (formato, non esistenza)
2. SEMPRE calcolare il bollo se dovuto (esente + importo > â¬77,47)
3. SEMPRE includere la dicitura obbligatoria per i forfettari
4. SEMPRE usare arrotondamento a 2 decimali
5. SEMPRE specificare Natura quando IVA = 0
6. SEMPRE generare XML well-formed e conforme allo schema XSD
7. Suggerire il codice destinatario "0000000" se il cliente usa la PEC
8. Calcolare automaticamente cassa previdenziale per categorie note
9. Proporre numerazione progressiva (es. 2026/001, 2026/002)

### COSA NON FARE:
1. MAI compilare sia AliquotaIVA > 0 sia Natura â sono mutuamente esclusivi
2. MAI dimenticare il bollo su operazioni esenti > â¬77,47
3. MAI applicare ritenuta d'acconto ai forfettari
4. MAI usare la virgola come separatore decimale nell'XML (solo punto)
5. MAI generare fatture con data futura
6. MAI inventare P.IVA o Codici Fiscali â chiedere sempre all'utente
7. MAI omettere la dicitura regime forfettario se RF19
8. MAI usare FPA12 per fatture a privati (solo FPR12)
9. MAI usare codice destinatario PA (6 caratteri) per privati (7 caratteri)
10. NON calcolare la cassa previdenziale se non richiesta/non applicabile

---

## Output Disponibili

Su richiesta, questa skill puÃ² generare:
- **XML FatturaPA** pronto per upload su SDI (via intermediario)
- **HTML fattura** â versione leggibile con layout professionale
- **Riepilogo calcoli** â breakdown dettagliato di tutti gli importi
- **Fattura ricorrente** â template da riusare ogni mese con lo stesso cliente
- **Registro fatture** â tabella riepilogativa di tutte le fatture emesse
- **Calcolo trimestrale IVA** â somma IVA a debito/credito per liquidazione

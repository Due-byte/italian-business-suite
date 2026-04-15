---
name: gdpr-compliance-checker-italia
description: >
  Verifica conformitÃ  GDPR e genera documenti privacy per aziende italiane. Usa questa
  skill SEMPRE quando l'utente vuole: verificare se un sito web Ã¨ conforme al GDPR,
  generare una privacy policy, creare un cookie banner conforme, scrivere informativa
  privacy (art. 13/14), generare un registro dei trattamenti (art. 30), creare un
  DPIA (Data Protection Impact Assessment), scrivere clausole contrattuali per DPA
  (Data Processing Agreement), verificare la conformitÃ  di un form di contatto,
  controllare la gestione dei consensi, o quando menziona parole come "GDPR", "privacy",
  "cookie", "privacy policy", "informativa", "consenso", "dati personali", "trattamento
  dati", "Garante Privacy", "registro trattamenti", "DPIA", "DPO", "data breach",
  "diritto all'oblio", "portabilitÃ  dati", "base giuridica", "legittimo interesse",
  "cookie banner". Questa skill conosce il GDPR (Reg. UE 2016/679), il D.Lgs. 196/2003
  (Codice Privacy italiano) aggiornato al D.Lgs. 101/2018, le Linee Guida del Garante
  Privacy italiano sui cookie (2021/2022) e le principali delibere e sanzioni.
---

# GDPR Compliance Checker Italia â Privacy a Norma in 5 Minuti

Skill professionale di AutomAI (info@lorenzonucci.com).
Verifica la conformitÃ  GDPR di siti web, app e processi aziendali, e genera tutti i
documenti privacy necessari â specifici per la normativa italiana.

**LINGUA:** Default italiano. I documenti privacy possono essere generati in inglese
se l'utente ha un sito/servizio internazionale â chiedere in quale lingua serve.

---

## Cosa Fa Questa Skill

Due modalitÃ  operative:

**MODALITÃ 1 â AUDIT:** Analizza un sito web/processo basandosi sulle informazioni fornite dall'utente (strumenti usati, dati raccolti, configurazione cookie, ecc.) e identifica le non-conformitÃ  GDPR con prioritÃ  (critico, alto, medio, basso) e azioni correttive specifiche. NOTA: Claude non puÃ² visitare direttamente i siti web â l'audit si basa su ciÃ² che l'utente descrive. Chiedi all'utente di elencare: tool installati, tipo di cookie banner, testo dell'informativa, form presenti, strumenti di terze parti.

**MODALITÃ 2 â GENERAZIONE:** Crea documenti privacy completi e personalizzati: privacy policy, cookie policy, informative, registro trattamenti, DPIA, DPA, consensi.

---

## Normativa di Riferimento

### Fonti principali:
- **GDPR** â Regolamento (UE) 2016/679 del 27 aprile 2016
- **Codice Privacy** â D.Lgs. 196/2003 modificato dal D.Lgs. 101/2018
- **Linee Guida Cookie** â Garante Privacy, provvedimento 10 giugno 2021 (n. 231)
- **Linee Guida Consenso** â EDPB Guidelines 05/2020
- **Linee Guida DPO** â WP243 rev.01
- **Linee Guida DPIA** â WP248 rev.01

### Basi giuridiche del trattamento (Art. 6 GDPR):
| Base | Quando si usa |
|------|--------------|
| Consenso (art. 6.1.a) | Marketing, profilazione, cookie non tecnici |
| Esecuzione contratto (art. 6.1.b) | Fornitura servizio richiesto, gestione ordini |
| Obbligo legale (art. 6.1.c) | Fatturazione, adempimenti fiscali, antiriciclaggio |
| Interesse vitale (art. 6.1.d) | Emergenze sanitarie (raramente applicabile) |
| Interesse pubblico (art. 6.1.e) | PA, enti pubblici |
| Legittimo interesse (art. 6.1.f) | Sicurezza, prevenzione frodi, marketing diretto a clienti esistenti |

### Categorie cookie e consenso:
| Categoria | Consenso richiesto | Esempio |
|-----------|-------------------|---------|
| Tecnici/necessari | NO | Sessione, carrello, preferenze lingua |
| Analitici first-party (anonimizzati) | NO (con condizioni*) | Matomo, GA4 con IP anonimizzato |
| Analitici third-party | SÃ | Google Analytics standard |
| Profilazione | SÃ (esplicito) | Facebook Pixel, remarketing |
| Marketing | SÃ | Newsletter popup, chat marketing |

*Condizioni per analitici senza consenso: first-party, IP troncato, no cross-site, no cessione a terzi.

### Sanzioni principali GDPR:
- **Fino a â¬10 milioni o 2% fatturato**: violazioni registro trattamenti, sicurezza, DPO, DPIA
- **Fino a â¬20 milioni o 4% fatturato**: violazioni principi base, consenso, diritti interessati, trasferimenti extra-UE
- Garante italiano: nel 2025 ha emesso sanzioni per oltre â¬50 milioni

### Diritti degli interessati (Artt. 15-22):
1. Diritto di accesso (art. 15)
2. Diritto di rettifica (art. 16)
3. Diritto alla cancellazione / oblio (art. 17)
4. Diritto di limitazione (art. 18)
5. Diritto alla portabilitÃ  (art. 20)
6. Diritto di opposizione (art. 21)
7. Diritto a non essere sottoposti a decisioni automatizzate (art. 22)

---

## Input Richiesti dall'Utente

### Per AUDIT:
1. **URL del sito web** o descrizione del processo aziendale
2. **Tipo di business** â E-commerce, servizi, SaaS, studio professionale, ecc.
3. **Dati trattati** â Che dati raccoglie? (nome, email, telefono, pagamenti, salute...)
4. **Strumenti usati** â Google Analytics, Mailchimp, Facebook Pixel, CRM, ecc.
5. **Target utenti** â Solo Italia, UE, globale? Minori inclusi?

### Per GENERAZIONE DOCUMENTI:
1. **Tipo documento** â Privacy policy, cookie policy, informativa, registro, DPIA, DPA
2. **Dati azienda** â Ragione sociale, P.IVA, sede, email privacy, DPO (se nominato)
3. **Trattamenti effettuati** â Lista dei dati raccolti e finalitÃ 
4. **Strumenti/fornitori** â Tool di terze parti che trattano dati
5. **Trasferimenti extra-UE** â Usano server fuori dall'UE? (AWS US, Google US, ecc.)

---

## Workflow MODALITÃ 1 â Audit ConformitÃ 

### Step 1 â Checklist Analisi

Analizza ogni area e assegna un punteggio di conformitÃ :

```
AUDIT GDPR â [NOME SITO/AZIENDA]
Data: [DATA]
Analista: AutomAI GDPR Compliance Checker

âââââââââââââââââââââââââââââââââââââââââââââââ
AREA 1: COOKIE E CONSENSO
âââââââââââââââââââââââââââââââââââââââââââââââ

â Cookie banner presente al primo accesso
â Banner blocca cookie non tecnici PRIMA del consenso
â Pulsante "Rifiuta tutto" presente e UGUALE visibilitÃ  di "Accetta tutto"
â Nessun cookie non tecnico installato prima del consenso
â PossibilitÃ  di scegliere categorie singole
â Link a cookie policy completa dal banner
â Cookie wall assente (non blocca l'accesso al sito)
â Consenso registrato con timestamp
â PossibilitÃ  di revocare il consenso facilmente
â Scroll e navigazione NON contano come consenso
â Cookie policy elenca TUTTI i cookie con finalitÃ  e durata

ConformitÃ : [X/11] â [CRITICO/ALTO/MEDIO/BASSO]

âââââââââââââââââââââââââââââââââââââââââââââââ
AREA 2: INFORMATIVA PRIVACY (Art. 13/14)
âââââââââââââââââââââââââââââââââââââââââââââââ

â Informativa presente e raggiungibile da ogni pagina
â IdentitÃ  e contatti del titolare
â Contatti DPO (se nominato)
â FinalitÃ  del trattamento per ogni tipologia di dato
â Base giuridica per ogni finalitÃ 
â Categorie di destinatari
â Trasferimenti extra-UE e garanzie (SCC, adequacy decision)
â Periodo di conservazione per ogni finalitÃ 
â Diritti dell'interessato elencati tutti (artt. 15-22)
â Diritto di reclamo al Garante Privacy
â Se consenso: indicazione che Ã¨ revocabile
â Se legittimo interesse: specificato quale
â Linguaggio chiaro, comprensibile, non legalese
â Data ultimo aggiornamento

ConformitÃ : [X/14] â [CRITICO/ALTO/MEDIO/BASSO]

âââââââââââââââââââââââââââââââââââââââââââââââ
AREA 3: FORM E RACCOLTA DATI
âââââââââââââââââââââââââââââââââââââââââââââââ

â Ogni form ha link all'informativa privacy
â Consenso marketing separato dal consenso al servizio
â Checkbox marketing non pre-spuntata
â Double opt-in per newsletter
â Dati raccolti minimizzati (solo il necessario)
â Form di contatto: no campi superflui
â Se raccolta dati sensibili (salute, etc.): consenso esplicito

ConformitÃ : [X/7] â [CRITICO/ALTO/MEDIO/BASSO]

âââââââââââââââââââââââââââââââââââââââââââââââ
AREA 4: SICUREZZA E ORGANIZZAZIONE
âââââââââââââââââââââââââââââââââââââââââââââââ

â HTTPS attivo su tutto il sito
â Registro dei trattamenti (art. 30) presente
â Procedura data breach documentata
â DPO nominato (se obbligatorio: PA, trattamenti su larga scala, dati sensibili)
â Formazione dipendenti documentata
â Contratti DPA con tutti i responsabili del trattamento
â Backup e disaster recovery
â Accesso ai dati limitato per ruolo (need-to-know)

ConformitÃ : [X/8] â [CRITICO/ALTO/MEDIO/BASSO]

âââââââââââââââââââââââââââââââââââââââââââââââ
AREA 5: DIRITTI DEGLI INTERESSATI
âââââââââââââââââââââââââââââââââââââââââââââââ

â Procedura per rispondere a richieste di accesso (30 giorni)
â Procedura per cancellazione dati
â Procedura per portabilitÃ  dati
â Canale dedicato per richieste (email privacy, form dedicato)
â Procedura per reclami

ConformitÃ : [X/5] â [CRITICO/ALTO/MEDIO/BASSO]
```

### Step 2 â Report con PrioritÃ 

```
âââââââââââââââââââââââââââââââââââââââââââââââ
RIEPILOGO AUDIT
âââââââââââââââââââââââââââââââââââââââââââââââ

Punteggio globale: [X/45] â [VOTO]

ð´ CRITICHE (rischio sanzione immediata):
1. [Problema] â [Azione correttiva] â [Tempo stimato]
2. ...

ð  ALTE (rischio elevato):
1. [Problema] â [Azione correttiva] â [Tempo stimato]
2. ...

ð¡ MEDIE (da risolvere):
1. [Problema] â [Azione correttiva] â [Tempo stimato]
2. ...

ð¢ BASSE (miglioramenti consigliati):
1. [Problema] â [Azione correttiva] â [Tempo stimato]
2. ...

PIANO D'AZIONE:
- Settimana 1: Risolvere tutte le criticitÃ  ð´
- Settimana 2: Risolvere le prioritÃ  alte ð 
- Mese 1: Risolvere le medie ð¡
- Ongoing: Implementare i miglioramenti ð¢

STIMA RISCHIO SANZIONE: â¬ [range stimato basato sulle violazioni]
```

---

## Workflow MODALITÃ 2 â Generazione Documenti

### Documento 1: Privacy Policy

Genera una privacy policy completa in italiano che includa:
- Titolare del trattamento (identitÃ , contatti, sede)
- DPO (se presente)
- Dati raccolti (elenco specifico per il business)
- FinalitÃ  e base giuridica per ciascuna
- Destinatari e categorie
- Trasferimenti extra-UE
- Periodi di conservazione (specifici, non generici)
- Diritti dell'interessato (tutti, artt. 15-22)
- Diritto di reclamo al Garante (con indirizzo e sito)
- Cookie (riferimento a cookie policy separata)
- Data e versione

**Regola**: linguaggio chiaro, paragrafi brevi, NO legalese incomprensibile.

### Documento 2: Cookie Policy

Genera una cookie policy con:
- Cosa sono i cookie (breve)
- Tabella di TUTTI i cookie usati:
  | Nome | Fornitore | FinalitÃ  | Durata | Tipo |
- Come gestire i consensi (link a impostazioni)
- Come disabilitare i cookie dal browser
- Riferimenti normativi

### Documento 3: Registro dei Trattamenti (Art. 30)

Tabella strutturata:
| AttivitÃ  | FinalitÃ  | Base giuridica | Categorie dati | Categorie interessati | Destinatari | Trasferimenti extra-UE | Termine cancellazione | Misure sicurezza |

### Documento 4: DPIA (Data Protection Impact Assessment)

Se richiesto, genera un DPIA con:
- Descrizione del trattamento
- NecessitÃ  e proporzionalitÃ 
- Rischi per i diritti e le libertÃ 
- Misure di mitigazione
- Consultazione preventiva (se necessaria)

### Documento 5: Informativa per Form/Newsletter

Versione breve dell'informativa (art. 13) da inserire sotto form:
```
Informativa breve: i tuoi dati saranno trattati da [TITOLARE] per [FINALITÃ], 
sulla base di [BASE GIURIDICA]. Informativa completa: [LINK]. 
Puoi esercitare i tuoi diritti scrivendo a [EMAIL].
```

---

## Regole e Vincoli

### COSA FARE:
1. SEMPRE indicare la base giuridica per OGNI finalitÃ  di trattamento
2. SEMPRE specificare periodi di conservazione concreti (non "il tempo necessario")
3. SEMPRE elencare TUTTI i diritti degli interessati (artt. 15-22)
4. SEMPRE includere i dati di contatto del Garante Privacy italiano
5. SEMPRE verificare che il cookie banner abbia "Rifiuta tutto" visibile
6. SEMPRE controllare se il DPO Ã¨ obbligatorio
7. Usare linguaggio chiaro e comprensibile
8. Personalizzare ogni documento per il business specifico
9. Indicare data e versione su ogni documento

### COSA NON FARE:
1. MAI generare documenti privacy generici/template â DEVONO essere personalizzati
2. MAI dimenticare i trasferimenti extra-UE (Google, Meta, AWS = tutti USA)
3. MAI suggerire "scroll = consenso" â vietato dal Garante dal 2021
4. MAI omettere il pulsante "Rifiuta tutto" dal cookie banner
5. MAI pre-spuntare checkbox di consenso marketing
6. MAI confondere "dati personali" con "dati sensibili" (categorie particolari art. 9)
7. MAI suggerire di raccogliere piÃ¹ dati del necessario (principio di minimizzazione)
8. MAI indicare periodi di conservazione vaghi
9. MAI dimenticare che anche l'email Ã¨ un dato personale
10. NON dare consulenza legale â specificare sempre che Ã¨ un supporto, non un parere legale

---

## Disclaimer

Questa skill genera documenti e analisi basati sulla normativa GDPR e sulla prassi del Garante Privacy italiano. Gli output sono un supporto operativo e NON sostituiscono la consulenza di un professionista legale. Per trattamenti complessi o ad alto rischio, si raccomanda sempre la revisione di un DPO o avvocato specializzato in privacy.

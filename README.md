# Mercato Immobiliare Italia — Power BI

Report interattivo in Power BI sul mercato immobiliare italiano (2016–2018).  
Analizza vendite, affitti e rendimento per tipologia e area geografica, con mappe e confronti rispetto al reddito medio.

## Contenuti del repository

- `/pbix/` — file Power BI Desktop (.pbix)
- `/data/` — dataset d’esempio o connettori (CSV/Excel/SQL)
- `/images/` — screenshot e icone usate nel report
- `/docs/` — note tecniche e specifiche (facoltativo)

> Aggiorna i nomi delle cartelle se diversi nel tuo progetto.

## Requisiti

- Power BI Desktop (ultima versione consigliata)
- Dati disponibili in `/data/` o accesso alle fonti originali
- Permessi di rete per eventuali origini esterne (se previste)

## Avvio rapido

1. Clona il repository.
2. Apri `pbix/Immobiliare_Italia.pbix` con Power BI Desktop.
3. Se richiesto, aggiorna i **percorsi delle origini dati** (Home → Trasforma dati → Impostazioni origine dati).
4. Carica i dati, quindi aggiorna (Home → Aggiorna).

## Struttura del modello (principali tabelle)

- `dati_2016_2018` — fatti per vendite/affitti per comune, tipologia, semestre.
- `Calendar` — tabella calendario con colonne di anno/semestre.
- `irpef_comuni_2017_clean` — reddito medio/mediano per contribuente (a livello territoriale).

Relazioni: `dati_2016_2018` ↔ `Calendar` (sulla data/semestre) e ↔ dimensioni geografiche (Regione/Comune).

## Pagine del report

- **Vendite** — analisi dei comuni con maggior valore di vendita e prezzo medio per tipologia; mappa per area.
- **Affitti** — confronto vendite vs affitto medio per tipologia e classifica dei comuni con affitti più alti.
- **Rendimento** — rendimento annuo stimato e anni per rientrare dell’investimento tramite affitto (YearToBuy).
- **Accessibilità** — prezzo medio al m² vs reddito medio per contribuente e m² acquistabili per regione.

Testo sintetico da posizionare in alto a ogni pagina (casella di testo):
- Vendite: “Analisi delle vendite per tipologia e comuni con i maggiori valori, con dettaglio geografico.”
- Affitti: “Confronto tra prezzo di vendita e affitto medio per tipologia; classifica dei comuni più cari.”
- Rendimento: “Rendimento annuo e anni necessari per rientrare dell’investimento tramite affitto.”
- Accessibilità: “Reddito medio vs prezzi al m² per stimare la superficie acquistabile e l’accessibilità.”

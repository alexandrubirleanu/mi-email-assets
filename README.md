# Manager Indipendente email assets

Repository pubblico per gli asset statici usati nelle email di Manager Indipendente.

## Asset disponibili

| File | Uso consigliato | Dimensioni | Peso |
| --- | --- | ---: | ---: |
| `mi-grafo.png` | Variante chiara per sfondi scuri | 400 × 400 px | 29 KB |
| `mi-grafo-dark.png` | Variante scura per sfondi chiari | 400 × 400 px | 23 KB |

Entrambi i file sono PNG RGBA con sfondo trasparente.

## Utilizzo

Per un'email è preferibile usare un URL assoluto e specificare sempre dimensioni e testo alternativo:

```html
<img
  src="https://raw.githubusercontent.com/alexandrubirleanu/mi-email-assets/main/mi-grafo-dark.png"
  width="80"
  height="80"
  alt="Manager Indipendente"
  style="display:block;border:0;outline:none;text-decoration:none"
/>
```

Per campagne già inviate o template che devono rimanere immutabili, sostituire `main` con lo SHA del commit che contiene l'asset. In questo modo una futura sostituzione del file non modifica retroattivamente il contenuto.

## Regole di pubblicazione

- usare nomi file minuscoli, descrittivi e senza spazi;
- comprimere le immagini prima del commit;
- mantenere lo sfondo trasparente quando previsto dal template;
- non sovrascrivere un asset già usato in produzione: aggiungere una nuova versione;
- verificare il rendering su sfondo chiaro e scuro;
- non inserire dati personali, credenziali o materiale riservato.

La CI controlla firma PNG, dimensioni, presenza del canale alpha e limite di 250 KB per ogni immagine.

## Licenza

Il repository non include al momento una licenza per il riutilizzo da parte di terzi. Gli asset restano destinati alle proprietà e alle comunicazioni autorizzate di Manager Indipendente.

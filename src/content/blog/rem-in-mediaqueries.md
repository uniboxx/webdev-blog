---
title: 'Unità di misura "rem" nelle media query'
description: 'Perchè usare l&apos;unità di misura relativa "rem" invece dell&apos;unità di misura fissa "px"'
pubDate: '2025-02-18'
cover: '@images/css.jpg'
coverAlt: 'Esempio di codice css'
---

Molto spesso, le applicazioni web utilizzano i pixel come unità di misura per i breakpoints usati nelle media query. Questo articolo spiega perchè non è una buona pratica e perchè, invece, si dovrebbe usare un'unità di misura relativa come rem.

(_Gli esempi di codice in questo articolo presuppongono una codifica mobile first ma i concetti rimangono gli stessi se si partisse da uno stile desktop first._)

Ecco un esempio di codice css per impostare una media query.

```css
@media screen and (min-width: 720px) {
  // qui il codice
}
```

Diciamo al browser che se lo schermo è più grande di 720 pixel deve applicare determinati stili alla pagina web. Questo permette, ad esempio, di disporre degli elementi su 2 colonne invece che sulla sola colonna impostata per schermi mobile.

Apparentemente non c'è nulla di sbagliato ma in realtà usare un'unita di misura assoluta porta con sè degli effetti indesiderati.

```css
.container {
  display: grid;
  grid-template-columns: 1fr;
}
.sidebar {
  display: none;
}

@media screen and (min-width: 720px) {
  .container {
    grid-template-columns: repeat(2, 1fr);

    .sidebar {
      display: flex;
    }
  }
}
```

![Visualizzazione pagina su schermo
  laptop con font di base a 16px](@images/page-16px.png)
_Visualizzazione pagina su schermo laptop (1280px) con font di base a 16px e breakpoint in px_

La sidebar viene visualizzata solo sopra i 720 pixel.

Molti sviluppatori trascurano il fatto che i browser hanno un'impostazione per il ridimensionamento del font di base (che normalmente è 16 pixel e che è diverso dall'ingrandimento della pagina), ed è usato dagli utenti con problemi di vista.

Questo significa che se un utente imposta un font di base, ad esempio, a 32 pixel, nel suo browser, sul suo laptop, il suo spazio nella pagina si dimezza e quindi usare degli stili previsti per il laptop in uno spazio molto più piccolo può risultare in un'esperienza utente non ottimale.

![Visualizzazione pagina su schermo
  laptop con font di base a 32px](@images/page-32px-width-breakpoint-in-px.png)
_Visualizzazione pagina su schermo laptop (1280px) con font di base a 32px e breakpoint in px_

Siamo abituati a pensare alle media query come grandezza dello schermo, ma sarebbe più appropriato pensare in termini di spazio disponibile.
Ecco che usando i rem si dice al browser di usare il layout appropriato in base allo spazio disponibile, che è influenzato dalle impostazioni del browser.

Considerando che 720/16px = 45:

```css
@media screen and (min-width: 45rem) {
  .container {
    grid-template-columns: repeat(2, 1fr);

    .sidebar {
      display: flex;
    }
  }
}
```

Se il font size del browser non è stato modificato non cambia nulla, avrò il layout ad una colonna sotto i 720px e il layout a 2 colonne sopra quella soglia.

Se, invece, il browser ha un font di base di 32 pixel la media query si attiverà a (32\*45 = 1440px) per cui sul laptop continuerò ad avere una vista "mobile".

![Visualizzazione pagina su schermo
  laptop con font di base a 32px](@images/page-32px-width-breakpoint-in-rem.png)
_Visualizzazione pagina su schermo laptop (1280px) con font di base a 32px e breakpoint in rem_

---
title: 'Guida a Markdown'
description: 'Ecco alcuni esempi di sintassi Markdown che può essere usata quando si scrivono contenuti Markdown.'
pubDate: 'Jun 19 2024'
cover: '../../assets/images/css.jpg'
coverAlt: 'Esempio di codice css'
---

Ecco alcuni esempi di sintassi Markdown che può essere usata quando si scrivono contenuti Markdown

## Titoli

I seguenti eleemnti HTML `<h1>`—`<h6>` rappresentano sei livelli di titoli. `<h1>` è il più elevato, `<h6>` il più basso.

# H1

## H2

### H3

#### H4

##### H5

###### H6

## Paragrafo

Xerum, quo qui aut unt expliquam qui dolut labo. Aque venitatiusda cum, voluptionse latur sitiae dolessi aut parist aut dollo enim qui voluptate ma dolestendit peritin re plis aut quas inctum laceat est volestemque commosa as cus endigna tectur, offic to cor sequas etum rerum idem sintibus eiur? Quianimin porecus evelectur, cum que nis nust voloribus ratem aut omnimi, sitatur? Quiatem. Nam, omnis sum am facea corem alique molestrunt et eos evelece arcillit ut aut eos eos nus, sin conecerem erum fuga. Ri oditatquam, ad quibus unda veliamenimin cusam et facea ipsamus es exerum sitate dolores editium rerore eost, temped molorro ratiae volorro te reribus dolorer sperchicium faceata tiustia prat.

Itatur? Quiatae cullecum rem ent aut odis in re eossequodi nonsequ idebis ne sapicia is sinveli squiatum, core et que aut hariosam ex eat.

## Immagini

### Sintassi

```markdown
![Alt text](./full/or/relative/path/of/image)
```

### Risultato

![blog placeholder](@images/hero.jpg)

## Citazioni

L'elemento blockquote rappresenta un contenuto che è citato da un'altra fonte, e può avere anche un riferimento alla fonte che può essere all'interno di un elemento `footer`o `cite`, e opzionalmente con modifiche come annotazioni e abbreviazioni.

### Citazione senza riferimenti

#### Sintassi

```markdown
> Tiam, ad mint andaepu dandae nostion secatur sequo quae.  
> **Nota** che puoi usare la sintassi Markdonw all'interno di una citazione.
```

#### Risultato

> Tiam, ad mint andaepu dandae nostion secatur sequo quae.  
> **Nota** che puoi usare la sintassi Markdonw all'interno di una citazione.

### Citazione con riferimento

#### Sintassi

```markdown
> Don't communicate by sharing memory, share memory by communicating.<br>
> — <cite>Rob Pike[^1]</cite>
```

#### Risultato

> Don't communicate by sharing memory, share memory by communicating.<br>
> — <cite>Rob Pike[^1]</cite>

[^1]: La citazione sopra è estratta dal [discorso] (https://www.youtube.com/watch?v=PAAkCSZUG1c) di Rob Pike's durante il Gopherfest, 18 Novembre, 2015.

## Tabelle

### Sintassi

```markdown
| Italics   | Bold     | Code   |
| --------- | -------- | ------ |
| _italics_ | **bold** | `code` |
```

### Risultato

| Italics   | Bold     | Code   |
| --------- | -------- | ------ |
| _italics_ | **bold** | `code` |

## Blocchi di codice

### Sintassi

Si possono usare 3 apici inversi ``` su una nuova riga, scrivere il codice e chiudere con 3 apici inversi in una nuova riga e evidenziare il linguaggio con una sintassi specifica scrivendo il nome del linguaggio con una parola dopo i primi 3 apici inversi, per esempio html, javascript, css, markdown, typescript, txt, bash

````markdown
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Example HTML5 Document</title>
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```
````

### Risultato

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Example HTML5 Document</title>
  </head>
  <body>
    <p>Test</p>
  </body>
</html>
```

## Tipi di liste

### Liste ordinate

#### Sintassi

```markdown
1. First item
2. Second item
3. Third item
```

#### Risultato

1. First item
2. Second item
3. Third item

### Liste non ordinate

#### Sintassi

```markdown
- List item
- Another item
- And another item
```

#### Risultato

- List item
- Another item
- And another item

### Liste nidificate

#### Sintassi

```markdown
- Fruit
  - Apple
  - Orange
  - Banana
- Dairy
  - Milk
  - Cheese
```

#### Risultato

- Fruit
  - Apple
  - Orange
  - Banana
- Dairy
  - Milk
  - Cheese

## Altri elementi — abbr, sub, sup, kbd, mark

### Sintassi

```markdown
<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Premi <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>Delete</kbd> per terminare la sessione.

Most <mark>salamanders</mark> are nocturnal, and hunt for insects, worms, and other small creatures.
```

### Risultato

<abbr title="Graphics Interchange Format">GIF</abbr> is a bitmap image format.

H<sub>2</sub>O

X<sup>n</sup> + Y<sup>n</sup> = Z<sup>n</sup>

Premi <kbd>CTRL</kbd> + <kbd>ALT</kbd> + <kbd>Delete</kbd> per terminare la sessione.

Most <mark>salamanders</mark> are nocturnal, and hunt for insects, worms, and other small creatures.

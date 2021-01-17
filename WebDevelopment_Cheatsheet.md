# Web Development I Cheatsheet (SEM I)

# 1. Basis HTML

## 1.1 Attribute tag

> Attributen geven extra informatie over een element (naam + waarde)

> In onderstaand voorbeeld is **href** een attribuut.

```HTML
<a href="https://google.com/">Klikbaar element</a>
```

<br/>

## 1.2 Block level vs inline

> **Block-elementen** nemen heel de paginabreedte in

> **Inline-elementen** komen na elkaar

<img src="images/blockinline.png" width="400px">

<br/></br>

## 1.2 Soorten secties

> Sinds HTML5 kunnen we verschillende inhoudsblokken makkelijk definiëren met tags. We onderscheiden:

```HTML
<header> <!-- Dit gebruiken we voor de hoofding-->
<nav> <!-- Dit gebruiken  we voor de navigatiebalk-->
<main> <!-- Dit gebruiken we voor de main content op je website-->
<article> <!-- Dit gebruiken we voor bepaalde herhalende elementen, zoals artikels bij een perswebsite-->
<aside> <!-- Dit gebruiken we als sidebar (zowel links als rechts)-->
<footer> <!-- Dit gebruiken we vanonder aan de website bij een footer-->
<section> <!-- Voor een onderdeel van een pagina-->
```

<br/>

## 1.3 Hoofdingen

> Om titels en ondertitels te maken, maken we gebruik van de `<h>` tag.

> Deze bestaan van `<h1>` tot en met `<h6>`.

> Door er het `id` attribuut aan toe te voegen kunnen we hier een ankerpunt van maken.

> **Let op:** dit is enkel voor titels. Onderliggende teksten markeren we met de `<p>` tag.

```HTML
<h1 id="hoofding1">Dit is een titel</h1>
<p>Dit is onderliggende tekst</p>
```

<br/>

## 1.4 Regeleinde

> Witruimte, regeleinde en tabs worden niet weergegeven in een browser. Daarom gebruiken we de `<br/>` tag om regels af te breken.

```HTML
<p>Dit is een<br/>regeleinde.</p>
```

<br/>

## 1.5 Speciale opmaaktags

> Hieronder vind je een lijst van de <cite>meest</cite> belangrijke tags

```HTML
<em> <!-- Klemtoon leggen, standaard cursief (emphasis)-->
<strong> <!-- Nadruk leggen, heel belangrijk, standaard vet-->
<small> <!--Aanvullende informatie-->
<cite> <!-- Citeren van de naam van een auteur (!NIET  VOOR BRONVERMELDING)-->
<q> <!-- Korte citaten in lopende zin-->
<abbr> <!--Afkortingen weergeven, in combinatie met title tag-->
<dfn> <!-- Markeert eerste keer dat definitie voorkomt-->
<code> <!-- Markeren van programmacode-->
<span> <!-- Een containerelement zonder betekenis, met mogelijke attirbuten-->
<pre> <!-- Behouden van tabs, witruimte, etc in code-->
<sub> <!-- Subscrips, bijvoorbeeld de 2 van H2O kleiner weergeven-->
<sup> <!-- Tegenovergestelde van sub-->
<s> <!--Strikethrough-->
<ins> <!-- Toegevoegde inhoud, zoals op Github (groene highlight)-->
<del> <!-- Verwijderde inhoud, zoals op Github (rode highlight)-->
<mark> <!--Markeren van tekst met 'fluostift'-->
<kbd> <!-- Gebruikersinvoermarkering-->
<samp> <!-- Computeruitvoer-->
```

<br/>

## 1.6 Inhoud groeperen

> We kunnen inhoud groeperen zoals adresgegevens, opsommingslijsten,...

### 1.6.1 Gegevens

> De `<address>` tag gebruiken we voor contactinformatie.

> De `<main>` tag gebruiken om de belangrijkste informatie te markeren (niet header, footer en navigatie).

> De `<blockquote>` tag gebruiken we voor langere citaten uit andere bron waarbij bron wordt vermeld met `cite` attribuut.

<br/>

### 1.6.2 Lijsten

> We gebruiken de `<ol>` tag voor een ordered list (met nummers). Dit altijd in combinatie met `<li>` tag (dit is om het lijstelement zelf te plaatsen).

<ol>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ol>

```HTML
<ol>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ol>
```

> We gebruiken de `<ul>`tag voor een niet ordered list (puntjes). Dit is eveneens in combinatie met de `<li>` tag.

<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>

```HTML
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>
```

> We gebruiken `<dl>` in combinatie met `<dt>` en `<dd>` voor een gepaarde lijst.

<dl>
    <dt>Hoofding</dt>
    <dd>Beschrijving</dd>
</dl>

```HTML
<dl>
    <dt>Hoofding</dt>
    <dd>Beschrijving</dd>
</dl>
```

> Lists kunnen ook genest worden.

<br/>

### 1.6.3 Illustraties en bijschiften

> We gebruiken de `<figure>` tag om illustraties met bijschrift te groeperen. Dit kan ook een tabel, grafiek, citaat of meer zijn. Dit in combinatie met `<figcaption>`.

```HTML
<figure>
    <img src="/olifant.jpg"
         alt="Elephant at sunset">
    <figcaption>An elephant at sunset</figcaption>
</figure>
```

<br/>

### 1.6.4 Makkelijk benaderen met opmaak en scripting

> Voor dit gebruiken we de `<div>` tag. In combinatie met het `class` attribuut kan je vanuit een CSS bestand de div tag makkelijk benaderen.

```HTML
<div class="voorbeeldclass">
    <p>Dit is een voorbeeldparagraaf</p>
</div>
```

```CSS
.voorbeeldclass {
    margin: 1rem;
    border: 1px;
}
```

<br/>

## 1.7 Koppelingen

### 1.7.1 Links

> Het gebruik van hyperlinks in HTML maakt het mogelijk om van de ene webpagina naar een andere te gaan. Dit kan binnen de website zijn, buiten, e-mail clients, telefoonnummer bellen,...

> We maken iets klikbaar met de `<a>` tag. Dit kan een kop, tekst, afbeelding,... zijn.

```HTML
<a href="https://google.com">Dit is klikbare tekst</a>
```

> Bij lokale links navigeren we door de mappen met `/` en om een niveau te stijgen gebruiken we `../`.

> Bij een link naar een e-mail adres gebruiken we `mailto:` en voor telefoneren gebruiken we `tel:`.

> Door `target:"_blank"` te gebruiken kunnen we de URL openen in een nieuw tabblad.

> Je kan als target ook een ankerpunt van een titel gebruiken.

```HTML
<a href="#hoofding1">Spring naar hoofding 1!</a>

<a href="/overons.html#hoofding1">Spring naar hoofding 1 op over ons!</a>
```

### 1.7.2 Bestanden linken (stylesheets)

> Om CSS te gebruiken in ons document moeten we de stylesheet linken aan onze HTML pagina. Dit doen we met onderstaande code.

```HTML
<link rel="stylesheet" href="main.css">
```

> Je kan ook het siteicoon veranderen met:

```HTML
<link rel="icon" href="favicon.ico" type="image/x-icon">
```

<br/>

## 1.8 Afbeeldingen

> We kunnen een afbeeldingen weergeven met de `<img>` tag. Dit altijd in combinatie met het `src` attribuut. Het `alt` attribuut is een tekst wanneer de afbeelding niet zichtbaar zou zijn. Met `width` en `height` kan je de afmetingen doorgeven. De browser weet dan wat er komt. NIET OM TE SCHALEN!

```HTML
<img src="olifant.jpg" alt="Een olifant uit Afrika" width="100" height="100">
```

> Omdat sommige beeldschermen een hele hoge pixeldensity hebben (denk maar aan Retina), kan het zijn dat je soms een betere versie van een afbeelding wilt inladen. De browser kan op zijn beurt verschillende resoluties inladen voor het geschikte beeldscherm. Dit gebeurt met het `srcset` attribuut.

```HTML
<img src="olifant640.jpg" alt="Een olifant uit Afrika"
    srcset="olifant640.jpg 1x,
            olifant1280.jpg 2x,
            olifant1920.jpg 3x">
```

> In CSS kunnen we een afbeelding de volledige grootte van zijn parent container laten innemen door zowel de `width` als `height` op `100%` te zetten.

<a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video">HTML video</a>
<br/>
<a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio">HTML audio</a>

> Om captions bij een afbeelding te plaatsen gebruiken we de `<figure>` en `<figcaption>` tags (zie puntje 1.6.3 in dit document).

<br/>

## 1.9 <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/table">Tabellen</a>

### 1.9.1 Algemeen

> Iedere tabel start met de root tag `<table>`. Daaronder komen rijen met de `<tr>` tag en daarin kolommen met de `<td>` tag (je definiëert dus per rij, kolommen).

<table>
    <thead>
        <tr>
        <th>Header</th>
        </tr>
    </thead>
    <tr>
        <td >Kolom 1.1</td>
        <td>Kolom 1.2</td>
    </tr>
    <tr>
        <td>Kolom 2.1</td>
        <td>Kolom 2.2</td>
    </tr>
</table>

```HTML
<table>
    <thead>
        <tr>
            <th>Header</th>
        </tr>
    </thead>
    <tr>
        <td>Kolom 1.1</td>
        <td>Kolom 1.2</td>
    </tr>
    <tr>
        <td>Kolom 2.1</td>
        <td>Kolom 2.2</td>
    </tr>
</table>
```

> Door de attributen `rowspan` en `colspan` te gebruiken kan je 1 cel meerdere kolommen of rijden laten overvloeien.

<br/>

<table>
    <tr>
        <td rowspan="2">Kolom 1.1</td>
        <td>Kolom 1.2</td>
    </tr>
    <tr>
        <td>Kolom 2.2</td>
    </tr>
</table>

<br/>

```HTML
<table>
    <tr>
        <td rowspan="2">Kolom 1.1</td>
        <td>Kolom 1.2</td>
    </tr>
    <tr>
        <td>Kolom 2.2</td>
    </tr>
</table>
```

> **TIP**: In CSS kunnen wet met `border-collapse: collapse` dubbele borders enkelvoudig maken.

<br/>

### 1.9.2 Tabelbijschrift

> Men kan bij tabellen een bijschrift plaatsen. Dit doen we met het [`<caption>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/caption) element. We zetten deze net binnen het `<table>` element.
>
> Je kan de caption-positie aanpassen in CSS met `caption-side`.

<br/>

## 1.10 [Formulieren](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/form)

> Met de `<form>` tag kunnen we een inputformulier maken. Met het attribuut `action` zeggen we naar welke URL het formulier moet gestuurd worden. Met het attribuut `method` zeggen we de methode van versturen. Dit of `get` (toevoegen aan url) of `post` (toevoegen aan header van HTTP request).

<br/>

> Ieder veld stoppen we in een `div` element. Om de tekst voor het veld te krijgen, gebruiken we `label` met daarin een link naar het inputveld met `for` (met het `id` van het `input` veld).

```HTML
<form action="" method="get">

  <div>
    <label for="name">Enter your name: </label>
    <input type="text" name="name" id="name" required>
  </div>

  <div>
    <label for="email">Enter your email: </label>
    <input type="email" name="email" id="email" required>
  </div>

  <div>
    <input type="submit" value="Subscribe!">
  </div>

</form>
```

> Je kan ook de `<label>` tag rond de `<input>` tag zetten.

```HTML
<div>
    <label>Enter your name
        <input type="text" name="name" required>
    </label>
</div>
```

> Bij de [`<input>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input) tag zijn er een paar attributen
> <br/>- `id` in combinatie met label of voor css
> <br/>- `name` nodig voor het versturen van het formulier
> <br/>- `value` waarde van een invoerveld als de gebruiker zelf niets ingeeft
> <br/>- `placeholder` voor helptekst.
> <br/> **We kunnen ook de invoer client-side valideren met:** <br/>- `required` verplichte infvoer
> <br/>- `minlenght` en `maxlenght` min- en max lengte van de invoer
> <br/>- `size` lengte van het invoerveld
> <br/>- `pattern` een regex patroon
> <br/>**Gebruikersbeperkingen:** <br/>- `readonly` veld kan niet worden aangepast, enkel getoond
> <br/>- `disabled` veld is uitgeschakeld

> Voor de `<input>` tag hebben we ook het `type` attribuut. <br/>
> Op Mozilla MDN vinden we hier een [hele lijst](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input#%3Cinput%3E_types) van.

> Er zijn nog een paar overige elementen die op een andere manier geïmplementeerd worden.
> <br/>- [`<button>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/button): knop
> <br/>- [`<textarea>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/textarea): uitgebreide tekstinvoer
> <br/>- [`<option>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select): keuzemogelijkheid
> <br/>- [`<optgroup>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/optgroup): groeperen van keuzemogelijkheden
> <br/>- [`<select>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select): keuzelijst
> <br/>- [`<datalist>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/datalist): keuzelijst met invoervak
> <br/>- [`<legend>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/legend): een legende toewijzen aan een formulier (tekst vanboven)

> Om een groot tekstvak te creëren maakt men gebruik van de `<textarea>` tag. Om het tekstvak onder het label te zetten kan je `<br>` gebruiken. Voorbeeld:

```HTML
<div>
  <label for="reden">Reden afspraak: <br></label>
  <textarea name="reden" id="reden" cols="60" rows="5">Dit is placeholder tekst</textarea>
</div>
```

> TIP: <br/> Als je van een formulier een flex box maakt, kan je de input boxes mooi aligneren.
>
> - Gehele formulier op `display: flex` zetten
> - Flex value van bv. 1 toekennen aan label met `flex: 1`.

 <br/>

### 1.10.1 [Fieldset](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset)

> We gebruiken het [`<fieldset>`](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/fieldset) element om rond een formulier een box te tekenen met eventueel een legenda. Voorbeeld:

```HTML
<form>
  <fieldset>
    <legend>Choose your favorite monster</legend>

    <input type="radio" id="kraken" name="monster">
    <label for="kraken">Kraken</label><br/>

    <input type="radio" id="sasquatch" name="monster">
    <label for="sasquatch">Sasquatch</label><br/>

    <input type="radio" id="mothman" name="monster">
    <label for="mothman">Mothman</label>
  </fieldset>
</form>
```

wordt:

<img src="images/fieldset.png" width=300px></img>

# 2. [CSS](https://developer.mozilla.org/en-US/docs/Web/CSS/Reference)

## 2.1 De plaatsing van CSS

> We kunnen CSS op verschillende manieren implementeren.
> <br/>- In een external stylesheet met `<link rel="stylesheet" href="css/stijlen.css">`.
> <br/>- In het HTML document zelf met de `<style>` tag.
> <br/>- Als inline element in de begin tag van het element. Bv. `<p style="font-family:'Courier New'; font-size: 20px;">Test</p>`

> We kunnen andere stijlbladen importeren met `@import url('bestand.css')`.

> Browsers hebben hun eigen standaard stylesheet. Soms kan dit voor inconsistenties zorgen tussen browsers. Hiervoor gebruiken we een [browser reset stylesheet](https://necolas.github.io/normalize.css/).

<br/>

## 2.2 [CSS eenheden](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units)

> CSS heeft verschillende eenheden. Hieronder een korte opsomming.
> <br/> **Absolute eenheden** <br/>- `px`: CSS pixel, optische referentie-eenheid
> <br/>**Relatieve eenheden** <br/>- `em`: gelijk aan de berekende tekstgrootte van het ouderelement
> <br/>- `rem`: de tekstgrootte van het rootelement
> <br/>- `ch`: breedte van tekst
> <br/> **Viewport percentages** <br/>- `vw`: 1% van de breedte van het venster
> <br/>- `vh`: 1% van de hoogte van het venster
> <br/>- `vmin`: de kleinste waarde van vh en vw
> <br/>- `vmax`: de grootste waarde van vh en vw

<br/>

## 2.3 Verwerking van CSS door de browser

> Als er meerdere waarden zijn toegewezen aan een property, zal de browser de meest specifieke kiezen. In het onderstaande geval zal de kleur dus rood zijn.

```CSS
body > div {
    background-color: red;
}

div {
    background-color: black;
}

* {
    background-color: green;
}
```

> In onderstaande tabel zien we wat belangrijker is. Hoe meer naar rechts, hoe minder belangrijk. Het helemaal linkse getal is inline style.

| Selector         | Specificiteit | Toelichting                                        |
| ---------------- | ------------- | -------------------------------------------------- |
| div ul ul li     | 0,0,0,4       | 4 elementselectors                                 |
| div.klasse ul li | 0,0,1,3       | 1 klasseselector, 3 elementselectors               |
| a::before        | 0,0,0,2       | 1 pseudoklasse, 1 elementselector                  |
| a.klasse:hover   | 0,0,2,1       | 1 klasse, 1 pseudoklasse, 1 elementselector        |
| p.eerste         | 0,0,1,1       | 1 klasseselector, 1 elementselector                |
| #id p.eerste     | 0,1,1,1       | 1 id-selector, 1 klasseselector, 1 elementselector |

<br/>

> Volgorde van gebruikte stijlbladen (naar belangrijkheid):
>
> - Declaraties in de browser
> - Declaraties van de gebruiker
> - Declaraties van de auteur
> - Declaraties van de auteur met kenmerk `!important`
> - Declaraties van de gebruiker met kenmerk `!important`

<br/>

## 2.4 Overerving

> Een opmaakeigenschap hoeft niet rechtstreeks een waarde te krijgen. De waarde kan overgeerfd worden van het ouderelement.

> Zonder de onderstaande CSS zal de `<em>` tag de tekst gewoon cursief maken (overerving van een ouderelement). Als we de onderstaande CSS dan wel gebruiken, zal hij de tekst tussen de `<em>` tags ook blauw maken.

```CSS
em {color:blue;}
```

```HTML
<p>Hey, <em>look</em> at that sheepdog</p>
```

> **Opgelet**: Eigenschappen zoals padding, width, height, background-color, border,... zijn niet erfelijk. Je kan dit toch forceren door `inherit` mee te geven.

```CSS
h2 { color: inherit; }
```

> **Welke properties worden overgeërfd?** <br/>
>
> - Tekst-gerelateerde properties <br/> `font-family`, `font-size`, `font-style`, `font-variant`, `font-weight`, `font`, `letter-spacing`, `line-height`, `text-align`, `text-indent`, `tekst-transform`, `word-spacing`
> - List-gerelateerde properties <br/> `list-style-image`, `list-style-position`, `list-style-type`, `list-style`
> - Kleuren <br/> `color`

<br/>

## 2.5 [Selectors](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Selectors)

### 2.5.1 Basisselectors

> **Basisselector (A)**<br/>
> Ieder `<p>` element zal groen kleuren.

```CSS
p {
  color: green;
}
```

> **Klassenselector (.A)**<br/>
> Ieder element met `class="klasse1"` als attribuut zal zwart kleuren. <br/>
> Ieder `<span>` element in een ander element met `class="klasse1` als attribuut kleurt rood. <br/>
> Bij het laatste voorbeeld zal ieder `<span>` element met het klasseattribuut `class=klasse1` rood kleuren.

```CSS
.klasse1 {
  color: black;
}

.klasse1 span {
  color: red;
}

span.klasse1 {
  color: red;
}
```

> **ID Selector (#A)**<br/>
> Ieder element met `id="uniekid1"` als attribuut zal aqua kleuren.

> ID's zijn altijd uniek en worden bij maar 1 element gebruikt!

```CSS
#uniekid1 {
  color: aqua;
}
```

### 2.5.2 Combinatieselectors

> **Combinatieselector (A>B)** <br/>
> Ieder `<p>` element waarvan de rechtstreekse parent een `<div>` element is zal blauw kleuren.

```CSS
div > p {
  color: blue;
}
```

> **Combinatieselector (A B)** <br/>
> Ieder `<p>` element dat een afstammeling is van `<div>` (kind, kleinkind,...) kleurt paars.

```CSS
div p {
  color: purple;
}
```

> **Combinatieselector (A+B)** <br/>
> Ieder `<p>` element, op hetzelfde nivau als `<div>` en dat onmiddelijk op `<div>` volgt kleurt geel.

```CSS
div+p {
  color: yellow;
}
```

> **Combinatieselector (A~B)** <br/>
> Ieder `<p>` element, op hetzelfde nivau als `<div>` en dat op `<div>` volgt kleurt groen (moet niet onmiddelijk).

```CSS
div~p {
  color: green;
}
```

> **Combinatieselector (A,B)** <br/>
> Ieder `<p>` en `<div>` element kleurt oranje. Op welk niveau dan ook.

```CSS
div,p {
  color: orange;
}
```

```CSS
div,p {
  color: orange;
}
```

### 2.5.3 Attribuutselectors

| Teken | Beschrijving              | Voorbeeld            | Betekenis voorbeeld                                                                    |
| ----- | ------------------------- | -------------------- | -------------------------------------------------------------------------------------- |
|       |                           | img[alt]             | elk element img met attribuut alt                                                      |
| =     | Exact gelijk aan          | img[alt="foto"]      | elk img element waarvan alt attribuut gelijk aan de waarde foto                        |
| ~=    | Bevat waarde              | img[alt~="fotoboek"] | elk img element waarvan class attribuut meerdere waarden kan hebben waaronder fotoboek |
| \|=   | Begint met waarde         | [hreflang\|="nl"]    | elk element waarvan hreflang attribuut gelijk aan nl, of begint met nl- (nl-NL, nl-BE) |
| ^=    | Begint met exacte waarde  | [name^="keuze"]      | name attribuut begint met het exacte woord "keuze" (bv. keuzevak of keuze2)            |
| $=    | Eindigt met exacte waarde | [href$=".com"]       | href attribuut eindigt op ".com" (bv. google.com)                                      |
| \*=   | Bevat exacte waarde       | [href\*="user"]      | href attribuut bevat het exacte woord "user" (bv. hogent.be/user/jan)                  |

> **TIP:**
> Door `:not()` te gebruiken achter een selector kan je een element selecteren waar een voorwaarde NIET van waar is. Voorbeeld: `a:not([href])`.

<br/>

### 2.5.4 [Pseudoklassen](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes)

> Pseudoklassen duiden een toestand van een element aan.

> **Hyperlink pseudoklassen**
>
> - [`a:link`](https://developer.mozilla.org/en-US/docs/Web/CSS/:link) onbezochte link
> - [`a:visited`](https://developer.mozilla.org/en-US/docs/Web/CSS/:visited) bezochte link
> - [`a:hover`](https://developer.mozilla.org/en-US/docs/Web/CSS/:hover) met cursor over gaan
> - [`a:active`](https://developer.mozilla.org/en-US/docs/Web/CSS/:active) actief (weinig gebruikt)

> **UI toestand**
>
> - [`:enabled`](https://developer.mozilla.org/en-US/docs/Web/CSS/:enabled) elementen die beschikbaar zijn
> - [`:disabled`](https://developer.mozilla.org/en-US/docs/Web/CSS/:disabled) elementen die niet beschikbaar zijn
> - [`:checked`](https://developer.mozilla.org/en-US/docs/Web/CSS/:checked) een keuzerondje of selectievakje die is ingeschakeld

> **Varia**
>
> - [`:focus`](https://developer.mozilla.org/en-US/docs/Web/CSS/:focus) element dat focus heeft (handeling gebruiker)
> - [`:target`](https://developer.mozilla.org/en-US/docs/Web/CSS/:target) doel van een element
> - [`:lang()`](https://developer.mozilla.org/en-US/docs/Web/CSS/:lang) taal
> - [`:not()`](https://developer.mozilla.org/en-US/docs/Web/CSS/:not) ontkenning

> **[Structurele pseudoklassen](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes#Tree-structural_pseudo-classes)**
>
> - `:root` hoofdelement `<html>`
> - `:first-child` een element dat het eerste child is van zijn parent-element
> - `:last-child` een element dat het laatste child is van zijn parent-element
> - `:only-child` een element waarvan de ouder geen andere child elementen heeft
> - `:first-of-type` het eerste element van dat type
> - `:last-of-type` het laatste element van dat type
> - `:only-of-type` het enige element van dat type
> - `:nth-child(n)` elk zoveelste kindelement (je kan ook `odd` oneven of `even` even gebruiken)
> - `:nth-last-child(n)` nu gerekend vanaf het laatste kind (je kan ook `odd` oneven of `even` even gebruiken)
> - `:nth-of-type(n)` elk zoveelste element van een type (je kan ook `odd` oneven of `even` even gebruiken)
> - `:nth-last-of-type(n)` nu gerekend vanaf laatste element (je kan ook `odd` oneven of `even` even gebruiken)
> - `:empty` leeg element

> **Pseudo elementen** <br/>
> Toegang tot onderdelen van een document waarvoor geen gewone elementen bestaan (bijvoorbeeld voor een URL).
>
> - [`::first-line`](https://developer.mozilla.org/en-US/docs/Web/CSS/::first-line) de eerste regel opgemaakte tekst van een element
> - [`::first-letter`](https://developer.mozilla.org/en-US/docs/Web/CSS/::first-letter) de eerste letter
> - [`::before`](https://developer.mozilla.org/en-US/docs/Web/CSS/::before) voor de inhoud van een element
> - [`::after`](https://developer.mozilla.org/en-US/docs/Web/CSS/::after) na de inhoud van een element
>
> Voorbeeld:

```CSS
/* Add a heart before links */
a::before {
  content: "♥";
}
```

<br/>

## 2.6 [CSS Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Properties_Reference)

> **Enkele CSS properties**
>
> - [`background`](https://developer.mozilla.org/en-US/docs/Web/CSS/background) achtergrondskleur
> - [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color) kleur tekst
> - [`font-family`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family) het lettertype
> - [`font-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/fontsize) tekstgrootte
> - [`font-weight`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight) het gewicht (vetheid) van het lettertype
> - [`line-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height) de regelafstand, hoeveelheid it tussen de regels tekst
> - [`margin-bottom`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-bottom) (of top/left/right) ruimte tussen de rand van een element en de rand van het parent element of angrenzend element
> - [`padding-bottom`](https://developer.mozilla.org/en-US/docs/Web/CSS/padding) (of top/left/right) de ruimte tussen de inhoud en de rand
> - [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align) uitlijnen van tekst
> - [`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration) lijneffecten
> - [`text-transform`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform) omzetten naar kleine/hoofdletters

<br/>

## 2.7 [Boxmodel](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Box_Model)

> Een HTML-pagina is opgebouwd uit blokken. Deze blokken worden bovenop mekaar geplaatst. Een box bestaat uit `content` (bv. tekst), `padding` (ruimte rond het content) een `border` (de rand rond de `padding`) en de `margin` (ruimte rond de border).

### 2.7.1 Box-sizing

> Er zijn 2 mogelijke manieren van [`box-sizing`](https://developer.mozilla.org/en-US/docs/Web/CSS/box-sizing):
>
> - `content-box` <br/>
>   Ingestelde width en height hebben enkel betrekking op de **content**.
> - `border-box` <br/>
>   Ingestelde width en height hebben betrekking op de **content** + **padding** + de **border**.

> Eigenschappen [`width`](https://developer.mozilla.org/en-US/docs/Web/CSS/width) en [`height`](https://developer.mozilla.org/en-US/docs/Web/CSS/height) (niet bij inline tekst)
>
> - `auto` (standaardwaarde) box is zo groot dat de inhoud erin past
> - `lengte of percentage`
> - `max-content` afmeting van het grootste item in de box
> - `min-content` de kleinst mogelijke afmeting zonder overloop te veroorzaken

> Eigenschappen [`min-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/min-width), [`max-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/max-width), [`min-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/min-height) en [`max-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/max-height). <br/>
> Deze waarden overriden `width` en `height`. <br/>
>
> - `auto` (standaardwaarde) box is zo groot dat de inhoud erin past
> - `none`
> - `lengte of percentage`
> - `max-content` afmeting van het grootste item in de box
> - `min-content` de kleinst mogelijke afmeting zonder overloop te veroorzaken

<br/>

### 2.7.2 Marges

> Marges ingesteld worden op 2 manieren:
>
> - [`margin-top`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-top)[`/right`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-right)[`/bottom`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-bottom)[`/left`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin-left)
> - [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin) (afgekort)

```CSS
/* Apply to all four sides */
margin: 1em;
margin: -3px;

/* vertical | horizontal */
margin: 5% auto;

/* top | horizontal | bottom */
margin: 1em auto 2em;

/* top | right | bottom | left */
margin: 2px 1em 0 auto;
```

> **Opgelet**: Marges worden aan de onder en bovenkant samengevoegd, zodat er geen dubbele marges ontstaan. Wanneer de bottom margin van een element de top margin van een ander element overlapt, is het resultaat **NIET** de som, maar **de grootste margin**.

> **Belangrijk**: om een gewone box te centreren, kunnen we de [`margin`](https://developer.mozilla.org/en-US/docs/Web/CSS/margin) waarde op `auto` zetten!

<br/>

### 2.7.3 Borders

> Van een border kunnen we 3 waarden instellen:
>
> - [`border-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-width) (px, %, em, rem, thin, medium, thick) (top/right/left/bottom)
> - [`border-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-style) (none, hidden, dotted, dashed, solid, double, groove, ridge, inset, outset)
> - [`border-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-color) (een kleurwaarde of _transparent_)
>
> Men kan deze eigenschappen ook combineren:
>
> ```CSS
> border: 1px solid black;
> ```
>
> De volgorde maakt niet uit. <br/>
> Aparte randen kunnen ook gedefinieerd worden met `border-left`, `border-right`, `border-top`, `border-bottom.`

<br/>

### 2.7.4 Overflow

> Overflow treedt op indien de content te groot wordt voor de box. Dit kan enkel als een breedte of hoogte is ingesteld. Wat er met die inhoud gebeurt hangt af van de waarde die wordt toegekend aan [`overflow`](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow).
>
> - [`overflow`](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow) (visible/hidden/scroll/auto)

<br/>

### 2.7.5 Weergavemodel - display

> De indeling van boxes wordt bepaald door de [`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display) eigenschap. Er wordt een onderscheid gemaakt tussen:
>
> - `display-outside` gedrag van boxen tov andere boxen (in flow). <br/> **block**/**inline**/run-in
> - `display-inside` gedrag van de afstammelingne van de box. <br/> **flow**/**flow-root**/table/**flex**/**grid**/list-item
> - `display-legacy` waarden kunnen ook gekoppeld worden <br/> **inline-block**/**inline-grid**/**inline-flex**

<br/>

### 2.7.6 Visibility

> Je kan makkelijk een element verbergen door de [`visibility`](https://developer.mozilla.org/en-US/docs/Web/CSS/visibility) eigenschap op `hidden` te zetten. Er wordt wel nog steeds een box aangemaakt en bestaat ook in de boomstructuur. Het wordt niet weergegeven in de browser, maar de ruimte nodig voor de box wordt wel gereserveerd op het scherm. Als je de [`visibility`](https://developer.mozilla.org/en-US/docs/Web/CSS/visibility) op `collapse` zet wordt er ook geen ruimte gereserveerd.

```CSS
a {
  visibility: hidden;
}
```

> Het is mogelijk dat `collapse` niet altijd de witruimte weglaat (bv. bij inline elementen). Om dit te overkomen kunnen we `display: none` gebruiken.

<br/>

## 2.8 Lay-out positionering

> Elk blok krijgt een positie toegewezen in het omvattende blok (containing blok). Schema's:
>
> - **normale flow** - plaatsing afhankelijk van [`display`](https://developer.mozilla.org/en-US/docs/Web/CSS/display) waarde
> - **floats**: vlottend/zwevend (links/rechts), uit normale flow gehaald
> - **absolute positionering**: krijgt absolute positie ten opzichte van de eerste niet static omvattende blok.

### 2.8.1 Position & offset

> [`Position`](https://developer.mozilla.org/en-US/docs/Web/CSS/position) **eigenschap**
>
> - `static` (standaard) <br/>
>   Het element volgt de normale positie van het document. Offsets hebben geen invloed.<br/> <img src="images/static.png" width=100px>
> - `relative` <br/>
>   Het element wordt gepositioneerd volgens zijn positie in de normale flow. Offsets zijn dus relatief aan zijn flow positie. <br/> <img src="images/relative.png" width=100px>
> - `absolute` <br/>
>   Het element wordt uit de normale flow gehaald en er wordt dus geen plaats voorzien. Zijn positie is relatief aan zijn voorouder (content area). <br/> <img src="images/absolute.png" width=100px>
> - `fixed` <br/>
>   Het element wordt uit de normale flow gehaald en er wordt dus geen plaats voorzien. Zijn positie is relatief aan de [`viewport`](https://developer.mozilla.org/en-US/docs/Glossary/viewport). Dit betekent dat bij scrollen het element blijft staan.
> - `sticky` <br/>
>   Het element varieert tussen `relative` en `fixed` afhankelijk van de scrollpositie. Zijn positie is relatief aan zijn dichtsbijzijnde scrolling voorouder (bijvoorbeeld een element met scrollbar door overflow). Als je verder scrollt zal deze blijven plakken en meegaan als `fixed` element.
>
> Met de eigenschappen `top`, `bottom`,... kan je de positie instellen van het element. Om het element voor of achter een element weer te geven kan je [`z-index`](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index) gebruiken.

> **Offset eigenschap**
>
> - [`top`](https://developer.mozilla.org/en-US/docs/Web/CSS/top), [`right`](https://developer.mozilla.org/en-US/docs/Web/CSS/right), [`bottom`](https://developer.mozilla.org/en-US/docs/Web/CSS/bottom), [`left`](https://developer.mozilla.org/en-US/docs/Web/CSS/left) <br/>
>   We gebruiken offsets om een element te positioneren afhankelijk van zijn relatieve positie (viewport, voorouder,...) <br/>Voorbeeld:
>
> ```CSS
> div.absolute {
>  position: absolute;
>  top: 80px;
>  right: 0;
>  width: 200px;
>  height: 100px;
> }
> ```
>
> Je kan hier een eenheid achter zetten (zie 2.2).

<br/>

### 2.8.2 [Float](https://developer.mozilla.org/en-US/docs/Web/CSS/float) & [clear](https://developer.mozilla.org/en-US/docs/Web/CSS/clear)

> Door [`float`](https://developer.mozilla.org/en-US/docs/Web/CSS/float) (left/right) te gebruiken haal je het blok uit de normale flow en kan de inhoud van de onderliggende blokken erom heen lopen. <br/>Voorbeeld met `float: left`: <br/> <img src="images/float_left.png" width="150px">

> Door [`clear`](https://developer.mozilla.org/en-US/docs/Web/CSS/clear) (none/left/right/both) te gebruiken kan men voorkomen dat de inhoud er rond loopt. Bij het gebruik van `clear` komt de inhoud van onderliggende blokken er onder te liggen. <br/> Voorbeeld met `clear: left`: <br/> <img src="images/clear_left.png" width="150px">

> Voor volledige pagina lay-outs gebruiken we eerder `flex` en `grid`.

<br/>

## 2.9 Responsive design

> **Responsive design: [media](https://developer.mozilla.org/en-US/docs/Web/CSS/@media) queries** <br/>
> We koppelen opmaak aan eigenschappen van een device.
>
> - [`media`](https://developer.mozilla.org/en-US/docs/Web/CSS/@media) queries:
>   - **apparaat type** (all, screen, print, speech)
>   - **media kenmerken** (breedte, orientatie)
>   - **een blok** van stijlregels die geldig izjn voor het gedeclareerde apparaat type en de media kenmerken
>
> ```CSS
> @media apparaat and (media feature) {
>  selector {
>    declaraties;
>  }
> }
> ```
>
> ```CSS
> @media screen and (min-width: 1024px) {
>  main {
>    display: grid;
>    grid-template-columns: 66% 34%;
>  }
> }
> ```
>
> In het bovenstaande voorbeeld zal indien het scherm minimaal 1024px breed is, het main element opgedeeld worden in twee kolommen van 66% en 34% van de breedte van het scherm.

## 2.10 Lay-out: [grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout)

> [Extra leermateriaal](https://gridbyexample.com/learn/) **(aangeraden**)

### 2.10.1 Grids aanmaken

> **Creëren van een _grid container_ element**
>
> - `display: grid` block-level grid
> - `display: inline-grid` inline-level grid

```CSS
#grid {
  display: grid;
  width: 100%;
  grid-template-columns: 50px 1fr;
  gap: 10px;
}
```

> **Definiëren van de grid**
>
> - [`grid-template-rows`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-rows) Rijen definiëren (aantal en hoogte)
> - [`grid-template-columns`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-columns) Kolommen definiëren (aantal en breedte)
> - [`grid-template-areas`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-areas) Area definiëren
> - `gap` Ruimte tussen grid-elementen

```CSS
#page {
  display: grid;
  width: 100%;
  height: 250px;
  grid-template-areas: "head head"
                       "nav  main"
                       "nav  foot";
  grid-template-rows: 50px 1fr 30px;
  grid-template-columns: 150px 1fr;
}
```

> **Gebruik van de [`repeat()`](<https://developer.mozilla.org/en-US/docs/Web/CSS/repeat()>) functie** <br/>
> Met de [`repeat()`](<https://developer.mozilla.org/en-US/docs/Web/CSS/repeat()>) functie kan je een deel van een 'track list' herhalen. Zo kan met in plaats van:
>
> ```CSS
> grid-template-columns: 1fr 1fr 1fr;
> ```
>
> Gebruik maken van:
>
> ```CSS
> grid-template-columns: repeat(3, 1fr)
> ```
>
> Het eerste getal geeft het aantal keer herhalen weer. Een meer uitgebreid voorbeeld:
>
> ```CSS
> grid-template-columns: 20px repeat(4, 1fr 2fr);
> ```
>
> Is hetzelfde dan:
>
> ```CSS
> grid-template-columns: 20px 1fr 2fr 1fr 2fr 1fr 2fr 1fr 2fr;
> ```
>
> Note: de eenheid `fr` is een flexibele ruimte die de overgebleven ruimte inneemt. Bij dus `2fr 1fr` zal 2 delen aan de eerste waarde gegeven worden en 1 deel aan de tweede waarde.
>
> Bij de `repeat()` functie kan men ook gebruik maken van `auto-fill` en `auto-fit` <br/>
> Hier zal de browser zelf het aantal kolommen of rijen bepalen aan de hand van de beschikbare ruimte van de container.
>
> ```CSS
> grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));
> ```
>
> Bij bovenstaand stuk CSS zal de browser de blokken naast elkaar zetten tot de elk minder dan 150px ruimte over hebben. Dan zal de browser de blokken beginnen te verzetten naar volgende rij. Hebben ze meer ruimte dan 150px, dan verdelen ze de ruimte.
> <br/>Het verschil tussen `auto-fill` en `auto-fit`, is dat bij `auto-fill` de browser kolommen zal blijven aanmaken. `auto-fit` zal de kolommen gewoon uitrekken. Onderstaande afbeelding maakt dit duidelijk. [(bron)](https://css-tricks.com/auto-sizing-columns-css-grid-auto-fill-vs-auto-fit/) <img src="images/autofillfit.png" width="500px">

<br/>

> **Expliciet en impliciet raster** <br/>
> Bij een **expliciet raster** definiëren we **manueel** de columns en rijen met de `grid-template-*` eigenschap (bovenstaand). <br/>
>
> Bij een **impliciet raster** zijn gedefiniëerde rijen en kolommen standaard 'auto-sized', maar je kan hiervoor een hoogte/breedte instellen via de properties [`grid-auto-rows`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-rows) en [`grid-auto-columns`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-columns). Een impliciet raster is het raster buiten het bereik van het expliciet raster. Voorbeeld (items 1 en 2 liggen in het impliciet grid):
> <br/> <img src="images/implicitgrid.png" width=500px>

> **Afmetingen tracks** <br/>
> Mogelijke afmetingen instellen voor tracks (lentewaarden px % fr):
>
> - [`max-content`](https://developer.mozilla.org/en-US/docs/Web/CSS/max-content) lengte van de maximale content van het element
> - [`min-content`](https://developer.mozilla.org/en-US/docs/Web/CSS/min-content) lengte van de minimale content van het element (bv. 1 woord van een zin)
> - [`minmax(min,max)`](<https://developer.mozilla.org/en-US/docs/Web/CSS/minmax()>) Vaak gebruikt bij grid-elementen, stelt de minimale en maximale waarde in van bv. een kolom
> - `fit-content(value)` zorgt er voor dat de content past door deze te verlenger naar onder toe
> - `auto`

<br/>

### 2.10.2 Plaatsen van elementen op raster

> **Rijen**
>
> - [`grid-row-start`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-row-start) startrij van het element
> - [`grid-row-end`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-row-start) eindrij van het element
> - `grid-row` afgekorte versie voor rijspan (bv. `1 / 3`)
>
> In het onderstaande voorbeeld kan `grid-row-end: 3` ook als `grid-row-end: span 2` geschreven worden.

```CSS
#item1 {
  background-color: lime;
  grid-row-start: 1;
  grid-row-end: 3;
}

#item2 {
  background-color: yellow;
  grid-row: 2 / 4;
}
```

> **Kolommen**
>
> - `grid-column-start` startkolom van element
> - `grid-column-end` eindkolom van element
> - `grid-column` afgekorte versie voor kolomspan (bv. `1 / 2`)
>
> In het onderstaande voorbeeld kan `grid-column-end: 3` ook als `grid-column-end: span 2` geschreven worden.

```CSS
#item1 {
  background-color: lime;
  grid-column-start: 1;
  grid-column-end: 3;
}

#item2 {
  background-color: yellow;
  grid-column: 2 / 4;
}
```

> **Grid area** <br/>
> We gebruiken [`grid-area`](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-area) om het element op een specifiek gedefiniëerde area (met [`grid-template-areas`](https://developer.mozilla.org/en-US/docs/Glossary/Grid_areas)) en om zowel de span van kolommen als rijen tegelijk te definiëren.
>
> - `grid-area`: rowstart/columnstart/rowend/columnend
>
> ```CSS
> #item1 {
>  background-color: lime;
>  grid-area: 2 / 2 / auto / span 3;
> }
> ```
>
> - `grid-area`: areaid
>
> ```CSS
> #item2 {
>  background-color: green;
>  grid-area: a;
> }
> ```
>
> <br/>

<br/>

> **Ruimte tussen tracks**
>
> - [`column-gap`](https://developer.mozilla.org/en-US/docs/Web/CSS/column-gap) ruimte tussen kolommen
> - [`row-gap`](https://developer.mozilla.org/en-US/docs/Web/CSS/row-gap) ruimte tussen rijen
> - [`gap`](https://developer.mozilla.org/en-US/docs/Web/CSS/gap) ruimte tussen zowel kolommen als rijen (rij, kolom) (beide)

<br/>

### 2.10.3 Uitlijnen

> Er zijn 2 mogelijke uitlijningen
>
> - Uitlijnen van grid in zijn container
>   - [`justify-content`](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content) (start/center/space-between/space-around/space-evenly) horizontaal uitlijnen
>   - [`align-content`](https://developer.mozilla.org/en-US/docs/Web/CSS/align-content) (start/center/space-between/space-around) verticaal uitlijnen
> - Uitlijnen van een item in een grid-cell/track/area
>   - Alle items in grid (flexbox, declaratie in container element)
>     - [`justify-items`](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-items) horizontaal uitlijnen
>     - [`align-items`](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items) verticaal uitlijnen
>   - Éen item zelf (declaratie in specifieke item)
>     - [`justify-self`](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-self) horizontaal uitlijnen
>     - [`aligin-self`](https://developer.mozilla.org/en-US/docs/Web/CSS/align-self) verticaal uitlijnen
>
> Automatisch staat deze waarde op `stretch` (volledig vullen van de cel).
>
> Voorbeeld: <br/> <img src="images/uitlijning.png" width="650px">
>
> **Belangrijk**: om een gewone box te centreren, kunnen we de `margin` waarde op `auto` zetten!

> **TIP:** Om elementen in hun respectievelijke cel zowel horizontaal als verticaal te centreren, maken we van het element een grid container met `display: grid` en gebruiken we `justify-items: center` en `align-items: center`. Voorbeeld:

```CSS
.grid-center {
  display: grid;
  justify-items: center;
  align-items: center;
}
```

<br/>

## 2.11 [Flex container](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)

> [Handige website](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

### 2.11.1 Aanmaken van een **flex container**

> Je creëert een **flex container**-element met
>
> - `display: flex`
> - `display: inline-flex`
>
> Alle directe kindelementen worden **flexitems**.

<br/>

### 2.11.2 Richting items

> **Flex containers** hebben een **main axis** en een **cross axis**. <br/>
> Standaard gaat de _main axis_ van links naar echts en de _cross axis_ van boven naar onder. Dit kan aangepast worden met de [`flex-direction`](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-direction) (row, row-reverse, column, column-reverse) property.

> De container wordt opgevuld langs de **main-axis**.
> <br/> <img src="images/flexcontainer.png" width=500px>

> **Overflow (flex wrap)** <br/>
> Overflow van inhoud wordt geregeld met [`flex-wrap`](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-wrap) (nowrap/wrap/wrap-reverse).
> <br/> Afgekort [`flex-flow`](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-flow).

<br/>

### 2.11.3 Uitlijning

> De uitlijning is op dezelfde manier van `grid`.
> Er zijn 2 mogelijke uitlijningen
>
> - Uitlijnen van grid in zijn container
>   - [`justify-content`](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content) (start/center/space-between/space-around/space-evenly) uitlijnen langs main axis
>   - [`align-content`](https://developer.mozilla.org/en-US/docs/Web/CSS/align-content) (start/center/space-between/space-around) uitlijnen langs cross axis
> - Uitlijnen van een item in een grid-cell/track/area
>   - Alle items in grid (flexbox, declaratie in container element)
>     - [`justify-items`](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-items) (stretch/start/center/end/base-line) uitlijnen langs main axis
>     - [`align-items`](https://developer.mozilla.org/en-US/docs/Web/CSS/align-items) (stretch/start/center/end/base-line) uitlijnen langs cross axis
>   - Éen item zelf (declaratie in specifieke item)
>     - [`justify-self`](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-self) (stretch/start/center/end/base-line) uitlijnen langs main axis
>     - [`aligin-self`](https://developer.mozilla.org/en-US/docs/Web/CSS/align-self) (stretch/start/center/end/base-line) uitlijnen langs cross axis

> Je kan bij flex-items makkelijk de tussenruimte verdelen met [`justify-content`](https://developer.mozilla.org/en-US/docs/Web/CSS/justify-content) op `space-between`, `space-evenly` of `space-around` te zetten.
> <br/>

### 2.11.4 Volgorde items & grootte

> Men kan de volgorde van items wijzigen met de [`order`](https://developer.mozilla.org/en-US/docs/Web/CSS/order) eigenschap (op item niveau).

> De initiële grootte van een flex item kan ingesteld worden met [`flex-basis`](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-basis).

> Flex items kunnen groeien of krimpen als er extra plaats (nodig) is in de container. Dit doen we met [`flex-grow`](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-grow) en [`flex-shrink`](https://developer.mozilla.org/en-US/docs/Web/CSS/flex-shrink). Als deze waarde 0 is, kan deze niet groeien of krimpen. Vanaf >0 kan dit wel. <br/>
> De afgekorte versie hiervan is gewoon [`flex`](https://developer.mozilla.org/en-US/docs/Web/CSS/flex).
>
> ```CSS
> flex-grow: 2;
> flex-shrink 1;
> flex-basis: auto;
> ```
>
> wordt:
>
> ```CSS
> flex: 2 1 auto;
> ```
>
> **Handig voorbeeld**: Om alle flex cellen even lang te maken over de breedte van een pagina, kan men de `flex-basis` op 0 zetten en de `flex-grow` op 1.
> <br/>

<br/>

### 2.11.5 Marges

> In het onderstaande voorbeeld staat `margin` op `auto` (standaardwaarde).

<table>
<tr>
<th>HTML</th>
<th>CSS</th>
</tr>
<tr>
<td>

```HTML
<ul>
  <li>Branding</li>
  <li>Home</li>
  <li>Services</li>
  <li>About</li>
  <li>Contact</li>
</ul>
```

</td>
<td>

```CSS
ul {
  display: flex;
}

li {
  flex: 0 0 auto;
}
```

</td>
</tr>
</table>
<br/>
<img src="images/menubar1.png" width=600px>

<br/>

> In het onderstaande stellen we de rechtermarge in op `auto`.

<table>
<tr>
<th>HTML</th>
<th>CSS</th>
</tr>
<tr>
<td>

```HTML
<ul>
  <li>Branding</li>
  <li>Home</li>
  <li>Services</li>
  <li>About</li>
  <li>Contact</li>
</ul>
```

</td>
<td>

```CSS
ul {
  display: flex;
}

li {
  flex: 0 0 auto;
}
li:nth-child(1) {
  margin-right: auto;
}
```

</td>
</tr>
</table>
<br/>
<img src="images/menubar2.png" width=600px>

> In het laatste voorbeeld zetten we ook de linkermargin op `auto`.

<img src="images/menubar3.png" width=600px>

<br/>
<br/>

## 2.12 Tekst en typografie

### 2.12.1 Lettertype

> Als je custom lettertypes wilt gebruiken zijn er 2 opties om deze op een webpagina te gebruiken.
>
> - Beschik je over fysieke bestanden:
>   - Download alle varianten
>   - Plaats deze op de webserver in een aparte folder
>   - Gebruik [`@font-face`](https://developer.mozilla.org/en-US/docs/Web/CSS/@font-face) in CSS om lettertypes beschikbaar te maken
> - Beschik je over een embedcode:
>   - Zoek bv. een [Google Font](https://fonts.google.com/) en kies de gewenste stijlen
>   - Kopieer de embedcode
>     - Plaats dit in `head` van HTML pagina
>     - Of `@import` regel in de CSS

> **Eigenschappen van lettertypes**
>
> - [`font-family`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family) geprioritiseerde lijst van lettertypes
> - [`font-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size) grootte van het lettertype
> - [`font-size-adjust`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-size-adjust) om de tekstgrootte gelijk te houden wanneer wordt teruggevallen op een 2de,.. keus in de font-family
> - [`line-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height) regelafstand, hoeveelheid wit tussen regels tekst
> - [`font-weight`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-weight) de vetheid, 100-900 of `normal`, `bold`, `bolder`, `lighter`
> - [`font-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-style) weergave tekst, zoals normal, italic of oblique
> - [`font-variant`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-variant) kleinkapitaal, zoals small-caps
> - [`font-stretch`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-stretch) uitrekken of indrukken
> - [`font`](https://developer.mozilla.org/en-US/docs/Web/CSS/font) de verzameleigenschap: _font-style font-variant font-weight font-size/line-height font-family_

<br/>

### 2.12.2 Teksteigenschappen

> **Eigenschappen van tekst** <br/>
>
> - [`color`](https://developer.mozilla.org/en-US/docs/Web/CSS/color) kleur
> - [`text-align`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align) uitlijnen (left, right, center, justify,..)
> - [`text-align-last`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-align-last) uitlijnen laatste regel
> - [`text-decoration`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-decoration) lijneffect
> - [`text-indent`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-indent) inspringen van de eerste regel van een tekstblok
> - [`text-orientation`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-orientation) horizontale of verticale tekst
> - [`text-overflow`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-overflow) overlopende tekst, bepaald welk visueel effect de gebruiker krijgt als er meer tekst is dna hij ziet
> - [`text-shadow`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-shadow) schaduw
> - [`text-transform`](https://developer.mozilla.org/en-US/docs/Web/CSS/text-transform) hoofdletters, kleine letters,..
> - [`white-space`](https://developer.mozilla.org/en-US/docs/Web/CSS/white-space) witruimte al dan niet behouden
> - [`letter-spacing`](https://developer.mozilla.org/en-US/docs/Web/CSS/letter-spacing) ruimte tussen letters
> - [`word-spacing`](https://developer.mozilla.org/en-US/docs/Web/CSS/word-spacing) ruimte tussen woorden
> - [`word-break`](https://developer.mozilla.org/en-US/docs/Web/CSS/word-break) automatisch afbreken
> - [`overflow-wrap`](https://developer.mozilla.org/en-US/docs/Web/CSS/overflow-wrap) is afbreken van een woord toegestan
> - [`line-height`](https://developer.mozilla.org/en-US/docs/Web/CSS/line-height) afstand tussen regels
> - [`border-bottom`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom) versiering lijn van de box

<br/>

### 2.12.3 Lijstopmaak

> **Eigenschappen voor lijstopmaak**
>
> - [`list-style-type`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-type) opsommingsteken
> - [`list-style-image`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-image) afbeelding als opsommingsteken
> - [`list-style-position`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style-position) plaatsing opsommingsteken
> - [`list-style`](https://developer.mozilla.org/en-US/docs/Web/CSS/list-style) afkorting

<br/>

## 2.13 [Kleuren](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Colors/Color_picker_tool)

> Kleuren kunnen op 4 manieren omschreven worden:
>
> - een rgb(a)-code: `rgba(145,233,12,0.7)` (red, green, blue, (opacity))
> - een (verkorte) hex-code: `#1e85af`
> - keyword: `red`, `green`, `blue`
> - een hsl(a)-code: `hsl(0, 100%, 100%)` (hue, saturation, lightness, (opacity))
>
> [`opacity`](https://developer.mozilla.org/en-US/docs/Web/CSS/opacity): transparantie (waarde tussen 0 en 1)

<br/>

### 2.13.1 Kleurverlopen

> **Kleurverlopen**
>
> - [`linear-gradient`](<https://developer.mozilla.org/en-US/docs/Web/CSS/linear-gradient()>) lineair verloop (bv. links naar rechts, boven naar onder)
> - [`radial-gradient`](<https://developer.mozilla.org/en-US/docs/Web/CSS/radial-gradient()>) radiaal verloop
>
> Het gemakkelijkste is om hier een [generator](https://cssgradient.io/) voor te gebruiken.
> <br/>

## 2.14 [Achtergrond](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Backgrounds_and_borders)

> Iedere box van een element heeft een achtergrond, default transparent
>
> - [`background-color`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-color) achtergrondkleur
> - [`background-image`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-image) de afbeelding
> - [`background-repeat`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-repeat) herhalen van de afbeelding tot alle ruimte in het blok is gevuld
> - [`background-attachment`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-attachment) een afbeelding schuift standaard mee met de rest van de pagina, maar je kan hem ook vastzetten
> - [`background-position`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-position) plaatsing
> - [`background-clip`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-clip) weergave overloop
> - [`background-origin`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-origin) plaatsing
> - [`background-size`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-size) schalen
> - [`background`](https://developer.mozilla.org/en-US/docs/Web/CSS/background) verkorte versie

<br/>

## 2.15 [Afgeronde hoeken](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius)

> Men kan de hoeken van elementen afronden. Dit doen we met:
>
> - [`border-radius`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-radius) alle hoeken afronden
> - [`border-top-left-radius`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-left-radius) linksboven afronden
> - [`border-top-right-radius`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-top-right-radius) rechtsboven afronden
> - [`border-bottom-left-radius`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom-left-radius) linksonder afronden
> - [`border-bottom-right-radius`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-bottom-right-radius) rechtsonder afronden
>
> Hier bestaat ook een [generator](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Background_and_Borders/Border-radius_generator) voor.

## 2.16 Randafbeeldingen

> Beeld voor de rand van een element
>
> - [`border-image`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-image) afgekorte versie
> - [`border-image-source`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-image-source) de afbeelding
> - [`border-image-slice`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-image-slice) opdelen van beeld in regio's
> - [`border-image-width`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-image-width) breedte
> - [`border-image-outset`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-image-outset) de afstand waarmee de randafbeelding wordt uitgezet ten opzichte van zijn randkader
> - [`border-image-repeat`](https://developer.mozilla.org/en-US/docs/Web/CSS/border-image-repeat) hoe vult het beeld de rand
>
> Hier bestaat eveneens een [generator](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Background_and_Borders/Border-image_generator) voor.

## 2.17 Boxshadow

> [`box-shadow`](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow) schaduw onder een element
>
> Hier bestaat een [generator](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Background_and_Borders/Box-shadow_generator) voor.

<br/>

## 2.18 Clip path

> [`clip-path`](https://developer.mozilla.org/en-US/docs/Web/CSS/clip-path) definieert een gebied/vorm en alles daarbuiten wordt weggeknipt
>
> Hier bestaat een [generator](https://bennettfeely.com/clippy/) voor.

<br/>

## 2.19 Beeldfilters en kleuren mengen

> **Beeldfilters**
>
> - [`filter`](https://developer.mozilla.org/en-US/docs/Web/CSS/filter) toepassen van grafische effecten, zoals blur of color shift, op afbeeldingen

> **Kleuren mengen**
>
> - [`background-blend-mode`](https://developer.mozilla.org/en-US/docs/Web/CSS/background-blend-mode) mengen van achtergrondsafbeeldingen en achtergrondskleur element
> - [`mix-blend-mode`](https://developer.mozilla.org/en-US/docs/Web/CSS/mix-blend-mode) inhoud van element mengne met zijn achtergrond en inhoud ouderelementen

<br/>

## 2.20 CSS variabelen en rekenen

> **Rekenen** <br/>
> Je kan `+`, `-`, `*` en `/` gebruiken met alle eenheden.

> **De functie `var()`**
> Je kan globale variabelen definiëren in het `:root` element (zie voorbeeld).
>
> ```CSS
> :root {
>  --main-bg-color: pink;
> }
>
> body {
>  background-color: var(--main-bg-color)
> }
> ```
>
> Dit doen we met een [`property value`](https://developer.mozilla.org/en-US/docs/Web/CSS/--*).

<br/>

# 3. SASS

> [SASS](https://sass-lang.com/guide) is een CSS extension language. Het voegt extra features toe aan CSS. Tot voor kort ondersteunde CSS geen variabelen, maar in SASS bestaan variabelen al meer dan 10 jaar. SASS biedt naast variabelen ook nog andere features zoals interpolation, nested rules, mixins, functions, partials,... aan.

> Voor SASS hebben we een preprocessor nodig, zoals 'Live Sass Compiler'. We schrijven deze code in een `.scss` bestand. Door op `Watch Sass` zal het bestand omgezet worden naar een normaal css bestand.

## 3.1 Variabelen

> Men kan makkelijk variabelen maken met een `$` teken. Voorbeeld: <br/>

```SCSS
// Variabelen
$primary-color: rgb(173, 178, 247);
$light: white;
$font: Calibri, sans-serif;
$nav-link-color: white;

//Basis stijlen

body {
  font-family: $font;
  font-size: 1.1rem;
}

h1 {
  font-size: 3rem;
  text-align: center;
}

body, header {
  background-color: $primary-color;
}

//...
```

> Vergeet geen link te leggen naar het **CSS** bestand vanuit HTML.

<br/>

## 3.2 Nested rules

> Met SASS kan je stijlregels nesten. Zo kan je onderstaande code

### 3.2.1 Descending selector

```CSS
nav ul {
  ...
}
nav a {
  ...
}
```

> Als volgt schrijven:

```SCSS
nav {
  ul {
    ...
  }

  a {
    ...
  }
}
```

<br/>

### 3.2.2 Parent selector

> Met het `&` teken kan men de parent selecteren in een nesting. Voorbeeld:

```SCSS
nav {
  a {
    display: block;
    color: $nav-link-color;
    text-decoration: none;
    &:hover {
      text-decoration: underline;
    }
  }
}
```

> `&:hover` staat in dit geval gelijk aan `nav a:hover`

<br/>

## 3.3 Partials

> Als je veel CSS `@import`-statements gebruikt dan kan dit het laden van de CSS in de browser vertragen. We doen dit beter uit slechts één file. <br/>
> We kunnen in de main SCSS klasse bv. `@import "variables"` zetten. Dan zal de file genaamd `_variables.scss` door de compiler meegecompiled worden in 1 klasse. Je kan zo veel import regels doen als je wilt. <br/> **Note:** de naam van een partial scss file moet met een `_` beginnen.

<br/>

# 4. Bootstrap

> Bootstrap is een CSS-framework om op een eenvoudige en snelle manier een responsive website te maken. Er zijn twee manieren om bootstrap te gebruiken.
>
> - **Compiled version** <br/>
>   Als we werken met de compiled version kan met Bootstrap gewoon zien als een CSS file (ev. met javascript).
> - **Source files** <br/>
>   Het is ook mogelijk om met de .SCSS source files te werken en zelf het framework aan te passen.
>
> We maken zelf meestal gebruik van gewoon de [`bootstrap.css`](https://getbootstrap.com/docs/4.5/getting-started/download/) file.

## 4.1 Containers

> Om de webpagina van enige padding te voorzien en om eventueel de inhoud te centreren moet je een bootstrap container gebruiken. We voegen dus `class="container"` toe aan bv. een `<div>` element. Naar mate je venster vergroot/verkleint zal de container zich aanpassen.

## 4.2 Bootstrap grid system

> Het bootstrap grid system gebruikt `containers`, `rows` en `columns`. Op onderstaande foto zie je hoe dit in zijn werk gaat.
> <br/> <img src="images/bootstrapgrid.png" width=500px>

## 4.3 Content

### 4.3.1 [Reboot](https://getbootstrap.com/docs/4.5/content/reboot/)

> Bootstrap maakt gebruik van een reboort-file die gebaseerd is op `normalize.css`. Je kan dit controleren door `bootstrap-reboot.css` eens te openen in VSCode.

<br/>

### 4.3.2 [Afbeeldingen](https://getbootstrap.com/docs/4.5/content/images/)

> We kunnen afbeeldingen makkelijk responsive maken door aan het `<img>` element de bootstrap klasse `img-fluid` toe te wijzen.

## 4.4 Componenten

### 4.4.1 [Buttons](https://getbootstrap.com/docs/4.5/components/buttons/)

> We kunnen met Bootstrap snel mooie buttons maken door bv. `class="btn btn-primary"` toe te voegen aan een `<button>` element. Meer voorbeelden: <br/> <img src="images/buttons.png" width=600px>

Er zijn nog veel componenten in bootstrap. Hiervoor ga je best naar de workshop `02_bootstrap_workshop.pdf` of naar de boostrap website.

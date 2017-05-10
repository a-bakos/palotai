# Bejegyzések - _típusok és közzétételi útmutató_

<a id="tartalom"></a>
## Tartalom

+ [Címsor és közvetlen hivatkozás](#cimsor-link)
	+ [Példa a mixek bejegyzéseihez](#cimsor-link_pelda-mix)
	+ [Példa a további bejegyzéstípusokhoz](#cimsor-link_pelda-altalanos)
+ [Bejegyzések dátumozása](#datum)
	+ [Példa](#datum_pelda)
	+ [Dátumozás intervallum esetén](#datum-intervallum)
		+ [Példa](#datum-intervallum_pelda)
+ [Bejegyzés fejléc-szerkezet a mixek számára](#bejegyzes-mix-fejlec)
	+ [Felépítés](#bejegyzes-mix-fejlec_felepites)
	+ [Példa-fejléc elérhető tracklist-tel és letölthető mix-szel](#bejegyzes-mix-fejlec_felepites-pelda)
		+ [Szerkezet](#bejegyzes-mix-fejlec_felepites-pelda-szerkezet)
		+ [Így jelenik meg](#bejegyzes-mix-fejlec_felepites-pelda-megjelenes)
+ [Tracklist szerkezet](#bejegyzes-mix-tracklist)
	+  [Példa](#bejegyzes-mix-tracklist_pelda)
		+ [Így jelenik meg](#bejegyzes-mix-tracklist_pelda-megjelenes)
+ [Interjú bejegyzések](#bejegyzes-interju)
	+ [Így jelenik meg](#bejegyzes-interju-megjelenes)

___

<a id="cimsor-link"></a>
## Címsor és közvetlen hivatkozás

![Bejegyzés hozzáadás - címek](img/bejegyzes-hozzaadas-cimek.png)

Címsorban legelső elem a `[TAG]`, ami meghatározza a bejegyzés tartalmát. Ez a `[TAG]` lehet `[MIX]`, `[INTERJÚ]`, `[KEDVENC LEMEZEK]`. Írjuk őket nagybetűvel, szögletes zárójelek közé téve.

Erre azért van szükség, hogy az oldalsávban megjelenő legutóbbi bejegyzések lista eseményei könnyebben áttekinthetőek legyenek:

![Bejegyzés hozzáadás - legutóbbi bejegyzések](img/bejegyzes-hozzaadas-legutobbiak.png)

A második elem a címsorban a bejegyzés címe. Ha dátumot tartalmaz, akkor az kerül előre, úgy mint: `2000-18-28 Jövőzene`. Legyen szépen prezentálva, figyeljünk a nagy kezdőbetűre.

<a id="cimsor-link_pelda-mix"></a>
#### Példa a mixek bejegyzéseihez

Mixek esetén, a közvetlen hivatkozásnál a slug-ból töröljük a `[TAG]`-et, csak a bejegyzés címe jelenjen meg.

**Címsor:** `[MIX] 2000-18-28 Jövőzene`

**Közvetlen hivatkozás:** `[...]/palotai-depo/2000-18-28-jovozene/`

<a id="cimsor-link_pelda-altalanos"></a>
#### Példa a további bejegyzéstípusokhoz

**Címsor:** `[INTERJÚ] Sokszínűség, sok szeméttel 2003-09-13`

**Közvetlen hivatkozás:** `[...]/palotai-depo/interju-sokszinuseg-sok-szemettel-2003-09-13`

_[(Ugrás a tartalomjegyzékhez)](#tartalom)_

---

<a id="datum"></a>
## Bejegyzések dátumozása

Minden olyan tartalmnál, ahol tudjuk az eredeti megjelenési dátumot, alkamazzuk azt.
Így lesz konzisztens az archívum, illetve ily módon sorrendben jelenik meg minden
felsorolásban a WordPress-ben.

<a id="datum_pelda"></a>
#### Példa

A `Jövőzene 2000/09/23` mix bejegyzésnél a következő beállítást alkalmazzuk:

![Bejegyzés hozzáadás - dátumozás](img/bejegyzes-hozzaadas-datum.png)

<a id="datum-intervallum"></a>
### Dátumozás intervallum esetén

Amikor olyan tartalomról van szó, ahol egy intervallum van megadva, ott annak az utolsó
napját állítsuk be.

<a id="datum-intervallum_pelda"></a>
#### Példa

`Az impulsecreator party-beszámolói 1999.09.18.-2001.05.19.` című bejegyzésnél a 2001. május 19-i
dátumot fogjuk használni.

_[(Ugrás a tartalomjegyzékhez)](#tartalom)_

---

<a id="bejegyzes-mix-fejlec"></a>
## Bejegyzés fejléc-szerkezet a mixek számára

<a id="bejegyzes-mix-fejlec_felepites"></a>
### Felépítés

**1. A bejegyzés indító**

A bejegyzés címét H3 tag-ek közé tegyük.

```HTML
<h3>Bejegyzes cime</h3>

<hr />

<p class="entry-header-info">
```

---

**2. Tracklist**

+ Ha van tracklist: `a opció`

+ Ha nincs tracklist: `b opció`

a)

``` HTML

<span class="text-highlight hi-lite-title">Tracklist:</span> <span class="text-highlight hi-lite-content hi-lite-yes">van &#10003;</span>

```

b)

``` HTML
<span class="text-highlight hi-lite-title">Tracklist:</span> <span class="text-highlight hi-lite-content hi-lite-no">nincs &#10008;</span>
```

---

**3. Mix.**

+ Ha van mix: `a opció`

+ Ha nincs mix: `b opció`

a) Ha van elérhető mix, akkor írjuk be a **hosszát**, illesszük be a **fájl linkjét**, majd töltsük ki a **mintavételt**, **formátumot** és a **méretét** a fájlnak. A hosszt szimpla 'perc:másodperc' alapon adjuk meg. Mintavétel, formátum és fájlméret a következőképp néz ki: `128kbps MP3 / 118MB`.

``` HTML
<span class="text-highlight hi-lite-title">Mix:</span> <span class="text-highlight hi-lite-content hi-lite-yes">van &#10003;</span>

<span class="text-highlight hi-lite-title">Hossz:</span> <span class="text-highlight hi-lite-content hi-lite-yes">?</span>

<span class="text-highlight hi-lite-title">Letöltés:</span> <a href="" class="letoltes"><span class="text-highlight hi-lite-content hi-lite-yes">?kbps MP3 / ?MB &#8628;</span></a>
```

b) Ha nincs letölthető mix, ne jelenítsük meg feleslegesen a hossz és letöltés sorokat, csak annyit, hogy `nincs`.

``` HTML
<span class="text-highlight hi-lite-title">Mix:</span> <span class="text-highlight hi-lite-content hi-lite-no">nincs &#10008;</span>
```

---

**4. Fejléc záró**

Választóvonal, tovább gomb és tracklist fejléc. Ezután következik maga a tracklist.

``` HTML
</p>

<hr />

<!--more-->

<p><span class="text-highlight hi-lite-title">Tracklist:</span></p>
```

---

<a id="bejegyzes-mix-fejlec_felepites-pelda"></a>
#### Példa-fejléc elérhető tracklist-tel és letölthető mix-szel

<a id="bejegyzes-mix-fejlec_felepites-pelda-szerkezet"></a>
##### Szerkezet

``` HTML
<h3>Jövőzene 2000/03/18</h3>

<hr />

<p class="entry-header-info">
<span class="text-highlight hi-lite-title">Tracklist:</span> <span class="text-highlight hi-lite-content hi-lite-yes">van &#10003;</span>

<span class="text-highlight hi-lite-title">Mix:</span> <span class="text-highlight hi-lite-content hi-lite-yes">van &#10003;</span>

<span class="text-highlight hi-lite-title">Hossz:</span> <span class="text-highlight hi-lite-content hi-lite-yes">103:18</span>

<span class="text-highlight hi-lite-title">Letöltés:</span> <a class="letoltes" href=""><span class="text-highlight hi-lite-content hi-lite-yes">160kbps MP3 / 118MB &#8628;</span></a>
</p>

<hr />

<!--more-->

<p><span class="text-highlight hi-lite-title">Tracklist:</span></p>
```

<a id="bejegyzes-mix-fejlec_felepites-pelda-megjelenes"></a>
##### Így jelenik meg a tovább kattintás után

![Bejegyzés hozzáadás - fejléc példa](img/bejegyzes-hozzaadas-fejlec-pelda.png)

_[(Ugrás a tartalomjegyzékhez)](#tartalom)_

---

<a id="bejegyzes-mix-tracklist"></a>
## Tracklist szerkezet

A tracklist következő felépítése elsősorban az esztétikai élmény és az olvashatóság miatt érdekes, de teljesen megfelelő az is, ha csak szimplán beillesztjük a listát a fenti fejléc után.

A tracklist-ben előforduló elemeket, azaz zenéket **általában** maximum 4 részre tudjuk osztani: sorszám, előadó + zene címe, remix (vagy zárójeles) megnevezés (ha van), kiadvány katalógus száma (ha van).

+ A sorszámot tegyük `<span>` tag-be és adjunk neki `text-highlight` class-ot.
``` HTML
<span class="text-highlight">25.</span>
```

+ Előadó + a zene szám címe marad natúr. Jobban olvasható lesz a lista, ha csak a kezdőbetűket írjuk naggyal.
``` HTML
Klute / Phone Call
```

+ A remix vagy zárójeles megnevezést tegyük `<span>` tag-be és kapjon `text-cream` class-t.
``` HTML
<span class="text-cream">(Matrix Remix)</span>
```

+ A kiadvány katalógus száma szintén `<span>`-be kerül és `text-mono` class-t kap.
``` HTML
<span class="text-mono">CERT 18 043</span>
```

<a id="bejegyzes-mix-tracklist_pelda"></a>
#### Példa

``` HTML
<span class="text-highlight">24.</span> Ram Jam World / Bluesy Baby <span class="text-cream">(Ed Rush & Optical Remix)</span> - <span class="text-mono">F-111</span>

<span class="text-highlight">25.</span> Klute / Phone Call <span class="text-cream">(Matrix Remix)</span> - <span class="text-mono">CERT 18 043</span>

<span class="text-highlight">26.</span> Crackpot / Tippy Tippy Toe - <span class="text-mono">TUCH 042</span>

<span class="text-highlight">27.</span> Dj Food featuring Ken Nordine / The Ageing Young Rebel <span class="text-cream">(Gentle Cruelty)</span> - <span class="text-mono">ZEN LP 049</span>
```

<a id="bejegyzes-mix-tracklist_pelda-megjelenes"></a>
##### Így jelenik meg

![Bejegyzés hozzáadás - tracklist](img/bejegyzes-hozzaadas-tracklist.png)

_[(Ugrás a tartalomjegyzékhez)](#tartalom)_

---

<a id="bejegyzes-interju"></a>
## Interjú bejegyzések

Az interjúkat értelemszerűen tartalmi változtatás nélkül közöljük minden esetben, amennyiben lehetséges minden forrással ellátva.

Az interjú szerkezete függ az eredeti interjútól, így ha nincs rá mód, akkor ne változtassunk semmin. Amennyiben van mód némi formázásra, akkor a következő szabályokat próbáljuk alkalmazni.

A legelső sorban a címet `H3` tag-gel írjuk.

Ha van idézet a cikk elején, vagy bárhol az írásban, azt `blockquote` blokkba tegyük.

A rövid, cikk összefoglaló bekezdést tegyük `span` tag-ek közé, és adjunk neki `text-cream` és `text-midsize` class-okat.

Az interjúztató, kérdező, riporter sorait tegyük `span`-ba `text-question` class hozzáadásával a jobb olvashatóság végett.

Palotai válaszai előtt (opcionálisan) megjeleníthető egy `P:`, vagy `P.Zs.:` jelzés `span` tag-ek között `text-pzs` class-szal ellátva. Esetlegesen, a legelső válasznál írjuk ki a teljes nevét.

<a id="bejegyzes-interju-megjelenes"></a>
##### Így jelenik meg

![Bejegyzés hozzáadás - interjú](img/bejegyzes-hozzaadas-interju.png)

_[(Ugrás a tartalomjegyzékhez)](#tartalom)_

---


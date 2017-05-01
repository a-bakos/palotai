### Bejegyzés fejléc a mixeknek

---

**1. A bejegyzés indító.**

```HTML
<h3>Bejegyzes cime</h3>

<hr />
```

---

**2. Tracklist.** `a opció`, ha van; `b opció`, ha nincs

a)

``` HTML

<p><span class="text-highlight hi-lite-title">Tracklist:</span> <span class="text-highlight hi-lite-content hi-lite-yes">van</span></p>

```

b)

``` HTML
<p><span class="text-highlight hi-lite-title">Tracklist:</span> <span class="text-highlight hi-lite-content hi-lite-no">nincs</span></p>
```

---

**3. Mix.** `a opció`, ha van; `b opció`, ha nincs

a) Ha van elérhető mix, akkor írjuk be a hosszát, a mintavételt és a méretét a fájlnak.

``` HTML
<p><span class="text-highlight hi-lite-title">Mix:</span> <span class="text-highlight hi-lite-content hi-lite-yes">van</span></p>

<p><span class="text-highlight hi-lite-title">Hossz:</span> <span class="text-highlight hi-lite-content hi-lite-yes">?</span></p>

<p><span class="text-highlight hi-lite-title">Letöltés:</span> <a class="letoltes" href=""><span class="text-highlight hi-lite-content hi-lite-yes">128kbps MP3 / 150MB</span></a></p>
```

b)

``` HTML
<p><span class="text-highlight hi-lite-title">Mix:</span> <span class="text-highlight hi-lite-content hi-lite-no">nincs</span></p>
```

---

**4. Fejléc záró**

``` HTML
<hr />

<!--more-->

<p><span class="text-highlight hi-lite-title">Tracklist:</span></p>
```
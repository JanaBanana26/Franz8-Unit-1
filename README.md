# L'échange scolaire – Französisch Klasse 8

Interaktive Wiederholung für den Französischunterricht in Klasse 8 im Comic-Look in Blau und Rot. Die Schrift ist Abadi, mit Gill Sans, Calibri und Systemschrift als Ersatz auf Geräten ohne Abadi.

- **Übersicht** mit Fortschritt pro Thema und dem „Reisepass“ (XP, Level, Trophäen)
- **Spickzettel** zu Objektpronomen, Komparativ und Superlativ (druckbar)
- **Vokabeln** aus *Découvertes 3, Unité 1* (109 Vokabeln): Wortliste, Karteikarten (FR→DE und DE→FR) und Schreibtest
- **Üben** mit 38 Grammatikaufgaben und dem Vokabel-Schreibtest, mit Spielmodus
- **Lernzielkontrolle** zum Ausdrucken mit Lösungsblatt und Selbsteinschätzung; jede Version wird zufällig zusammengestellt (3 Multiple-Choice- und 3 Lückenaufgaben je Grammatikthema plus 8 Vokabeln, 26 Punkte)

Die gesamte Anwendung besteht aus einer einzigen Datei (`index.html`). Es gibt keine externen Bibliotheken, keine Schriften von Drittanbietern und kein Tracking. Fortschritt, XP und Trophäen werden nur lokal im Browser gespeichert.

## Spielmodus

- **XP:** 10 XP pro richtiger Antwort, dazu Bonus für Serien (bis +10) und Zusatzaufgaben (+10). Die Karteikarte „Gewusst“ gibt 3 XP.
- **Combo:** Mehrere richtige Antworten in Folge bauen eine Serie auf.
- **Sterne:** Am Rundenende gibt es 1 bis 3 Sterne (ab 50 %, 70 % und 90 %) mit XP-Bonus.
- **Level und Ränge:** Alle 100 XP steigt das Level, vom Neuankömmling bis zum „Maître de l'échange“.
- **Trophäen:** 8 Stück, zum Beispiel „Erste Reise“, „Feuer & Flamme“ (5 in Folge), „Parfait !“ (Runde ohne Fehler), „Fehlerjäger“ und „Vokabelheld“.

## Veröffentlichen mit GitHub Pages

1. Neues Repository auf GitHub anlegen (Public) und `index.html` sowie `README.md` hochladen.
2. Im Repository: **Settings → Pages**.
3. Unter **Build and deployment** bei *Source* **Deploy from a branch** wählen, Branch `main` und Ordner `/ (root)` auswählen, speichern.
4. Nach ca. einer Minute ist die Seite unter `https://<benutzername>.github.io/<repository>/` erreichbar.

## Vokabeln anpassen

Die Vokabeln stehen in `index.html` im Array `VRAW`, eine Zeile pro Wort (Französisch, Deutsch):

```js
["un échange scolaire","ein Schüleraustausch"],
["gentil/gentille","nett"],
["un/e partenaire d'échange","ein Austauschpartner, eine Austauschpartnerin",["un partenaire d'échange","une partenaire d'échange"]]
```

- Die Nummer ergibt sich aus der Reihenfolge. Die Teile in `CATS` (je ca. 27 Wörter) werden ebenfalls aus der Position abgeleitet.
- Beim Schreibtest werden Varianten automatisch erkannt: `/` und `,` trennen männliche und weibliche Form, `=` trennt gleichwertige Wendungen, `qn` / `qc` am Ende darf fehlen, Satzzeichen sind egal.
- Eine dritte Angabe (Liste) legt die akzeptierten Schreibweisen selbst fest.

## Grammatikaufgaben ergänzen

Die Aufgaben stehen im Array `EX`:

```js
// Multiple Choice: a = Index der richtigen Option
{t:'obj', type:'mc',  q:"Je vois Marie. → Je ___ vois.", opts:["la","le","lui"], a:0, e:"Erklärung"}

// Lückentext: a = Liste akzeptierter Antworten
{t:'comp', type:'gap', q:"Il joue ___ que moi. (bien, mehr)", a:["mieux"], e:"Erklärung"}
```

- `t` ist das Thema: `obj`, `comp` oder `sup`. Mit `bonus:true` wird eine Aufgabe zur Zusatzaufgabe (mehr XP, nicht in der Lernzielkontrolle).
- Bei Lücken werden fehlende Akzente nicht akzeptiert, es gibt aber einen Hinweis und einen zweiten Versuch.

## Drucken

- **Spickzettel:** im Bereich „Spickzettel“ auf „Drucken“ klicken.
- **Test:** im Bereich „Lernzielkontrolle“ „Test drucken“ wählen, das Lösungsblatt über „Lösungsblatt drucken“.

## Lizenz

Für Unterrichtsmaterial bietet sich zum Beispiel CC BY-SA 4.0 an. Die Vokabeln stammen aus dem Lehrwerk *Découvertes 3* (Klett); prüfe vor einer öffentlichen Veröffentlichung, ob die Wortliste frei geteilt werden darf, oder veröffentliche das Repository nur für deine Klasse.

# Français 8 – Wiederholungs-Widget

Interaktive Wiederholung für den Französischunterricht in Klasse 8:

- **Objektpronomen** (le, la, les, lui, leur …)
- **Komparativ** (plus/aussi/moins … que, meilleur, mieux)
- **Superlativ** (le plus, la moins, le meilleur …)

Enthalten sind eine Übersicht mit Lernfortschritt, ein druckbarer **Grammatikspickzettel** und **Übungen** (Multiple Choice und Lückentexte mit Sofort-Feedback, Erklärungen und Fehlerwiederholung).

Die gesamte Anwendung besteht aus einer einzigen Datei (`index.html`). Es gibt keine externen Bibliotheken, keine Schriftarten von Drittanbietern und kein Tracking. Der Lernfortschritt wird nur lokal im Browser gespeichert.

## Veröffentlichen mit GitHub Pages

1. Neues Repository auf GitHub anlegen und `index.html` sowie `README.md` hochladen.
2. Im Repository: **Settings → Pages**.
3. Unter **Build and deployment** bei *Source* **Deploy from a branch** wählen, Branch `main` und Ordner `/ (root)` auswählen, speichern.
4. Nach ca. einer Minute ist die Seite unter `https://<benutzername>.github.io/<repository>/` erreichbar. Diesen Link kannst du an die Klasse weitergeben (zum Beispiel als QR-Code).

Einbetten in eine andere Seite:

```html
<iframe src="https://<benutzername>.github.io/<repository>/" title="Français 8 Wiederholung" width="100%" height="800" style="border:0"></iframe>
```

## Aufgaben ergänzen oder ändern

Die Aufgaben stehen in `index.html` im Array `EX`. Jede Aufgabe ist ein Objekt:

```js
// Multiple Choice: a = Index der richtigen Option
{t:'obj', type:'mc',  q:"Je vois Marie. → Je ___ vois.", opts:["la","le","lui"], a:0, e:"Erklärung"}

// Lückentext: a = Liste akzeptierter Antworten
{t:'comp', type:'gap', q:"Il joue ___ que moi. (bien, mehr)", a:["mieux"], e:"Erklärung"}
```

- `t` ist das Thema: `obj` (Objektpronomen), `comp` (Komparativ) oder `sup` (Superlativ).
- `___` markiert die Lücke.
- Mit `bonus:true` wird eine Aufgabe als Zusatzaufgabe gekennzeichnet.
- Bei Lückentexten werden fehlende Akzente nicht akzeptiert, die Lernenden erhalten aber einen Hinweis und einen zweiten Versuch. Unter der Lücke gibt es Buttons für französische Sonderzeichen.

## Lizenz

Für Unterrichtsmaterial bietet sich zum Beispiel CC BY-SA 4.0 an. Ergänze bei Bedarf eine `LICENSE`-Datei.

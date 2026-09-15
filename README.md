<!--
author:   Sebastian Zug, André Dietrich, Ines Aubel
email:    sebastian.zug@informatik.tu-freiberg.de
version:  1.0.0
language: de
narrator: Deutsch Female
comment:  Vortrag DELFI 2026 — Feature-Adoption in LiaScript.
          20 Minuten. Diese Folien sind selbst ein LiaScript-Kurs.
mode:     Presentation

@quote: > **„@0"**
>
> <div style="text-align:right">— @1</div>

@bigfact
<div style="text-align:center;padding:1.2rem 0">
<div style="font-size:3.4rem;font-weight:700;line-height:1.1;color:#2E86AB">@0</div>
<div style="font-size:1.15rem;color:#555;margin-top:.4rem">@1</div>
</div>
@end

@twocol
<div style="display:flex;gap:2rem;align-items:flex-start">
<div style="flex:1">@0</div>
<div style="flex:1">@1</div>
</div>
@end
-->

# Was nutzen sie wirklich?

**Feature-Adoption in einem System ohne Telemetrie**

Sebastian Zug · André Dietrich · Ines Aubel
*TU Bergakademie Freiberg*

---

DELFI 2026

                                  {{1}}
<div style="margin-top:2rem;padding:.8rem 1.2rem;border-left:4px solid #2E86AB;background:#f0f6fa">
Diese Folien sind selbst ein LiaScript-Kurs.
</div>

## Teil 1 — LiaScript

### Markdown rein, Kurs raus

@twocol(**Ein Kurs ist eine Markdown-Datei.**

Kein Server. Keine Accounts.
Keine Installation.

Der Browser rendert sie zur
Lehrveranstaltung — mit Quiz,
Sprachausgabe und Code-Ausführung.)(```markdown
# Mein Kurs

Was ist 2 + 2?

[[4]]

**Text mit Sprachausgabe.**
```)

### Sovereignty by Design

@quote(Die Eigenschaft, die LiaScript für OER richtig macht, macht uns blind.)(Der Ausgangspunkt dieses Papers)

- **kein Server** → keine Logs
- **keine Accounts** → keine Nutzerprofile
- **keine Telemetrie** → keine Nutzungsdaten

                                  {{1}}
Autor:innen behalten die volle Kontrolle über ihre Inhalte.

                                  {{2}}
Wir wissen dafür **nicht**, wie LiaScript verwendet wird.

### Die Community wächst

![Kumulierte Kurse und Autoren 2017–2026](img/growth.png)

**293 Autor:innen**, 5.042 Kurse (Stand August 2026)

                                  {{1}}
> Die blaue Fläche ist **ein einziges Projekt**. Merken Sie sich das.

## Teil 2 — Das Problem

### Wir bauen Workshops. Für wen?

@bigfact(0)(Rückmeldungen aus der Nutzung)

Wir führen Tutorials und Workshops durch — und entscheiden dabei laufend:

- Welche Features zeigen wir zuerst?
- Was lassen wir weg?
- Wo hakt es in der Praxis?

                                  {{1}}
**Bisher: Bauchgefühl.**

### Kurze Frage an Sie

Wer von Ihnen entwickelt Lehrmaterial oder Werkzeuge,
**ohne** zu wissen, wie sie tatsächlich genutzt werden?

                                  {{1}}
<div style="margin-top:1.5rem;padding:1rem;background:#fff8e6;border-left:4px solid #F18F01">
Genau dieses Problem haben dezentrale, datensparsame Systeme —
strukturell und dauerhaft.
</div>

## Teil 3 — Methodik

### GitHub als einziger Beobachtungspunkt

Kurse liegen in öffentlichen Repositories. Das ist der **einzige** Kanal,
über den wir Nutzung sehen können.

| | |
|---|---|
| Validierte Kurse | **3.317** |
| Autor:innen | **314** |
| Stand | März 2026 |

                                  {{1}}
**Wichtige Einschränkung:** Wir messen *author adoption* —
welche Features Autor:innen **einbauen**.
Nicht, was Lernende damit tun.

### Taxonomie

Vier didaktisch motivierte Kategorien, 44 Features:

- **Presentation** — Narrator, TTS, Animationen, Logo
- **Interaction** — Quizze, Umfragen, Aufgabenlisten
- **Reuse** — Makros, Imports, externe Skripte
- **Embedding** — Code, Mathematik, WebApps, Medien

## Teil 4 — Ergebnisse

### Die gute Nachricht

@bigfact(89 %)(des Feature-Raums werden messbar genutzt)

Nur **5 von 44** Features liegen unter 1 %.

                                  {{1}}
Das Problem ist also **nicht**, dass Features ungenutzt bleiben.

### Aber: jede Gruppe nutzt ihr eigenes Subset

![Feature-Profile der vier Gruppen](img/three_group_radar.png)

### Uni und Schule — gegenläufige Profile

| Feature | Comm-Uni | Comm-School |
|---|---:|---:|
| Narrator | **88,5 %** | 60,8 % |
| Code-Blöcke | **53,7 %** | 28,5 % |
| WebApps | 4,8 % | **24,2 %** |
| Logo / Branding | 21,4 % | **57,0 %** |

                                  {{1}}
Gleiche Sprache. Zwei Communities. **Entgegengesetzte Schwerpunkte.**

### Zwischenfrage

Welches Feature nutzen **Schul**-Autor:innen deutlich häufiger
als Autor:innen an Hochschulen?

[( )] Narrator
[( )] Code-Blöcke
[(X)] WebApps und visuelles Branding
[( )] ASCII-Diagramme
****************************************

Schulische Kurse setzen auf **Medien und Gestaltung**,
Hochschulkurse auf **narrativen Text und Code**.

****************************************

### Infrastruktur schlägt Didaktik

Erinnern Sie sich an die blaue Fläche?

@twocol(**MINT-the-GAP**

Ein Schulprojekt mit
einheitlichem Template.)(Makros **99,7 %**
Imports **98,3 %**

Narrator **9,4 %**
Animationen **0,6 %**)

                                  {{1}}
Eine geteilte Konfiguration hebt alles **in ihrem Rahmen** —
und lässt alles außerhalb unberührt.

### Konsequenz für unsere Tutorials

Die Gruppen steigen auf **unterschiedlichen Leitern** ein:

                                  {{1}}
**Hochschule:** Narrator → Code & Makros → *stockt bei Animationen*

                                  {{2}}
**Schule:** visuelle Medien → Quizze → *erreicht Code kaum*

                                  {{3}}
<div style="margin-top:1.5rem;padding:1rem;background:#eaf5ea;border-left:4px solid #4daf4a">
<b>Ein linearer Tutorial-Pfad ist deshalb falsch.</b><br>
Onboarding muss dort ansetzen, wo die jeweilige Gruppe steht.
</div>

### Zusammengefasst

- **89 %** des Feature-Raums werden genutzt — das ist nicht das Problem
- Jede Community erkundet nur **ihr eigenes Subset**
- **Autoren-Infrastruktur** prägt Adoption so stark wie Didaktik
- Onboarding braucht **kontextspezifische Einstiege**

                                  {{1}}
Und: Ein Korpus ist bei fehlender Telemetrie ein **tragfähiger Proxy** —
wiederholbar, ohne die Datensparsamkeit aufzugeben.

### Vielen Dank

**Fragen?**

sebastian.zug@informatik.tu-freiberg.de

---

Diese Folien: `github.com/LiaPlayground/DELFI_2026_presentation`

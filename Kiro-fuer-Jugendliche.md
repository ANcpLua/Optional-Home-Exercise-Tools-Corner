# Kiro für Jugendliche 🤖 — der Roboter, der zuerst nachdenkt und dann programmiert

> Begleit-Text zur Präsentation (`Kiro_IDE_Orchestrator_2026_Jugend.pptx`).
> Deutsche Erklärung, **englische Fachbegriffe** (Spec, Hook, IDE, MCP) — die heißen überall so.
> Stand: **Juni 2026**.

---

## 🎯 In einem Satz

**Kiro** ist ein Programmier-Werkzeug von **AWS (Amazon)**, das aus einem normalen Satz wie
*„Bau mir ein Schach-Spiel"* zuerst einen **Plan** schreibt — und erst dann den Code. Kein wildes
Drauflos-Tippen, sondern **„erst denken, dann coden"**.

---

## 🧠 Das Problem: „Vibe Coding"

Viele KI-Tools machen heute **Vibe Coding**: Du sagst „mach was Cooles", die KI tippt 200 Zeilen Code,
es sieht gut aus … aber niemand weiß genau, **was** das Programm eigentlich können soll. Bei Änderungen
bricht alles zusammen, weil es **keinen Plan** gibt.

> 🔑 **Merksatz:** Vibe Coding = plausibel aussehender Code, der zu **keiner Anforderung** passt.
> Klingt schlau, ist aber Raten.

---

## 💡 Die Idee von Kiro: Spec-Driven Development

Kiro dreht die Reihenfolge um. Bevor *eine einzige Zeile* Code entsteht, schreibt Kiro **drei Dateien**
(„the **Spec**"):

| Datei | Was drinsteht | Auf Deutsch |
|---|---|---|
| **`requirements.md`** | Was soll das Programm können? | Die **Anforderungen** |
| **`design.md`** | Wie wird es aufgebaut? | Der **Bauplan** (Architektur, Diagramme) |
| **`tasks.md`** | Welche Schritte sind nötig? | Die **To-do-Liste** |

Erst wenn **du** (der Mensch) diesen Plan absegnest, fängt Kiro an zu programmieren. Jede Code-Zeile lässt
sich später zur Anforderung zurückverfolgen → **Traceability**.

### EARS: Anforderungen, die man testen kann

Anforderungen schreibt Kiro in einem festen Muster namens **EARS**:

```
WHEN [wenn das passiert]
THE SYSTEM SHALL [dann soll das Programm das tun]
```

Beispiel aus einem Schach-Spiel:
```
WENN jemand einen verbotenen Zug macht
SOLL DAS SYSTEM den Grund anzeigen, warum der Zug nicht erlaubt ist.
```

Das ist eindeutig — man kann es **testen** und es gibt kein „hab ich anders gemeint".

---

## ⚙️ Die Superkräfte von Kiro

- **🪝 Agent Hooks** — kleine Automatik-Helfer. Beispiel: *„Immer wenn ich speichere, aktualisiere die
  Dokumentation."* Du beschreibst es in normaler Sprache, Kiro baut den **Hook**.
- **🧭 Steering Files** — Kiros „Hausregeln". Hier stehen z. B. dein Programmierstil und Namensregeln,
  damit alles einheitlich bleibt (`.kiro/steering/`).
- **🖼️ Multimodal** — du kannst ein **Foto von einer Whiteboard-Skizze** hochladen, und Kiro macht daraus
  Architektur und Code.
- **🧩 MCP** — Kiro kann sich mit externen Werkzeugen verbinden (GitHub, Dokumentation, eigene Tools).
- **👥 Subagents** — Kiro kann **mehrere Aufgaben gleichzeitig** erledigen (mehrere kleine Agenten parallel).

---

## 🆕 Was 2026 neu ist (wichtig fürs Präsentieren!)

Kiro startete im **Juli 2025** als Preview. Seitdem ist viel passiert:

- ✅ **Generally Available (GA) seit 17. November 2025** — kein „Beta" mehr.
- 💻 Es gibt jetzt nicht nur die **IDE**, sondern auch eine **Kiro CLI** (im Terminal) und **Kiro Web**
  (im Browser, [app.kiro.dev](https://app.kiro.dev)).
- ⚡ **Parallel-Arbeit**: früher nur eine Aufgabe nach der anderen — heute laufen mehrere gleichzeitig.
- 🧠 **Modelle zur Auswahl**: ein „**Auto**"-Modus mischt die besten Modelle; man kann auch fix Claude
  Sonnet/Opus oder Open-Weight-Modelle wählen.
- 🔐 **IDE 1.0 (25. Juni 2026)**: Agent-Focus-Modus, feine **Permissions** (du bestimmst, was die KI darf),
  eigene Custom Agents.

---

## 💳 Was kostet das? (Stand Juni 2026)

Kiro rechnet mit **Credits** (1 Credit = ein Stück Arbeit; einfache Sachen kosten weniger als 1 Credit).

| Plan | Preis / Monat | Credits / Monat |
|---|---|---|
| **Free** | 0 $ | 50 |
| **Pro** | 20 $ | 1.000 |
| **Pro+** | 40 $ | 2.000 |
| **Pro Max** | 100 $ | 5.000 |
| **Power** | 200 $ | 10.000 |

> Zum Ausprobieren reicht der **Free-Plan** (Anmeldung mit Social-Login oder AWS Builder ID — **kein**
> Amazon-Konto mit Kreditkarte nötig). Aktuelle Preise: [kiro.dev/pricing](https://kiro.dev/pricing/).

### 😬 Kleine Drama-Story (gut zum Erzählen!)

Als Kiro 2025 die Preise einführte, ging es **schief**: ein **Bug** zog manchen Leuten viel zu viele
Credits ab. AWS hat sich **entschuldigt**, das Geld **zurückerstattet** und das Preismodell danach **zweimal
neu gebaut** — vom alten „vibe/spec request"-System hin zum heutigen **Credit-Pool**. Lektion: Selbst
riesige Firmen machen Fehler — **wichtig ist, wie man sie behebt.**

---

## 🛠️ In 5 Schritten selbst ausprobieren

1. **Herunterladen** von [kiro.dev](https://kiro.dev/) (es ist ein VS-Code-Fork — sieht vertraut aus).
2. Mit **Free-Plan** anmelden (Social-Login).
3. In den **Spec-Modus** wechseln und einen Wunsch eintippen, z. B.
   *„Build a to-do app with a checkbox per item."*
4. Die drei Dateien (`requirements.md`, `design.md`, `tasks.md`) **anschauen und freigeben**.
5. Kiro **implementieren** lassen — und dabei zusehen, wie jede Zeile zu einer Anforderung passt.

---

## 🧩 Kiro vs. „normale" KI-Tools

| | Vibe Coding (z. B. einfacher Chat-Bot) | **Kiro (Spec-Driven)** |
|---|---|---|
| Reihenfolge | Sofort Code | **Erst Plan, dann Code** |
| Nachvollziehbar? | Oft nicht | **Ja — jede Zeile → Anforderung** |
| Bei Änderungen | Bricht schnell | Plan wird mit angepasst |
| Gut für | Schnelle Experimente | **Echte, wartbare Projekte** |

---

## 🏁 Take-away für die Präsentation

> **Kiro = „erst denken, dann coden".**
> Aus einem Satz wird ein **Plan** (Spec), aus dem Plan wird **nachvollziehbarer Code**.
> Das ist der Unterschied zwischen *Raten* und *Engineering*.

**Mehr:** [kiro.dev](https://kiro.dev/) · Docs: [kiro.dev/docs](https://kiro.dev/docs) ·
Changelog: [kiro.dev/changelog/ide](https://kiro.dev/changelog/ide/)

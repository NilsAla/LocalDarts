# LocalDarts
A fully local alternative to the Autodarts.io frontend for basic x01 games with up to 6 players

[![AI-Powered](https://img.shields.io/badge/Proudly-Slopcoded%20by%20Gemini-orange?style=for-the-badge&logo=google-gemini)](https://github.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

Ein extrem leichtgewichtiger, blitzschneller und **100% offline-fähiger** Web-Tracker für das **Autodarts-Kamerasystem**. Diese App fungiert als autarkes, touch-optimiertes Premium-Frontend, das direkt mit der lokalen API deines Board Managers kommuniziert – ganz ohne Internet, ohne Account und mit absolutem Fokus auf maximale Performance beim Zocken mit Freunden.

---

## 🎯 Das Problem & Die Lösung

Das offizielle `autodarts.io` ist großartig, hat aber einen massiven Haken: Es erfordert zwingend eine aktive Internetverbindung, das Routen aller Würfe über einen Cloud-Server und einen registrierten Benutzeraccount. Wer einfach nur unkompliziert mit ein paar Kumpels im Hobbyraum Dart spielen möchte – mit einem absolut simplen, lokalen Setup –, steht im Regen.

**Die Lösung:** Dieser Tracker kappt die Nabelschnur zur Cloud. Es ist eine reine Client-Side-Anwendung (Single HTML), die komplett autark läuft. Keine Registrierung, kein Cloud-Ping, kein Internetzugang nötig. Du spielst rein lokal, mit absolut null Latenz.

---

## 🔌 Das Basic-Setup (Plug & Play)

Dieses Projekt ist für das ultimativ simple, robuste Setup gedacht:
1. **Autodarts-PC:** Ein lokaler Rechner, an dem die Kameras hängen und der den *Autodarts Board Manager* (Port 3180) ausführt.
2. **Touch-Monitor:** Direkt an diesem Rechner angeschlossen.
3. **Browser im Kiosk-Modus:** Du öffnest einfach die `index.html` lokal im Browser im Vollbild – fertig. Alles läuft auf einer Maschine, offline und latenzfrei.

---

## 🚀 Key Features

* **100% Offline & Account-Free:** Spiel sofort los, ohne Logins oder Internet-Zwang.
* **Dynamic Multiplayer (1 bis 6 Spieler):** Keine starren Tabellen. Das flexible CSS-Grid-Spielfeld passt sich vollautomatisch an jede Spieleranzahl und Displaygröße an.
* **Vollständige Board-Kontrolle:** Steuere die Hardware direkt aus der App heraus über das Status-Banner unten:
  * **START:** Wecke das Board per Klick auf (`PUT /api/start`).
  * **STOP:** Versetze die Kameras in den Ruhezustand (`PUT /api/stop`), um Hardware und CPU zu schonen.
  * **RESET:** Hängt sich das Tracking mal auf? Ein Klick triggert einen sauberen Kamera-Reset (`POST /api/reset`).
* **Touch-Optimierte Bildschirmtastatur (OSK):** Da native Systemtastaturen auf Touch-Monitoren oft zicken, bringt die App ihre eigene QWERTZ-Tastatur mit – perfekt abgestimmt auf die Namenseingabe.
* **Echtzeit API-Status & UI-Feedback:** Ein großes Status-Banner zeigt auch aus mehreren Metern Entfernung an, was das Board gerade macht (*WIRFT...*, *PFEILE ZIEHEN* etc.). Inklusive visueller Dart-Popups ("T20", "BUST!").
* **Spielvarianten & Out-Regeln:** Setup für 301, 501 oder 701, sowie Straight-Out und echte Double-Out-Logik.
* **Dual-Theme:** Passend zu den Ringen deines Boards gibt es ein klassisches Dart-Grün und ein eSports-Orange.
* **Crash-Resistenz (Local Storage):** Das Spiel überlebt Browser-Reloads. Nach dem Neuladen bist du exakt beim selben Leg und Score. Auch Spielernamen werden für die nächste Session gemerkt.

---

## 🛡️ Sicherheit & Datenschutz (Privacy by Design)

Dieses Projekt verfolgt aus tiefer Überzeugung eine strikte **Zero-Data-Policy**. Alles ist so gewollt und konzipiert:
* **Keine externen Server:** Es gibt kein Backend. Nichts wird ins Internet gesendet.
* **Keine Benutzerdaten:** Kein Tracking, keine Analytics, keine E-Mail-Adressen.
* **Lokaler Speicher:** Alle Einstellungen (Themes, Namen, Spielstand) bleiben exakt da, wo sie hingehören: Im `LocalStorage` deines lokalen Browsers am Dartboard.

---

## 🤖 Credits & Disclaimer

This project is **proudly slopcoded by Gemini** (Google LLM). 

Es entstand in enger, iterativer Zusammenarbeit zwischen einem Dart-Enthusiasten und einer KI. Jede Zeile Code wurde pragmatisch und zielgerichtet auf reale UX-Probleme am lokalen Board optimiert. 

*Slopcoding at its finest: Schnell, autark, offline und absolut tödlich auf die Doppel!* 🎯

---

## 📄 Lizenz

Dieses Projekt ist unter der **MIT-Lizenz** lizenziert. Modifiziere, kopiere und nutze es nach Belieben für deinen eigenen Dartraum.

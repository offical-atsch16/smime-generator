# 🔐 CryptoStudio v2.0 – S/MIME & Secret Generator

[![License: MIT](https://img.shields.io/badge/License-MIT-emerald.svg)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Live-brightgreen.svg)](https://offical-atsch16.github.io)
[![Client-Side Privacy](https://img.shields.io/badge/Privacy-100%25%20Client--Side-blue.svg)](#-datenschutz--sicherheit)

**CryptoStudio** ist eine moderne, browserbasierte Kryptographie-Suite. Sie ermöglicht die Erstellung von **S/MIME-E-Mail-Zertifikaten**, **SSH-Schlüsselpaaren**, **OpenPGP/GPG-Schlüsseln**, **sicheren Passwörtern/Secrets** sowie die Berechnung von **Hashes & Encodings** – komplett lokal im Browser, ohne Server und ohne Datenübertragung.

---

## ✨ Features & Funktionen

| Modul | Beschreibung & Details |
| :--- | :--- |
| **✉️ S/MIME Zertifikate** | Generiert eine eigene Root-CA, ein S/MIME-Nutzerzertifikat sowie ein verpacktes PKCS#12 Bundle (`.p12`) inkl. `.crt` und `.key` PEM-Downloads (RSA 2048/4096 Bit). |
| **🔑 SSH Key Pairs** | Erstellt OpenSSH-kompatible Schlüsselpaare (`id_rsa` & `id_rsa.pub`) mit benutzerdefiniertem Kommentar für Server-Zugriffe. |
| **🛡️ OpenPGP / GPG** | Erzeugt PGP-Schlüsselpaare (RSA 2048/4096 Bit oder ECC Curve25519) inkl. Fingerprint- & Key-ID-Anzeige für Mailvelope oder GnuPG. |
| **🎲 Passwörter & Secrets** | Kryptographisch sicherer Passwort-Generator (Web Crypto API) sowie UUID v4, 256-Bit Hex-Tokens & Base64 Secrets. |
| **⚡ Hashes & Encoding** | Echtzeit-Berechnung von SHA-256, SHA-512, Base64 und Hex-Repräsentationen für beliebige Texteingaben. |

---

## 🛡️ Datenschutz & Sicherheit

* **0% Server-Speicherung (Zero Storage):** Alle Schlüssel und Zertifikate werden ausschließlich über die Web Crypto API, `node-forge` und `openpgp.js` im Arbeitsspeicher deines Browsers berechnet.
* **Offline-fähig:** Nach dem ersten Laden der Seite kann die Anwendung vollständig ohne aktive Internetverbindung verwendet werden.
* **Open Source:** Der gesamte Quellcode ist einsehbar und nachvollziehbar.

---

## 🚀 Live-Demo & GitHub Pages

Du kannst CryptoStudio direkt online nutzen:

👉 **[CryptoStudio Live-Version auf GitHub Pages öffnen](https://offical-atsch16.github.io)** *(Link nach dem Deployment anpassen)*

---

## 💻 Lokale Nutzung

Da CryptoStudio aus einer einzigen Standalone-HTML-Datei besteht, benötigst du kein Node.js, kein Docker und kein Backend:

1. Klone das Repository oder lade die `index.html` herunter:
   ```bash
   git clone https://github.com/offical-atsch16/cryptostudio.git
   ```
2. Öffne die `index.html` per Doppelklick in einem beliebigen modernen Webbrowser (Chrome, Firefox, Edge, Safari).

---

## 📖 Kurzanleitung: S/MIME in E-Mail-Clients einrichten

1. **Root-CA importieren (`ca.crt`):**
   * Importiere die generierte `ca.crt` in dein Betriebssystem oder E-Mail-Programm unter **Vertrauenswürdige Stammzertifizierungsstellen**.
2. **S/MIME-Bundle importieren (`smime.p12`):**
   * Importiere die `.p12`-Datei in **Apple Mail**, **Thunderbird** oder **Outlook** unter *Zertifikate/Sicherheit* und gib dein beim Erstellen gewähltes Passwort ein.
3. **Signieren & Verschlüsseln:**
   * Wähle das Zertifikat in den Kontoeinstellungen deines Mail-Clients für die digitale Signatur und Verschlüsselung aus.

---

## 🧰 Verwendete Bibliotheken & Tech Stack

* **UI & Styling:** [Tailwind CSS](https://tailwindcss.com/)
* **X.509 & PKCS#12 Crypto:** [node-forge](https://github.com/digitalbazaar/forge)
* **OpenPGP Engine:** [OpenPGP.js](https://openpgpjs.org/)
* **Web Crypto API:** Native Browser-Schnittstelle für Zufallszahlen, Web-Hashes & SSH-Generierung

---

## 👤 Author & Support

❤️ **OpenSource & Datenschutz made by** [offical-atsch16](https://github.com/offical-atsch16)

Wenn dir das Projekt gefällt, hinterlasse gerne einen ⭐️ **Star** auf GitHub!

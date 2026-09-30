# ProbeOSINT

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![C++17](https://img.shields.io/badge/C++-17-blue.svg)](https://en.cppreference.com/)
[![Linux](https://img.shields.io/badge/platform-Linux-green.svg)](https://www.linux.org/)

**ProbeOSINT** è un framework open source per l'Open Source Intelligence (OSINT), progettato per professionisti della sicurezza informatica, giornalisti investigativi e ricercatori.

> ⚠️ **Questo tool è progettato esclusivamente per scopi etici e legali.**

---

## 🎯 Scopo

ProbeOSINT raccoglie informazioni da fonti **pubblicamente accessibili** sul web senza richiedere API key o servizi a pagamento. L'obiettivo è fornire un toolkit self-hosted per:

- **Security Assessment** - Valutare la propria impronta digitale
- **Threat Intelligence** - Monitorare la presenza di dati sensibili esposti
- **Investigazione Giornalistica** - Ricerca di fonti aperte
- **Digital Forensics** - Analisi di metadati e correlazione dati

---

## ⚖️ Disclaimer Legale ed Etico

**Utilizzando questo software, accetti le seguenti condizioni:**

### ✅ Usi Consentiti
- Analizzare la **propria** impronta digitale e sicurezza
- Ricerche per **giornalismo investigativo** su argomenti di interesse pubblico
- **Penetration testing autorizzato** con documento di consenso scritto
- Ricerca accademica e formazione in cybersecurity
- Indagini difensive su **propri** asset digitali

### ❌ Usi Vietati (STRICTLY PROHIBITED)
- Stalking, doxxing o molestie verso individui
- Raccolta non autorizzata di dati personali di terzi
- Violazione di privacy o diritti personali
- Attività illegali secondo le leggi locali o internazionali
- Accesso a sistemi protetti o dati non pubblici
- Condivisione di dati raccolti per scopi malevoli

**L'autore non è responsabile per un uso improprio del software. Gli utenti sono gli unici responsabili del rispetto delle leggi applicabili nella propria giurisdizione.**

---

## 🚀 Caratteristiche

- **100% Gratuito** - Nessuna API key, nessun abbonamento
- **Self-Hosted** - Tutti i dati rimangono sul tuo sistema
- **Modulare** - Architettura a plugin per estensibilità
- **Offline Capable** - Funziona con database locali
- **Cross-Platform** - Linux (Windows/macOS in sviluppo)

### Moduli Inclusi
| Modulo | Descrizione |
|--------|-------------|
| `scraper` | HTTP client con rate limiting e rotazione proxy |
| `social` | Ricerca username su piattaforme pubbliche |
| `geolocation` | Analisi EXIF e database WiFi locali |
| `network` | DNS enum, subdomain discovery, WHOIS |
| `breach` | Ricerca su database breach locali |
| `search` | Dorking su motori di ricerca |

---

## 📋 Requisiti

### Sistema
- Linux (Ubuntu 20.04+, Debian 11+, Arch)
- Compilatore C++17 (GCC 9+ o Clang 10+)
- CMake 3.14+
- ~500MB spazio libero

### Dipendenze
```bash
sudo apt install build-essential cmake libcurl4-openssl-dev libsqlite3-dev
🔧 Compilazione
bash
# Clona il repository
git clone https://github.com/tuousername/ProbeOSINT.git
cd ProbeOSINT

# Crea build directory
mkdir build && cd build

# Genera Makefile
cmake ..

# Compila
make -j$(nproc)

# Esegui
./probeosint --help
📖 Utilizzo Base
bash
# Avvia interfaccia web
./probeosint --web

# Ricerca username
./probeosint --username target_username

# Ricerca dominio
./probeosint --domain example.com

# Modalità offline (solo DB locali)
./probeosint --offline --email user@example.com
🤝 Contribuire
Le contribuzioni sono benvenute! Leggi CONTRIBUTING.md per le linee guida.

Nota: Tutte le contribuzioni devono rispettare i principi di etica OSINT. Codice per aggirare protezioni o raccogliere dati non pubblici non sarà accettato.

📜 Licenza
ProbeOSINT è rilasciato sotto licenza GNU GPL v3.

Questo programma è software libero: puoi redistribuirlo e/o modificarlo secondo i termini della GNU General Public License pubblicata dalla Free Software Foundation.

📚 Risorse
OSINT Framework
Privacy International
Electronic Frontier Foundation
⚠️ Avviso Tecnico
Questo tool effettua richieste HTTP a siti web pubblici. Gli utenti sono responsabili di:

Rispettare i file robots.txt dei siti target
Implementare rate limiting appropriato
Non sovraccaricare i server di terze parti
Rispettare i Termini di Servizio delle piattaforme
Progetto creato per scopi educativi e di ricerca in cybersecurity.

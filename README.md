# ProbeOSINT

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![C++17](https://img.shields.io/badge/C++-17-blue.svg)](https://en.cppreference.com/)
[![Linux](https://img.shields.io/badge/platform-Linux-green.svg)](https://www.linux.org/)

**ProbeOSINT** is an open-source framework for Open Source Intelligence (OSINT), designed for cybersecurity professionals, investigative journalists, and researchers.

> ⚠️ **This tool is designed exclusively for ethical and legal purposes.**

---

## 🎯 Purpose

ProbeOSINT collects information from **publicly accessible** sources on the web without requiring API keys or paid services. The goal is to provide a self-hosted toolkit for:

- **Security Assessment** - Evaluate your digital footprint
- **Threat Intelligence** - Monitor exposure of sensitive data
- **Investigative Journalism** - Open source research
- **Digital Forensics** - Metadata analysis and data correlation

---

## ⚖️ Legal and Ethical Disclaimer

**By using this software, you accept the following conditions:**

### ✅ Permitted Uses
- Analyzing **your own** digital footprint and security
- Research for **investigative journalism** on matters of public interest
- **Authorized penetration testing** with written consent documentation
- Academic research and cybersecurity training
- Defensive investigations on **your own** digital assets

### ❌ Prohibited Uses (STRICTLY PROHIBITED)
- Stalking, doxxing, or harassment of individuals
- Unauthorized collection of personal data from third parties
- Privacy violation or violation of personal rights
- Illegal activities according to local or international laws
- Access to protected systems or non-public data
- Sharing collected data for malicious purposes

**The author is not responsible for misuse of the software. Users are solely responsible for complying with applicable laws in their jurisdiction.**

---

## 🚀 Features

- **100% Free** - No API keys, no subscriptions
- **Self-Hosted** - All data remains on your system
- **Modular** - Plugin architecture for extensibility
- **Offline Capable** - Works with local databases
- **Cross-Platform** - Linux (Windows/macOS in development)

### Included Modules
| Module | Description |
|--------|-------------|
| `scraper` | HTTP client with rate limiting and proxy rotation |
| `social` | Username search on public platforms |
| `geolocation` | EXIF analysis and local WiFi database |
| `network` | DNS enumeration, subdomain discovery, WHOIS |
| `breach` | Search on local breach databases |
| `search` | Dorking on search engines |

---

## 📋 Requirements

### System
- Linux (Ubuntu 20.04+, Debian 11+, Arch)
- C++17 Compiler (GCC 9+ or Clang 10+)
- CMake 3.14+
- ~500MB free space

### Dependencies
```bash
sudo apt install build-essential cmake libcurl4-openssl-dev libsqlite3-dev
```

## 🔧 Compilation

```bash
# Clone the repository
git clone https://github.com/yourusername/ProbeOSINT.git
cd ProbeOSINT

# Create build directory
mkdir build && cd build

# Generate Makefile
cmake ..

# Compile
make -j$(nproc)

# Run
./probeosint --help
```

## 📖 Basic Usage

```bash
# Start web interface
./probeosint --web

# Username search
./probeosint --username target_username

# Domain search
./probeosint --domain example.com

# Offline mode (local DBs only)
./probeosint --offline --email user@example.com
```

## 🤝 Contributing

Contributions are welcome! Read CONTRIBUTING.md for guidelines.

**Note:** All contributions must respect OSINT ethical principles. Code to bypass protections or collect non-public data will not be accepted.

## 📜 License

ProbeOSINT is released under the GNU GPL v3 license.

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation.

## 📚 Resources

- [OSINT Framework](https://osintframework.com/)
- [Privacy International](https://privacyinternational.org/)
- [Electronic Frontier Foundation](https://www.eff.org/)

## ⚠️ Technical Notice

This tool makes HTTP requests to public websites. Users are responsible for:

- Respecting the robots.txt file of target websites
- Implementing appropriate rate limiting
- Not overloading third-party servers
- Respecting the Terms of Service of platforms
- Project created for educational and cybersecurity research purposes.

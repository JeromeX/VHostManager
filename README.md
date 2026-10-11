# VHostManager

**Webbasierte Verwaltung von virtuellen Hosts, IP-Sicherheit und Serveraktivitäten.**

> VHostManager ist eine Eigenentwicklung von Malte Speck.

VHostManager bündelt Verwaltungs- und Sicherheitsfunktionen in einer zentralen Weboberfläche. Die folgenden Screenshots sind nach dem tatsächlich sichtbaren Menübereich zugeordnet – nicht nach der Uhrzeit im Dateinamen.

---

## Screenshots

### Dashboard

Übersicht mit Kennzahlen, Besuchern, Sicherheitsereignissen und Dienststatus.

<img src="screenshots/2026-10-11%2022_57_24-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png" alt="VHostManager – Dashboard" width="100%" />

### IP-Security

Gesperrte IP-Adressen, Whitelist und Sperrgründe.

<img src="screenshots/2026-10-11%2022_59_20-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png" alt="VHostManager – IP-Security" width="100%" />

### Security Events

Chronologische Liste protokollierter Sicherheitsereignisse.

<img src="screenshots/2026-10-11%2023_00_09-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png" alt="VHostManager – Security Events" width="100%" />

### Visitor Security

Besucheranalyse, verdächtige Requests und Auto-Block-Einstellungen.

<img src="screenshots/2026-10-11%2023_00_57-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png" alt="VHostManager – Visitor Security" width="100%" />

### Backup / Restore

Sicherungen für VHost Manager, MeerHeimatLiebe und System.

<img src="screenshots/2026-10-11%2023_01_59-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png" alt="VHostManager – Backup / Restore" width="100%" />

### Restore

Vorhandene Backups prüfen und gezielt wiederherstellen.

<img src="screenshots/2026-10-11%2023_02_57-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png" alt="VHostManager – Restore" width="100%" />

### Automatisierung / Cron

Zeitpläne für Backups, Housekeeping und Security Collector.

<img src="screenshots/2026-10-11%2023_03_35-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png" alt="VHostManager – Automatisierung / Cron" width="100%" />

### Housekeeping

Aufbewahrungsfristen und Regeln für kontrollierte Bereinigung.

<img src="screenshots/2026-10-11%2023_04_05-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png" alt="VHostManager – Housekeeping" width="100%" />

### System

Dienste, Ressourcen und geplante Cron-Jobs.

<img src="screenshots/2026-10-11%2023_04_48-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png" alt="VHostManager – System" width="100%" />

### Self-Test

Prüfergebnisse zu Diensten, SQLite, GeoIP, Firewall und Pfaden.

<img src="screenshots/2026-10-11%2023_05_08-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png" alt="VHostManager – Self-Test" width="100%" />

### Logs

Protokollierte Ereignisse mit Zeit, Land, Aktion und Ergebnis.

<img src="screenshots/2026-10-11%2023_05_51-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png" alt="VHostManager – Logs" width="100%" />

### Einstellungen

Grundkonfiguration, GeoIP, Whitelist, Aufbewahrung und Runtime-Pfade.

<img src="screenshots/2026-10-11%2023_06_52-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png" alt="VHostManager – Einstellungen" width="100%" />

### Tool-Pfade

Konfigurierte Programm- und Runtime-Pfade.

<img src="screenshots/2026-10-11%2023_08_32-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png" alt="VHostManager – Tool-Pfade" width="100%" />

---

## Funktionen

- **Dashboard** – zentrale Übersicht über Status und Aktivitäten.
- **IP-Sicherheit** – gesperrte IPs, Whitelist und zugehörige Ereignisse verwalten.
- **Besuchersicherheit** – verdächtige Requests prüfen und Auto-Block konfigurieren.
- **Sicherheitsereignisse und Logs** – protokollierte Vorgänge nachvollziehen.
- **Backup und Wiederherstellung** – verfügbare Sicherungen prüfen, erstellen und wiederherstellen.
- **Automatisierung** – zeitgesteuerte Backups, Housekeeping und Security Collector.
- **Housekeeping** – Daten nach konfigurierten Aufbewahrungsfristen bereinigen.
- **System und Self-Test** – Dienste, Ressourcen und grundlegende Integrationen prüfen.
- **Einstellungen und Tool-Pfade** – Konfiguration und verwendete Pfade anzeigen.

## Datenspeicherung

In der bekannten Konfiguration verwendet VHostManager SQLite:

```text
/var/lib/vhost-manager/vhost-manager.sqlite3
```

Wichtige Tabellen:

| Tabelle | Inhalt |
|---|---|
| `allowed_ips` | Freigegebene IP-Adressen |
| `blocked_ips` | Als gesperrt gespeicherte IP-Adressen |
| `security_events` | Sicherheitsereignisse |
| `settings` | Anwendungseinstellungen |

**Hinweis:** Ein gespeicherter Sperreintrag allein beweist nicht, dass eine Firewall-Regel aktiv ist. Die technische Durchsetzung hängt von der aktivierten Systemintegration und deren Status ab. Funktionen können je nach Version und Konfiguration variieren.

---

**VHostManager – Zugriffe prüfen, Ereignisse nachvollziehen und den Hosting-Betrieb kontrolliert verwalten.**

## Urheberrecht und Nutzung

Copyright © 2026 Malte Speck. Alle Rechte vorbehalten.

VHostManager ist eine Eigenentwicklung von Malte Speck. Der Quellcode wird ausschließlich zur öffentlichen Ansicht bereitgestellt.

Die Nutzung, Vervielfältigung, Veränderung oder Weiterverbreitung des Quellcodes ist ohne vorherige ausdrückliche Genehmigung des Urhebers nicht gestattet, soweit gesetzlich zulässig.

**Es wird keine Open-Source-Lizenz erteilt.**

# VHostManager

**Webbasierte Verwaltung von virtuellen Hosts, IP-Sicherheit und Serveraktivitäten.**

VHostManager ist eine Eigenentwicklung von **Malte Speck**.

## Screenshots

Die Screenshots werden direkt aus dem Repository-Ordner [`screenshots/`](https://github.com/JeromeX/VHostManager/tree/main/screenshots) geladen.

### Dashboard

![VHostManager – Dashboard](screenshots/2026-10-11%2022_57_24-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png)

### Besucher

![VHostManager – Besucher](screenshots/2026-10-11%2022_59_20-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png)

### IP-Security

![VHostManager – IP-Security](screenshots/2026-10-11%2023_00_09-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png)

### Security Events

![VHostManager – Security Events](screenshots/2026-10-11%2023_00_57-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png)

### Visitor Security

![VHostManager – Visitor Security](screenshots/2026-10-11%2023_01_59-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png)

### Backup

![VHostManager – Backup](screenshots/2026-10-11%2023_02_57-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png)

### Restore

![VHostManager – Restore](screenshots/2026-10-11%2023_03_35-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png)

### Automatisierung

![VHostManager – Automatisierung](screenshots/2026-10-11%2023_04_05-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png)

### Housekeeping

![VHostManager – Housekeeping](screenshots/2026-10-11%2023_04_48-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png)

### System

![VHostManager – System](screenshots/2026-10-11%2023_05_08-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png)

### Self-Test

![VHostManager – Self-Test](screenshots/2026-10-11%2023_05_51-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png)

### Logs

![VHostManager – Logs](screenshots/2026-10-11%2023_06_52-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png)

### Einstellungen

![VHostManager – Einstellungen](screenshots/2026-10-11%2023_08_32-VHost%20Manager%20und%202%20weitere%20Seiten%20-%20Pers%C3%B6nlich%20%E2%80%93%20Microsoft%E2%80%8B%20Edge.png)

## Funktionen

- Zentrale Weboberfläche für die verfügbaren VHostManager-Funktionen
- Verwaltung gespeicherter IP-Freigaben und Sperreinträge
- Übersicht über erfasste Sicherheitsereignisse und Besucheraktivitäten
- Anzeige verfügbarer Discovery- und Systeminformationen
- Backup- und Wiederherstellungsfunktionen
- Automatisierung, Cron-Jobs und Housekeeping
- Systemstatus, Selbsttests, Logs und Konfiguration

## Datenspeicherung

In der dokumentierten Konfiguration verwendet VHostManager SQLite:

```text
/var/lib/vhost-manager/vhost-manager.sqlite3
```

Wichtige Tabellen:

| Tabelle | Inhalt |
|---|---|
| `allowed_ips` | Gespeicherte freigegebene IP-Adressen |
| `blocked_ips` | Gespeicherte gesperrte IP-Adressen |
| `security_events` | Sicherheitsereignisse |
| `settings` | Anwendungseinstellungen |

**Wichtig:** Ein gespeicherter Sperreintrag allein beweist nicht, dass die IP-Adresse tatsächlich durch die Firewall blockiert wird. Das hängt von der aktiven Systemintegration und deren Status ab.

## Urheberrecht und Nutzung

Copyright © 2026 Malte Speck. Alle Rechte vorbehalten.

VHostManager ist eine Eigenentwicklung von Malte Speck. Der Quellcode wird ausschließlich zur öffentlichen Ansicht bereitgestellt.

Die Nutzung, Vervielfältigung, Veränderung oder Weiterverbreitung des Quellcodes ist ohne vorherige ausdrückliche Genehmigung des Urhebers nicht gestattet, soweit gesetzlich zulässig.

**Es wird keine Open-Source-Lizenz erteilt.**

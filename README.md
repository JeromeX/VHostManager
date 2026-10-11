# VHostManager

**Webbasierte Verwaltung von virtuellen Hosts, IP-Sicherheit und
Serveraktivitäten.**

> **VHostManager ist eine Eigenentwicklung von Malte Speck.**

VHostManager bündelt wichtige Verwaltungs- und Sicherheitsfunktionen in
einer zentralen Weboberfläche. Ziel sind eine klare Übersicht,
nachvollziehbare Ereignisse und die kontrollierte Verwaltung
sicherheitsrelevanter Daten.

---

## Screenshots
### Dashboard
<img width="2560" height="1440" alt="2026-10-11 22_57_24-VHost Manager und 2 weitere Seiten - Persönlich – Microsoft​ Edge" src="https://github.com/user-attachments/assets/64f0e68c-50b8-4891-8a7e-56dbe1846a06" />

### SCREENSHOTS DES VHOSTMANAGERS
### MEHR SCREENSHOTS IM ORDNER "SCREENSHOTS"

## Funktionen

-   **Dashboard** -- zentrale Übersicht über verfügbare Status- und
    Aktivitätsinformationen.
-   **Besuchersicherheit** -- sicherheitsbezogene Prüfung von Besucher-
    und IP-Aktivitäten.
-   **IP-Verwaltung** -- gespeicherte IP-Einträge prüfen und -- abhängig
    von der Version -- verwalten.
-   **Gesperrte IPs** -- gespeicherte Sperreinträge kontrollieren und
    pflegen.
-   **Freigegebene IPs** -- zugelassene beziehungsweise
    vertrauenswürdige Adressen verwalten.
-   **Sicherheitsereignisse** -- erfasste Vorgänge zeitlich
    nachvollziehen und untersuchen.
-   **Discovery** -- erkannte Informationen zur weiteren Prüfung
    anzeigen.
-   **Firewall-Anbindung** -- IP-Regeln prüfen oder anwenden, sofern die
    entsprechende Systemintegration aktiv ist.
-   **Backups und Wiederherstellung** -- unterstützte Sicherungs- und
    Wiederherstellungsabläufe verwalten.
-   **Automatisierung** -- eingerichtete Aufgaben wie Backups oder
    Security Collector zeitgesteuert ausführen.
-   **Housekeeping** -- Datenbestände nach konfigurierten Regeln
    pflegen.
-   **Einstellungen und Protokolle** -- verfügbare Optionen verwalten
    und Vorgänge nachvollziehen.

## Datenspeicherung

In der bekannten Konfiguration verwendet VHostManager SQLite:

``` text
/var/lib/vhost-manager/vhost-manager.sqlite3
```

Wichtige Tabellen:

  Tabelle             Inhalt
  ------------------- ---------------------------------------
  `allowed_ips`       Freigegebene IP-Adressen
  `blocked_ips`       Als gesperrt gespeicherte IP-Adressen
  `security_events`   Sicherheitsereignisse
  `settings`          Anwendungseinstellungen

**Hinweis:** Ein in VHostManager gespeicherter Sperreintrag beweist
nicht allein, dass eine Firewall-Regel tatsächlich aktiv ist. Die
technische Durchsetzung hängt von der Systemintegration und deren Status
ab. Verfügbare Funktionen können je nach Version und Konfiguration
variieren.

------------------------------------------------------------------------

**VHostManager -- Zugriffe prüfen, Ereignisse nachvollziehen und den
Hosting-Betrieb kontrolliert verwalten.**

## Urheberrecht und Nutzung

Copyright © 2026 Malte Speck. Alle Rechte vorbehalten.

VHostManager ist eine Eigenentwicklung von Malte Speck. Der Quellcode wird ausschließlich zur öffentlichen Ansicht bereitgestellt.

Die Nutzung, Vervielfältigung, Veränderung oder Weiterverbreitung des Quellcodes ist ohne vorherige ausdrückliche Genehmigung des Urhebers nicht gestattet, soweit gesetzlich zulässig.

**Es wird keine Open-Source-Lizenz erteilt.**

<img width="2560" height="1440" alt="2026-10-11 23_04_05-VHost Manager und 2 weitere Seiten - Persönlich – Microsoft​ Edge" src="https://github.com/user-attachments/assets/2b0078b3-964d-477b-bc8d-c8946c2af241" />
<img width="2560" height="1440" alt="2026-10-11 23_03_35-VHost Manager und 2 weitere Seiten - Persönlich – Microsoft​ Edge" src="https://github.com/user-attachments/assets/2fe9086b-ac36-401e-8ed1-7dffd25bbd1a" />
<img width="2560" height="1440" alt="2026-10-11 23_02_57-VHost Manager und 2 weitere Seiten - Persönlich – Microsoft​ Edge" src="https://github.com/user-attachments/assets/bce1c198-044a-4ee7-acac-bdfc43789115" />
<img width="2560" height="1440" alt="2026-10-11 23_06_52-VHost Manager und 2 weitere Seiten - Persönlich – Microsoft​ Edge" src="https://github.com/user-attachments/assets/6762bc98-d928-494e-aed2-1c7b3fc9a3c8" />
<img width="2560" height="1440" alt="2026-10-11 23_05_51-VHost Manager und 2 weitere Seiten - Persönlich – Microsoft​ Edge" src="https://github.com/user-attachments/assets/d4ad2d91-95b6-428b-9567-760022c40e8f" />
<img width="2560" height="1440" alt="2026-10-11 23_05_08-VHost Manager und 2 weitere Seiten - Persönlich – Microsoft​ Edge" src="https://github.com/user-attachments/assets/76bd5810-dca0-4377-aac8-79d1437e6b95" />
<img width="2560" height="1440" alt="2026-10-11 23_04_48-VHost Manager und 2 weitere Seiten - Persönlich – Microsoft​ Edge" src="https://github.com/user-attachments/assets/431e7905-a0d2-449e-809e-9a9d93a7c226" />
<img width="2560" height="1440" alt="2026-10-11 23_08_32-VHost Manager und 2 weitere Seiten - Persönlich – Microsoft​ Edge" src="https://github.com/user-attachments/assets/819e0030-f20e-4547-af04-d2a314cf09c8" />
<img width="2560" height="1440" alt="2026-10-11 22_57_24-VHost Manager und 2 weitere Seiten - Persönlich – Microsoft​ Edge" src="https://github.com/user-attachments/assets/2cbd2a80-5689-4293-be74-dca8bc81e846" />
<img width="2560" height="1440" alt="2026-10-11 23_01_59-VHost Manager und 2 weitere Seiten - Persönlich – Microsoft​ Edge" src="https://github.com/user-attachments/assets/3a5e02e4-e782-40fa-99c5-e7d6ca43881f" />
<img width="2560" height="1440" alt="2026-10-11 23_00_57-VHost Manager und 2 weitere Seiten - Persönlich – Microsoft​ Edge" src="https://github.com/user-attachments/assets/fdec8ac1-8e15-4697-bff3-8f8f144229ea" />
<img width="2560" height="1440" alt="2026-10-11 23_00_09-VHost Manager und 2 weitere Seiten - Persönlich – Microsoft​ Edge" src="https://github.com/user-attachments/assets/b6ac6248-a30b-4110-bd1d-908cbf499130" />
<img width="2560" height="1440" alt="2026-10-11 22_59_20-VHost Manager und 2 weitere Seiten - Persönlich – Microsoft​ Edge" src="https://github.com/user-attachments/assets/64504c54-37d6-4a5f-87e4-434274d57ada" />
<img width="2560" height="1440" alt="2026-10-11 23_13_26-Clipboard" src="https://github.com/user-attachments/assets/bdffd783-4b00-42b2-b25b-e56263f539ad" />



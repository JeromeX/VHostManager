# VHostManager

**Webbasierte Verwaltung von virtuellen Hosts, IP-Sicherheit und
Serveraktivitäten.**

> **VHostManager ist eine Eigenentwicklung von Malte Speck.**

VHostManager bündelt wichtige Verwaltungs- und Sicherheitsfunktionen in
einer zentralen Weboberfläche. Ziel sind eine klare Übersicht,
nachvollziehbare Ereignisse und die kontrollierte Verwaltung
sicherheitsrelevanter Daten.

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

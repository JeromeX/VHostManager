# VHostManager

### Webbasierte Verwaltung für virtuelle Hosts und sicherheitsrelevante Serveraktivitäten

VHostManager bündelt zentrale Verwaltungs- und Sicherheitsinformationen
einer Hosting-Umgebung in einer webbasierten Oberfläche. Der Schwerpunkt
liegt auf der Übersicht von IP-Adressen, der Prüfung von
Sicherheitsereignissen, der Verwaltung von Freigaben und Sperren sowie
auf nachvollziehbaren Wartungs- und Sicherungsabläufen.

Die Oberfläche soll dabei helfen, relevante Informationen schnell zu
finden, Aktivitäten im Kontext zu bewerten und administrative
Entscheidungen kontrolliert auszuführen.

> **Versionshinweis:** Die konkret verfügbaren Ansichten und Aktionen
> können je nach installierter Version und Backend-Konfiguration
> variieren. Diese Dokumentation beschreibt die Aufgaben der Bereiche
> und unterscheidet zwischen gespeicherten Anwendungsdaten und
> tatsächlich durchgesetzten Systemregeln.

------------------------------------------------------------------------

## Inhaltsverzeichnis

-   [Projektüberblick](#projektüberblick)
-   [Dashboard](#dashboard)
-   [Besuchersicherheit](#besuchersicherheit)
-   [IP-Verwaltung](#ip-verwaltung)
-   [Gesperrte IP-Adressen](#gesperrte-ip-adressen)
-   [Freigegebene IP-Adressen](#freigegebene-ip-adressen)
-   [Sicherheitsereignisse](#sicherheitsereignisse)
-   [Discovery](#discovery)
-   [Firewall und Durchsetzung](#firewall-und-durchsetzung)
-   [Backups und Wiederherstellung](#backups-und-wiederherstellung)
-   [Automatisierung](#automatisierung)
-   [Housekeeping](#housekeeping)
-   [Einstellungen](#einstellungen)
-   [Protokolle und
    Nachvollziehbarkeit](#protokolle-und-nachvollziehbarkeit)
-   [Datenspeicherung](#datenspeicherung)
-   [Sicherheitsgrundsätze](#sicherheitsgrundsätze)

------------------------------------------------------------------------

## Projektüberblick

VHostManager stellt unterschiedliche Verwaltungsbereiche an einem
zentralen Ort bereit. Dazu gehören -- abhängig von der jeweiligen
Konfiguration -- insbesondere:

-   **Übersicht:** zentrale Statusinformationen und Einstieg in die
    Detailbereiche.
-   **Besuchersicherheit:** sicherheitsbezogene Auswertung von Besucher-
    und IP-Aktivitäten.
-   **IP-Verwaltung:** Prüfung und Verwaltung gespeicherter IP-Einträge.
-   **Sicherheitsereignisse:** nachvollziehbare Darstellung erfasster
    Ereignisse.
-   **Discovery:** Übersicht über erkannte oder zur Prüfung
    bereitgestellte Informationen.
-   **Firewall-bezogene Abläufe:** Verwaltung beziehungsweise Kontrolle
    von Sperren, sofern die entsprechende Systemintegration aktiv ist.
-   **Backups und Wartung:** Sicherung, Wiederherstellung und
    Datenpflege, soweit die Module eingerichtet sind.

VHostManager ist eine Verwaltungsoberfläche. Ob eine Regel auf
Betriebssystem- oder Firewall-Ebene tatsächlich aktiv ist, hängt von der
angebundenen Systemkomponente und deren Status ab.

------------------------------------------------------------------------

## Dashboard

Das Dashboard ist der zentrale Einstiegspunkt. Es bietet eine
zusammenfassende Sicht auf wichtige Statusinformationen und führt von
dort zu den passenden Detailansichten.

### Zweck

-   Den Zustand wichtiger Bereiche schnell erfassen.
-   Auffällige Kennzahlen oder Hinweise erkennen.
-   Von einer Übersicht zu den zugrunde liegenden Datensätzen wechseln.

Eine Kennzahl ist ein Ausgangspunkt für eine Prüfung, nicht automatisch
eine vollständige Diagnose. Für die Bewertung sollten immer Zeitraum,
Ereignisdetails und weitere verfügbare Informationen berücksichtigt
werden.

------------------------------------------------------------------------

## Besuchersicherheit

Der Bereich **Besuchersicherheit** unterstützt die Prüfung von Zugriffen
und sicherheitsrelevanten Mustern. Er hilft, Aktivitäten zu erkennen,
die näher untersucht werden sollten.

### Typische Fragestellungen

-   Welche Zugriffe oder Muster fallen im ausgewählten Zeitraum auf?
-   Gibt es wiederholte oder ungewöhnliche Anfragen?
-   Welche IP-Adresse oder welches Ereignis sollte genauer geprüft
    werden?
-   Muss ein Eintrag in der IP-Verwaltung überprüft werden?

Ein auffälliger Zugriff ist nicht automatisch ein Angriff. Die Bewertung
sollte auf den vorhandenen Details und dem jeweiligen Kontext beruhen.

------------------------------------------------------------------------

## IP-Verwaltung

Die **IP-Verwaltung** ist der zentrale Arbeitsbereich für IP-bezogene
Einträge. Je nach installierter Version können Einträge gesucht,
gefiltert, ausgewählt und einzeln oder gesammelt bearbeitet werden.

### Mögliche Aufgaben

-   Eine IP-Adresse und ihre verfügbaren Details prüfen.
-   Den gespeicherten Status nachvollziehen.
-   Eine Adresse sperren oder freigeben, sofern die jeweilige Aktion
    vorhanden ist.
-   Nicht mehr benötigte Einträge entfernen, sofern dies unterstützt
    wird.
-   Mehrere Einträge gemeinsam bearbeiten, wenn die Oberfläche
    Sammelaktionen anbietet.

### Empfohlener Ablauf

1.  Den richtigen Eintrag anhand der IP-Adresse identifizieren.
2.  Status und Kontext prüfen.
3.  Vor einer Sammelaktion die Auswahl kontrollieren.
4.  Nach der Änderung den gespeicherten und -- falls relevant -- den
    tatsächlich angewendeten Status prüfen.

Sammelaktionen sollten vorsichtig verwendet werden, weil sie mehrere
Datensätze gleichzeitig betreffen können.

------------------------------------------------------------------------

## Gesperrte IP-Adressen

Dieser Bereich zeigt IP-Adressen, die in VHostManager als gesperrt
gespeichert sind. Er dient zur Kontrolle und Pflege der Sperrliste.

### Typische Aufgaben

-   Gespeicherte Sperreinträge kontrollieren.
-   Einzelne Adressen und deren verfügbaren Kontext prüfen.
-   Eine Sperre aufheben, wenn dies erforderlich und als Aktion
    verfügbar ist.
-   Nicht mehr benötigte Einträge entfernen, sofern die Version dies
    unterstützt.

**Wichtige Unterscheidung:** Ein Eintrag in der Sperrliste bestätigt
zunächst den gespeicherten Anwendungsstatus. Er beweist nicht allein,
dass sämtliche Zugriffe dieser Adresse bereits auf Netzwerk- oder
Firewall-Ebene blockiert werden. Die tatsächliche Durchsetzung hängt von
der Systemintegration und dem Status der zugehörigen Regel ab.

------------------------------------------------------------------------

## Freigegebene IP-Adressen

Der Bereich für **freigegebene IP-Adressen** verwaltet Adressen, die
ausdrücklich als zugelassen oder vertrauenswürdig hinterlegt wurden.

Freigaben können helfen, bekannte Zugriffe von anderen Aktivitäten zu
unterscheiden. Sie sollten jedoch nur mit nachvollziehbarem Grund
gesetzt und regelmäßig überprüft werden.

### Empfehlungen

-   Nur bekannte und erforderliche Adressen freigeben.
-   Den Zweck einer Freigabe dokumentieren, sofern ein entsprechendes
    Feld vorhanden ist.
-   Nicht mehr benötigte Ausnahmen entfernen.
-   Prüfen, welche Wirkung die Freigabe in der aktuellen Konfiguration
    tatsächlich hat.

Eine Freigabeliste ersetzt keine umfassende Sicherheitsprüfung und
sollte nicht unbegrenzt wachsen.

------------------------------------------------------------------------

## Sicherheitsereignisse

Der Bereich **Sicherheitsereignisse** stellt erfasste
sicherheitsrelevante Vorgänge zur Analyse bereit. Er unterstützt dabei,
Ereignisse zeitlich einzuordnen und mit IP-Einträgen oder anderen
Informationen abzugleichen.

Je nach Datenquelle können Ereignisse unter anderem einen Zeitstempel,
eine IP-Adresse, einen Ereignistyp und eine Beschreibung enthalten.

### Zweck

-   Vorgänge nachvollziehen.
-   Wiederholungen und zeitliche Muster erkennen.
-   Ereignisse mit der IP-Verwaltung abgleichen.
-   Entscheidungen auf konkrete Informationen stützen.

Die Aussagekraft hängt davon ab, welche Daten tatsächlich erfasst
werden. Ein protokolliertes Ereignis beweist für sich genommen nicht
immer einen erfolgreichen Angriff.

------------------------------------------------------------------------

## Discovery

**Discovery** dient zur Darstellung erkannter oder zusammengetragener
Informationen, die weiter geprüft werden sollen. Der genaue Inhalt hängt
von der aktivierten Erkennung und den angebundenen Datenquellen ab.

### Empfohlener Ablauf

1.  Einen erkannten Eintrag öffnen oder die verfügbaren Details prüfen.
2.  Quelle und Kontext nachvollziehen.
3.  Entscheiden, ob weitere Prüfung notwendig ist.
4.  Eine erforderliche Änderung im passenden Verwaltungsbereich
    durchführen.
5.  Das Ergebnis anschließend kontrollieren.

Erkennungsergebnisse sollten als Hinweise behandelt werden, nicht als
ungeprüfte Anweisung für eine automatische Sperre.

------------------------------------------------------------------------

## Firewall und Durchsetzung

IP-Verwaltung und Firewall-Durchsetzung sind miteinander verbunden, aber
nicht identisch. VHostManager kann gespeicherte IP-Regeln anzeigen oder
Aktionen zu ihrer Anwendung anstoßen, sofern die entsprechende
Integration eingerichtet ist.

### Bei einer Sperre ist zu unterscheiden

-   **Anwendungsstatus:** Die IP-Adresse ist in VHostManager als
    gesperrt gespeichert.
-   **Regelstatus:** Eine entsprechende Firewall- oder Systemregel wurde
    erzeugt oder aktualisiert.
-   **Wirksamkeit:** Die Regel ist aktiv und blockiert den betreffenden
    Verkehr im vorgesehenen Geltungsbereich.

Diese Zustände sollten nicht ohne Prüfung gleichgesetzt werden. Bei
sicherheitskritischen Änderungen sind die Rückmeldung der Anwendung und
der Status der Systemkomponente zu berücksichtigen.

------------------------------------------------------------------------

## Backups und Wiederherstellung

Der Backup-Bereich unterstützt -- sofern in der installierten Version
vorhanden -- die Sicherung relevanter VHostManager-Daten und die
kontrollierte Wiederherstellung.

Eine Sicherung sollte nicht allein deshalb als erfolgreich gelten, weil
eine Aufgabe gestartet wurde. Entscheidend sind das tatsächliche
Ergebnis, die Vollständigkeit der enthaltenen Daten und die spätere
Lesbarkeit.

### Gute Praxis

-   Sicherungen mit nachvollziehbaren Zeitpunkten aufbewahren.
-   Speicherplatz und Berechtigungen des Sicherungsziels prüfen.
-   Ergebnisse und Fehlermeldungen kontrollieren.
-   Vor einer Wiederherstellung prüfen, welche Daten überschrieben oder
    ergänzt werden.
-   Nach einer Wiederherstellung die Anwendung und die relevanten
    Datensätze kontrollieren.

Welche Dateien und Konfigurationen enthalten sind, hängt vom jeweiligen
Sicherungsverfahren ab.

------------------------------------------------------------------------

## Automatisierung

Der Bereich **Automatisierung** dient der Übersicht und Steuerung
wiederkehrender Aufgaben, sofern die betreffenden Module eingerichtet
sind.

Je nach Installation können dazu beispielsweise gehören:

-   **VHostManager-Backup:** Sicherung der vorgesehenen
    VHostManager-Daten.
-   **MeerHeimatLiebe-Backup:** separate Sicherungsaufgabe für
    MeerHeimatLiebe, sofern eingerichtet.
-   **Security Collector:** wiederkehrende Erfassung
    sicherheitsrelevanter Informationen.
-   **Housekeeping:** Datenpflege nach den konfigurierten Aufbewahrungs-
    und Bereinigungsregeln.

Zeitpläne, Aktivierungsschalter und Statusanzeigen sind nur insoweit
verfügbar, wie das jeweilige Modul sie bereitstellt.

### Vor dem Aktivieren prüfen

-   Ist die Aufgabe eingerichtet?
-   Ist der Zeitplan korrekt?
-   Sind Zielverzeichnis und Berechtigungen passend?
-   Kann der tatsächliche Lauf anhand eines Status oder Protokolls
    kontrolliert werden?

Ein aktivierter Zeitplan bedeutet nicht automatisch, dass jeder Lauf
erfolgreich abgeschlossen wird.

------------------------------------------------------------------------

## Housekeeping

**Housekeeping** bezeichnet die kontrollierte Pflege von Datenbeständen
und Protokollen. Je nach Konfiguration können ältere Einträge archiviert
oder nach festgelegten Regeln entfernt werden.

### Ziel

-   Unnötiges Anwachsen von Datenbeständen begrenzen.
-   Aufbewahrungsregeln nachvollziehbar anwenden.
-   Die Übersichtlichkeit des laufenden Betriebs erhalten.

### Vor und nach einem Lauf

-   Klären, welche Datentypen betroffen sind.
-   Aufbewahrungszeiträume kontrollieren.
-   Sicherstellen, dass benötigte Informationen nicht unbeabsichtigt
    entfernt werden.
-   Das Ergebnis und mögliche Fehler prüfen.

Housekeeping ist kein Ersatz für Backups. Vor einer Bereinigung sollte
bekannt sein, welche Daten erhalten bleiben müssen.

------------------------------------------------------------------------

## Einstellungen

Der Bereich **Einstellungen** enthält die von der Anwendung
bereitgestellten Konfigurationsoptionen. Abhängig von der Version können
dies allgemeine Optionen, Aufbewahrungswerte oder modulbezogene
Aktivierungen sein.

### Empfehlungen

-   Änderungen bewusst und möglichst einzeln vornehmen.
-   Vor dem Speichern prüfen, ob der Wert zur beabsichtigten Funktion
    passt.
-   Nach der Änderung kontrollieren, ob sie übernommen wurde.
-   Kritische Werte nachvollziehbar dokumentieren.

Manche Einstellungen werden erst bei einem späteren Aufgabenlauf oder
nach einer erneuten Erzeugung der zugehörigen Konfiguration wirksam.

------------------------------------------------------------------------

## Protokolle und Nachvollziehbarkeit

Protokolle und Ereignislisten helfen, Vorgänge und Fehler
nachzuvollziehen. Für eine aussagekräftige Prüfung sollten -- soweit
vorhanden -- Zeitpunkt, betroffener Bereich, ausgeführte Aktion,
Ergebnis und Fehlermeldung gemeinsam betrachtet werden.

Eine leere Liste beweist nicht zwingend, dass kein Vorgang stattgefunden
hat. Mögliche Ursachen sind unter anderem aktive Filter, fehlende
Datenquellen oder ein nicht laufender Collector.

------------------------------------------------------------------------

## Datenspeicherung

In der bekannten VHostManager-Konfiguration wird SQLite als persistenter
Speicher verwendet. Der konfigurierte Datenbankpfad lautet:

``` text
/var/lib/vhost-manager/vhost-manager.sqlite3
```

Die bekannte Datenbank enthält unter anderem folgende Tabellen:

  Tabelle             Zweck
  ------------------- ----------------------------------------------------
  `allowed_ips`       Gespeicherte Einträge für freigegebene IP-Adressen
  `blocked_ips`       Gespeicherte Einträge für gesperrte IP-Adressen
  `security_events`   Erfasste sicherheitsrelevante Ereignisse
  `settings`          Persistente Anwendungseinstellungen

Weitere Protokolle, Archive, Sicherungen oder automatisch erzeugte
Systemkonfigurationen können außerhalb der Datenbank in separaten
Dateien und Verzeichnissen liegen.

**Wichtig:** Die Datenbank zeigt, was VHostManager gespeichert hat. Ob
eine IP-Sperre auf Firewall-Ebene tatsächlich aktiv ist, muss zusätzlich
anhand der zuständigen Systemkomponente geprüft werden.

------------------------------------------------------------------------

## Sicherheitsgrundsätze

-   **Nachvollziehbarkeit:** Entscheidungen auf konkrete Einträge und
    Ereignisse stützen.
-   **Minimale Ausnahmen:** Freigaben nur vergeben, wenn sie tatsächlich
    erforderlich sind.
-   **Kontrollierte Sammelaktionen:** Auswahl vor einer Massenänderung
    prüfen.
-   **Verifizierte Backups:** Ergebnisse kontrollieren und
    Wiederherstellbarkeit berücksichtigen.
-   **Transparente Wartung:** Vor Housekeeping-Aktionen den betroffenen
    Datenumfang klären.
-   **Getrennte Zustände:** Gespeicherte Anwendungsdaten nicht mit
    aktiven Firewall-Regeln gleichsetzen.
-   **Regelmäßige Kontrolle:** Sperren, Freigaben, Einstellungen und
    automatisierte Aufgaben wiederkehrend prüfen.

------------------------------------------------------------------------

## Zusammenfassung

VHostManager bringt die wesentlichen Bereiche für die Verwaltung von
IP-Adressen, die Analyse von Sicherheitsereignissen und die Organisation
wiederkehrender Aufgaben in einer zentralen Oberfläche zusammen.

Der Nutzen entsteht durch das Zusammenspiel der Bereiche: Eine
Auffälligkeit aus der Besuchersicherheit kann in den
Sicherheitsereignissen untersucht, in der IP-Verwaltung bewertet und --
falls erforderlich -- über die angebundene Systemkomponente behandelt
werden. Backups, Protokollierung und kontrolliertes Housekeeping
unterstützen den nachvollziehbaren Betrieb.

**VHostManager -- Zugriffe prüfen, Sicherheitsereignisse verstehen und
den Hosting-Betrieb kontrolliert verwalten.**

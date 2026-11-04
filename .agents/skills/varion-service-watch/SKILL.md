---
name: varion-service-watch
description: "Prueft bestehende Shop-, Worker- und Schnittstellenfunktionen fuer die Technical-Rolle und ordnet neue Stoerungen ein. Nutzen fuer Betriebschecks und Fehlertriage; keine automatische Reparatur oder Bereitstellung."
metadata:
  owner_role: technical
  version: "1.0.1"
---

# varion-service-watch

## Auftrag: Technische Betriebsüberwachung

1. Ermittle aus dem aktuellen Vertrag und dem Auftrag die tatsächlich relevanten
   bestehenden Dienste, Produktions-/Vorschauidentität und deren Sollzustand.
   Verwende keine geratenen Endpunkte und keinen allgemeinen Netzwerkscan.
2. Nutze bestehende autorisierte Lesezugriffe für Erreichbarkeit, Authentisierung,
   Fehler und konkrete Funktionsnachweise. Ein Worker-Status ersetzt keinen
   frischen Provider-Readback. Wenn nur ein eingeschränkter Test möglich ist,
   nenne genau dessen Grenze.
3. Für einen Shop-Check trenne aktive Theme-/Umgebungsidentität, Produktanzeige,
   beabsichtigten Bestellstatus und wirklich geprüften Kaufpfad. Eine absichtliche
   Sperre nicht eigenmächtig entsperren; daraus keinen pauschalen Ausfall ableiten.
   Keine Bestellung oder Zahlung für einen Erreichbarkeitscheck erzeugen.
4. Vergleiche gegen den letzten passenden bestätigten Befund im bestehenden
   Auftrags-/Ergebnisbestand. Falls ein früherer Befund fehlt, kennzeichne die
   Baseline als neu. Verändere keine Aufbewahrung und erzeuge keinen zweiten Store.
5. Priorisiere neue handlungsrelevante Abweichungen und Erholungen. Wiederholte
   identische Zustände nicht als neue Vorfälle duplizieren. Bericht und eventuell
   bereits autorisierte interne Übergabe getrennt von tatsächlicher Zustellung halten.

Ergebnis: Dienst/Umgebung, Ist gegen Soll, Fach-Testtiefe, betroffene Funktion,
Beleg und Zeitstand, erkennbare Änderung, zuständige Rolle und kleinster nächster
Diagnose- oder Reparaturschritt. Ohne Beleg keine Uptime-Prozentzahl, Ursache oder
Entwarnung erfinden. Dieser Skill repariert, deployt oder ändert keine Secrets,
Sicherheitseinstellungen, Providerkonfiguration oder Zeitpläne.

## Einordnung und bestehender Kontext

Dieser zusätzliche Skill arbeitet im Auftrag der jeweiligen Rolle. Lies deren
aktuelle AGENTS.md und ROLE-REFERENCE.md und führe den dort vorgegebenen gemeinsamen
Kontext-/Memory-Start aus. Verwende die aktuelle Vertragsrevision und bestehende
Fach-Reader. Der Skill erweitert deren Berechtigungen nicht und ersetzt keinen
vorhandenen Skill, fachlichen Ablauf oder Freigabeprozess.

Sein eigener Umfang ist Lesen, Prüfen und ein interner Bericht oder Entwurf.
Schon autorisierte andere Abläufe bleiben getrennt gültig. Er richtet keine neue
Automatik, Infrastruktur, Erinnerung, kostenpflichtige API oder Nachrichtenroutine ein.
Keine private Kunden-, Finanz- oder Lieferanteninformation, Rohantwort oder Zugangsdaten
in dieses Rollen-Repository schreiben. Ergebnisse gehören in die bestehende,
tatsächlich als privat bestätigte Auftrags-/Ergebnisablage. Die Bezeichnung „privat“
in einer alten Notiz ersetzt keine Zugriffsprüfung.

## Nachweis und Abschluss

- Binde Erkenntnisse an tatsächliche Quellen-IDs, deren ursprüngliche Beobachtungszeit,
  den Prüfzeitpunkt, die Vertragsrevision sowie den gelesenen Ausschnitt und seine Abdeckung.
  Ein interner Status, Cache, HTTP 200 oder vorhandener Schlüssel belegt keinen Facherfolg.
- Fehlende Daten bleiben unbekannt. Veraltete, historische und synthetische Quellen
  ausdrücklich kennzeichnen; Testdaten autorisieren keine echte Geschäftsaktion.
- Berichte evidenceStatus complete, partial oder unavailable für den geprüften Umfang;
  wechsle deshalb nicht eigenmächtig das Statusschema der bestehenden Aufgaben.
- Liefere die wesentlichen Befunde mit owner, sourceRefs, nächstem konkretem Schritt
  und einem tatsächlich prüfbaren Ergebnisverweis. Zeige nur belegte Beträge und Wirkungen.
- Nutze für zugeordnete Aufgaben den bestehenden shared_tasks.py-/TaskPort-Vertrag
  einschließlich erwarteter Version, operationId und Ergebnis-Readback. Ein unklarer
  Schreibausgang wird vor Wiederholung abgeglichen. Ohne aktuelle Aufgabe keine
  beliebige fremde Aufgabe übernehmen oder als abgeschlossen markieren.
- Beende den gemeinsamen Kontextlauf wie in AGENTS.md vorgesehen. Fehlt ein Zugriff,
  benenne den genauen Reader/Scope/Fehler, setze nur abhängige Arbeit aus und behaupte
  weder gespeicherte Ergebnisse noch eine erfolgreiche Live-Abnahme.

## Sichere Diagnoseausgabe
Bei Einrichtung, Leseproben und Tests private Kontext-/Providerdaten im privaten
Scratch verarbeiten. Keine Rohantworten, Finanzreferenzen oder Memory-Treffer in
Toolprotokolle ausgeben. Nutze `node tools/safe-readback.mjs /tmp/readback.json`
für Status, Umfang und Prüfsumme; der Metadatennachweis ersetzt keine Fachprüfung.
Eine ausdrücklich nur lesende Testanweisung schließt schreibende Bootstrap-
Receipts aus. Automatische Erkennung, manuelles Laden und Fachtest getrennt belegen.

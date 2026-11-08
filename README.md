# vnext-technical-executor
VARION Technology &amp; Infrastructure Cloud-Umgebung

## VARION Cloud-Arbeitsressourcen

Dieses Repository bindet die Kernrolle **vnext-technical-executor**. Das Rollenprofil liegt in [ROLE-REFERENCE.md](ROLE-REFERENCE.md). Der gemeinsame Anwendungsquellcode bleibt im privaten Repository [varion-platform](https://github.com/varioncompany-crypto/varion-platform), damit die fünf Rollen nicht fünf auseinanderlaufende Kopien bearbeiten.

In einer autorisierten Codex-Cloud-Umgebung kann [scripts/prepare-workspace.sh](scripts/prepare-workspace.sh) den gemeinsamen Code als benachbartes Checkout bereitstellen. Das Skript enthält keine Zugangsdaten und bricht ab, wenn GitHub den Zugriff nicht erlaubt. Die Cloud-Umgebung muss separat veröffentlicht und ihr tatsächlicher Repositoryzugriff geprüft werden.

## Aktueller Astra-Auftrag

Der [Arbeitsauftrag vom 9. November](ASTRA-ARBEITSAUFTRAG-2026-11-09.md) priorisiert VARION-Aufgaben, die ein lokaler Astra-Chat ohne Boss-Aufmerksamkeit und sichtbare Maus-/Fensterübernahme ausführen kann, und nennt echte Abnahmegrenzen. Die [Zugangs- und Quellenkarte](ASTRA-ZUGAENGE-QUELLEN-2026-11-09.md) enthält nur Secret-Namen, keine Werte. Beide Dateien sind eine datierte Übergabe; aktuelle Provider- und Memory-Zustände werden vor Ausführung neu geprüft.

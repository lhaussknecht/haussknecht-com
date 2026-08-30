+++
date = '2026-08-30T10:00:00+02:00'
draft = false
title = 'Mobile Wareneingangs-App mit Keyence-Scannern bei Kaltbandproduzent'
tags = ['Success Story', 'Flutter', 'App-Entwicklung']
aliases = ['/posts/keyence-scanner-app-kaltbandproduzent/']
summary = 'Flutter-App auf Keyence BT-A600 Industrie-Handhelds für Wareneingang, Umlagerung und Warenausgang – mit Scanner-Integration, Fotodokumentation und Bluetooth-Etikettendruck.'
+++
# Vom Handscanner zur modernen Flutter-App – Digitalisierung der Hallenprozesse in der Stahlverarbeitung

Für einen mittelständischen Hersteller und Händler von Kaltband und Draht hat Haußknecht IT-Consulting eine mobile App entwickelt, mit der Mitarbeiter direkt in der Halle Wareneingang, Umlagerung und Warenausgang erfassen – auf robusten [**Keyence BT-A600**](https://www.keyence.de/products/mobile-computers/handheld-computers/bt-a600/) Industrie-Handhelds mit integriertem Barcode-Scanner.

## Ausgangslage

Die bisherige Erfassung lief über in die Jahre gekommene Windows-Mobile-Scanner (Zebra MC9090). Ersatzgeräte wurden knapp, die Oberfläche war nicht mehr zeitgemäß und neue Anforderungen – etwa Fotodokumentation oder Etikettendruck am Erfassungsort – ließen sich damit kaum umsetzen. Gefordert war eine zukunftssichere Lösung, die sich nahtlos in das bestehende Lager- und Produktionssystem einfügt.

## Die Lösung: Eine Flutter-App für die Halle

Mit **Flutter** haben wir eine Android-App entwickelt, die konsequent auf den Arbeitsalltag in der Halle ausgelegt ist: große Bedienelemente, klar geführte Schritt-für-Schritt-Abläufe und Bedienung fast ausschließlich über die Scan-Taste des Geräts.

### Wareneingang Coil
 - Auswahl von Lieferant und Bestellung
 - Erfassung der Coils per Scan der Lieferantenetiketten
 - Geführte Fotodokumentation des Anlieferungszustands
 - Erfassung von Gewicht, Qualitätsprüfung und Stichproben
 - Direkte Übergabe an den Kran zur Einlagerung

### Wareneingang Draht
 - Automatische Vergabe von Ringnummern
 - **Etikettendruck direkt am Gerät** über Bluetooth-Etikettendrucker (ZPL)
 - Mehrere Fotos je Bund, Upload im Hintergrund
 - Lieferscheinerfassung und automatische Benachrichtigung per E-Mail

### Umlagerung, Warenausgang und Suche
Bestände lassen sich per Scan umlagern, für den Versand kommissionieren und jederzeit im Lager wiederfinden – auch bei kurzzeitig fehlender WLAN-Abdeckung, da die Abläufe offline-fähig ausgelegt sind.

## Nahtlose Scanner-Integration

Die [Keyence BT-A600](https://www.keyence.de/products/mobile-computers/handheld-computers/bt-a600/) Handhelds – Android-Geräte mit 4,3-Zoll-Display, Quad-Kamera-Scanner und Pistolengriff-Option – liefern Scanergebnisse über das **Keyence ScanManager SDK** an die App. Über eine native Android-Anbindung landen die Scans ohne Umweg direkt im aktuellen Arbeitsschritt – kein Antippen von Eingabefeldern, kein Wechsel zwischen Apps. Die Integration ist herstellerunabhängig aufgebaut und unterstützt parallel auch Zebra-Geräte (DataWedge), sodass der Umstieg auf die neue Hardware schrittweise und ohne Stillstand erfolgen konnte.

## Integration in die bestehende Systemlandschaft

Die App ist keine Insellösung, sondern Teil des Lager- und Produktionssystems, das wir für den Kunden betreiben:

 - **.NET 8 Backend** mit PostgreSQL als zentrale Datenhaltung
 - **Echtzeit-Anbindung des Krans** über SignalR – der Kranfahrer sieht sofort, welches Coil wohin soll
 - **Objektspeicher (MinIO)** für die Fotodokumentation
 - **Automatische App-Updates** auf allen Geräten ohne manuelle Installation
 - **CI/CD mit GitHub Actions** für Backend und App

# Ergebnis

 - **Schnellere Erfassung** durch Scan-basierte Bedienung ohne Tastatureingaben
 - **Lückenlose Dokumentation** mit Fotos und Etiketten direkt beim Wareneingang
 - **Weniger Fehler** durch geführte Abläufe und Plausibilitätsprüfungen
 - **Zukunftssichere Hardware** und eine Codebasis, die auch auf iOS und Web läuft

Das Projekt zeigt, wie sich mit Flutter und moderner Industrie-Hardware Hallenprozesse spürbar beschleunigen lassen – ohne die gewachsene Systemlandschaft zu ersetzen. Sie möchten Ihre Erfassungsprozesse ebenfalls modernisieren? Sprechen Sie uns an!

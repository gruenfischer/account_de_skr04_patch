#############################
Account De Skr04 Patch Module
#############################

.. to remove, see https://www.tryton.org/develop/guidelines/documentation#index.rst

.. toctree::
   :maxdepth: 2

 .. This file is part of gf_mds_account_de_skr04_patch
   Licensed under the GNU Free Documentation License v1.3 or any later version.
   The COPYRIGHT file at the top level of this repository contains the
   full copyright notices and license terms.
   SPDX-License-Identifier: GFDL-1.3-or-later

#######################
account_de_skr04_patch
#######################

Documentation in German, module handles specific german taxation and accountig rules for the SKR04 account plan.

Ergänzung des Moduls mds_accout_de_skr04:

* Berücksichtigung der Unterscheidung Ware/Dienstleistung bei der Umsatzsteuer
* Hierarchische Struktur der Umsatzsteuer, so dass Steuersatzänderunge durch Setzen der Gültigkeiten 
   der jeweiligen Steuer erreicht umgesetzt werden könen. 
* Ergänzung fehlender Umsatzsteuertatbestände
* Ergänzung fehlender Konten
* Vereinfachung der Steuerkennzifferntabelle und Anpassung an das aktuelle ELSTER-Formular
* Integration von Steuerregeln

Berücksichtigte Szenarien
-----

* Ein- und Verkauf von Waren und Dienstleistungen (sonstigen Leistungen) innerhalb von Deutschland,
    in die EU und in Drittländer
* voller, ermäßigter und USt-freier Umsatzsteuersatz
* Import von Waren aus Drittländern über einen Zolldienstleister
* Kleinunternehmerregelung nach § 19 UStG
* Reverse Charge im Inland

U.A. nicht berücksichtigte Szenarien
-----

* Selbstimport von Waren mit eigener Zollnummer
* Export in EU-Länder an Endverbraucher mit Jahresumsatz  > OSS Schwelle pro Kunde (OSS-Verfahren); das kann über das über Modul `trytond_account_tax_rule_country` geregelt werden
* grenzüberschreitender Handel mit steuerlich individuell behandelter Waren, wie Gold. 
* ...


Umstellung vom bisherigen SKR04
-----

Folgende Schritte sind erforderlich:

0. Planung

* Empfehlung: Umstellung zum Stichtag (zum Beispiel Ende Rechnungsjahr)
* Prüfen: Soll bei dieser Gelegenheit die Aufwands- und Ertragskonten geändert werden?

1. Patch installieren:

2. Tryton-Menü: "Kontenplan von Vorlage aktualisieren"

3. gegebenenfalls neue Artikelkategorien anlegen

4. "alte" Umsatzsteuern durch neue ersetzen:

 
5. ...


Ausblick
-----

* auf Anforderung: Implementierung SKR42 und SKR14
* wünschenswert wäre ein einheitlicher "SKR_DE", der kompakt alle üblichen Standardkontenrahmen (03, 04, 42, 14) enthält. 


Autoren
-----

* Jakob Fischer – Grünfischer Consulting (Programmierung)
* Wolf Drechsel – Komponentenkontor Berlin GmbH (Dokumentation)
* MDS - Original Modul Skr04



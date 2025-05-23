# ediarum.INTRO.edit

Version: 1.2.0

© 2024-2025 by Berlin-Brandenburg Academey of Sciences and Humanities

Part of ediarum (https://www.ediarum.org, ediarum@bbaw.de)

Developed by TELOTA (https://www.bbaw.de/telota, telota@bbaw.de), a DH working group of the Berlin-Brandenburg Academey of Sciences and Humanities.

Ediarum Core Team:

* Nadine Arndt
* Martin Fechner
* Jan Wierzoch

Developers of ediarum.REGISTER:

* Sascha Grabsch
* Jan Wierzoch

## What does it do?

ediarum.INTRO.edit is an oXygen framework designed for the Author mode of the
oXygen XML-Editor (http://www.oxygenxml.com). It is optimized for oXygen XML
version 24.1. With the help of ediarum.INTRO.edit, scholars can create and edit
TEI-XML based introductory and accompanying texts and essays for digital
editions. The framework is intedend as a companion to ediarum.BASE.edit (see
<https://www.ediarum.org/module.html> for all the modules belonging to ediarum)
but can also be used independently as a standalone framework.
ediarum.REGISTER.edit complements ediarum.BASE.edit and enables the editing of
TEI-XML based indexes for people, places, organizations and terms in ediarum.

## Components

The oXygen framework ediarum.INTRO.edit comes as a ZIP archive containing the
following components:

- framework extension script file (`.exf`) for oXygen XML Author
- two JAVA files `ediarum.jar` and `tei.jar`
- Cascading Stylesheets
- Icons for the toolbar
- Other resources, i.e. XSLT stylesheets and XML templates

## Documentation

TBD

### projektspezifisches INTRO anlegen

**ACHTUNG:** Die Frameworks auf EXF-Basis unterstützten Default Schema (`<defaultSchema>`) erst ab Oxygen v25.1!

1.) Vorbereitung
* INTRO muss installiert sein!
  * => http://telota.bbaw.de/ediarum/intro/edit/update.xml
* Die Editorvariable `${ediarum_id}` muss eingetragen sein, damit ID richtig vergeben werden.
  * Falls das Projekt den ediarum-ID-Generator verwendet, ist die Variable bereits eingetragen. Andernfalls siehe <https://www.ediarum.org/docs/set-up/DE/topics/setup/oxygen_projekt-anlegen.html> bzw. <https://www.ediarum.org/docs/set-up/DE/topics/customization/id-generator.html>

2.) Projektdatei
* Optionen > Orte: Muss auf projektspezifisch umgestellt werden. Bei Benutzerdefinierter Pfad dann `${pdu}` eintragen, damit sowohl Framework als auch EXF erkannt werden.

3.) EXF-Datei anlegen
* Wichtig: Basis-Framework, welches erweitert wird, in `<script @base>` (hier ="ediarum.INTRO.edit") eintragen.
  * Bezüge auf das Basis-Framework werden dann automatisch gesetzt und in der GUI-Ansicht in Oxygen angezeigt, z.B. `${framework(ediarum.INTRO.edit)}/css/standard.css`.
* Tipp: Als Vorlage-Datei das Basis-EXF nehmen und dann auskommentieren/entfernen, was nicht benötigt wird.
* Tipp: Direkt einen Ordner für projektspezifische Aktionen anlegen: "externalAuthorActions"

4.) Aktionen anpassen
* Nach erstellen des EXF-Files Oxygen einmal neu starten. Dann wird automatisch ein Ordner (z.B. "ediarum.AVHR.intro_externalAuthorActions") im Projektverzeichnis angelegt. In diesem sind die Aktionen-XMLs des Basis-Frameworks hinterlegt.
  * Ordner wird bei jedem Neustart von Oxygen erstellt, Änderungen werden zurückgesetzt => Hier nur Basis-Aktionen.
* Probeweise z.B. PDF-Ausgabe anpassen
  * XML nach "externalAuthorActions" (NICHT "ediarum.AVHR.intro_externalAuthorActions"!) kopieren, ID und Dateinamen anpassen.

#### Weiteres
* Wie fügt man Aktionen hinzu? => addAction id="XXX"
* Wie entfernt man Basis-Aktionen aus dem Projekt-Menü? => removeAction id="XXX"

#### Probleme und Fragen
- Wenn die Datei fehlerhaft ist (z.B. eine fehlerhafte Verlinkung), wird das Framework in der Optionen (Dokumenttypen-Zuordnung) nicht angezeigt.
- Man kann eigene Aktionen nicht in der Oxygen-Ansicht öffenen. (Warum?)


## Contribution

If you want to contribute to ediarum, feel free to open an pull request on the main branch.

## License

ediarum.INTRO.edit is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.
ediarum.INTRO.edit is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.
You should have received a copy of the GNU General Public License
along with ediarum.INTRO.edit. If not, see <http://www.gnu.org/licenses/>.

## Third party licences

ediarum.INTRO.edit includes and makes use of software from third parties, which are
licensed seperately.

### tei.jar
The oXygen framework ediarum.INTRO.edit makes partly use of the oXygen TEI P5-Framework
(all files with copryright statement of Syncro Soft SRL and the file tei.jar), which
is distributed under the New BSD License (http://opensource.org/licenses/BSD-3-Clause):
Copyright 2011 Syncro Soft SRL, Romania. All rights reserved.
Redistribution and use in source and binary forms, with or without modification, are
permitted provided that the following conditions are met:


Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY Syncro Soft SRL ''AS IS'' AND ANY EXPRESS OR IMPLIED
WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND
FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL Syncro Soft SRL OR
CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR
SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON
ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING
NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF
ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

The views and conclusions contained in the software and documentation are those of the
authors and should not be interpreted as representing official policies, either expressed
or implied, of Syncro Soft SRL.

THIRD-PARTY LIBRARIES  
The following libraries are redistributed in this package, and subject to their respective licenses.

Name: Text Encoding Initiative (TEI) Consortium materials
Link: http://www.tei-c.org/Guidelines/access.xml
License: Dual-licensed: Creative Commons Attribution-ShareAlike 3.0 Unported License or BSD 2-Clause license.

### Font Linux Libertine

ediarum.INTRO.edit contains also the fonts Linux Libertine and Biolinum. You'll find their respective
licences in the font directory.

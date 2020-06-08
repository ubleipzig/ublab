# Hinweise zur Entwicklung von Open-Source-Software an der Universitätsbibliothek Leipzig

<!-- MDTOC maxdepth:6 firsth1:2 numbering:0 flatten:0 bullets:0 updateOnSave:1 -->

 [1\. Einstieg](#1-einstieg)<br>
[2\. Versionsverwaltung](#2-versionsverwaltung)<br>
[3\. Lizenzierung](#3-lizenzierung)<br>
[3.1 Outbound Lizenzierung](#31-outbound-lizenzierung)<br>
[3.2 Inbound Lizenzierung - Contributors License Agreement (CLA)](#32-inbound-lizenzierung-contributors-license-agreement-cla)<br>
[4\. Archivierung](#4-archivierung)<br>
[5\. Zitierung und Publikation](#5-zitierung-und-publikation)<br>
[6\. Minimalanforderungen an eine Projektdokumentation](#6-minimalanforderungen-an-eine-projektdokumentation)<br>
[6.1 Changelog](#61-changelog)<br>
[6.2 Readme](#62-readme)<br>
[6.3 Citation.cff](#63-citationcff)<br>
[6.4 Contributing](#64-contributing)<br>
[6.5 Licence](#65-licence)

<!-- /MDTOC -->

## 1\. Einstieg

Eine allgemeine Übersicht zum Einstieg in die Open-Source-Entwicklung liefert der [Open-Source-Guide](https://opensource.guide/de). Kriterien für Open-Source-Software findet man bei der [Open Source Initiative](https://opensource.org/docs/osd). Vorteile der Verwendung von Open Source werden u. a. [hier](http://oss-watch.ac.uk/resources/whoneedssource) erklärt. Ein offener Standard für offene Software wird von der Initiative [Public Code](https://standard.publiccode.net/) entwickelt.

## 2\. Versionsverwaltung

(Hinweis: Leider nur für Mitarbeiter\*innen zugänglich) Stefan Freitag beschreibt im redmine [Hinweise zur Verwaltung von Softwarecode](https://projekte.ub.uni-leipzig.de/projects/bdd/wiki/Git) mit Hilfe von git unter Nutzung des institutionellen GitLabs des URZ.

## 3\. Lizenzierung

Die dienstrechtliche Regelung zur Entwicklung von Open-Source-Software wird in der [Anweisung zur Veröffentlichung von Open-Source-Software an der Universitätsbibliothek Leipzig]() erklärt. Während die (Outbound-)Lizenzen, unter denen der Quellcode und die Dokumentationen lizenziert werden, die Regeln beschreiben, nach denen das Produkt verwendet werden darf, beschreibt das Contributors License Agreement (CLA) die Bedingungen, unter denen Beiträge zum Projekt abgewickelt werden (Inbound-Lizenzen).

### 3.1 Outbound-Lizenzierung

Eine [Übersicht zu Open-Source-Lizenzen](https://opensource.org/licenses/category) stellt die Open Source Initiative sowie [choosealicense](https://choosealicense.com/appendix/) zur Verfügung. Mithilfe des [Joinup Licensing Assistants](https://joinup.ec.europa.eu/collection/eupl/joinup-licensing-assistant-jla) können Lizenzen interaktiv anhand ihrer Eigenschaften ausgewählt werden. Die Wahl einer passenden Lizenz für Quellcode hängt vom Projektkontext ab und sollte wenn möglich bereits vor der eigentlichen Entwicklungstätigkeit mit allen Projektbeteiligten abgestimmt werden. Das Projekt [REUSE](https://reuse.software/) (sprich Re-Use und nicht [Reuse](https://de.wikipedia.org/wiki/Reuse)) stellt das Lizenzierungswerkzeug [reuse](https://github.com/fsfe/reuse-tool) zur Verfügung und gibt in einem [Tutorial](https://reuse.software/tutorial/) und in den [FAQ](https://reuse.software/faq/) viele wichtige Hilfestellungen zur Lizenzierung.

<!-- -Wir empfehlen die Wahl einer freizügigen Open-Source-Lizenz (z.B. GPL), um es allen zu ermöglichen, öffentlich finanzierte Forschung zu lesen und weiterzuverwenden (**ODER DOCH lieber Copyleft, GPL3 etc.?**). --> Beispiele aus der Universitätsbibliothek Leipzig:

- [Provit](https://github.com/diggr/provit) - Für Provit wurde mit der [MIT License](https://choosealicense.com/licenses/mit/) eine freizügige (permissive) Lizenz gewählt, die eine Weiterverwendung unter sehr geringen Anforderungen in einem sehr breiten Kontext ermöglicht (u.a. auch in proprietärer Software). Ausschlaggebend für die Verwendung einer freizügigen Lizenz war, dass dadurch die Akzeptanz von Provit als Softwarebibliothek erhöht wird.
- [PYG](https://github.com/diggr/pyg) - PYG wiederum verwendet eine [GPLv3](https://choosealicense.com/licenses/gpl-3.0/) Lizenz, eine sehr starke Copyleft-Lizenz, die eine Weiterverwendung nur unter [gleichen Bedingungen](https://www.gnu.org/licenses/license-list.html#GPLCompatibleLicenses) möglich macht.

Für Dokumentation und Textanteile des Projektes sind [Creative-Commons-Lizenzen](https://creativecommons.org) relevant. Kompatibilität bei der Verwendung mehrerer Lizenzen wird [hier](https://creativecommons.org/faq/#can-i-combine-material-under-different-creative-commons-licenses-in-my-work) erklärt. Wir empfehlen hier die Verwendung einer liberalen und offenen Lizenz, wie z.B. die [CC-BY-Lizenz](https://creativecommons.org/licenses/by/4.0/legalcode).

### 3.2 Inbound-Lizenzierung – Contributors License Agreement (CLA)

Das CLA wird verwendet, um sicherzustellen, dass die Beitragenden tatsächlich alle erforderlichen Rechte an ihrem Beitrag besitzen. Insbesondere bei externen Kooperationen an einer Software unter einer Copyleft-Lizenz (z.B. GPL) wird empfohlen, eine CLA aufzusetzen, um mögliche Konflikte in der Zukunft zu vermeiden. Bei Projekten, die zu Beginn ihrer Entwicklung keine offene Strategie vorsahen, müssen alle Beteiligten identifiziert und um Erlaubnis gebeten werden.

- <http://contributoragreements.org> - für die Erstellung einer CLA
- In Github kann dafür der [GAV-Assistent](https://cla-assistant.io) benutzt werden (prüft automatisch alle Push-Anfragen).

## 4\. Archivierung

Eine kurze Einführung in die Archivierung von Forschungssoftware liefern Seiten der UB Stuttgart: [Forschungssoftware archivieren](https://www.ub.uni-stuttgart.de/forschen-publizieren/forschungssoftware/archivieren/).

Die 'Langzeitarchivierung' von Software wird z.B. von [Software Heritage](https://www.softwareheritage.org) als Dienst angeboten und vom französischen Forschungsinstitut [INRIA](https://www.inria.fr/en/) gehostet. Software Heritage ingesten dabei automatisch öffentliche Repositorien folgender Dienste (Stand 20.06.2019) : Debian, Framagit, GitHub, GitLab, Gitorius, Google code, Gnu, HAL, INRIA, npm, pypi. Für alle anderen Fälle gibt es die Option "[Save code now](https://archive.softwareheritage.org/browse/origin/save/)".

## 5\. Zitierung und Publikation

Die Auffindbarkeit und Sichtbarkeit von Software kann erhöht werden, indem gängige Zitationsstandards berücksichtigt werden. Wieso wir Software-Zitierung brauchen und die grundlegenden Prinzipien dafür finden sich hier: [Software Citation Principles](https://www.force11.org/software-citation-principles). Das [Citation File Format](https://citation-file-format.github.io/) ist ein gängiges Dateiformat für das Zitieren von Software. Es wird empfohlen dieses in die Projektdokumentation aufzunehmen.

Mittlerweile bieten verschiedene Anbieter die Integration mit [DataCite](https://blog.datacite.org/doi-registrations-software/) und den damit verbundenen Bezug eines DOIs an:

- [Zenodo](https://zenodo.org/) ist der Klassiker für den Bezug einer DOI für Software. Wie das für GitHub-Code funktioniert, wird hier beschrieben: [Making your _GitHub_ code citeable](https://guides.github.com/activities/citable-code/). Das Helmholtz-Zentrum Dresden-Rossendorf entwickelt gerade eine ähnliche Integration von [GitLab](https://www.gitlab.com) und Zenodo: [Invenio-GitLab](https://gitlab.hzdr.de/rodare/invenio-gitlab)

- [figshare](https://figshare.com) liefert ebenfalls die Option, Software über eine DOI zitierbar zu machen. Für GitHub wird dies hier erklärt: [How to connect figshare with your GitHub account](https://knowledge.figshare.com/articles/item/how-to-connect-figshare-with-your-github-account-1). Jedes figshare Projekt erhält automatisch eine DOI zugewiesen.

- Auf [Code Ocean](https://codeocean.com) werden ebenfalls DOIs für Softwarepublikationen vergeben. Alles in Bezug auf den Umgang mit DOIs findet sich hier: [Your compute capsule's DOI](https://help.codeocean.com/publishing-on-code-ocean/after-your-capsule-is-accepted-for-publication/your-compute-capsules-doi).

Es empfiehlt sich, für jedes größere Softwarerelease zur Herstellung der Zitierfähigkeit eine DOI zu beziehen.

[CodeMeta](https://codemeta.github.io/) wiederum liefert Crosswalks für diverse Plattformen. Unter [Create](https://codemeta.github.io/create/) kann man sich eine CodeMeta JSON-LD für seine Software anlegen. Praktische Anwendungen stehen allerdings noch aus.

## 6\. Minimalanforderungen an eine Projektdokumentation

Die Minimalanforderungen (hier abgebildet als Markdown) dienen als Richtlinie für jedes neue Softwareprojekt und orientieren sich an gängigen Werkzeugen und Dokumentationsstandards aus der Softwareentwicklung.

### 6.1 Changelog

Ein Changelog soll einen groben Überblick über wesentliche Änderungen an der Software liefern. Wieso es wichtig ist ein Changelog zu führen, wird auf [(keepachangelog.com)](https://keepachangelog.com/de/1.0.0/) erklärt.

**Beispiel**:

```
# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2019-06-20
### Added
- Version navigation.
- Links to latest released version in previous versions.

### Changed
- Start using "changelog" over "change log" since it's the common usage.
- Fix typos in English translation

### Removed
- Section about "changelog" vs "CHANGELOG".

## ...
```

### 6.2 Readme

Eine Readme ist der zentrale Einstieg in die Dokumentation von Software und enthält die wichtigsten Punkte zur Entwicklung, Nutzung, Zitierung und Änderungen an der Software.

**Beispiel**

```
# Software Name

[Leipzig University Library](https://ub.uni-Leipzig.de/en).

Kurze Beschreibung der Software
...

For further informations: Link Website

## Published versions

- Leipzig University Library. (2018). Software Name. v1.0\. doi:[...](https://doi.org/...)
- Leipzig University Library. (2018). Software Name. v0.3\. doi:[...](https://doi.org/...)

--------------------------------------------------------------------------------

# Developer guide

## About these instructions

- These instructions were tested on Ubuntu 16.04.3 LTS xenial.
- Other versions of the tools may also be usable.
- Installing tools requires you to have sudo access to install ...

## Install dependencies

### Dep 1

...

### Dep 2

...

## Next Step

...

--------------------------------------------------------------------------------

# User guide

## About these instructions

- These instructions were tested on Ubuntu 16.04.3 LTS xenial.
- Other versions of the tools may also be usable.
- Installing tools requires you to have sudo access to install ...

## Install dependencies

### Dep 1

...

### Dep 2

...

## Next Step

## ...

--------------------------------------------------------------------------------

# Contributing

See [Contributing](./CONTRIBUTING.md).

--------------------------------------------------------------------------------

# Copyright and Licence

Copyright (c) 2017-2019, Leipzig University Library

- Documentation: Creative Commons Attribution 4.0 International
- Source code: Apache License, Version 2.0, January 2004

For full details, see [LICENCE](./LICENCE.md).

The Leipzig University Library provides the source code on an
"as-is" basis, makes no warranties regarding any information
provided within and disclaims liability for damages resulting
from using this source code. You are solely responsible for
determining the appropriateness of any advice and guidance
provided and assume any risks associated with your use of the
source code.

--------------------------------------------------------------------------------

# Acknowledgements

Software Name has its origins in:

A Publication | A research project | Another Software |...

SoftwareName has evolved in response to feedback from:
Name, Institution;
Name, Istitution;
...

We also acknowledge the valuable assistance and generosity of
Geldgeber | Kooperierende Institutionen | ...

# Repo Status

[![Project Status: Active – The project has reached a stable, usable state and is being actively developed.](https://www.repostatus.org/badges/latest/active.svg)](https://www.repostatus.org/#active)
```

Im letzten Punkt der Readme wird mithilfe eines Badges der aktuelle Status des Repositories in sowohl maschinen- als auch für Menschen lesbarer Form dargestellt. Weitere Status siehe [Repostatus Badges](https://www.repostatus.org/): Concept, WIP, Suspended, Abandoned, Active, Inactive, Unsupported, Moved.

### 6.3 Citation.cff

Das [Citation File Format (CFF)](https://citation-file-format.github.io/) trägt Zitationsmetadaten für Software im [YAML 1.2 Format](https://yaml.org/spec/1.2/spec.html). Die Spezifikation findet sich [hier](https://citation-file-format.github.io/1.0.3/). Auf den Github-Seiten des Projekts finden sich außerdem [Tools für die Nutzung des CFF](https://github.com/citation-file-format/citation-file-format#tools), wie z.B. ein doi2cff Generator.

**Beispiel**

```
cff-version: 1.0.3
message: If you use this software, please cite it as below.
authors:
  - family-names: Nachname
    given-names: Vorname
    orcid: https://orcid.org/0000-...
  - family-names: Nachname2
    ...
title: SoftwareName
version: 1.0
doi: ...
date-released: 2017-12-18
license: Apache-2.0
repository-code: https://github.com/...
keywords:
  - research software
  - software maintenance
  - ...
```

### 6.4 Contributing

Um zukünftigen Mitwirkenden an der Entwicklung den Einstieg so leicht wie möglich zu machen, empfiehlt es sich eine CONTRIBUTING Datei anzulegen und darin das Vorgehen zu erklären. Dazu z.B. die Hilfeseiten auf GitHub: [Setting guidelines for repository contributors](https://help.github.com/en/articles/setting-guidelines-for-repository-contributors).

**Beispiel**

```
For major suggestions or comments about the source code and documentation:

  1\. Check that an existing issue has not already been created that may cover the scope of your suggestion or comment.
  2\. If an existing issue already covers the scope of your suggestion or comment, then please add your own to the issue.
  3\. If there isn't an applicable issue then please create a new issue.

For minor rewordings or rephrasings:

  Either raise an issue, as above.
  Or create a pull request with the suggested changes:
    * Fork this repository into your own GitHub account.
    * Check out the master branch.
    * Read README.md on how to start coding.
    * Make your changes to your local fork.
    * Make sure that your changes look OK, always test your suggested code if possible.
    * When you are ready to contribute your changes, submit a pull request.
```

### 6.5 Licence

Neben dem Hinweis auf die verwendeten Lizenzen im Readme sollte der Projektdokumentation noch eine separate Datei hinzugefügt werden, welche die einzelnen Lizenztexte aufführt.

**Beispiel**

```
------------
Source Code
------------
Copyright (c) 2014-2019, Leipzig University Library

Apache License
Version 2.0, January 2004
http://www.apache.org/licenses/

TEXT
TEXT
...

----------------------------------------------------

-------------
Documentation
-------------
Copyright (c) 2014-2019, Leipzig University Library

Creative Commons Attribution 4.0 International
https://creativecommons.org/licenses/by/4.0/legalcode

TEXT
TEXT
...
```

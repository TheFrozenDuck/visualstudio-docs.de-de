---
title: Arbeitsauslastungs- und Komponenten-IDs in Visual Studio Build Tools 2017 | Microsoft-Dokumentation
description: Verwenden von Arbeitsauslastungs- und Komponenten-IDs in Visual Studio zum Erstellen klassischer Windows-basierter Anwendungen
keywords: 
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.date: 12/01/2017
ms.topic: article
helpviewer_keywords:
- workload ID, Visual Studio
- component ID, Visual Studio
- install Visual Studio, administrator guide
ms.service: 
ms.technology: vs-acquisition
ms.assetid: b99298df-0280-47fc-af73-44cd7a8ac553
ms.workload: multiple
ms.openlocfilehash: 4b41304a893dbee45b7de08edb9a37e07ef8656d
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="visual-studio-build-tools-2017-component-directory"></a>Visual Studio Build Tools 2017-Komponentenverzeichnis

In den Tabellen auf dieser Seite sind die IDs aufgeführt, die Sie verwenden können, um Visual Studio über die Befehlszeile zu installieren. Beachten Sie, dass weitere Komponenten hinzugefügt werden, wenn wir Updates für Visual Studio veröffentlichen.

Beachten Sie zudem Folgendes im Hinblick auf diese Seite:

* Für jede Arbeitsauslastung gibt es einen eigenen Abschnitt, gefolgt von der Arbeitsauslastungs-ID und einer Tabelle der Komponenten, die für die Arbeitsauslastung zur Verfügung stehen.
* Die **erforderlichen** Komponenten werden standardmäßig bei der Installation der Arbeitsauslastung installiert. Bei Bedarf können Sie auch die **empfohlenen** und **optionalen** Komponenten installieren.
* Wir haben auch einen Abschnitt hinzugefügt, in dem die zusätzlichen Komponenten aufgeführt sind, die keiner Arbeitsauslastung zugeordnet sind.

Weitere Informationen zur Verwendung dieser IDs finden Sie auf der Seite [Verwenden von Befehlszeilenparametern zum Installieren von Visual Studio 2017](use-command-line-parameters-to-install-visual-studio.md). Eine Liste der Arbeitsauslastungs- und Komponenten-IDs für andere Produkte finden Sie auf der Seite [Arbeitsauslastungs- und Komponenten-IDs in Visual Studio 2017](workload-and-component-ids.md).

## <a name="msbuild-tools"></a>MSBuild-Tools

**ID:** Microsoft.VisualStudio.Workload.MSBuildTools

**Beschreibung:** Stellt die erforderlichen Tools zum Erstellen von MSBuild-basierten Anwendungen bereit.

### <a name="components-included-by-this-workload"></a>Komponenten in dieser Arbeitsauslastung

Komponenten-ID | name | Version | Abhängigkeitstyp
--- | --- | --- | ---
Microsoft.Component.MSBuild | MSBuild | 15.0.27019.1 | Erforderlich
Microsoft.VisualStudio.Component.CoreBuildTools | Visual Studio Build Tools, Core | 15.0.27005.2 | Erforderlich
Microsoft.VisualStudio.Component.Roslyn.Compiler | C#- und Visual Basic-Roslyn-Compiler | 15.0.27019.1 | Erforderlich
Microsoft.VisualStudio.Component.FSharp.MSBuild | F#-Compiler | 15.0.27019.1 | Optional

## <a name="net-core-build-tools"></a>.NET Core-Buildtools

**ID:** Microsoft.VisualStudio.Workload.NetCoreBuildTools

**Beschreibung:** Tools zum Erstellen von .NET Core-Anwendungen.

### <a name="components-included-by-this-workload"></a>Komponenten in dieser Arbeitsauslastung

Komponenten-ID | name | Version | Abhängigkeitstyp
--- | --- | --- | ---
Microsoft.Net.Core.Component.SDK | .NET Core 1.0 – 1.1-Entwicklungstools | 15.0.26606.0 | Erforderlich
Microsoft.VisualStudio.Component.NuGet.BuildTools | NuGet-Ziele und Buildtasks | 15.0.26919.1 | Erforderlich
Microsoft.Net.Core.Component.SDK.1x | Entwicklungstools von .NET Core 1.0 – 1.1 für Desktop | 15.0.26919.1 | Optional

## <a name="visual-c-build-tools"></a>Visual C++ Build Tools

**ID:** Microsoft.VisualStudio.Workload.VCTools

**Beschreibung:** Erstellen Sie klassische Windows-basierte Anwendungen mit dem leistungsfähigen Visual C++-Toolset, ATL und optionalen Features wie MFC und C++/CLI.

### <a name="components-included-by-this-workload"></a>Komponenten in dieser Arbeitsauslastung

Komponenten-ID | name | Version | Abhängigkeitstyp
--- | --- | --- | ---
Microsoft.VisualStudio.Component.VC.CoreBuildTools | Visual C++ Build Tools Kernfunktionen | 15.0.27005.2 | Erforderlich
Microsoft.VisualStudio.Component.VC.Redist.14.Latest | Visual C++ 2017 Redistributable Update | 15.0.27019.1 | Erforderlich
Microsoft.VisualStudio.Component.Windows10SDK | Windows Universal C Runtime | 15.0.26621.2 | Erforderlich
Microsoft.VisualStudio.Component.Static.Analysis.Tools | Statische Analysetools | 15.0.26208.0 | Empfohlen
Microsoft.VisualStudio.Component.VC.CMake.Project | Visual C++-Tools für CMake | 15.0.27019.1 | Empfohlen
Microsoft.VisualStudio.Component.VC.Tools.x86.x64 | VC++ 2017 v141-Toolset (x86, x64) | 15.0.27019.1 | Empfohlen
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop | Windows 10 SDK (10.0.16299.0) für Desktop C++ [x86 und x64] | 15.0.27128.1 | Empfohlen
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP | Windows 10 SDK (10.0.16299.0) für UWP: C#, VB, JS | 15.0.27128.1 | Empfohlen
Microsoft.VisualStudio.Component.Windows10SDK.16299.UWP.Native | Windows 10 SDK (10.0.16299.0) für UWP: C++ | 15.0.27128.1 | Empfohlen
Microsoft.VisualStudio.ComponentGroup.WebToolsExtensions | ASP.NET und Webentwicklung | 15.0.27005.2 | Empfohlen
Microsoft.Component.VC.Runtime.UCRTSDK | Windows Universal CRT SDK | 15.0.27019.1 | Optional
Microsoft.Net.Component.4.6.1.SDK | .NET Framework 4.6.1 SDK | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.6.1.TargetingPack | Paket zur Festlegung von Zielversionen von .NET Framework 4.6.1 | 15.0.26621.2 | Optional
Microsoft.VisualStudio.Component.VC.140 | VC++-2015.3 v140 Toolset für Desktop (x86, x64) | 15.0.27019.1 | Optional
Microsoft.VisualStudio.Component.VC.ATL | Visual C++-ATL-Unterstützung | 15.0.26823.1 | Optional
Microsoft.VisualStudio.Component.VC.ATLMFC | MFC- und ATL-Unterstützung (x86 und x64) | 15.0.27005.2 | Optional
Microsoft.VisualStudio.Component.VC.ClangC2 | Clang/C2 (experimentell) | 15.0.27019.1 | Optional
Microsoft.VisualStudio.Component.VC.CLI.Support | C++-/CLI-Unterstützung | 15.0.27019.1 | Optional
Microsoft.VisualStudio.Component.VC.Modules.x86.x64 | Module für die Standardbibliothek (experimentell) | 15.0.27019.1 | Optional
Microsoft.VisualStudio.Component.VC.Tools.ARM | Visual Studio C++-Compiler und -Bibliotheken für ARM | 15.0.27019.1 | Optional
Microsoft.VisualStudio.Component.VC.Tools.ARM64 | Visual C++-Compiler und -Bibliotheken für ARM64 | 15.0.27019.1 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.10240 | Windows 10 SDK (10.0.10240.0) | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.10586 | Windows 10 SDK (10.0.10586.0) | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.14393 | Windows 10 SDK (10.0.14393.0) | 15.0.26208.0 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.15063.Desktop | Windows 10 SDK (10.0.15063.0) für Desktop C++ [x86 und x64] | 15.0.27128.1 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.15063.UWP | Windows 10 SDK (10.0.15063.0) für UWP: C#, VB, JS | 15.0.27128.1 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.15063.UWP.Native | Windows 10 SDK (10.0.15063.0) für UWP: C++ | 15.0.27128.1 | Optional
Microsoft.VisualStudio.Component.Windows10SDK.16299.Desktop.arm | Windows 10 SDK (10.0.16299.0) für Desktop C++ [ARM und ARM64] | 15.0.27128.1 | Optional
Microsoft.VisualStudio.Component.Windows81SDK | Windows 8.1 SDK | 15.0.26208.0 | Optional
Microsoft.VisualStudio.ComponentGroup.NativeDesktop.Win81 | Windows 8.1 SDK und UCRT SDK | 15.0.27019.1 | Optional

## <a name="web-development-build-tools"></a>Development Build

**ID:** Microsoft.VisualStudio.Workload.WebBuildTools

**Beschreibung:** MSBuild-Aufgaben und -Ziele zum Erstellen von Webanwendungen.

### <a name="components-included-by-this-workload"></a>Komponenten in dieser Arbeitsauslastung

Komponenten-ID | name | Version | Abhängigkeitstyp
--- | --- | --- | ---
Microsoft.Net.Component.4.6.1.SDK | .NET Framework 4.6.1 SDK | 15.0.26621.2 | Erforderlich
Microsoft.Net.Component.4.6.1.TargetingPack | Paket zur Festlegung von Zielversionen von .NET Framework 4.6.1 | 15.0.26621.2 | Erforderlich
Microsoft.Net.ComponentGroup.DevelopmentPrerequisites | .NET Framework 4.6.1-Entwicklungstools | 15.0.27005.2 | Erforderlich
Microsoft.VisualStudio.Wcf.BuildTools.ComponentGroup | WCF Development Build-Tools | 15.0.27019.1 | Erforderlich
Microsoft.VisualStudio.Web.BuildTools.ComponentGroup | Development Build | 15.0.26323.1 | Erforderlich
Microsoft.Net.Component.4.5.1.TargetingPack | Paket zur Festlegung von Zielversionen von .NET Framework 4.5.1 | 15.0.26621.2 | Empfohlen
Microsoft.Net.Component.4.5.2.TargetingPack | Paket zur Festlegung von Zielversionen von .NET Framework 4.5.2 | 15.0.26621.2 | Empfohlen
Microsoft.Net.Component.4.5.TargetingPack | Paket zur Festlegung von Zielversionen von .NET Framework 4.5 | 15.0.26621.2 | Empfohlen
Microsoft.Net.Component.4.6.TargetingPack | Paket zur Festlegung von Zielversionen von .NET Framework 4.6 | 15.0.26621.2 | Empfohlen
Microsoft.Net.Component.4.TargetingPack | Paket zur Festlegung von Zielversionen von .NET Framework 4 | 15.0.26621.2 | Empfohlen
Microsoft.Net.ComponentGroup.TargetingPacks.Common | Entwicklungstools für .NET Framework 4 – 4.6 | 15.0.26606.0 | Empfohlen
Microsoft.Net.Core.Component.SDK | .NET Core 1.0 – 1.1-Entwicklungstools | 15.0.26606.0 | Empfohlen
Microsoft.VisualStudio.Component.NuGet.BuildTools | NuGet-Ziele und Buildtasks | 15.0.26919.1 | Empfohlen
Microsoft.Net.Component.3.5.DeveloperTools | .NET Framework 3.5-Entwicklungstools | 15.0.26621.2 | Optional
Microsoft.Net.Component.4.6.2.SDK | .NET Framework 4.6.2 SDK | 15.0.26208.0 | Optional
Microsoft.Net.Component.4.6.2.TargetingPack | Paket zur Festlegung von Zielversionen von .NET Framework 4.6.2 | 15.0.26208.0 | Optional
Microsoft.Net.Component.4.7.1.SDK | .NET Framework 4.7.1 SDK | 15.0.27128.1 | Optional
Microsoft.Net.Component.4.7.1.TargetingPack | Paket zur Festlegung von Zielversionen von .NET Framework 4.7.1 | 15.0.27019.1 | Optional
Microsoft.Net.Component.4.7.SDK | .NET Framework 4.7 SDK | 15.0.26419.1 | Optional
Microsoft.Net.Component.4.7.TargetingPack | Paket zur Festlegung von Zielversionen von .NET Framework 4.7 | 15.0.26621.2 | Optional
Microsoft.Net.ComponentGroup.4.6.2.DeveloperTools | .NET Framework 4.6.2-Entwicklungstools | 15.0.26621.2 | Optional
Microsoft.Net.ComponentGroup.4.7.1.DeveloperTools | .NET Framework 4.7.1-Entwicklungstools | 15.0.27019.1 | Optional
Microsoft.Net.ComponentGroup.4.7.DeveloperTools | .NET Framework 4.7-Entwicklungstools | 15.0.27005.2 | Optional

## <a name="unaffiliated-components"></a>Nicht zugeordnete Komponenten

Dies sind Komponenten, die in keiner Arbeitsauslastung enthalten sind, jedoch als einzelne Komponenten ausgewählt werden können.

Komponenten-ID | name | Version
--- | --- | ---
Microsoft.VisualStudio.Component.VC.Tools.14.11 | VC++ 2017, Version 15.4, Toolset 14.11 | 15.0.27128.1

## <a name="get-support"></a>Support aufrufen
Manchmal kann etwas schiefgehen. Wenn bei der Installation von Visual Studio ein Fehler auftritt, lesen Sie den Artikel [Problembehandlung bei Visual Studio 2017-Installations- und -Upgradefehlern](troubleshooting-installation-issues.md). Wenn keiner der Schritte zur Problembehandlung hilfreich ist, können Sie uns per Livechat kontaktieren, um Hilfe bei der Installation zu erhalten (nur in englischer Sprache). Einzelheiten finden Sie auf der [Visual Studio-Supportseite](https://www.visualstudio.com/vs/support/#talktous).

Hier sind einige weitere Supportoptionen:
* Sie können uns über Produktprobleme mit dem Tool [Problem melden](../ide/how-to-report-a-problem-with-visual-studio-2017.md) informieren, das sowohl im Visual Studio-Installer als auch in der Visual Studio-IDE angezeigt wird.
* Sie können uns einen Produktvorschlag unter [UserVoice](https://visualstudio.uservoice.com/forums/121579) mitteilen.
* Sie können Probleme mit Produkten im Portal [Visual Studio Developer Community](https://developercommunity.visualstudio.com/) im Blick behalten, Fragen stellen und Antworten finden.
* Über die [Visual Studio-Unterhaltung in der Gitter-Community](https://gitter.im/Microsoft/VisualStudio) können Sie auch Kontakt zu uns oder zu anderen Visual Studio-Entwicklern aufnehmen.  (Diese Option erfordert ein [GitHub](https://github.com/)-Konto.)

## <a name="see-also"></a>Siehe auch

* [Arbeitsauslastung und Komponenten-IDs von Visual Studio](workload-and-component-ids.md)
* [Administratorhandbuch für Visual Studio 2017 RC](visual-studio-administrator-guide.md)
* [Verwenden von Befehlszeilenparametern zum Installieren von Visual Studio](use-command-line-parameters-to-install-visual-studio.md)
  * [Beispiele für Befehlszeilenparameter](command-line-parameter-examples.md)
* [Erstellen einer Offlineinstallation von Visual Studio](create-an-offline-installation-of-visual-studio.md)

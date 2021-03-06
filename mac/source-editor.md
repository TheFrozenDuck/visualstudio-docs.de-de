---
title: Quellcode-Editor | Microsoft-Dokumentation
description: "Verwendung des Quellcode-Editors in Visual Studio für Mac"
author: asb3993
ms.author: amburns
ms.date: 04/14/2017
ms.topic: article
ms.assetid: A018A314-C1C4-4F36-BCB6-2D434208FCFE
ms.openlocfilehash: f52e60c0ade8cebc78b3408b4ef81ef85fcd767b
ms.sourcegitcommit: f40311056ea0b4677efcca74a285dbb0ce0e7974
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2017
---
# <a name="source-editor"></a>Quellcode-Editor

Ein zuverlässiger Quellcode-Editor ist entscheidend für kurzen und effizienten Code. Visual Studio für Mac bietet einen anspruchsvollen Quellcode-Editor, der das Herzstück der IDE darstellt. Der Quellcode-Editor stellt nicht nur die erwarteten Funktionen bereit, sondern auch solche, die Sie für reibungslose Arbeitsabläufe benötigen: von den Grundlagen wie der Syntaxhervorhebung, über Codeausschnitte und der Codefaltung, bis hin zu den Vorteilen der Roslyn-Compilerintegration wie eine voll funktionale IntelliSense-Codevervollständigung.

Der Quellcode-Editor in Visual Studio für Mac funktioniert problemlos mit allen anderen Funktionen der IDE, z.B. dem Debuggen, dem Refactoring und die der Integration der Versionskontrolle.

In diesem Thema werden die wichtigsten Funktionen des Quellcode-Editors eingeführt, und es wird erklärt, wie Sie Visual Studio für Mac so effektiv wie möglich verwenden können.

## <a name="the-source-editor-experience"></a>Benutzeroberfläche des Quellcode-Editors

Die Fähigkeit, den Code anzuzeigen und sich schnell darin bewegen zu können, ist wesentlich für den Entwicklungsworkflow. Wie Sie den Code anzeigen und verwalten, ist eine persönliche Entscheidung, die sich je nach Entwickler und Projekt unterscheidet.

Visual Studio für Mac bietet viele leistungsstarke Funktionen, mit denen die plattformübergreifende Entwicklung zugänglich und so übersichtlich wie möglich gestaltet wird. In den folgenden Abschnitten werden einige der Highlights beschrieben.


### <a name="code-folding"></a>Codefaltung

Die Codefaltung erleichtert das Verwalten großer Quellcodedateien, da Entwickler vollständige Codeabschnitte wie using-Direktiven, Codebausteine und -kommentare und #region-Anweisungen anzeigen oder ausblenden können. Dies ist in Visual Studio für Mac standardmäßig deaktiviert.

Um die Codefaltung zu aktivieren, navigieren Sie zu **Visual Studio > Einstellungen... > Text-Editor > Allgemein > Codefaltung**:

![Optionen für die Codefaltung](media/source-editor-image1.png)

Neben der Option zur Optimierung der Codefaltung enthält dieses Menü auch eine zum standardmäßigen falten von #regions und Kommentaren, wobei ein benannter Hinweis anstelle von Code angezeigt wird.

Verwenden Sie zum Anzeigen oder Ausblenden von Abschnitten das Anzeigewidget neben der Zeilennummer:

 ![Ein- oder Ausblenden von Abschnitten im Code](media/source-editor-image2.png)

Sie können auch zwischen dem Einblenden und Ausblenden von der Faltungen mithilfe der Menüelemente **Ansicht > Faltung > Toggle Fold (Faltung umschalten)/Alle Faltungen umschalten**:

 ![Menüelement „Faltung“](media/source-editor-image19.png)

Dieses Menüelement kann auch zur Aktivierung oder Deaktivierung der Codefaltung verwendet werden.

### <a name="white-space"></a>Leerraum

Es kann für Sie notwendig sein, unsichtbare Zeichen im Quellcode sehen zu können. So können Sie sicherstellen, dass Codierungsstandards eingehalten und Speicherplatz nicht unnötigerweise verschwendet wird. Auch beim Programmieren in F# ist dies sehr nützlich, denn dabei kommt es bei der Bewertung von Code genau auf die eingezogenen Zeilen an.

Um Leerzeichen anzuzeigen, navigieren Sie zu **Visual Studio > Einstellungen > Text-Editor > Markierungen und Lineale**, wie unten dargestellt. Wenn Sie diese Option auswählen, können Sie festlegen, _wann_ unsichtbare Zeichen angezeigt werden: Never (Nie), On Selection (Bei Auswahl) oder Always (Immer):

 ![Optionen zum Anzeigen unsichtbarer Zeichen](media/source-editor-image3.png)

Es ist ebenfalls eine Option zum Anzeigen von Registerkarten, Leerzeichen und Zeilenenden verfügbar:

 ![Anzeigen von Registerkarten und Leerzeichen](media/source-editor-image4.png)

 Unsichtbare Zeichen werden als grauer Punkte angezeigt, wie unten dargestellt:

 ![Leerzeichen angezeigt](media/source-editor-image22.png)


### <a name="ruler"></a>Lineal

Das Spaltenlineal ist sehr hilfreich für die Bestimmung von Zeilenlängen, insbesondere dann, wenn ein Team Vorgaben für die Zeilenlänge hat. Das Spaltenlineal kann aktiviert oder deaktiviert werden, indem Sie zu **Visual Studio > Einstellungen... > Text-Editor > Markierungen und Lineale** navigieren und **Show Column ruler** (Spaltenlineal anzeigen) wie unten gezeigt aktivieren (bzw. deaktivieren):

 ![](media/source-editor-image5.png)

 Dadurch wird im Quellcode-Editor eine vertikale, hellgraue Linie angezeigt.


### <a name="highlight-identifier-references"></a>Hervorheben von Bezeichnerverweisen

Wenn diese Option aktiviert ist, kann ein Entwickler den Mauszeiger auf jedem Symbol im Quellcode platzieren, und der Quellcode-Editor stellt eine visuelle Anleitung zu allen anderen Verweisen in dieser Datei bereit. Diese Option wird aktiviert, indem Sie zu **Visual Studio > Einstellungen... > Text-Editor > Markierungen und Lineale** navigieren und _Highlight identifier references_ (Bezeichnerverweise hervorheben) wie unten gezeigt auswählen:

![](media/source-editor-image6.png)

Die Farbe der Hervorhebung ist auch hilfreich, wenn angegeben werden soll, dass etwas zugewiesen oder darauf verwiesen wird. Wenn etwas zugewiesen wird, wird es in Rot hervorgehoben. Wenn darauf verwiesen wird, ist die Hervorhebung blau:

![](media/source-editor-image7.png)




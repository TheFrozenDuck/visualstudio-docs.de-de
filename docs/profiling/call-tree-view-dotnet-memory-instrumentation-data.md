---
title: 'Aufrufstrukturansicht: .NET-Speicherinstrumentationsdaten | Microsoft-Dokumentation'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-debug
ms.tgt_pltfrm: 
ms.topic: article
helpviewer_keywords: Call Tree view
ms.assetid: dd359707-245a-4a36-8305-2e980b9edd53
caps.latest.revision: "11"
author: mikejo5000
ms.author: mikejo
manager: ghogen
ms.workload: dotnet
ms.openlocfilehash: 043259d4ffd403abcffcfdfa724c8a8044caf5ab
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="call-tree-view---net-memory-instrumentation-data"></a>Aufrufstrukturansicht: .NET-Speicherinstrumentationsdaten
Die Aufrufstrukturansicht von .NET-Profilerstellungsdaten zur Speicherreservierung, die über die Instrumentationsmethoden erfasst werden, zeigt die Funktionsausführungspfade an, die in der Anwendung mit Profil durchlaufen wurden. Der Stamm der Struktur ist der Einstiegspunkt in die Anwendung oder Komponente. Jeder Funktionsknoten listet alle von ihm aufgerufenen Funktionen sowie den .NET-Speicher und Zeitdaten für die Funktion auf.  
  
 Die Werte in der Aufrufstrukturansicht beziehen sich auf die Funktionsinstanzen, die von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurden. Prozentwerte werden berechnet, indem der Funktionsinstanzwert mit der Gesamtanzahl oder Größe der Zuordnungen bei der Profilerstellung verglichen wird.  
  
## <a name="highlighting-the-execution-hot-path"></a>Hervorheben des langsamsten Ausführungspfads  
 Die Aufrufstrukturansicht kann erweitert werden und den Ausführungspfad des Prozesses oder der Funktion hervorheben, für die die größten oder meisten Arbeitsspeicherobjekte erstellt wurden. Klicken Sie mit der rechten Maustaste auf den Prozess oder die Funktion, und klicken Sie dann auf **Langsamsten Pfad erweitern**, um den Pfad mit der höchsten Aktivität anzuzeigen.  
  
## <a name="setting-the-call-tree-root-node"></a>Festlegen des Stammknotens der Aufrufstruktur  
 Jeder Prozess in der Profilerstellung wird als Stammknoten angezeigt. Sie können den Startknoten der Aufrufstrukturansicht festlegen, indem Sie mit der rechten Maustaste auf den Knoten klicken, der als Startknoten festgelegt werden soll, und dann auf **Stamm festlegen** klicken.  
  
 Durch das Festlegen eines Stammknotens wird sichergestellt, dass in der Ansicht lediglich die Teilstruktur des ausgewählten Knotens angezeigt wird. Sie können den Stammknoten auf den Knoten zurückzusetzen, den Sie zu diesem Zeitpunkt angesehen haben. Klicken Sie mit der rechten Maustaste auf das Aufrufstrukturansichtsfenster, und klicken Sie dann auf **Stamm zurücksetzen**.  
  
## <a name="general"></a>Allgemein  
  
|Spalte|description|  
|------------|-----------------|  
|**Funktionsname**|Der Name der Funktion.|  
|**Funktionsadresse**|Die Adresse der Funktion.|  
|**Funktionszeilennummer**|Die Zeilennummer des Anfangs dieser Funktion in der Quelldatei.|  
|**Anzahl der Aufrufe**|Die Gesamtzahl der Aufrufe dieser Funktion.|  
|**Quelldatei**|Die Quelldatei, die die Definition der Funktion enthält.|  
|**Modulname**|Der Name des Moduls, das die Funktion enthält.|  
|**Modulpfad**|Der Pfad des Moduls, das die Funktion enthält.|  
|**Prozess-ID**|Die Prozess-ID (PID) der Profilerstellung.|  
|**Prozessname**|Der Name, der dem Prozess zugewiesen ist.|  
|**Exklusive Zeit der Restkapazität für Überprüfungen**|Der von der Instrumentierung verursachte zusätzliche Zeitaufwand für diese Funktion. Der zusätzliche Testaufwand wurde von allen exklusiven Zeiten subtrahiert.|  
|**Inklusive Zeit der Restkapazität für Überprüfungen**|Der von der Instrumentierung verursachte zusätzliche Zeitaufwand für diese Funktion und ihre untergeordneten Funktionen. Der zusätzliche Testaufwand wurde von allen inklusiven Zeiten subtrahiert.|  
|**Type**|Der Kontext der Funktion:<br /><br /> -   **0** – die aktuelle Funktion<br />-   **1** – eine Funktion, die die aktuelle Funktion aufruft<br />-   **2** – eine Funktionen, die von der aktuellen Funktion aufgerufen wird<br /><br /> Nur in [VSPerfReport](../profiling/vsperfreport.md)-Befehlszeilenberichten.|  
|**Name der Stammfunktion**|Der Name der aktuellen Funktion. Nur in [VSPerfReport](../profiling/vsperfreport.md)-Befehlszeilenberichten.|  
  
## <a name="net-memory-values"></a>.NET-Arbeitsspeicherwerte  
 Die vollständigen .NET-Arbeitsspeicherwerte einer Funktion geben die Anzahl (Zuordnungen) und die Größe (Bytes) der Objekte an, die von der Funktion und den von dieser Funktion aufgerufenen Funktionen erstellt wurden.  
  
 Die exklusiven Arbeitsspeicherwerte geben die Anzahl und die Größe der Objekte an, die durch Code im Funktionsrumpf, nicht jedoch von den Funktionen erstellt wurden, die von der Funktion aufgerufen wurden.  
  
|Spalte|description|  
|------------|-----------------|  
|**Inklusive Speicherbelegungen**|Die Anzahl von Objekten, die von den Instanzen dieser Funktion zugeordnet wurden, die von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurden. Diese Zahl beinhaltet Zuordnungen, die von untergeordneten Funktion erstellt wurden.|  
|**Inklusive Speicherbelegungen in %**|Der Anteil aller Objekte, die bei der Profilerstellung erstellt wurden und vollständige Zuordnungen der Funktionsinstanzen beinhalten, die von der übergeordneten Funktion in der Aufrufansicht aufgerufen wurden.|  
|**Exklusive Speicherbelegungen**|Die Anzahl von Objekten, die von den Instanzen dieser Funktion zugeordnet wurden, die von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurden. Diese Zahl beinhaltet keine Zuordnungen, die von untergeordneten Funktionen erstellt wurden.|  
|**Exklusive Zuordnungen %**|Der Anteil aller Objekte, die bei der Profilerstellung erstellt wurden und keine Zuordnungen der Funktionsinstanzen beinhalten, die von der übergeordneten Funktion in der Aufrufansicht aufgerufen wurden.|  
  
## <a name="elapsed-inclusive-values"></a>Verstrichene inklusive Zeit  
 Werte für die verstrichene inklusive Zeit geben an, wie lange sich eine Funktion in der Aufrufliste befunden hat. Die Zeit umfasst die von den Funktionen, die von der Funktion aufgerufen wurden, beanspruchte Zeit und die Zeit für Aufrufe des Betriebssystems, z.B. Kontextwechsel und Eingabe-/Ausgabeoperationen.  
  
|Spalte|description|  
|------------|-----------------|  
|**verstrichene inklusive Zeit**|Die insgesamt bei den Aufrufen dieser Funktion verstrichene inklusive Zeit, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**verstrichene inklusive Zeit %**|Der Anteil der gesamten bei der Profilerstellung verstrichenen inklusiven Zeit, die innerhalb der gesamten verstrichenen inklusiven Zeit dieser Funktion aufgewendet wurde, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**Durchschnittliche verstrichene inklusive Zeit**|Die durchschnittlich bei den Aufrufen dieser Funktion verstrichene inklusive Zeit, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**Maximal verstrichene inklusive Zeit**|Die maximal bei den Aufrufen dieser Funktion verstrichene inklusive Zeit, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**Mindestens verstrichene inklusive Zeit**|Die mindestens bei den Aufrufen dieser Funktion verstrichene inklusive Zeit, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
  
## <a name="elapsed-exclusive-values"></a>Verstrichene exklusive Zeit  
 Werte für verstrichene exklusive Zeit geben die Zeit an, die eine Funktion direkt an erster Stelle der Aufrufliste ausgeführt wurde. Die Zeit beinhaltet die Zeit für Aufrufe des Betriebssystems, z.B. Kontextwechsel und Eingabe-/Ausgabeoperationen. Dies umfasst nicht die Zeit, die in von der Funktion aufgerufenen Funktionen aufgewendet wurde.  
  
|Spalte|description|  
|------------|-----------------|  
|**verstrichene exklusive Zeit**|Die insgesamt bei den Aufrufen dieser Funktion verstrichene exklusive Zeit, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**verstrichene exklusive Zeit %**|Der Anteil der insgesamt bei der Profilerstellung verstrichenen exklusiven Zeit, die innerhalb der gesamten verstrichenen exklusiven Zeit dieser Funktion aufgewendet wurde, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**Durchschnittlich verstrichene exklusive Zeit**|Die durchschnittlich bei den Aufrufen dieser Funktion verstrichene exklusive Zeit, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**Maximal verstrichene exklusive Zeit**|Die maximal bei den Aufrufen dieser Funktion verstrichene exklusive Zeit, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**Mindestens verstrichene exklusive Zeit**|Die mindestens bei den Aufrufen dieser Funktion verstrichene exklusive Zeit, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
  
## <a name="application-inclusive-values"></a>Werte für inklusive Anwendungszeit  
 Werte für die inklusive Anwendungszeit geben die Zeit an, die sich eine Funktion in der Aufrufliste befunden hat. Die Zeit umfasst nicht die Zeit für Aufrufe des Betriebssystems, z.B. Kontextwechsel und Eingabe-/Ausgabeoperationen. Die Zeit umfasst nicht die Zeit, die in von der Funktion aufgerufenen untergeordneten Funktionen aufgewendet wurde.  
  
|Spalte|description|  
|------------|-----------------|  
|**inklusive Anwendungszeit**|Die gesamte inklusive Anwendungszeit aller Aufrufe dieser Funktion, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**inklusive Anwendungszeit %**|Der Anteil der insgesamt bei der Profilerstellung verstrichenen inklusiven Zeit, die innerhalb der inklusiven Gesamtanwendungszeit dieser Funktion in diesem Kontext aufgewendet wurde, als die Funktion in der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**Durchschnittliche inklusive Anwendungszeit**|Die durchschnittliche inklusive Anwendungszeit eines Aufrufs dieser Funktion, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**Maximale inklusive Anwendungszeit**|Die maximale inklusive Anwendungszeit eines Aufrufs dieser Funktion, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**Minimale inklusive Anwendungszeit**|Die minimale inklusive Anwendungszeit eines Aufrufs dieser Funktion, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
  
## <a name="application-exclusive-values"></a>Exklusive Anwendungszeit  
 Werte für die exklusive Anwendungszeit geben die Zeit an, die für die Funktion aufgewendet wurde, jedoch ohne die Zeit, die für untergeordnete Funktionen aufgewendet wurde, die von der Funktion aufgerufen wurden. Die Zeit schließt außerdem Aufrufe des Betriebssystems aus (z. B. Kontextwechsel oder Eingabe-/Ausgabevorgänge).  
  
|Spalte|description|  
|------------|-----------------|  
|**exklusive Anwendungszeit**|Die exklusive Gesamtanwendungszeit aller Aufrufe dieser Funktion, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**exklusive Anwendungszeit %**|Der Anteil der insgesamt bei der Profilerstellung verstrichenen exklusiven Zeit, die innerhalb der exklusiven Gesamtanwendungszeit dieser Funktion aufgewendet wurde, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**Durchschnittliche exklusive Anwendungszeit**|Die durchschnittliche exklusive Anwendungszeit eines Aufrufs dieser Funktion, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**Maximale exklusive Anwendungszeit**|Die maximale exklusive Anwendungszeit eines Aufrufs dieser Funktion, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|  
|**Minimale exklusive Anwendungszeit**|Die minimale exklusive Anwendungszeit eines Aufrufs dieser Funktion, als diese von der übergeordneten Funktion in der Aufrufstruktur aufgerufen wurde.|
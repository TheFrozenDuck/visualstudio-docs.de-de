---
title: 'CA2003: Fibers nicht als Threads behandeln | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-code-analysis
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CA2003
- DoNotTreatFibersAsThreads
helpviewer_keywords:
- CA2003
- DoNotTreatFibersAsThreads
ms.assetid: 15398fb1-f384-4bcc-ad93-00e1c0fa9ddf
caps.latest.revision: "16"
author: gewarren
ms.author: gewarren
manager: ghogen
ms.workload: multiple
ms.openlocfilehash: 5afde6273a7730804746fe03446ea4c16c415302
ms.sourcegitcommit: 32f1a690fc445f9586d53698fc82c7debd784eeb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/22/2017
---
# <a name="ca2003-do-not-treat-fibers-as-threads"></a>CA2003: Fibers nicht als Threads behandeln
|||  
|-|-|  
|TypeName|DoNotTreatFibersAsThreads|  
|CheckId|CA2003|  
|Kategorie|Microsoft.Reliability|  
|Unterbrechende Änderung|Nicht unterbrechend|  
  
## <a name="cause"></a>Ursache  
 Ein verwalteter Thread wird als Win32-Thread behandelt wird.  
  
## <a name="rule-description"></a>Regelbeschreibung  
 Führen Sie Sie nicht davon gehen Sie aus, dass ein verwalteter Thread ein Win32-Thread ist. Es handelt sich um eine Fiber. Die common Language Runtime (CLR) wird als Fibers im Kontext von realen Threads, die im Besitz von SQL, verwaltete Threads ausgeführt. Diese Threads können über Anwendungsdomänen und selbst Datenbanken im SQL Server-Prozess gemeinsam genutzt werden. Mit verwalteten Thread, die lokaler Speicher verwendet werden kann, aber möglicherweise nicht verwenden, nicht verwalteten threadlokalen Speicher oder davon ausgehen, dass der Code erneut auf dem aktuellen Betriebssystemthread ausgeführt wird. Ändern Sie Einstellungen wie z. B. das Gebietsschema des Threads nicht. Rufen Sie nicht CreateCriticalSection oder CreateMutex über P/Invoke, da sie erfordern, dass der Thread, der eine Sperre eintritt auch, die Sperre beenden muss. Da dies beim Verwenden von Fibers nicht der Fall ist, werden wichtige Win32-Abschnitte und Mutexe in SQL nutzlos. Sie können die meisten der Status sicher auf einem verwalteten System.Thread-Objekt verwenden. Dies schließt verwaltete threadlokaler Speicher und der aktuelle Benutzer-Benutzeroberfläche (UI)-Kultur des Threads. Programmiermodells, Sie werden jedoch in der Lage, ändern die aktuelle Kultur eines Threads bei der Verwendung von SQL; Dies wird durch eine neue Berechtigung erzwungen werden.  
  
## <a name="how-to-fix-violations"></a>Behandeln von Verstößen  
 Untersuchen Sie die Verwendung von Threads, und ändern Sie den Code entsprechend.  
  
## <a name="when-to-suppress-warnings"></a>Wann sollten Warnungen unterdrückt werden?  
 Diese Regel sollte nicht unterdrückt werden.
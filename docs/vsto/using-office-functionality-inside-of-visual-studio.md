---
title: Office-Funktionen in Visual Studio mit | Microsoft Docs
ms.custom: 
ms.date: 02/02/2017
ms.reviewer: 
ms.suite: 
ms.technology: office-development
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- VB
- CSharp
helpviewer_keywords:
- security [Office development in Visual Studio], document protection
- Office applications [Office development in Visual Studio]
- Office functionality inside Visual Studio
author: TerryGLee
ms.author: tglee
manager: ghogen
ms.workload: office
ms.openlocfilehash: fa848d522096b5df12db113cf0c7272ab61c80be
ms.sourcegitcommit: f9fbf1f55f9ac14e4e5c6ae58c30dc1800ca6cda
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/10/2018
---
# <a name="using-office-functionality-inside-of-visual-studio"></a>Verwenden von Office-Funktionen in Visual Studio
  Wenn Sie ein Projekt auf Dokumentebene erstellen, werden das Dokument und der zugehörigen Anwendung innerhalb von Visual Studio gehostet, damit Sie entwerfen und direkt mit dem Dokument arbeiten. Wenn Sie über eine Microsoft Office öffnen Sie die Anwendung in Visual Studio verfügen, werden im Allgemeinen erwartungsgemäß funktioniert. Einige der Funktionen der Anwendung ist jedoch unterschiedliche oder kann nicht zugegriffen werden.  
  
 [!INCLUDE[appliesto_alldoc](../vsto/includes/appliesto-alldoc-md.md)]  
  
## <a name="document-protection"></a>Dokumentschutz  
 Microsoft Office Word und Microsoft Office Excel bieten Protection-Funktionen, die Sie in Ihren Projekten verwenden können. Jedoch wenn Dokumentschutz aktiviert ist, während das Dokument im Visual Studio geöffnet ist, können Sie verhindern einige Designänderungen vornehmen. Weitere Informationen finden Sie unter [Dokumentschutz in Projektmappen auf Dokumentebene](../vsto/document-protection-in-document-level-solutions.md).  
  
## <a name="information-rights-management"></a>Information Rights Management  
 Information Rights Management (IRM) ist in Microsoft Office Word und Microsoft Office Excel verfügbar. IRM können Sie verhindern, dass nicht autorisierte Benutzer nicht anzeigen oder ändern vertraulichen Informationen. Allerdings kann IRM auch Code Ausführung verhindert. Weitere Informationen finden Sie unter [Information Rights Management und Erweiterungen – Übersicht für verwalteten Code](../vsto/information-rights-management-and-managed-code-extensions-overview.md).  
  
## <a name="password-protection"></a>Kennwortschutz  
 Microsoft Office Word-Dokumenten und Microsoft Office Excel-Arbeitsmappen können festgelegt werden, damit sie von einem Benutzer geöffnet werden können, die nicht das Kennwort kennt. Kennwortschutz in Word und Excel anders behandelt, und den Entwicklungsprozess beeinflussen kann. Weitere Informationen finden Sie unter [Kennwortschutz für Office-Dokumente](../vsto/password-protection-on-office-documents.md).  
  
## <a name="see-also"></a>Siehe auch  
 [Dokumentschutz in Projektmappen auf Dokumentebene](../vsto/document-protection-in-document-level-solutions.md)   
 [Information Rights Management und Erweiterungen – Übersicht von verwaltetem Code](../vsto/information-rights-management-and-managed-code-extensions-overview.md)   
 [Kennwortschutz für Office-Dokumente](../vsto/password-protection-on-office-documents.md)   
 [Vorgehensweise: Öffnen von Office-Projektmappen ohne die Ausführung von Code](../vsto/how-to-open-office-solutions-without-running-code.md)  
  
  
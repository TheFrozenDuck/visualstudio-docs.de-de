---
title: "Anpassen von Features der Benutzeroberfl&#228;che mithilfe von Erweiterungsschnittstellen"
ms.custom: ""
ms.date: "02/02/2017"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "office-development"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "VB"
  - "CSharp"
helpviewer_keywords: 
  - "IcustomTaskPaneConsumer-Schnittstelle"
  - "IribbonExtensibility-Schnittstelle"
  - "Anpassen der Benutzeroberfläche [Office-Entwicklung in Visual Studio]"
  - "Benutzeroberflächen [Office-Entwicklung in Visual Studio], Anpassen"
  - "Add-Ins auf Anwendungsebene [Office-Entwicklung in Visual Studio], Erweiterungsschnittstellen"
  - "Anpassen von Funktionen der Benutzeroberfläche [Office-Entwicklung in Visual Studio]"
  - "FormRegionStartup-Schnittstelle"
  - "Add-Ins [Office-Entwicklung in Visual Studio], Erweiterungsschnittstellen"
  - "Erweiterungsschnittstellen [Office-Entwicklung in Visual Studio]"
ms.assetid: 3f3f7908-9404-4eda-8899-4d18c75e3b4a
caps.latest.revision: 40
author: "kempb"
ms.author: "kempb"
manager: "ghogen"
caps.handback.revision: 39
---
# Anpassen von Features der Benutzeroberfl&#228;che mithilfe von Erweiterungsschnittstellen
  Die Office\-Entwicklungstools in Visual Studio umfassen Klassen und Designer, mit denen viele Implementierungsdetails behandelt werden können, wenn Sie sie zum Erstellen von benutzerdefinierten Aufgabenbereichen, Menübandanpassungen und Outlook\-Formularbereichen in einem VSTO\-Add\-In verwenden. Sie können jedoch zudem die *Erweiterbarkeitsschnittstelle* manuell für jede Funktion implementieren, wenn Sie über besondere Anforderungen verfügen.  
  
 [!INCLUDE[appliesto_allapp](../vsto/includes/appliesto-allapp-md.md)]  
  
## Übersicht der Erweiterbarkeitsschnittstellen  
 Microsoft Office definiert eine Gruppe von Erweiterbarkeitsschnittstellen, die COM\-VSTO\-Add\-Ins implementieren können, um bestimmte Funktionen wie das Menüband anzupassen. Diese Schnittstellen bieten die vollständige Kontrolle über die Funktionen, auf die sie den Zugriff gewähren. Die Implementierung dieser Schnittstellen erfordert jedoch das entsprechende Know\-how in Bezug auf die COM\-Interoperabilität in verwalteten Code. In einigen Fällen ist das Programmierungsmodell von diesen Schnittstellen auch nicht intuitiv für Entwickler, die an .NET Framework gewöhnt sind.  
  
 Wenn Sie ein VSTO\-Add\-In erstellen, indem Sie die Office\-Projektvorlagen in Visual Studio verwenden, müssen Sie nicht die Erweiterbarkeitsschnittstellen implementieren, um Funktionen wie das Menüband anzupassen. Die [!INCLUDE[vsto_runtime](../vsto/includes/vsto-runtime-md.md)] implementiert diese Schnittstellen für Sie. Sie können stattdessen intuitivere Klassen und Designer verwenden, die Visual Studio bereitstellt. Sie können die Erweiterbarkeitsschnittstellen bei Bedarf jedoch direkt in Ihr VSTO\-Add\-In implementieren.  
  
 Weitere Informationen über die Klassen und Designer, die Visual Studio für diese Funktionen bereitstellt, finden Sie unter [Benutzerdefinierte Aufgabenbereiche](../vsto/custom-task-panes.md), [Multifunktionsleisten-Designer](../vsto/ribbon-designer.md) und [Erstellen von Outlook-Formularbereichen](../vsto/creating-outlook-form-regions.md).  
  
## In einem VSTO\-Add\-In implementierbare Erweiterbarkeitsschnittstellen  
 Die folgende Tabelle führt die Erweiterbarkeitsschnittstellen auf, die Sie implementieren können, sowie die Anwendungen, die sie unterstützen.  
  
|Interface|Beschreibung|Anwendungen|  
|---------------|------------------|-----------------|  
|<xref:Microsoft.Office.Core.IRibbonExtensibility>|Implementieren Sie diese Schnittstelle zum Anpassen der Menüband\-Benutzeroberfläche. **Note:**  Sie können einem Projekt ein **Menübandelement \(XML\)** hinzufügen, um eine standardmäßige <xref:Microsoft.Office.Core.IRibbonExtensibility>\-Implementierung in Ihrem VSTO\-Add\-In zu generieren. Weitere Informationen finden Sie unter [Multifunktionsleisten-XML](../vsto/ribbon-xml.md).|Excel<br /><br /> [!INCLUDE[InfoPath_15_short](../vsto/includes/infopath-15-short-md.md)]<br /><br /> InfoPath 2010<br /><br /> Outlook<br /><br /> PowerPoint<br /><br /> Projekt<br /><br /> Visio<br /><br /> Word|  
|<xref:Microsoft.Office.Core.ICustomTaskPaneConsumer>|Implementieren Sie diese Schnittstelle zum Erstellen eines benutzerdefinieren Aufgabenbereichs.|Excel<br /><br /> Outlook<br /><br /> PowerPoint<br /><br /> Word|  
|<xref:Microsoft.Office.Interop.Outlook.FormRegionStartup>|Implementieren Sie diese Schnittstelle zum Erstellen eines Outlook\-Formularbereichs.|Outlook|  
  
 Es gibt verschiedene andere Erweiterbarkeitsschnittstellen, die durch Microsoft Office definiert werden, beispielsweise <xref:Microsoft.Office.Core.IBlogExtensibility>, <xref:Microsoft.Office.Core.EncryptionProvider> und <xref:Microsoft.Office.Core.SignatureProvider>. Visual Studio unterstützt nicht die Implementierung dieser Schnittstellen in einem VSTO\-Add\-In, das mithilfe der Office\-Projektvorlagen erstellt wurde.  
  
## Verwenden von Erweiterbarkeitsschnittstellen  
 Implementieren Sie zum Anpassen einer Benutzeroberflächenfunktion mithilfe einer Erweiterbarkeitsschnittstelle die entsprechende Schnittstelle in Ihrem VSTO\-Add\-In\-Projekt. Überschreiben Sie anschließend die Methode <xref:Microsoft.Office.Tools.AddInBase.RequestService%2A>, um eine Instanz der Klasse zurückzugeben, die die Schnittstelle implementiert.  
  
 Eine Beispielanwendung, die die Art und Weise der Implementierung der <xref:Microsoft.Office.Core.IRibbonExtensibility>\-, <xref:Microsoft.Office.Core.ICustomTaskPaneConsumer>\- und <xref:Microsoft.Office.Interop.Outlook.FormRegionStartup>\-Schnittstellen in einem VSTO\-Add\-In für Outlook veranschaulicht finden Sie unter „UI\-Manager – Beispiel“ in [Office-Entwicklungsbeispiele](../vsto/office-development-samples.md).  
  
### Beispiel der Implementierung einer Erweiterbarkeitsschnittstelle  
 Das folgende Codebeispiel veranschaulicht eine einfache Implementierung der <xref:Microsoft.Office.Core.ICustomTaskPaneConsumer>\-Schnittstelle zum Erstellen eines benutzerdefinierten Aufgabenbereichs. Im Beispiel werden zwei Klassen definiert:  
  
-   Die `TaskPaneHelper`\-Klasse implementiert <xref:Microsoft.Office.Core.ICustomTaskPaneConsumer> zum Erstellen und Anzeigen eines benutzerdefinierten Aufgabenbereichs.  
  
-   Die `TaskPaneUI`\-Klasse stellt die Benutzeroberfläche des Aufgabenbereichs bereit. Die Attribute für die `TaskPaneUI`\-Klasse machen die Klasse sichtbar für COM, wodurch Microsoft Office\-Anwendungen die Klasse erkennen können. In diesem Beispiel ist die Benutzeroberfläche ein leeres <xref:System.Windows.Forms.UserControl>. Sie können jedoch Steuerelemente hinzufügen, indem Sie den Code ändern.  
  
    > [!NOTE]  
    >  Damit die `TaskPaneUI`\-Klasse für COM verfügbar ist, müssen Sie zudem die Eigenschaft **Für COM\-Interop registrieren** für das Projekt festlegen.  
  
 [!code-csharp[Trin_SimpleExtensibilityInterface#1](../snippets/csharp/VS_Snippets_OfficeSP/Trin_SimpleExtensibilityInterface/CS/ThisAddIn.cs#1)]
 [!code-vb[Trin_SimpleExtensibilityInterface#1](../snippets/visualbasic/VS_Snippets_OfficeSP/Trin_SimpleExtensibilityInterface/VB/ThisAddIn.vb#1)]  
  
 Weitere Informationen über die Implementierung von <xref:Microsoft.Office.Core.ICustomTaskPaneConsumer> finden Sie unter [Erstellen von benutzerdefinierten Aufgabenbereichen in Office \(2007\)](http://msdn.microsoft.com/de-de/256313db-18cc-496c-a961-381ed9ca94be) in der Microsoft Office\-Dokumentation.  
  
### Beispiel der Überschreibung der Methode "RequestService"  
 Das folgende Codebeispiel veranschaulicht, wie die Methode <xref:Microsoft.Office.Tools.AddInBase.RequestService%2A> überschrieben wird, um eine Instanz der Klasse `TaskPaneHelper` aus dem vorherigen Codebeispiel zurückzugeben. Es prüft die Werte des Parameters *serviceGuid*, um zu bestimmen, welche Schnittstelle angefordert wird, und gibt dann ein Objekt zurück, das diese Schnittstelle implementiert.  
  
 [!code-csharp[Trin_SimpleExtensibilityInterface#2](../snippets/csharp/VS_Snippets_OfficeSP/Trin_SimpleExtensibilityInterface/CS/ThisAddIn.cs#2)]
 [!code-vb[Trin_SimpleExtensibilityInterface#2](../snippets/visualbasic/VS_Snippets_OfficeSP/Trin_SimpleExtensibilityInterface/VB/ThisAddIn.vb#2)]  
  
## Siehe auch  
 [Beispiele und exemplarische Vorgehensweisen für die Programmierung mit Office](../vsto/office-development-samples-and-walkthroughs.md)   
 [Programmieren von VSTO-Add-Ins](../vsto/programming-vsto-add-ins.md)   
 [Entwickeln von Office-Projektmappen](../vsto/developing-office-solutions.md)   
 [Aufrufen von Code in VSTO-Add-Ins aus anderen Office-Projektmappen](../vsto/calling-code-in-vsto-add-ins-from-other-office-solutions.md)   
 [Gewusst wie: Erstellen von Office-Projekten in Visual Studio](../vsto/how-to-create-office-projects-in-visual-studio.md)   
 [Architektur von VSTO-Add-Ins](../vsto/architecture-of-vsto-add-ins.md)  
  
  
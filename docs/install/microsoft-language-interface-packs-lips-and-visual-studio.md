---
title: "Microsoft Language Interface Packs (LIPs) und Visual Studio | Microsoft Docs"
ms.custom: ""
ms.date: "12/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-install"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "Sprachumstellung [Visual Studio]"
  - "Sprachen, Unterstützung mehrerer Sprachen"
  - "MUI [Visual Studio]"
  - "Mehrsprachige Benutzeroberfläche [Visual Studio]"
  - "Unterstützung mehrerer Sprachen [Visual Studio SDK]"
  - "Text [Visual Studio], Mehrere Sprachen"
  - "Sprache des Benutzeroberflächentexts [Visual Studio]"
  - "Windows Multilingual User Interface"
ms.assetid: dc86304b-65b7-47e6-9314-1dfd02ecfa65
caps.latest.revision: 28
caps.handback.revision: 28
author: "TerryGLee"
ms.author: "tglee"
manager: "ghogen"
---
# Microsoft Language Interface Packs (LIPs) und Visual Studio
[!INCLUDE[vs2017banner](../code-quality/includes/vs2017banner.md)]

Mit dem Windows Multilingual User Interface Packs \(LIP\) können Sie eine Sprachversion von Windows und anschließend verschiedene Sprachpakete für die Benutzeroberfläche installieren.  Sprachpakete für die Benutzeroberfläche stellen eine lokalisierte Benutzeroberfläche für das Betriebssystem bereit.  Beispielsweise können Sie ein japanisches Sprachpaket für die Benutzeroberfläche über einer englischsprachigen Windows\-Version installieren und dann zwischen den Windows\-Benutzeroberflächensprachen Japanisch und Englisch umschalten.  Mit LIP können Sie mehrere Sprachversionen von Windows auf einem Computer installieren.  
  
 Auf Computern mit installierten LIPs und mehreren Sprachversionen von Visual Studio werden durch Änderungen der Einstellungen für die Windows\-Anzeigesprache sowohl Windows\- als auch Visual Studio\-Einstellungen festgelegt, wenn entsprechende Sprachpakete installiert sind.  
  
## Einschränkungen von mehrsprachigen Installationen  
 Wenn Sie verschiedene Sprachversionen von Visual Studio auf demselben Computer installieren, können Sie nur zwischen Sprachen entsprechender Editionen umschalten.  Wenn beispielsweise eine englische Express Edition, eine deutsche Express Edition und eine Professional Edition installiert sind, können Sie nur zwischen den Sprachen der Express Editions, nicht aber die der Professional Edition umschalten.  
  
 Visual Studio verwendet ein einheitliches Sprachpaket.  Um mehr als eine Sprachversion dieser Produkte zu installieren, müssen Sie das vollständige Sprachenprodukt zuerst installieren und dann ein oder mehrere Sprachpakete einrichten.  
  
> [!NOTE]
>  Visual Studio unterstützt nicht die Installation mehrerer Sprachversionen des vollständigen Sprachenprodukts auf demselben Computer.  Wenn Sie ein vollständiges Sprachenprodukt installiert haben, müssen Sie die Sprachversionen mithilfe von Sprachpaketen hinzufügen.  Sie können immer noch mehrere vollständige Sprachenprodukte der Express\-Editionen auf demselben Computer installieren.  
  
### Unterstützung für Codepages  
 In einigen Visual Studio\-Tools wird Text nicht korrekt angezeigt, wenn er Zeichen enthält, die nicht in der aktuellen Codepage verfügbar sind.  Stattdessen werden Fragezeichen oder fehlerhafter Text angezeigt.  Die folgenden Tools oder Bereiche sind betroffen:  
  
-   Über FTP bereitgestellte Websites  
  
-   Computernamen mit Nicht\-ASCII\-Zeichen in einigen Steuerelementen.  
  
-   Außerhalb von Visual Studio ausgeführte Befehlszeilentools  
  
-   Visual Basic\-Assistent für die Migration  
  
-   Testcontainer für ActiveX\-Steuerelemente  
  
-   OLE\/COM\-Objektkatalog  
  
-   ISAPI\-Webdebugtool  
  
-   MFC\-Anwendungsprojekte mit HTML\-Hilfeinhalt  
  
-   Die Visual SourceSafe\/SCCI\-Benutzeroberfläche schaltet bei einer nicht kompatiblen Codepage automatisch auf Englisch zurück.  
  
-   Visual SourceSafe unterstützt keine Unicode\-Dateinamen.  
  
-   Vom Endbenutzer definierte Zeichen \(private gebrauchte Zone\) können nicht als Token\/Bezeichner verwendet werden.  
  
-   Erweiterte Lateinisch\-B\-Zeichen können in einigen Visual Studio\-Toolfenstern nicht angezeigt werden, wenn die Windows\-Codepage auf eine ostasiatische Sprache festgelegt ist.  
  
-   Bei Lauftexten, die aus Zeichen von mehreren Sprachskripts bestehen, wird möglicherweise das standardmäßige Symbol für einige Zeichen angezeigt.  
  
-   Das Kopieren und Einfügen von komplexen Skriptzeichenfolgen in allgemeine Steuerelemente bewirkt möglicherweise, dass die Zeichenstrukturierung verloren geht.  Geben Sie Text stattdessen über die entsprechende Sprachtastatur ein.  
  
##### So zeigen Sie nicht in der aktuellen Codepage enthaltene Zeichen ordnungsgemäß an  
  
1.  Klicken Sie auf **Start** und dann auf **Systemsteuerung**. Rufen Sie die **Regions\- und Sprachoptionen** \(oder **Region** in[!INCLUDE[win8](../debugger/includes/win8_md.md)]\) auf.  
  
    > [!NOTE]
    >  Sie müssen auf dem Computer als Administrator angemeldet sein, um die folgenden Schritte auszuführen.  
  
2.  Klicken Sie auf die Registerkarte **Erweitert**.  
  
3.  Wählen Sie in der Liste **Wählen Sie die Sprachversion der Programme aus, die Unicode nicht unterstützen** die aktuell verwendete Sprache aus.  
  
4.  Klicken Sie auf **OK**.  
  
## Ändern der in Visual Studio für den Benutzeroberflächen\-Text verwendeten Sprache  
 Wenn Sie mehrere Sprachversionen von [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] auf demselben Computer installieren, wird die [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)]\-Benutzeroberfläche standardmäßig auf **Wie Microsoft Windows** gesetzt.  Diese Einstellung gibt an, dass [!INCLUDE[vsprvs](../code-quality/includes/vsprvs_md.md)] den Text für die Benutzeroberfläche in der als Anzeigesprache für das Betriebssystem angegebenen Sprache anzeigt.  
  
> [!NOTE]
>  Wenn Visual Studio auf die Verwendung von **Wie Microsoft Windows** festgelegt ist und das entsprechende Visual Studio\-Sprachpaket nicht installiert ist, verwendet Visual Studio die Sprache der ersten Visual Studio\-Installation.  
  
#### So legen Sie die in Visual Studio für den Benutzeroberflächentext verwendete Sprache fest  
  
1.  Klicken Sie im Menü **Extras** auf **Optionen**.  
  
2.  Erweitern Sie im Dialogfeld **Optionen** die Option **Umgebung**, und klicken Sie dann auf **Internationale Einstellungen**.  
  
3.  Wählen Sie in der Liste **Sprache** die Sprache aus, in der der Benutzeroberflächentext in der Entwicklungsumgebung angezeigt werden soll.  
  
     Damit der Text für die Benutzeroberfläche in der IDE mit der Einstellung für die Anzeigesprache des Betriebssystems übereinstimmt, wählen Sie **Wie Microsoft Windows** aus.  
  
 Sie können auch den devenv\-Befehl verwenden, um die Sprache festzulegen, die für Benutzeroberfläche verwendet wird.  Weitere Informationen finden Sie unter [\/LCID](../ide/reference/lcid-devenv-exe.md).  
  
## Siehe auch  
 [Internationale Einstellungen, Umgebung, Dialogfeld "Optionen"](../ide/reference/international-settings-environment-options-dialog-box.md)
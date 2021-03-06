---
title: 'Schnellstart: Erstellen einer ersten Konsolenanwendung in Visual Studio mit Visual Basic | Microsoft-Dokumentation'
ms.custom: 
ms.date: 12/10/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-acquisition
ms.tgt_pltfrm: 
ms.topic: quickstart
ms.devlang: vb
author: TerryGLee
ms.author: tglee
manager: ghogen
dev_langs: vb
ms.workload: multiple
ms.openlocfilehash: 2573e1a2344b858b721fb234d6b228b421a36550
ms.sourcegitcommit: 9357209350167e1eb7e50b483e44893735d90589
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2018
---
# <a name="quickstart-create-your-first-console-app-in-visual-studio-with-visual-basic"></a>Schnellstart: Erstellen einer ersten Konsolenanwendung in Visual Studio mit Visual Basic
Mithilfe dieser Einführung in die integrierte Entwicklungsumgebung (IDE) von Visual Studio, die fünf bis zehn Minuten Ihrer Zeit in Anspruch nehmen wird, können Sie eine einfache Visual Basic-Anwendung erstellen, die in der Konsole ausgeführt werden kann.

Wenn Sie Visual Studio noch nicht installiert haben, können Sie es auf der Seite [Visual Studio-Downloads](https://aka.ms/vsdownload?utm_source=mscom&utm_campaign=msdocs) kostenlos herunterladen.

## <a name="create-a-project"></a>Erstellen eines Projekts
Erstellen Sie zunächst ein Visual Basic-Anwendungsprojekt. Der Projekttyp enthält, schon bevor Sie mit der Bearbeitung beginnen, alle Vorlagendateien, die Sie benötigen.

1. Öffnen Sie Visual Studio 2017.

2. Klicken Sie in der Menüleiste im oberen Bereich auf **Datei** > **Neu** > **Projekt...**.

3. Erweitern Sie im Dialogfeld **Neues Projekt** links den Eintrag **Visual Basic**, und klicken Sie auf **.NET Core**. Wählen Sie im mittleren Bereich die Option **Konsolenanwendung (.NET Core)** aus. Nennen Sie dann das Projekt *HalloWelt*.

   ![Projektvorlage „Console App (.NET Core)“ im Dialogfeld „Neues Projekt“ in der Visual Studio-IDE](../ide/media/new-project-vb-dotnetcore-helloworld-console-app.png)

     Falls Sie die Projektvorlage **Konsolenanwendung (.NET Core)** nicht finden, klicken Sie auf den Link **Visual Studio-Installer öffnen** auf der linken Seite des Dialogfelds **Neues Projekt**.

   ![Klicken Sie auf den Link „Visual Studio-Installer öffnen“ im Dialogfeld „Neues Projekt“](../ide/media/vb-open-visual-studio-installer-hello-world.png)

     Der Visual Studio-Installer wird gestartet. Wählen Sie die Workload **Plattformübergreifende .NET Core-Entwicklung** aus, und klicken Sie dann auf **Anpassen**.

     ![Workload „Plattformübergreifende .NET Core-Entwicklung“ im Visual Studio-Installer](../ide/media/dot-net-core-xplat-dev-workload.png)

## <a name="create-the-application"></a>Erstellen der Anwendung
Nachdem Sie Ihre Visual Basic-Projektvorlage ausgewählt haben und Ihr Projekt benannt haben, erstellt Visual Studio eine einfache „Hallo Welt“-Anwendung für Sie. Sie ruft die <xref:System.Console.WriteLine%2A>-Methode auf, um die literale Zeichenfolge „Hello World!“ im Konsolenfenster anzuzeigen.

![Sehen Sie sich den Standardcode für „Hallo Welt“ in der Vorlage an](../ide/media/vb-console-helloworld-template.png)

Sie können das Programm im Debugmodus ausführen, indem Sie in der IDE auf die Schaltfläche **Hallo Welt** klicken.

  ![Klicken Sie auf die Schaltfläche „Hallo Welt“, um das Programm im Debugmodus auszuführen](../ide/media/vb-console-hello-world-button.png)

Wenn Sie dies tun, öffnet sich das Konsolenfenster nur für einen kurzen Moment, bevor es wieder geschlossen wird. Der Grund dafür ist, dass die Methode `Main` beendet wird, nachdem ihre einzige Anweisung ausgeführt wird, also wird die Anwendung geschlossen.

### <a name="add-some-code"></a>Hinzufügen von Code
Fügen Sie Code hinzu, um die Anwendung zu pausieren und den Benutzer zur Eingabe aufzufordern.

1. Fügen Sie direkt nach dem Aufruf der <xref:System.Console.WriteLine%2A>-Methode folgenden Code ein:

   ```vb
   Console.Write("Press any key to continue...")
   Console.ReadKey(true)
   ```
   Durch diesen Code wird das Programm pausiert, bis eine Taste gedrückt wird.

2. Wählen Sie auf der Menüleiste **Erstellen** > **Projektmappe erstellen** aus.

   Dies kompiliert Ihr Programm in eine Zwischensprache (IL), die dann von einem JIT-Compiler (Just in Time) in Binärcode konvertiert wird.

## <a name="run-the-application"></a>Ausführen der Anwendung
1. Klicken Sie auf der Symbolleiste auf die Schaltfläche **HalloWelt**.

   ![Klicken Sie die Schaltfläche „HalloWelt“, um das Programm von der Symbolleiste aus auszuführen](../ide/media/vb-console-hello-world-button.png)

2. Drücken Sie eine beliebige Taste, um das Konsolenfenster zu schließen.

   ![Konsolenfenster mit „Hallo Welt“ und „Drücken Sie eine beliebige Taste um fortzufahren“](../ide/media/vb-console-hello-world-press-any-key.png)

Damit haben Sie den Schnellstart erfolgreich abgeschlossen. Wir hoffen, dass Sie etwas über Visual Basic und die Visual Studio-IDE gelernt haben. Wenn Sie mehr über diese Themen erfahren möchten, können Sie gerne mit einem Tutorial fortfahren, das Sie im Inhaltsverzeichnis im Abschnitt **Tutorials** finden.

## <a name="see-also"></a>Siehe auch
* [Schnellstart: Erstellen einer Windows Forms-App in Visual Studio mit Visual Basic](quickstart-visual-basic-winforms.md)
* [Tutorial: Erste Schritte mit Visual Basic in Visual Studio](tutorial-visual-basic-console.md)
* [IntelliSense für Visual Basic-Codedateien](visual-basic-specific-intellisense.md)

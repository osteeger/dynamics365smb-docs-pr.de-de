---
title: "Vorgehensweise: Planen der Ausführung eines Berichts | Microsoft Docs"
description: "Geplante Aufgaben sind von der Aufgabenwarteschlange verwaltet. Diese Projektausführungsberichte und Codeunits. Die Projekte können entweder einmalig oder wiederholt ausgeführt werden."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 05d2941d5124f333602cb2f73103389601ff3e85
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="use-job-queues-to-schedule-tasks"></a><span data-ttu-id="2f3d1-105">Verwenden von Aufgabenwarteschlangen für die Aufgabenplanung</span><span class="sxs-lookup"><span data-stu-id="2f3d1-105">Use Job Queues to Schedule Tasks</span></span>
<span data-ttu-id="2f3d1-106">Die Aufgabenwarteschlangen in [!INCLUDE[d365fin](includes/d365fin_md.md)] ermöglichen es Benutzern, bestimmte Berichte und Codeunits zu planen und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-106">Job queues in [!INCLUDE[d365fin](includes/d365fin_md.md)] enables users to schedule and run specific reports and codeunits.</span></span> <span data-ttu-id="2f3d1-107">Die Projekte können entweder einmalig oder wiederholt ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-107">You can set jobs to run one time, or on a recurring basis.</span></span> <span data-ttu-id="2f3d1-108">So kann es beispielsweise empfehlenswert sein, den Bericht **Verkäufer - Verkäuferstatistik** wöchentlich auszuführen, um jede Woche die Verkaufserfolge eines Verkäufers im Auge zu haben, während die Codenit  **Service-E-Mail-Warteschlange** verarbeiten" täglich ausgeführt wird, um sicherzustellen, dass ausstehende, serviceauftragsbezogene E-Mails rechtzeitig an die entsprechenden Debitoren versendet werden.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-108">For example, you might want to run the **Salesperson - Sales Statistics** report weekly, to track sales by salesperson each week, or you might want to run the **Process Service E-mail Queue** codeunit daily, to make sure pending email messages to customers regarding their service orders are sent out in a timely manner.</span></span>  

## <a name="add-jobs-to-the-job-queue"></a><span data-ttu-id="2f3d1-109">Fügen Sie Projekte der Aufgabenwarteschlange hinzu</span><span class="sxs-lookup"><span data-stu-id="2f3d1-109">Add Jobs to the Job Queue</span></span>
<span data-ttu-id="2f3d1-110">Im Fenster **Projektwarteschlangeneinträge** sind alle aktuellen Aufgabenwarteschlangenposten aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-110">The **Job Queue Entries** window lists all existing jobs.</span></span> <span data-ttu-id="2f3d1-111">Wenn Sie eine neue Projektwarteschlange hinzufügen, die Sie planen möchten, müssen Sie die Informationen über die Art des Objekts, das Sie ausführen möchten, angeben, wie der Name und die Objekt-ID, die Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-111">If you add a new job queue entry that you want to schedule, you must specify information about the type of object you want to run, such as a report or codeunit, and the name and object ID of the object that you want to run.</span></span> <span data-ttu-id="2f3d1-112">Sie können auch Parameter hinzufügen, um das Verhalten eines Aufgabenwarteschlangenpostens festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-112">You can also add parameters to specify the behavior of the job queue entry.</span></span> <span data-ttu-id="2f3d1-113">So können Sie beispielsweise einen Parameter hinzufügen, um nur gebuchte Verkaufsaufträge zu senden.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-113">For example, you can add a parameter to only send posted sales orders.</span></span> <span data-ttu-id="2f3d1-114">Sie benötigen die entsprechende Berechtigung zum Ausführen des jeweiligen Berichts oder der jeweiligen Codeunit, da ansonsten beim Ausführen der Projektwarteschlange ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-114">You must have permission to run the particular report or codeunit, or an error will be returned when the job queue is run.</span></span>  

<span data-ttu-id="2f3d1-115">Optional im Feld **Kategorienfilter für Aufgabenwarteschlange** Feld, Sie wählen einen Filter, der gelten soll.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-115">Optionally, you can set a filter in the **Job Queue Category Filter** field.</span></span> <span data-ttu-id="2f3d1-116">Aufgabenwarteschlangenkategorien können verwendet werden, um Projekte in der Liste zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-116">Job queue categories can be used to group jobs in the list.</span></span>

[!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="2f3d1-117"> automatisch aktiviert die Projekte entsprechend den angegebenen Plänen für jeden Aufgabenwarteschlangenposten.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-117"> automatically runs the jobs according to the specified schedules for each job queue entry.</span></span> <span data-ttu-id="2f3d1-118">Sie können einen Projektwarteschlangenposten auch manuell beginnen, beenden und aktivieren.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-118">You can also start, stop, and put a job queue entry on hold manually.</span></span>

### <a name="log-files"></a><span data-ttu-id="2f3d1-119">Transaktionsprotokoll</span><span class="sxs-lookup"><span data-stu-id="2f3d1-119">Log Files</span></span>
<span data-ttu-id="2f3d1-120">Die Fehler werden im Fenster **Aufgabenwarteschlangen-Protokolleinträge** aufgeführt, das Sie im Menüband zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-120">Errors are listed in the **Job Queue Log Entries** window that you can access from the ribbon.</span></span> <span data-ttu-id="2f3d1-121">Sie können auch Aufgabenwarteschlangenfehler beheben.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-121">You can also troubleshoot job queue errors.</span></span> <span data-ttu-id="2f3d1-122">Die Daten, die beim Ausführen einer Aufgabenwarteschlange generiert werden, werden an der Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-122">Data that is generated when a job queue is run is stored in the database.</span></span>  

### <a name="background-posting-with-job-queues"></a><span data-ttu-id="2f3d1-123">Buchen im Hintergrund mit Aufgabenwarteschlangen</span><span class="sxs-lookup"><span data-stu-id="2f3d1-123">Background Posting with Job Queues</span></span>
<span data-ttu-id="2f3d1-124">Aufgabenwarteschlangen sind ein effektives Werkzeug, um die Ausführung von Geschäftsprozessen im Hintergrund zu planen.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-124">Job queues are an effective tool to schedule the running of business processes in the background.</span></span> <span data-ttu-id="2f3d1-125">Ein Beispiel hierfür ist eine Instanz, in der mehrere Benutzer versuchen, Verkaufsaufträge gleichzeitig zu buchen, aber nur ein Auftrag gleichzeitig verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-125">For example, there may be an instance in which multiple users are trying to post sales orders at the same time, but only one order can be processed at a time.</span></span> <span data-ttu-id="2f3d1-126">Indem Sie eine Buchungsroutine im Hintergrund erstellen, können Sie die Buchungen in eine Warteschlange zur Bearbeitung im Hintergrund einreihen.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-126">By setting up a background posting routine, you can place the postings in a queue for processing in the background.</span></span>  

 <span data-ttu-id="2f3d1-127">Alternativ können Sie Buchungen zu bestimmten Betriebszeiten planen, wenn es für Ihre Organisation hilfreich ist.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-127">Alternatively, you may want to schedule postings for hours when it is convenient for your organization.</span></span> <span data-ttu-id="2f3d1-128">Beispielsweise kann es in Ihrem Unternehmen sinnvoll sein, bestimmte Routinen dann auszuführen, wenn ein Großteil der Dateneingaben für einen Arbeitstag abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-128">For example, it may make sense in your business to run certain routines when most of the data entry for the day has concluded.</span></span> <span data-ttu-id="2f3d1-129">Sie können dieses erreichen, indem Sie die oben Aufgabenwarteschlange auf Batch-Beitragsberichte des Ausführens verschiedene, wie **Aufträge stapelbuchen** **Verk. Rechnungen stapelbuchen** die **Verk.Gutschriften stapelbuchen** festlegen.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-129">You can achieve this by setting the job queue up to run various batch post reports, such as the **Batch Post Sales Orders**, **Batch Post Sales Invoices**, and **Batch Post Sales Credit Memos** reports.</span></span>  

 [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="2f3d1-130"> unterstützt die Hintergrundbuchung für die folgenden Belegarten:</span><span class="sxs-lookup"><span data-stu-id="2f3d1-130"> supports background posting for the following document types:</span></span>  

-   <span data-ttu-id="2f3d1-131">Vertrieb: Verkaufsauftrag, Verkaufsreklamation, Gutschrift, Rechnung</span><span class="sxs-lookup"><span data-stu-id="2f3d1-131">Sales: sales order, return order, credit memo, invoice</span></span>  

-   <span data-ttu-id="2f3d1-132">Einkauf: Bestellung, Verkaufsreklamation, Gutschrift, Rechnung</span><span class="sxs-lookup"><span data-stu-id="2f3d1-132">Purchases: purchase order, return order, credit memo, invoice</span></span>  

 <span data-ttu-id="2f3d1-133">Wenn die Aufgabenwarteschlange den Verkaufsauftrag nicht buchen kann, wird der Status auf **Fehler** geändert, und der Verkaufsauftrag wird der Liste von Verkaufsaufträgen hinzugefügt, die der Benutzer verarbeiten muss.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-133">If the job queue cannot post the sales order, the status is changed to **Error**, and the sales order is added to the list of sales orders that the user will have to handle.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2f3d1-134">Wenn Sie einen Beleg für die Buchung planen und den Buchungsvorgang starten, wird die Buchungsroutine automatisch das Timeout eines Aufgabenwarteschlangenpostens innerhalb von zwei Stunden konfigurieren, wenn die Buchungsroutine, aus beliebigen Grund aufhört zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-134">When you schedule a document for posting and the posting process begins, the posting routine is automatically configured to time out within two hours if the posting routine stops responding for any reason.</span></span>  

<span data-ttu-id="2f3d1-135">Sie richten diese mithilfe der Projektwarteschlange im Fenster **Debitoren & Verkauf Einr.** oder im Fenster **Kreditoren & Einkauf**, fest.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-135">You set up this use of the job queue in the **Sales & Receivables Setup** window or the **Purchases & Payables** window, respectively.</span></span> <span data-ttu-id="2f3d1-136">Im Inforegister **Hintergrundbuchung** wählen Sie das Kontrollkästchen **Beitrags-Belege über Aufgabenwarteschlange** und füllen Sie die entsprechenden Informationen ein.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-136">On the **Background Posting** FastTab, you choose the **Post Documents via Job Queue** check box and then fill in the relevant information.</span></span> <span data-ttu-id="2f3d1-137">Hier können Sie das Feld **Aufgabenwarteschlange - Kategoriencode** verwenden, um die Aufgabenwarteschlangenposten mit diesem Code auszuführen.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-137">Here you can also use the **Job Queue Category Code** field to run all job queue entries with that code.</span></span> <span data-ttu-id="2f3d1-138">Wenn Sie diese Kategorie auswählen, können Sie die **Verkauf buchen** Kategorie nutzen, die alle Aufträge filtert, die mit einer Projektwarteschlange übereinstimmen, die denselben Kategoriencode hat.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-138">For example, you can use  a **SalesPost** category that filters to all sales orders that match any job queue that has the same category code.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="2f3d1-139">Wenn Sie einen Beleg an einen Drucker senden und der Drucker ein Dialogfeld anzeigt, wie eine Anforderung für Anmeldeinformationen oder eine Warnung über geringe Druckertinte, wird der Beleg gebucht, aber nicht gedruckt.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-139">If you set up a job that will post and print documents, and the printer displays a dialog box, such as a request for credentials or a warning about low printer ink, your document is posted but not printed.</span></span> <span data-ttu-id="2f3d1-140">Die entsprechenden Aufgabenwarteschlangenposten überschreiten letztendlich die Zeit und das Feld **Status** ist auf **Fehler** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-140">The corresponding job queue entry eventually times out and the **Status** field is set to **Error**.</span></span> <span data-ttu-id="2f3d1-141">Entsprechend empfiehlt es sich, dass Sie kein Druckersetup verwenden, das Aktivität mit der Anzeige von Druckerdialogfeldern in Verbindung mit Hintergrundbuchung benötigt.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-141">Accordingly, we recommend that you do not use a printer setup that requires interaction with the display of printer dialog boxes in conjunction with background posting.</span></span>  

## <a name="use-the-my-job-queue-part"></a><span data-ttu-id="2f3d1-142">Nutzen Sie den Teil Meine Aufgabenwarteschange</span><span class="sxs-lookup"><span data-stu-id="2f3d1-142">Use the My Job Queue Part</span></span>
<span data-ttu-id="2f3d1-143">Der **Meine Aufgabenwarteschlange**-Teil zeigt die Aufgabenwarteschlangenposten an, die ein Benutzer gestartet hat, die jedoch noch nicht abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-143">The **My Job Queue** part shows the job queues entries that a user has started, but which are not yet finished.</span></span> <span data-ttu-id="2f3d1-144">Standardmäßig ist dieser Teil nicht sichtbar, Sie müssen ihn also Ihrem Rollencenter hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-144">By default, the part is not visible, so you have to add it to your Role Center.</span></span> <span data-ttu-id="2f3d1-145">Weitere Informationen finden Sie unter [Ändern von Grundeinstellungen](ui-change-basic-settings.md).</span><span class="sxs-lookup"><span data-stu-id="2f3d1-145">For more information, see [Changing Basic Settings](ui-change-basic-settings.md).</span></span>  

<span data-ttu-id="2f3d1-146">In diesem Teil können Sie die Dokumente einsehen, die verarbeitet oder in die Warteschlange eingereiht werden und für die Ihre ID im Feld **Zugewiesene Benutzer-ID** angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-146">In this part, you can see those documents that are being processed or that are queued for which your ID is specified in the **Assigned User ID** field.</span></span> <span data-ttu-id="2f3d1-147">Dieser Teil hilft Ihnen bei der Nachverfolgung aller Projektwarteschlangenposten, einschließlich derer, die sich auf die Hintergrundbuchung beziehen.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-147">The part helps you keep track of all job queue entries, including those related to background posting.</span></span> <span data-ttu-id="2f3d1-148">Dieser Teil informiert Sie auf einen Blick darüber, ob bei der Buchung eines Belegs ein Fehler aufgetreten ist, oder ob ein Projektwarteschlangenposten einen Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-148">The part can tell you at a glance whether there has been an error in the posting of a document or if there are errors in a job queue entry.</span></span> <span data-ttu-id="2f3d1-149">Mit diesem Teil können Sie auch eine Buchung stornieren, wenn diese nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-149">The part also lets you cancel a document posting if it is not running.</span></span>  

## <a name="security"></a><span data-ttu-id="2f3d1-150">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="2f3d1-150">Security</span></span>  
<span data-ttu-id="2f3d1-151">Aufgabenwarteschlangenposten werden auf Basis von Berechtigungen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-151">Job queue entries run based on permissions.</span></span> <span data-ttu-id="2f3d1-152">Diese Berechtigungen müssen die Ausführung des Berichts oder der Codeunit ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-152">Those permissions must allow the execution of the report or codeunit.</span></span>  

<span data-ttu-id="2f3d1-153">Wenn eine Aufgabenwarteschlange manuell aktiviert wird, wird sie mit den Anmeldeinformationen des Benutzers ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-153">When a job queue is activated manually, it is run with the credentials of the user.</span></span> <span data-ttu-id="2f3d1-154">Wenn eine Aufgabenwarteschlange über NAS aktiviert wird, wird sie mit den Anmeldeinformationen der Serverinstanz ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-154">When a job queue is activated as a scheduled task, it is run with the credentials of the server instance.</span></span> <span data-ttu-id="2f3d1-155">Wenn ein Projekt ausgeführt wird, wird es mit den Anmeldeinformationen der Aufgabenwarteschlange ausgeführt, mit der das Projekt aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-155">When a job is run, it is run with the credentials of the job queue that activates it.</span></span> <span data-ttu-id="2f3d1-156">Jedoch muss der Benutzer, der den Aufgabenwarteschlangenposten erstellt hat, auch über Berechtigungen verfügen.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-156">However, the user who created that job queue entry must also have permissions.</span></span> <span data-ttu-id="2f3d1-157">Wenn ein Projekt in einer Benutzersession ausgeführt wird (zum Beispiel bei der Hintergrundbuchung), wird es mit den Anmeldeinformationen des Benutzers ausgeführt, der dieses Projekt erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-157">When a job is “run in user session” (such as during background posting), it is run with the credentials of the user who created that job.</span></span>  

> [!IMPORTANT]  
>  <span data-ttu-id="2f3d1-158">Wenn Sie den SUPER-Zugriffsrechtsatz der Demolizenz für [!INCLUDE[d365fin](includes/d365fin_md.md)] verwenden, sind Sie und Ihre Benutzer zum Ausführen aller Objekte berechtigt.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-158">If you use the SUPER permissions set that comes with [!INCLUDE[d365fin](includes/d365fin_md.md)], you and your users have permissions to run all objects.</span></span> <span data-ttu-id="2f3d1-159">In diesem Fall ist der Zugriff für jeden Benutzer nur durch Berechtigungen für Daten beschränkt.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-159">In this case, access for each user is only limited by permissions for data.</span></span>  

## <a name="using-job-queues-effectively"></a><span data-ttu-id="2f3d1-160">Effektive Verwendung von Aufgabenwarteschlangen</span><span class="sxs-lookup"><span data-stu-id="2f3d1-160">Using Job Queues Effectively</span></span>  
<span data-ttu-id="2f3d1-161">Der Aufgabenwarteschlangenposten hat viele Felder, deren Zweck darin besteht, Parameter in die Codeunit zu übertragen, die Sie für die Ausführung mit einer Aufgabenwarteschlange festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-161">The job queue entry record has many fields whose purpose is to carry parameters into a codeunit that you have specified to be run with a job queue.</span></span> <span data-ttu-id="2f3d1-162">Dies bedeutet auch, dass Codeunits, die über die Aufgabenwarteschlange ausgeführt werden sollen, beim Warteschlangenposten als Parameter im **OnRun**-Trigger angegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-162">This also means that codeunits that are to be run via the job queue must be specified with the Job Queue Entry record as a parameter in the **OnRun** trigger.</span></span> <span data-ttu-id="2f3d1-163">Dies gewährleistet ein zusätzliches Maß an Sicherheit, da so Benutzer über die Aufgabenwarteschlange keine beliebigen Codeunits ausführen können.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-163">This helps provide an extra level of security, as this prevents users from running random codeunits via the job queue.</span></span> <span data-ttu-id="2f3d1-164">Wenn der Benutzer Parameter einem Bericht weiterleiten muss, besteht hierfür die einzige Möglichkeit darin, die Berichtsausführung in eine Codeunit einzubinden, die anschließend die Eingabeparameter analysiert und in den Bericht einfügt, bevor dieser ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2f3d1-164">If the user must pass parameters to a report, the only way to do this is by wrapping the report execution into a codeunit, which then parses the input parameters and enters them into the report before executing it.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2f3d1-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f3d1-165">See Also</span></span>  
[<span data-ttu-id="2f3d1-166">Einrichtung und Verwaltung in Business Central</span><span class="sxs-lookup"><span data-stu-id="2f3d1-166">Setup and Administration in Business Central</span></span>](admin-setup-and-administration.md)  
[<span data-ttu-id="2f3d1-167">Einrichten von Business Central</span><span class="sxs-lookup"><span data-stu-id="2f3d1-167">Setting Up Business Central</span></span>](setup.md)  

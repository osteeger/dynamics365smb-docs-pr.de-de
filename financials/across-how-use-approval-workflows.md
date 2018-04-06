---
title: Genehmigen und Ablehnen von Belegen im Arbeitsablauf | Microsoft Docs
description: Anfordern, ablehnen oder delegieren einer Genehmigung, beispielsweise einen Einkaufs- oder Verkaufsbeleg, als Teil eines Workflows.
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: reject, delegate, request
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 68f1af1ec5662e2c13b2695f8b1291734bf9450e
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="use-approval-workflows"></a><span data-ttu-id="7d3b1-103">Artikelgenehmigungsworkflow verwenden</span><span class="sxs-lookup"><span data-stu-id="7d3b1-103">Use Approval Workflows</span></span>
<span data-ttu-id="7d3b1-104">Wenn ein Datensatz, wie ein Einkaufsbeleg oder eine Debitorenkarte, von einer Person in Ihrer Organisation genehmigt werden muss, senden Sie eine Genehmigungsanforderung als Teil eines Workflows.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-104">When a record, such as a purchase document or a customer card, needs to be approved by someone in your organization, you send an approval request as part of a workflow.</span></span> <span data-ttu-id="7d3b1-105">Je nachdem, wie der Workflow eingerichtet ist, wird der entsprechende Genehmiger dann benachrichtigt, dass der Datensatz genehmigt werden muss.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-105">Based on how the workflow is set up, the appropriate approver is then notified that the record requires their approval.</span></span>

<span data-ttu-id="7d3b1-106">Sie richten Genehmigungsworkflows im Fenster **Workflow** ein.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-106">You set up approval workflows in the **Workflow** window.</span></span> <span data-ttu-id="7d3b1-107">Weitere Informationen erhalten Sie unter [Workflows einrichten](across-set-up-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="7d3b1-107">For more information, see [Setting Up Workflows](across-set-up-workflows.md).</span></span>

<span data-ttu-id="7d3b1-108">Neben der Genehmigung von Workflows, wie in diesem Thema beschrieben, können Sie auch verschiedene andere Aufgaben für Workflows ausführen.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-108">In addition to approval workflows described in this topic, you can perform various other workflow tasks.</span></span> <span data-ttu-id="7d3b1-109">Weitere Informationen erhalten Sie unter [Workflows verwenden](across-use-workflows.md).</span><span class="sxs-lookup"><span data-stu-id="7d3b1-109">For more information, [Using Workflows](across-use-workflows.md).</span></span>

<span data-ttu-id="7d3b1-110">Wesentliche Genehmigungsworkflows für Einkaufsbelege, Verkaufsbelege, Zahlungsausgangs Buch.-Blätter, Debitorenkarten und Artikelkarten können als unterstützte Einrichtung gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-110">Core approval workflows for purchases documents, sales documents, payment journals, customer cards, and item cards are ready to start as assisted setup.</span></span> <span data-ttu-id="7d3b1-111">Weitere Informationen finden Sie unter [Willkommen bei[!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)</span><span class="sxs-lookup"><span data-stu-id="7d3b1-111">For more information, see [Welcome to [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md).</span></span>

## <a name="to-request-approval-of-a-record"></a><span data-ttu-id="7d3b1-112">So fordern Sie die Genehmigung eines Datensatzes an</span><span class="sxs-lookup"><span data-stu-id="7d3b1-112">To request approval of a record</span></span>
<span data-ttu-id="7d3b1-113">Die nächste Aufgabe wird durch einen genehmigenden Benutzer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-113">The following task is performed by an approval user.</span></span>

1. <span data-ttu-id="7d3b1-114">Wählen Sie im Fenster, das den Datensatz anzeigt, die Aktion **Genehmigungsanforderung senden**.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-114">In the window that presents the record, choose the **Send Approval Request** action.</span></span>
2. <span data-ttu-id="7d3b1-115">Um alle Genehmigungsanforderungen anzuzeigen, wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") aus, geben **Genehmigungsanforderungsposten** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-115">To see all your approval requests, choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Approval Request Entries**, and then choose the related link.</span></span>  

<span data-ttu-id="7d3b1-116">Der Status des Genehmigungspostens wird von **Erstellt** in **Offen** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-116">The status of the approval entry is updated from **Created** to **Open**.</span></span> <span data-ttu-id="7d3b1-117">Der Status des Datensatzes, z. B. einer Einkaufsrechnung wird von **Offen** zu **Ausstehende Genehmigung** aktualisiert und ist für eine Bearbeitung gesperrt, bis alle Genehmiger den Datensatz genehmigt haben.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-117">The status of the record, for example a purchase invoice, is updated from **Open** to **Pending Approval** and remains locked for processing until all approvers have approved the record.</span></span>

<span data-ttu-id="7d3b1-118">Wenn der Genehmiger den Datensatz genehmigt hat, ändert sich der Status zu **Freigegeben**.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-118">When the approver has approved the record, the status changes to **Released**.</span></span> <span data-ttu-id="7d3b1-119">Sie können dann Ihre Aufgaben für diesen Datensatz fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-119">You can then continue your tasks with the record.</span></span>

## <a name="to-cancel-requests-for-approval"></a><span data-ttu-id="7d3b1-120">So stornieren Sie Genehmigungsanforderungen</span><span class="sxs-lookup"><span data-stu-id="7d3b1-120">To cancel requests for approval</span></span>
<span data-ttu-id="7d3b1-121">Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-121">The following task is performed by an approval user with approver rights.</span></span>

<span data-ttu-id="7d3b1-122">Ein Debitor möchte möglicherweise Änderungen an einem Auftrag vornehmen, nachdem dieser zur Genehmigung übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-122">A customer may want to change an order after it has been submitted for approval.</span></span> <span data-ttu-id="7d3b1-123">In diesem Fall können Sie den Genehmigungsvorgang abbrechen und die notwendigen Änderungen an dem Auftrag durchführen, bevor Sie eine erneute Genehmigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-123">In this case, you can cancel the approval process and make the necessary changes to the order before you request approval again.</span></span>

- <span data-ttu-id="7d3b1-124">Wählen Sie im Fenster, das den Datensatz anzeigt, die Aktion **Genehmigungsanforderung stornieren**.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-124">In the window that displays the record, choose the **Cancel Approval Request** action.</span></span>

<span data-ttu-id="7d3b1-125">Wenn die Genehmigungsanforderung storniert wurde, wird der Status des entsprechenden Genehmigungspostens zu **Storniert** geändert.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-125">When the approval request has been canceled, the status of the related approval entry is changed to **Canceled**.</span></span> <span data-ttu-id="7d3b1-126">Der Status des Datensatzes wird von **Ausstehende Genehmigung** in **Offen** aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-126">The status of the record is updated from **Pending Approval** to **Open**.</span></span> <span data-ttu-id="7d3b1-127">Der Genehmigungsvorgang kann dann von vorne begonnen werden.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-127">The approval process can then start again.</span></span>

## <a name="to-approve-or-reject-requests-for-approval"></a><span data-ttu-id="7d3b1-128">So können Sie Genehmigungsanforderungen genehmigen oder ablehnen</span><span class="sxs-lookup"><span data-stu-id="7d3b1-128">To approve or reject requests for approval</span></span>
<span data-ttu-id="7d3b1-129">Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-129">The following task is performed by an approval user with approver rights.</span></span>

<span data-ttu-id="7d3b1-130">Sie können Genehmigungsanforderungen im Fenster **Zu genehmigende Anforderungen** verarbeiten, beispielsweise um mehrere Anforderungen gleichzeitig zu genehmigen.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-130">You can process approval requests in the **Requests to Approve** window, for example to approve multiple requests at a time.</span></span> <span data-ttu-id="7d3b1-131">Alternativ können Sie jede Anforderung im entsprechenden Datensatz, wie dem Fenster **Einkaufsrechnung** verarbeiten, indem Sie den Link in der Benachrichtigung auswählen, die Sie erhalten.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-131">Alternatively, you can process each request on the related record, such as the **Purchase Invoice** window, by choosing the link in the notification that you receive.</span></span>

1. <span data-ttu-id="7d3b1-132">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suche") und geben **Zu genehmigende Anforderungen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-132">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Requests to Approve**, and then choose the related link.</span></span>
2. <span data-ttu-id="7d3b1-133">Wählen Sie mindestens eine Zeile für den Datensatz (oder die Datensätze) zur Genehmigung oder Ablehnung aus.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-133">Select one or more lines for the record or records that you want to approve or reject.</span></span>
3. <span data-ttu-id="7d3b1-134">Wählen Sie die Aktion **Genehmigen**, **Ablehnen**, oder **Delegieren** aus.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-134">Choose the **Approve**, **Reject**, or **Delegate** actions.</span></span>

<span data-ttu-id="7d3b1-135">Wenn ein Datensatz genehmigt oder abgelehnt wurde, ändert sich der Genehmigungsstatus im Feld **Status** zu **Genehmigt** oder **Abgelehnt**.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-135">When a record has been approved or rejected, the approval status in the **Status** field changes to **Approved** or **Rejected**.</span></span>

<span data-ttu-id="7d3b1-136">Wenn eine Genehmigerhierarchie eingerichtet wurde, bleibt der Datensatzstatus auf **Ausstehende Genehmigung**, bis alle Genehmiger den Datensatz genehmigt haben.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-136">If an approver hierarchy is set up, the record status will be **Pending Approval** until all approvers have approved the record.</span></span> <span data-ttu-id="7d3b1-137">Dann ändert sich der Datensatzstatus zu **Freigegeben**.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-137">Then the record status will change to **Released**.</span></span>

<span data-ttu-id="7d3b1-138">Gleichzeitig ändert sich der Genehmigungsstatus von **Erstellt** zu **Offen**, sobald eine Genehmigungsanforderung für den Datensatz erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-138">At the same time, the approval status changes from **Created** to **Open** as soon as an approval request for the record is created.</span></span> <span data-ttu-id="7d3b1-139">Wenn die Anforderung abgelehnt wurde, ändert sich der Genehmigungsstatus zu **Abgelehnt**.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-139">If the request is rejected, the approval status changes to **Rejected**.</span></span> <span data-ttu-id="7d3b1-140">Der Status bleibt **Offen** oder **Abgelehnt**, bis alle Genehmiger die Anforderung genehmigt haben.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-140">The status remains **Open** or **Rejected** until all approvers have approved the request.</span></span>

## <a name="to-delegate-requests-for-approval"></a><span data-ttu-id="7d3b1-141">So delegieren Sie Genehmigungsanforderungen</span><span class="sxs-lookup"><span data-stu-id="7d3b1-141">To delegate requests for approval</span></span>
<span data-ttu-id="7d3b1-142">Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-142">The following task is performed by an approval user with approver rights.</span></span>

<span data-ttu-id="7d3b1-143">Damit verhindert wird, dass sich Belege ansammeln oder anderweitig den Workflow blockieren, können der Genehmiger und der Genehmigungsadministrator eine Genehmigungsanforderung an einen stellvertretenden Genehmiger delegieren.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-143">To prevent documents from piling up or otherwise block the workflow, the approver and the approval administrator can delegate an approval request to a substitute approver.</span></span> <span data-ttu-id="7d3b1-144">Der Ersatz kann entweder ein festgelegter Ersatz, der direkte Genehmiger oder der Genehmigungsadministrator sein (in dieser Prioritätenreihenfolge).</span><span class="sxs-lookup"><span data-stu-id="7d3b1-144">The substitute can either be a designated substitute, the direct approver, or the approval administrator, in that order of priority.</span></span> <span data-ttu-id="7d3b1-145">In der Regel nutzen Sie diese Funktion dann, wenn sich ein Genehmiger außer Haus befindet und Anforderungen nicht vor dem Fälligkeitsdatum genehmigen kann.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-145">You typically use this feature if an approver is out of office and is unable to approve requests before the due date.</span></span>

1. <span data-ttu-id="7d3b1-146">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suche") und geben **Zu genehmigende Anforderungen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-146">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Requests to Approve**, and then choose the related link.</span></span>
2. <span data-ttu-id="7d3b1-147">Wählen Sie mindestens eine Zeile für die Genehmigungsanforderungen aus, die Sie an einen Ersatzgenehmiger delegieren möchten, und wählen Sie dann die Aktion **Delegieren**.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-147">Select one or more lines for the approval requests that you want to delegate to a substitute approver, and then choose the **Delegate** action.</span></span>

<span data-ttu-id="7d3b1-148">Eine Benachrichtigung zur Genehmigung der Anforderung wird an den stellvertretenden Genehmiger gesendet.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-148">A notification to approve the request is sent to the substitute approver.</span></span>

## <a name="to-manage-overdue-approval-requests"></a><span data-ttu-id="7d3b1-149">So verwalten Sie fällige Genehmigungsanforderungen</span><span class="sxs-lookup"><span data-stu-id="7d3b1-149">To manage overdue approval requests</span></span>
<span data-ttu-id="7d3b1-150">Die nächste Aufgabe wird durch einen genehmigenden Benutzer mit Genehmigerrechten ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-150">The following task is performed by an approval user with approver rights.</span></span>

<span data-ttu-id="7d3b1-151">In regelmäßigen Abständen müssen Sie Genehmigungs-Workflowbenutzer an überfällige Genehmigungsanforderungen erinnern, auf die sie reagieren müssen.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-151">At regular intervals, you must remind approval workflow users of overdue approval requests that they must react on.</span></span> <span data-ttu-id="7d3b1-152">Dazu verwenden Sie die Funktion **Fällige Genehmigungsbenachrichtigungen senden**.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-152">You use the **Send Overdue Approval Notifications** function for this.</span></span>

<span data-ttu-id="7d3b1-153">Die Funktion **Fällige Genehmigungsbenachrichtigungen senden** ermittelt alle offenen Genehmigungsanforderungen, die zurzeit fällig sind.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-153">The **Send Overdue Approval Notifications** function checks for all open approval requests that are currently overdue.</span></span> <span data-ttu-id="7d3b1-154">Jeder Genehmiger, für den mindestens ein fälliger Genehmigungsposten vorhanden ist, erhält eine Benachrichtigung mit der Liste aller fälligen Genehmigungsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-154">Each approver that has at least one overdue approval entry receives a notification with the list of all their overdue approval requests.</span></span> <span data-ttu-id="7d3b1-155">Die Benachrichtigung wird auch an den Genehmiger und an alle Anforderer der fälligen Genehmigungen gesendet.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-155">The notification is also sent to their approver and all the requesters of the overdue approvals.</span></span> <span data-ttu-id="7d3b1-156">Dies ist hilfreich, wenn der fällige Genehmigungsposten an einen Stellvertreter delegiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-156">This helps if the overdue approval entry must be delegated to a substitute.</span></span>

1. <span data-ttu-id="7d3b1-157">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suche") und geben **Überfällige Genehmigungsanforderungen** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-157">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Overdue Approval Requests**, and then choose the related link.</span></span>
2. <span data-ttu-id="7d3b1-158">Wählen Sie im Fenster **Überfällige Genehmigungsanfragen** die Aktion **Überfällige Genehmigungsbenachrichtigungen senden** aus.</span><span class="sxs-lookup"><span data-stu-id="7d3b1-158">In the **Overdue Approval Requests** window, choose the **Send Overdue Approval Notifications** action.</span></span>

## <a name="see-also"></a><span data-ttu-id="7d3b1-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d3b1-159">See Also</span></span>
<span data-ttu-id="7d3b1-160">[Verkauf](sales-manage-sales.md)  </span><span class="sxs-lookup"><span data-stu-id="7d3b1-160">[Sales](sales-manage-sales.md)  </span></span>  
[<span data-ttu-id="7d3b1-161">Eingehende Belege</span><span class="sxs-lookup"><span data-stu-id="7d3b1-161">Incoming Documents</span></span>](across-income-documents.md)  
[<span data-ttu-id="7d3b1-162">Einkauf</span><span class="sxs-lookup"><span data-stu-id="7d3b1-162">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="7d3b1-163">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="7d3b1-163">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

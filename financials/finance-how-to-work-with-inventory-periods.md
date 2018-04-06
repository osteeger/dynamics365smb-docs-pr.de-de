---
title: Arbeiten mit Lagerbuchungsperioden | Microsoft Docs
description: "Sie können den Zeitrahmen steuern, auf den Mitarbeiter Beitragsänderungen des Lagerbestandes buchen können, indem Sie Lagerbuchungsperioden definieren."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: inventory, periods
ms.date: 08/07/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 8f3d24dda00e3234dfcf7538c7f4fb7fbc008221
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="work-with-inventory-periods"></a><span data-ttu-id="8cf1d-103">Arbeiten mit Lagerbuchungsperioden</span><span class="sxs-lookup"><span data-stu-id="8cf1d-103">Work with Inventory Periods</span></span>
<span data-ttu-id="8cf1d-104">Eine Lagerbuchungsperiode definiert eine Zeitspanne, in der Sie Änderungen des Lagerbestandes buchen können.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-104">Inventory periods define a period of time in which you can post changes to inventory.</span></span> <span data-ttu-id="8cf1d-105">Eine Lagerbuchungsperiode ist durch das Datum definiert, an dem sie endet (wird auch als Enddatum bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="8cf1d-105">An inventory period is defined by the date on which it ends, or the ending date.</span></span> <span data-ttu-id="8cf1d-106">Wenn Sie eine Lagerbuchungsperiode schließen, können Sie vor diesem Enddatum keine Änderungen des erwarteten oder in Rechnung gestellten Lagerbestandes buchen.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-106">When you close an inventory period, you cannot post any changes to inventory, either expected or invoiced, before this ending date.</span></span> <span data-ttu-id="8cf1d-107">Vor diesem Enddatum können Sie keine neuen Werte im Lager buchen.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-107">You cannot post any new values to inventory before the ending date.</span></span> <span data-ttu-id="8cf1d-108">Wenn Sie in der geschlossenen Periode offene Artikelposten haben, es also positive Mengen gibt, die noch nicht für ausgehende Transaktion ausgeglichen wurden, können Sie weiterhin ausgehende Mengen mit diesen Posten verknüpfen, auch wenn die Periode geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-108">If you have open item entries in the closed period, meaning positive quantities that have not yet been applied to outbound transactions, you can still apply outbound quantities to these entries, even if the period is closed.</span></span>  

<span data-ttu-id="8cf1d-109">In den folgenden Abschnitten werden diese Schritte beschrieben:</span><span class="sxs-lookup"><span data-stu-id="8cf1d-109">The following sections describe how to:</span></span>  

* <span data-ttu-id="8cf1d-110">Lagerbuchungsperioden erstellen.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-110">Create inventory periods.</span></span>  
* <span data-ttu-id="8cf1d-111">Lagerbuchungsperioden schließen.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-111">Close inventory periods.</span></span>  
* <span data-ttu-id="8cf1d-112">Lagerbuchungsperioden erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-112">Reopen inventory periods.</span></span>  

## <a name="to-create-an-inventory-period"></a><span data-ttu-id="8cf1d-113">Eine Lagerbuchungsperiode erstellen</span><span class="sxs-lookup"><span data-stu-id="8cf1d-113">To create an inventory period</span></span>  
1. <span data-ttu-id="8cf1d-114">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Lagerbuchungsperioden** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8cf1d-115">Erstellen Sie eine neue Zeile.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-115">Create a new line.</span></span>  
3. <span data-ttu-id="8cf1d-116">Geben Sie in das Feld **Enddatum** das letzte Datum der Lagerbuchungsperiode ein, die Sie definieren möchten.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-116">In the **Ending Date** field, enter the last date in the inventory period that you want to define.</span></span> <span data-ttu-id="8cf1d-117">Wenn die Periode geschlossen ist, können Sie vor diesem Datum keine Lagerbestandsänderungen buchen.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-117">When the period is closed, you will not be able to post inventory changes before this date.</span></span>  
4. <span data-ttu-id="8cf1d-118">Geben Sie im Feld **Name** einen beschreibenden Namen ein.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-118">Enter a descriptive name in the **Name** field.</span></span> <span data-ttu-id="8cf1d-119">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-119">Choose the **OK** button.</span></span>  

## <a name="closing-inventory-periods"></a><span data-ttu-id="8cf1d-120">Lagerbuchungsperioden schließen</span><span class="sxs-lookup"><span data-stu-id="8cf1d-120">Closing Inventory Periods</span></span>  
<span data-ttu-id="8cf1d-121">Das Feld **Abgeschlossen** gibt an, ob die Lagerbuchungsperiode hinsichtlich Änderungen der Lagerbestandswerte geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-121">The **Closed** field indicates whether or not the inventory period is closed to inventory value changes.</span></span> <span data-ttu-id="8cf1d-122">Sie können dieses Feld nicht bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-122">You cannot edit this field.</span></span>  

<span data-ttu-id="8cf1d-123">Sofern die folgenden Aussagen zutreffen, können Sie jede Lagerbuchungsperiode schließen:</span><span class="sxs-lookup"><span data-stu-id="8cf1d-123">You can close any inventory period, provided that the following is true:</span></span>  

* <span data-ttu-id="8cf1d-124">In dieser Periode gibt es keine offenen ausgehenden Artikelposten (d. h., es gibt keinen negativen Lagerbestand).</span><span class="sxs-lookup"><span data-stu-id="8cf1d-124">There are no open outbound item ledger entries, meaning negative inventory, in that period.</span></span>  
* <span data-ttu-id="8cf1d-125">Die Preise aller Artikel wurden mit dem Batchauftrag **Lagerreg. fakt. Einst. Preise** angepasst.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-125">The cost of all items has been adjusted using the **Adjust Cost – Item Entries** batch job.</span></span>  

<span data-ttu-id="8cf1d-126">Das heißt, dass alle ausgehenden Transaktionsmengen (z. B. von Verkaufsaufträgen, ausgehenden Umlagerungen, Verkaufsrechnungen, Einkaufsreklamationen oder Einkaufsgutschriften) mit der im Lagerbestand vorhandenen Menge ausgeglichen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-126">This means that all outbound transaction quantities, such as those from sales orders, outbound transfers, sales invoices, purchase returns, or purchase credit memos, must be applied to existing quantity in inventory.</span></span>  

### <a name="to-close-an-inventory-period"></a><span data-ttu-id="8cf1d-127">Eine Lagerbuchungsperiode schließen</span><span class="sxs-lookup"><span data-stu-id="8cf1d-127">To close an inventory period</span></span>  
1. <span data-ttu-id="8cf1d-128">Bevor Sie eine Lagerbuchungsperiode schließen, sollten Sie den Batchauftrag **Lagerreg. fakt. Einst. Preise** ausführen, um sich zu vergewissern, dass alle Kostenregulierungen gebucht sind.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-128">Before closing an inventory period, run the **Adjust Cost – Item Entries** batch job to ensure that all cost adjustments are posted.</span></span> <span data-ttu-id="8cf1d-129">Wählen Sie auf der Registerkarte **Aktionen** in der Gruppe **Funktionen** die Option **Kosten anpassen - Artikel** aus.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-129">On the **Actions** tab, in the **Functions** group, choose **Adjust Cost – Item Entries**.</span></span>  

     <span data-ttu-id="8cf1d-130">Führen Sie den Bericht **Lagerbuchungsperiode schließen - Test** aus, um zu ermitteln, ob es in der Lagerbuchungsperiode offene ausgehende Artikelposten oder Artikel gibt, deren Preise noch nicht reguliert wurden.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-130">Run the **Close Inventory Period – Test** report to determine if there are any open outbound item entries within the inventory period or any items whose cost has not yet been adjusted.</span></span>  
2. <span data-ttu-id="8cf1d-131">Wählen Sie die Aktion **Lagerbuchungsperiode schließen - Test**.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-131">Choose the **Close Inventory Period – Test** action.</span></span>  

     <span data-ttu-id="8cf1d-132">Führen Sie den Batchauftrag **Lagerregulierung buchen** aus, damit sichergestellt ist, dass alle Preise in der Finanzbuchhaltung gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-132">Run the **Post Inventory Cost to G/L** batch job to ensure that all costs are posted to the general ledger.</span></span>  
3. <span data-ttu-id="8cf1d-133">Wählen Sie die Aktion **Lager auf Sachkonten buchen** aus.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-133">Choose the **Post Inventory to G/L** action.</span></span>  
4. <span data-ttu-id="8cf1d-134">Wählen Sie im Fenster  **Lagerbuchungsperioden** die Lagerbuchungsperiode aus, die geschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-134">In the **Inventory Periods** window, select the inventory period you want to close.</span></span>  
5. <span data-ttu-id="8cf1d-135">Wählen Sie die Aktion **Periode schließen**.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-135">Choose the **Close Period** action.</span></span> <span data-ttu-id="8cf1d-136">Nachdem die Lagerbuchungsperiode geschlossen wurde, können Sie vor dem Enddatum keine Lagerbestandsänderungen mehr buchen.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-136">After the inventory period has been closed, you cannot post inventory changes before the ending date.</span></span> <span data-ttu-id="8cf1d-137">Die Preise aller Artikel müssen mit der Stapelverarbeitung **Kosten anpassen - Artikelposten** reguliert sein, bevor Sie die Lagerbuchungsperiode schließen.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-137">The cost of all items must be adjusted with the **Adjust Cost – Item Entries** batch job before you close the inventory period.</span></span>  
6. <span data-ttu-id="8cf1d-138">Wählen Sie die Schaltfläche **Ja**, wenn Sie bestätigen möchten, dass die Periode geschlossen werden soll, oder wählen Sie die Schaltfläche **Nein**, wenn Sie das Schließen abbrechen möchten.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-138">Choose the **Yes** button to confirm that you want to close the period, or choose **No** to cancel the closing.</span></span>  
7. <span data-ttu-id="8cf1d-139">Die Lagerbuchungsperiode wird geschlossen und nach Beendigung dieses Vorgangs wird eine Bestätigungsmeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-139">The inventory period is closed and a confirmation message is displayed when it is finished.</span></span>  

## <a name="reopening-inventory-periods"></a><span data-ttu-id="8cf1d-140">Lagerbuchungsperioden erneut öffnen</span><span class="sxs-lookup"><span data-stu-id="8cf1d-140">Reopening Inventory Periods</span></span>  
<span data-ttu-id="8cf1d-141">Nachdem Sie eine Lagerbuchungsperiode geschlossen haben, können Sie diese Periode nicht mehr löschen.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-141">After you have closed the inventory period, you cannot delete the inventory period.</span></span> <span data-ttu-id="8cf1d-142">Sie können sie aber erneut öffnen, wenn Sie Buchungen vor dem Enddatum der Lagerbuchungsperiode zulassen möchten.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-142">You can, however, reopen it, if you would like to allow posting before the ending date of the inventory period.</span></span> <span data-ttu-id="8cf1d-143">Ein erneutes Öffnen einer Periode bewirkt, dass auch jede Lagerbuchungsperiode geöffnet wird, deren Enddatum hinter dem Enddatum der Periode liegt, die Sie erneut öffnen.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-143">Reopening a period also reopens all inventory periods with ending dates later than the period you reopen.</span></span>  

### <a name="to-reopen-an-inventory-period"></a><span data-ttu-id="8cf1d-144">So öffnen Sie eine Lagerbuchungsperiode erneut</span><span class="sxs-lookup"><span data-stu-id="8cf1d-144">To reopen an inventory period</span></span>  
1. <span data-ttu-id="8cf1d-145">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Symbol Nach Seite oder Bericht suchen"), geben **Lagerbuchungsperioden** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-145">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Inventory Periods**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8cf1d-146">Wählen Sie die Lagerbuchungsperiode aus, die erneut geöffnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-146">Select the inventory period you want to reopen.</span></span>  
3. <span data-ttu-id="8cf1d-147">Wählen Sie die Aktion **Periode erneut öffnen**.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-147">Choose the **Reopen Period** period action.</span></span> <span data-ttu-id="8cf1d-148">Bestätigen Sie, dass Sie die Periode erneut öffnen möchten.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-148">Confirm that you want to reopen the period.</span></span>  
4. <span data-ttu-id="8cf1d-149">Alle Lagerbuchungsperioden, deren Enddatum nach der von Ihnen ausgewählten Periode liegt, werden erneut geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8cf1d-149">All inventory periods with ending dates later than the period you selected are reopened.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8cf1d-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8cf1d-150">See Also</span></span>  
[<span data-ttu-id="8cf1d-151">Designdetails: Bestandsperioden</span><span class="sxs-lookup"><span data-stu-id="8cf1d-151">Design Details: Inventory Periods</span></span>](design-details-inventory-periods.md)  
[<span data-ttu-id="8cf1d-152">Finanzen</span><span class="sxs-lookup"><span data-stu-id="8cf1d-152">Finance</span></span>](finance.md)  
[<span data-ttu-id="8cf1d-153">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="8cf1d-153">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="8cf1d-154">Arbeiten mit Financials</span><span class="sxs-lookup"><span data-stu-id="8cf1d-154">Working with Financials</span></span>](ui-work-product.md)

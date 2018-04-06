---
title: 'Designdetails: Erwartete Kostenbuchung | Microsoft Docs'
description: "Soll-Kosten repräsentieren die Schätzung der Kosten, z. B. für die Kosten eines Einkaufsartikels, die Sie registrieren, bevor Sie die Rechnung für den Artikel erhalten."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 50ac9cbb946fedc687eb5ea1373c99d68f3d322b
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-expected-cost-posting"></a><span data-ttu-id="0dba8-103">Designdetails: Soll-Kosten-Buchen</span><span class="sxs-lookup"><span data-stu-id="0dba8-103">Design Details: Expected Cost Posting</span></span>
<span data-ttu-id="0dba8-104">Soll-Kosten repräsentieren die Schätzung der Kosten, z. B. für die Kosten eines Einkaufsartikels, die Sie registrieren, bevor Sie die Rechnung für den Artikel erhalten.</span><span class="sxs-lookup"><span data-stu-id="0dba8-104">Expected costs represent the estimation of, for example, a purchased item’s cost that you record before you receive the invoice for the item.</span></span>  

 <span data-ttu-id="0dba8-105">Sie können Soll-Kosten buchen, um sowie Fibu-Posten in den Lagerbestand zurückgeführt.</span><span class="sxs-lookup"><span data-stu-id="0dba8-105">You can post expected cost to inventory and to the general ledger.</span></span> <span data-ttu-id="0dba8-106">Wenn Sie eine Menge buchen, die nur erhalten oder geliefert, aber nicht fakturiert wurde, kann ein Wertposten mit den Soll-Kosten erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0dba8-106">When you post a quantity that is only received or shipped but not invoiced, then a value entry is created with the expected cost.</span></span> <span data-ttu-id="0dba8-107">Diese Soll-Kosten beeinflussen den Lagerwert, werden aber nicht in der Finanzbuchhaltung gebucht, es sei denn, das System wird entsprechend eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="0dba8-107">This expected cost affects the inventory value, but is not posted to the general ledger unless you set up the system up to do so.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="0dba8-108">Soll-Kosten werden nur für Artikeltransaktionen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0dba8-108">Expected costs are only managed for item transactions.</span></span> <span data-ttu-id="0dba8-109">Soll-Kosten sind nicht für immaterielle Transaktionstypen, wie etwa Kapazität und Artikel Zu-/Abschläge.</span><span class="sxs-lookup"><span data-stu-id="0dba8-109">Expected costs are not for immaterial transaction types, such as capacity and item charges.</span></span>  

 <span data-ttu-id="0dba8-110">Wenn nur der Mengenteil eine Bestandserhöhung gebucht wurde, dann ändert sich der Lagerwert in der Finanzbuchhaltung nicht, es sei denn, Sie haben das Kontrollkästchen E**rwartete Soll-Kosten buchen** im Fenster **Bestand einrichten** ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="0dba8-110">If only the quantity part of an inventory increase has been posted, then the inventory value in the general ledger does not change unless you have selected the **Expected Cost Posting to G/L** check box in the **Inventory Setup** window.</span></span> <span data-ttu-id="0dba8-111">In diesem Fall werden die Soll-Kosten auf Interimskonten zum Zeitpunkt des Wareneingangs gebucht.</span><span class="sxs-lookup"><span data-stu-id="0dba8-111">In that case, the expected cost is posted to interim accounts at the time of receipt.</span></span> <span data-ttu-id="0dba8-112">Nachdem der Wareneingang vollständig fakturiert wurde, werden die Interimskonten ausgeglichen und die Ist-Kosten werden im Lagerkonto gebucht.</span><span class="sxs-lookup"><span data-stu-id="0dba8-112">After the receipt has been fully invoiced, the interim accounts are then balanced and the actual cost is posted to the inventory account.</span></span>  

 <span data-ttu-id="0dba8-113">Um Abstimmung und Verfolgbarkeit zu unterstützen, zeigt der fakturierte Wertposten den Soll-Kostenbetrag, der zum Ausgleichen der Interimskonten gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="0dba8-113">To support reconciliation and traceability work, the invoiced value entry shows the expected cost amount that has been posted to balance the interim accounts.</span></span>  

## <a name="example"></a><span data-ttu-id="0dba8-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0dba8-114">Example</span></span>  
 <span data-ttu-id="0dba8-115">Das folgende Beispiel zeigt erwartete Kosten an, wenn das Kontrollkästchen **Automatische Lagerbuchung** und das Kontrollkästchen **Erwartete Kostenbuchung** im Fenster **Lager Einrichtung** ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="0dba8-115">The following example shows expected cost if the **Automatic Cost Posting** check box and the **Expected Cost Posting to G/L** check box are selected in the **Inventory Setup** window.</span></span>  

 <span data-ttu-id="0dba8-116">Sie buchen eine Einkaufsbestellung als erhalten.</span><span class="sxs-lookup"><span data-stu-id="0dba8-116">You post a purchase order as received.</span></span> <span data-ttu-id="0dba8-117">Die erwarteten Kosten sind MW 95,00.</span><span class="sxs-lookup"><span data-stu-id="0dba8-117">The expected cost is LCY 95.00.</span></span>  

 <span data-ttu-id="0dba8-118">**Wertposten**</span><span class="sxs-lookup"><span data-stu-id="0dba8-118">**Value Entries**</span></span>  

|<span data-ttu-id="0dba8-119">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="0dba8-119">Posting Date</span></span>|<span data-ttu-id="0dba8-120">Postentyp</span><span class="sxs-lookup"><span data-stu-id="0dba8-120">Entry Type</span></span>|<span data-ttu-id="0dba8-121">Einstandsbetrag (erwartet)</span><span class="sxs-lookup"><span data-stu-id="0dba8-121">Cost Amount (Expected)</span></span>|<span data-ttu-id="0dba8-122">Auf Sachkonto geb. Soll-Kosten</span><span class="sxs-lookup"><span data-stu-id="0dba8-122">Expected Cost Posted to G/L</span></span>|<span data-ttu-id="0dba8-123">Soll-Kosten</span><span class="sxs-lookup"><span data-stu-id="0dba8-123">Expected Cost</span></span>|<span data-ttu-id="0dba8-124">Artikelposten Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="0dba8-124">Item Ledger Entry No.</span></span>|<span data-ttu-id="0dba8-125">Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="0dba8-125">Entry No.</span></span>|  
|------------------|----------------|------------------------------|----------------------------------|-------------------|---------------------------|---------------|  
|<span data-ttu-id="0dba8-126">01-01-20</span><span class="sxs-lookup"><span data-stu-id="0dba8-126">01-01-20</span></span>|<span data-ttu-id="0dba8-127">EK-Preis</span><span class="sxs-lookup"><span data-stu-id="0dba8-127">Direct Cost</span></span>|<span data-ttu-id="0dba8-128">95.00</span><span class="sxs-lookup"><span data-stu-id="0dba8-128">95.00</span></span>|<span data-ttu-id="0dba8-129">95.00</span><span class="sxs-lookup"><span data-stu-id="0dba8-129">95.00</span></span>|<span data-ttu-id="0dba8-130">Ja</span><span class="sxs-lookup"><span data-stu-id="0dba8-130">Yes</span></span>|<span data-ttu-id="0dba8-131">1</span><span class="sxs-lookup"><span data-stu-id="0dba8-131">1</span></span>|<span data-ttu-id="0dba8-132">1</span><span class="sxs-lookup"><span data-stu-id="0dba8-132">1</span></span>|  

 <span data-ttu-id="0dba8-133">**Relationsposten im Sachkonto – Tabelle Artikelpostenrelation**</span><span class="sxs-lookup"><span data-stu-id="0dba8-133">**Relation Entries in the G/L – Item Ledger Relation Table**</span></span>  

|<span data-ttu-id="0dba8-134">Sachposten Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="0dba8-134">G/L Entry No.</span></span>|<span data-ttu-id="0dba8-135">Wertposten Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="0dba8-135">Value Entry No.</span></span>|<span data-ttu-id="0dba8-136">Fibujournalnr.</span><span class="sxs-lookup"><span data-stu-id="0dba8-136">G/L Register No.</span></span>|  
|--------------------|---------------------|-----------------------|  
|<span data-ttu-id="0dba8-137">1</span><span class="sxs-lookup"><span data-stu-id="0dba8-137">1</span></span>|<span data-ttu-id="0dba8-138">1</span><span class="sxs-lookup"><span data-stu-id="0dba8-138">1</span></span>|<span data-ttu-id="0dba8-139">1</span><span class="sxs-lookup"><span data-stu-id="0dba8-139">1</span></span>|  
|<span data-ttu-id="0dba8-140">2</span><span class="sxs-lookup"><span data-stu-id="0dba8-140">2</span></span>|<span data-ttu-id="0dba8-141">1</span><span class="sxs-lookup"><span data-stu-id="0dba8-141">1</span></span>|<span data-ttu-id="0dba8-142">1</span><span class="sxs-lookup"><span data-stu-id="0dba8-142">1</span></span>|  

 <span data-ttu-id="0dba8-143">**Sachposten**</span><span class="sxs-lookup"><span data-stu-id="0dba8-143">**General Ledger Entries**</span></span>  

|<span data-ttu-id="0dba8-144">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="0dba8-144">Posting Date</span></span>|<span data-ttu-id="0dba8-145">Sachkonto</span><span class="sxs-lookup"><span data-stu-id="0dba8-145">G/L Account</span></span>|<span data-ttu-id="0dba8-146">Kontonr. (En-US-Demo)</span><span class="sxs-lookup"><span data-stu-id="0dba8-146">Account No. (En-US Demo)</span></span>|<span data-ttu-id="0dba8-147">Betrag</span><span class="sxs-lookup"><span data-stu-id="0dba8-147">Amount</span></span>|<span data-ttu-id="0dba8-148">Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="0dba8-148">Entry No.</span></span>|  
|------------------|------------------|---------------------------------|------------|---------------|  
|<span data-ttu-id="0dba8-149">01-01-20</span><span class="sxs-lookup"><span data-stu-id="0dba8-149">01-01-20</span></span>|<span data-ttu-id="0dba8-150">Lagerzugangskonto (Interim)</span><span class="sxs-lookup"><span data-stu-id="0dba8-150">Inventory Accrual Account (Interim)</span></span>|<span data-ttu-id="0dba8-151">5530</span><span class="sxs-lookup"><span data-stu-id="0dba8-151">5530</span></span>|<span data-ttu-id="0dba8-152">-95.00</span><span class="sxs-lookup"><span data-stu-id="0dba8-152">-95.00</span></span>|<span data-ttu-id="0dba8-153">2</span><span class="sxs-lookup"><span data-stu-id="0dba8-153">2</span></span>|  
|<span data-ttu-id="0dba8-154">01-01-20</span><span class="sxs-lookup"><span data-stu-id="0dba8-154">01-01-20</span></span>|<span data-ttu-id="0dba8-155">Lagerkonto (Interim)</span><span class="sxs-lookup"><span data-stu-id="0dba8-155">Inventory Account (Interim)</span></span>|<span data-ttu-id="0dba8-156">2131</span><span class="sxs-lookup"><span data-stu-id="0dba8-156">2131</span></span>|<span data-ttu-id="0dba8-157">95.00</span><span class="sxs-lookup"><span data-stu-id="0dba8-157">95.00</span></span>|<span data-ttu-id="0dba8-158">1</span><span class="sxs-lookup"><span data-stu-id="0dba8-158">1</span></span>|  

 <span data-ttu-id="0dba8-159">Sie können die Einkaufsbestellung sofort oder zu einem späteren Zeitpunkt buchen.</span><span class="sxs-lookup"><span data-stu-id="0dba8-159">At a later date, you post the purchase order as invoiced.</span></span> <span data-ttu-id="0dba8-160">Die fakturierten Kosten sind MW 100,00.</span><span class="sxs-lookup"><span data-stu-id="0dba8-160">The invoiced cost is LCY 100.00.</span></span>  

 <span data-ttu-id="0dba8-161">**Wertposten**</span><span class="sxs-lookup"><span data-stu-id="0dba8-161">**Value Entries**</span></span>  

|<span data-ttu-id="0dba8-162">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="0dba8-162">Posting Date</span></span>|<span data-ttu-id="0dba8-163">Einstandsbetrag (tatsächl.)</span><span class="sxs-lookup"><span data-stu-id="0dba8-163">Cost Amount (Actual)</span></span>|<span data-ttu-id="0dba8-164">Einstandsbetrag (erwartet)</span><span class="sxs-lookup"><span data-stu-id="0dba8-164">Cost Amount (Expected)</span></span>|<span data-ttu-id="0dba8-165">Gebuchte Lagerregulierung an G/L</span><span class="sxs-lookup"><span data-stu-id="0dba8-165">Cost Posted to G/L</span></span>|<span data-ttu-id="0dba8-166">Soll-Kosten</span><span class="sxs-lookup"><span data-stu-id="0dba8-166">Expected Cost</span></span>|<span data-ttu-id="0dba8-167">Artikelposten Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="0dba8-167">Item Ledger Entry No.</span></span>|<span data-ttu-id="0dba8-168">Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="0dba8-168">Entry No.</span></span>|  
|------------------|----------------------------|------------------------------|-------------------------|-------------------|---------------------------|---------------|  
|<span data-ttu-id="0dba8-169">01-15-20</span><span class="sxs-lookup"><span data-stu-id="0dba8-169">01-15-20</span></span>|<span data-ttu-id="0dba8-170">100.00</span><span class="sxs-lookup"><span data-stu-id="0dba8-170">100.00</span></span>|<span data-ttu-id="0dba8-171">-95.00</span><span class="sxs-lookup"><span data-stu-id="0dba8-171">-95.00</span></span>|<span data-ttu-id="0dba8-172">100.00</span><span class="sxs-lookup"><span data-stu-id="0dba8-172">100.00</span></span>|<span data-ttu-id="0dba8-173">Nein</span><span class="sxs-lookup"><span data-stu-id="0dba8-173">No</span></span>|<span data-ttu-id="0dba8-174">1</span><span class="sxs-lookup"><span data-stu-id="0dba8-174">1</span></span>|<span data-ttu-id="0dba8-175">2</span><span class="sxs-lookup"><span data-stu-id="0dba8-175">2</span></span>|  

 <span data-ttu-id="0dba8-176">**Relationsposten im Sachkonto – Tabelle Artikelpostenrelation**</span><span class="sxs-lookup"><span data-stu-id="0dba8-176">**Relation Entries in the G/L – Item Ledger Relation Table**</span></span>  

|<span data-ttu-id="0dba8-177">Sachposten Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="0dba8-177">G/L Entry No.</span></span>|<span data-ttu-id="0dba8-178">Wertposten Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="0dba8-178">Value Entry No.</span></span>|<span data-ttu-id="0dba8-179">Fibujournalnr.</span><span class="sxs-lookup"><span data-stu-id="0dba8-179">G/L Register No.</span></span>|  
|--------------------|---------------------|-----------------------|  
|<span data-ttu-id="0dba8-180">3</span><span class="sxs-lookup"><span data-stu-id="0dba8-180">3</span></span>|<span data-ttu-id="0dba8-181">2</span><span class="sxs-lookup"><span data-stu-id="0dba8-181">2</span></span>|<span data-ttu-id="0dba8-182">2</span><span class="sxs-lookup"><span data-stu-id="0dba8-182">2</span></span>|  
|<span data-ttu-id="0dba8-183">4</span><span class="sxs-lookup"><span data-stu-id="0dba8-183">4</span></span>|<span data-ttu-id="0dba8-184">2</span><span class="sxs-lookup"><span data-stu-id="0dba8-184">2</span></span>|<span data-ttu-id="0dba8-185">2</span><span class="sxs-lookup"><span data-stu-id="0dba8-185">2</span></span>|  
|<span data-ttu-id="0dba8-186">5</span><span class="sxs-lookup"><span data-stu-id="0dba8-186">5</span></span>|<span data-ttu-id="0dba8-187">2</span><span class="sxs-lookup"><span data-stu-id="0dba8-187">2</span></span>|<span data-ttu-id="0dba8-188">2</span><span class="sxs-lookup"><span data-stu-id="0dba8-188">2</span></span>|  
|<span data-ttu-id="0dba8-189">6</span><span class="sxs-lookup"><span data-stu-id="0dba8-189">6</span></span>|<span data-ttu-id="0dba8-190">2</span><span class="sxs-lookup"><span data-stu-id="0dba8-190">2</span></span>|<span data-ttu-id="0dba8-191">2</span><span class="sxs-lookup"><span data-stu-id="0dba8-191">2</span></span>|  

 <span data-ttu-id="0dba8-192">**Sachposten**</span><span class="sxs-lookup"><span data-stu-id="0dba8-192">**General Ledger Entries**</span></span>  

|<span data-ttu-id="0dba8-193">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="0dba8-193">Posting Date</span></span>|<span data-ttu-id="0dba8-194">Sachkonto</span><span class="sxs-lookup"><span data-stu-id="0dba8-194">G/L Account</span></span>|<span data-ttu-id="0dba8-195">Kontonr. (En-US-Demo)</span><span class="sxs-lookup"><span data-stu-id="0dba8-195">Account No. (En-US Demo)</span></span>|<span data-ttu-id="0dba8-196">Betrag</span><span class="sxs-lookup"><span data-stu-id="0dba8-196">Amount</span></span>|<span data-ttu-id="0dba8-197">Lfd. Nr.</span><span class="sxs-lookup"><span data-stu-id="0dba8-197">Entry No.</span></span>|  
|------------------|------------------|---------------------------------|------------|---------------|  
|<span data-ttu-id="0dba8-198">01-15-20</span><span class="sxs-lookup"><span data-stu-id="0dba8-198">01-15-20</span></span>|<span data-ttu-id="0dba8-199">Lagerzugangskonto (Interim)</span><span class="sxs-lookup"><span data-stu-id="0dba8-199">Inventory Accrual Account (Interim)</span></span>|<span data-ttu-id="0dba8-200">5530</span><span class="sxs-lookup"><span data-stu-id="0dba8-200">5530</span></span>|<span data-ttu-id="0dba8-201">95.00</span><span class="sxs-lookup"><span data-stu-id="0dba8-201">95.00</span></span>|<span data-ttu-id="0dba8-202">4</span><span class="sxs-lookup"><span data-stu-id="0dba8-202">4</span></span>|  
|<span data-ttu-id="0dba8-203">01-15-20</span><span class="sxs-lookup"><span data-stu-id="0dba8-203">01-15-20</span></span>|<span data-ttu-id="0dba8-204">Lagerkonto (Interim)</span><span class="sxs-lookup"><span data-stu-id="0dba8-204">Inventory Account (Interim)</span></span>|<span data-ttu-id="0dba8-205">2131</span><span class="sxs-lookup"><span data-stu-id="0dba8-205">2131</span></span>|<span data-ttu-id="0dba8-206">-95.00</span><span class="sxs-lookup"><span data-stu-id="0dba8-206">-95.00</span></span>|<span data-ttu-id="0dba8-207">3</span><span class="sxs-lookup"><span data-stu-id="0dba8-207">3</span></span>|  
|<span data-ttu-id="0dba8-208">01-15-20</span><span class="sxs-lookup"><span data-stu-id="0dba8-208">01-15-20</span></span>|<span data-ttu-id="0dba8-209">Direkte Kosten Verrech.-Konto</span><span class="sxs-lookup"><span data-stu-id="0dba8-209">Direct Cost Applied Account</span></span>|<span data-ttu-id="0dba8-210">7291</span><span class="sxs-lookup"><span data-stu-id="0dba8-210">7291</span></span>|<span data-ttu-id="0dba8-211">-100</span><span class="sxs-lookup"><span data-stu-id="0dba8-211">-100</span></span>|<span data-ttu-id="0dba8-212">6</span><span class="sxs-lookup"><span data-stu-id="0dba8-212">6</span></span>|  
|<span data-ttu-id="0dba8-213">01-15-20</span><span class="sxs-lookup"><span data-stu-id="0dba8-213">01-15-20</span></span>|<span data-ttu-id="0dba8-214">Lagerkonto</span><span class="sxs-lookup"><span data-stu-id="0dba8-214">Inventory Account</span></span>|<span data-ttu-id="0dba8-215">2130</span><span class="sxs-lookup"><span data-stu-id="0dba8-215">2130</span></span>|<span data-ttu-id="0dba8-216">100</span><span class="sxs-lookup"><span data-stu-id="0dba8-216">100</span></span>|<span data-ttu-id="0dba8-217">5</span><span class="sxs-lookup"><span data-stu-id="0dba8-217">5</span></span>|  

## <a name="see-also"></a><span data-ttu-id="0dba8-218">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dba8-218">See Also</span></span>
 <span data-ttu-id="0dba8-219">[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md) </span><span class="sxs-lookup"><span data-stu-id="0dba8-219">[Design Details: Inventory Costing](design-details-inventory-costing.md) </span></span>  
 <span data-ttu-id="0dba8-220">[Designdetails: Kostenregulierung](design-details-cost-adjustment.md) </span><span class="sxs-lookup"><span data-stu-id="0dba8-220">[Design Details: Cost Adjustment](design-details-cost-adjustment.md) </span></span>  
 <span data-ttu-id="0dba8-221">[Designdetails: Abgleich mit der Finanzbuchhaltung](design-details-reconciliation-with-the-general-ledger.md) </span><span class="sxs-lookup"><span data-stu-id="0dba8-221">[Design Details: Reconciliation with the General Ledger](design-details-reconciliation-with-the-general-ledger.md) </span></span>  
 <span data-ttu-id="0dba8-222">[Designdetails: Bestandsbuchung](design-details-inventory-posting.md) </span><span class="sxs-lookup"><span data-stu-id="0dba8-222">[Design Details: Inventory Posting](design-details-inventory-posting.md) </span></span>  
 [<span data-ttu-id="0dba8-223">Designdetails: Abweichung</span><span class="sxs-lookup"><span data-stu-id="0dba8-223">Design Details: Variance</span></span>](design-details-variance.md)  
 [<span data-ttu-id="0dba8-224">Verwalten der Lagerregulierung</span><span class="sxs-lookup"><span data-stu-id="0dba8-224">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
 [<span data-ttu-id="0dba8-225">Finanzen</span><span class="sxs-lookup"><span data-stu-id="0dba8-225">Finance</span></span>](finance.md)  
 <span data-ttu-id="0dba8-226">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="0dba8-226">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

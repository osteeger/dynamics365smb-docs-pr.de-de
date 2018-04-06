---
title: Buchungsdatum auf Wertposten
description: Erfahren Sie wie die Stapelverarbeitung Lagerreg gekennzeichnet wird und ein Buchungsdatum auf Wertposten zugewiesen wird, der die Stapelverarbeitung erstellt.
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 11/23/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: b34f276a764f0e828fbc1f015429df9852242a4c
ms.openlocfilehash: 254d4451504c06091cd3fc5050f29da09db0de7f
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-posting-date-on-adjustment-value-entry"></a><span data-ttu-id="4fdd0-103">Designdetails: Buchungsdatum auf Ausgleichs-Wertposten</span><span class="sxs-lookup"><span data-stu-id="4fdd0-103">Design Details: Posting Date on Adjustment Value Entry</span></span>
<span data-ttu-id="4fdd0-104">Dieser Artikel setzt Anleitung für Benutzer der Lager-Kostenberechnungsfunktionalität fest in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span><span class="sxs-lookup"><span data-stu-id="4fdd0-104">This article provides guidance for users of the Inventory Costing functionality in [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span> <span data-ttu-id="4fdd0-105">Der spezifische Artikel informiert, wie die Stapelverarbeitung **Lagerreg. fakt. Einst.-Preise** kennzeichnet und ein Buchungsdatum auf Wertposten zuweist, die die Stapelverarbeitung erstellt.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-105">The specific article is providing guidance in how the **Adjust Cost - Item Entries** batch job identifies and assigns a posting date to the value entries that the batch job is about to create.</span></span>  

<span data-ttu-id="4fdd0-106">Zuerst wird der Begriff des Prozesses wiederholt, wie die Stapelverarbeitung das Buchungsdatum zuweist und Wertposten erstellt.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-106">First the concept of the process is reviewed, how the batch job identifies and assigns the Posting Date to the Value Entry to be created.</span></span> <span data-ttu-id="4fdd0-107">Danach gibt es einige freigegebene Szenarien, auf die wir Support-Team gelegentlich stoßen und es gibt eine Zusammenfassung der Begriffe, die aus Version 3.0 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-107">Thereafter there are some scenarios shared that we in the support team come across from time to time and finally there is a summary of the concepts used from version 3.0.</span></span>  

## <a name="the-concept"></a><span data-ttu-id="4fdd0-108">Das Konzept</span><span class="sxs-lookup"><span data-stu-id="4fdd0-108">The Concept</span></span>  
<span data-ttu-id="4fdd0-109">Ab Version 5.0 weist die **Lagerreg. fakt. Einst. Preise** Stapelverarbeitung ein Buchungsdatum dem Wertposten zu, den sie im Begriffe ist, in den nachfolgenden Schritten zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-109">From version 5.0, the **Adjust Cost – Item Entries** batch job assigns a posting date to the value entry it is about to create in the following steps:</span></span>  

1.  <span data-ttu-id="4fdd0-110">Das Buchungsdatum des Postens hat das gleiche Datum, wie der angepasste Posten.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-110">Initially the Posting Date of the entry to be created is the same date as the entry it adjusts.</span></span>  

2.  <span data-ttu-id="4fdd0-111">Das Buchungsdatum wird mit den Lagerbuchungsperioden und/oder Finanzbuchhaltungseinrichtung überprüft.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-111">The Posting Date is validated against Inventory Periods and/or General Ledger Setup.</span></span>  

3.  <span data-ttu-id="4fdd0-112">Zuweisung des Buchungdatums; wenn das ursprüngliche Buchungsdatum nicht innerhalb des Bereichs des zugelassenen Buchungszeitraums liegt, wird die Stapelverarbeitung ein zulässiges Buchungsdatum aus entweder Finanzbuchhaltungseinrichtung oder Lagerbuchungsperiode zuweisen.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-112">Assignment of Posting Date; If the initial Posting Date is not within allowed posting date range the batch job will assign an allowed Posting Date from either General Ledger Setup or Inventory Period.</span></span> <span data-ttu-id="4fdd0-113">Wenn die Lagerbuchungsperioden und die zugelassenen Buchungszeiträume in der Finanzbuchhaltungseinrichtung festgelegt wurden, wird das Datum der beiden dem Ausgleichs-Wertposten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-113">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will be assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="4fdd0-114">Lassen Sie uns dieses Verfahren in der Praxis überprüfen.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-114">Let’s review this process more in practice.</span></span> <span data-ttu-id="4fdd0-115">Angenommen, wir haben einen Artikelposten zum Verkauf.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-115">Assume we have an Item Ledger Entry of Sale.</span></span> <span data-ttu-id="4fdd0-116">Der Artikel wurde am 5. September 2013 geliefert und er wurde am darauffolgenden Tag fakturiert.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-116">The item was shipped on September 5th, 2013 and it was invoiced the day after.</span></span>  

<span data-ttu-id="4fdd0-117">![Artikelposten: Datumsformat JJJJ MM TT](media/helene/TechArticleAdjustcost1.png "TechArticleAdjustcost1")</span><span class="sxs-lookup"><span data-stu-id="4fdd0-117">![Item Ledger Entry: Date format: YYYY MM DD](media/helene/TechArticleAdjustcost1.png "TechArticleAdjustcost1")</span></span>  

<span data-ttu-id="4fdd0-118">Unten zeigt der erste Wertposten (379) die Lieferung an und enthält dasselbe Buchungsdatum wie der Posten des übergeordneten Artikels.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-118">Below, the first Value Entry (379) represents the shipment and carry the same Posting Date as the parent Item ledger Entry.</span></span>  

<span data-ttu-id="4fdd0-119">Der zweite Wertposten (381) zeigt die Rechnung an.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-119">The second Value Entry (381) represents the invoice.</span></span>  

 <span data-ttu-id="4fdd0-120">Der dritte Wertposten (391) ist eine Anpassung des Wertpostens Rechnungsstellung (381)</span><span class="sxs-lookup"><span data-stu-id="4fdd0-120">The third Value Entry (391) is an Adjustment of the invoicing Value Entry (381)</span></span>  

 <span data-ttu-id="4fdd0-121">![Artikelposten: Datumsformat JJJJ MM TT](media/helene/TechArticleAdjustcost2.png "TechArticleAdjustcost2")</span><span class="sxs-lookup"><span data-stu-id="4fdd0-121">![Item Ledger Entry: Date format: YYYY MM DD](media/helene/TechArticleAdjustcost2.png "TechArticleAdjustcost2")</span></span>  

 <span data-ttu-id="4fdd0-122">Schritt 1: Der zu erstellende Wertposten wird dem selben Buchungsdatum zugeordnet, wie der angepasste Eintrag, wie in oben durch Wertposten 391 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-122">Step 1: Adjustment Value Entry to be created is assigned same Posting Date as the entry it adjusts, illustrated above by Value entry 391.</span></span>  

 <span data-ttu-id="4fdd0-123">Schritt 2: Prüfung des zugewiesenen Buchungsdatums.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-123">Step 2: Validation of initial assigned Posting Date.</span></span>  

<span data-ttu-id="4fdd0-124">Die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise** bestimmt, ob das ursprüngliche Buchungsdatum des Ausgleichs-Wertpostens innerhalb des Bereichs des zugelassenen Buchungszeitraums ist, der auf Lagerbuchungsperioden und/oder Finanzbuchhaltungseinrichtung basiert.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-124">The **Adjust Cost – Item Entries** batch job determines if the initial Posting Date of the Adjustment Value Entry is within allowed posting date range based upon Inventory Periods and/or General Ledger Setup.</span></span>  

 <span data-ttu-id="4fdd0-125">Wir überprüfen den oben erwähnten Verkauf, indem wir die zugelassenen Buchungszeiträume hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-125">Let’s review the above mentioned Sale by adding setup of allowed posting date ranges.</span></span>  

 <span data-ttu-id="4fdd0-126">Lagerbuchungsperioden:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-126">Inventory Periods:</span></span>  

<span data-ttu-id="4fdd0-127">![Kosten anpassen; Artikeleingabedaten](media/helene/TechArticleAdjustcost3.png "TechArticleAdjustcost3")</span><span class="sxs-lookup"><span data-stu-id="4fdd0-127">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost3.png "TechArticleAdjustcost3")</span></span>

 <span data-ttu-id="4fdd0-128">Erster zugelassener Buchungszeitraum ist der erste Tag der ersten offenen Periode.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-128">First allowed posting date is the first day in the first open period.</span></span> <span data-ttu-id="4fdd0-129">1. September 2013.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-129">September 1st, 2013.</span></span>  

 <span data-ttu-id="4fdd0-130">Finanzbuchhaltungs-Einrichtung:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-130">General Ledger Setup:</span></span>  

<span data-ttu-id="4fdd0-131">![Kosten anpassen; Artikeleingabedaten](media/helene/TechArticleAdjustcost4.png "TechArticleAdjustcost4")</span><span class="sxs-lookup"><span data-stu-id="4fdd0-131">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost4.png "TechArticleAdjustcost4")</span></span>

 <span data-ttu-id="4fdd0-132">Erster zugelassener Buchungszeitraum ist das Datum, das im Feld angezeigt wird, ab 10. September 2013.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-132">First allowed posting date is the date stated in field Allow Posting From: September 10th, 2013.</span></span>  

 <span data-ttu-id="4fdd0-133">Wenn die Lagerbuchungsperioden und die zugelassenen Buchungszeiträume in der Finanzbuchhaltungseinrichtung festgelegt wurden, wird das Datum der beiden dem zugelassenen Ausgleichs-Wertposten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-133">If both Inventory Periods and allowed posting dates in General Ledger Setup are defined, the later date of the two will define the allowed posting date range.</span></span>  

 <span data-ttu-id="4fdd0-134">Schritt 3: Zuweisung eines zugelassenen Buchungszeitraums;</span><span class="sxs-lookup"><span data-stu-id="4fdd0-134">Step 3: Assignment of an allowed posting date;</span></span>  

 <span data-ttu-id="4fdd0-135">Das zugewiesene Buchungsdatum war 6. September, wie in Schritt 1 veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-135">The initial assigned Posting Date was September 6th as illustrated in step 1.</span></span> <span data-ttu-id="4fdd0-136">Wenn jedoch in 2. Schritt die Stapelverarbeitung Lagerreg kennzeichnet, dass frühester zugelassener Buchungszeitraum am 10. September ist weist sie den 10. September dem Ausgleichs-Wertposten zu.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-136">However, in the 2nd step the Adjust Cost – Item entries batch job identifies that earliest allowed Posting Date is September 10th and thereby assigns September 10th to the Adjustment Value Entry, below.</span></span>  

 <span data-ttu-id="4fdd0-137">![Kosten anpassen; Artikeleingabedaten](media/helene/TechArticleAdjustcost5.png "TechArticleAdjustcos5")</span><span class="sxs-lookup"><span data-stu-id="4fdd0-137">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost5.png "TechArticleAdjustcost5")</span></span>

 <span data-ttu-id="4fdd0-138">Es haben jetzt das Vorgehen für das Zuweisen von Buchungsdaten für Werteinträge wiederholt, durch die Stapelverarbeitung Lagerreg. fakt. Einst. Preise.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-138">We have now reviewed the concept for assigning Posting Dates to Value Entries created by the Adjust Cost - Item entries batch job.</span></span>  

 <span data-ttu-id="4fdd0-139">Lassen Sie uns fortfahren, um verschiedene Szenarien zu überprüfen, auf die wir im Support-Team gelegentlich stoßen, und zwar in Bezug auf ein Buchungsdatum in der Stapelverarbeitung Lagerreg und dem Zuordnen der zugehörigen Einrichtung.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-139">Let’s continue to review some scenarios that we in the support team comes across from time to time in relation to assigned Posting Dates in the Adjust Cost – Item entries batch job and related setups.</span></span>  

## <a name="scenarios"></a><span data-ttu-id="4fdd0-140">Szenarien</span><span class="sxs-lookup"><span data-stu-id="4fdd0-140">Scenarios</span></span>  

### <a name="scenario-i-posting-date-is-not-within-your-range-of-allowed-posting-dates"></a><span data-ttu-id="4fdd0-141">Szenario I: "Buchungsdatum liegt nicht innerhalb des zugelassenen Buchungszeitraums..."</span><span class="sxs-lookup"><span data-stu-id="4fdd0-141">Scenario I: “Posting Date is not within your range of allowed posting dates…”</span></span>  
 <span data-ttu-id="4fdd0-142">Dies ist ein Szenario, in dem ein Benutzer eine Fehlermeldung erhält, wenn die Lagerreg. fakt. Einst. Preise Stapelverarbeitung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-142">This is a scenario where a user is experiencing mentioned error message when the Adjust Cost – Item entries batch job is run.</span></span>  

 <span data-ttu-id="4fdd0-143">Im vorherigen Abschnitt wird das Vorgehen für das Zuweisen des Buchungdatums beschrieben, die  Absicht der Stapelverarbeitung Lagerreg. fakt. Einst. Preise ist es, einen Wertposten mit Buchungsdatum am 10. September zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-143">In the previous section, describing the concept of assigning posting dates, the intention of the Adjust Cost – Item entries batch job is to create a Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="4fdd0-144">![Kosten anpassen; Artikeleingabedaten](media/helene/TechArticleAdjustcost6.png "TechArticleAdjustcos6")</span><span class="sxs-lookup"><span data-stu-id="4fdd0-144">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost6.png "TechArticleAdjustcost6")</span></span>

 <span data-ttu-id="4fdd0-145">Wir nehmen die Benutzer Einrichtung nochmals auf:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-145">We follow up on the User Setup:</span></span>  

<span data-ttu-id="4fdd0-146">![Kosten anpassen; Artikeleingabedaten](media/helene/TechArticleAdjustcost7.png "TechArticleAdjustcos7")</span><span class="sxs-lookup"><span data-stu-id="4fdd0-146">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost7.png "TechArticleAdjustcost7")</span></span>

 <span data-ttu-id="4fdd0-147">Der Anwender hat in diesem Fall einen Bereich des zugelassenen Buchungszeitraums vom 11. September bis zum 30. September und es wird dadurch nicht erlaubt, den Ausgleichs-Wertposten mit dem Buchungsdatum am 10. September zu buchen.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-147">The user in this case has an allowed posting date range from September 11th to September 30th and is thereby not allowed to post the Adjustment Value Entry with Posting Date September 10th.</span></span>  

<span data-ttu-id="4fdd0-148">![Kosten anpassen; Artikeleingabedaten](media/helene/TechArticleAdjustcost8.png "TechArticleAdjustcos8")</span><span class="sxs-lookup"><span data-stu-id="4fdd0-148">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost8.png "TechArticleAdjustcost8")</span></span>

 <span data-ttu-id="4fdd0-149">Knowledge Base-Artikel [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) erläutert die zusätzlichen Szenarien, die mit erwähnter Fehlermeldung verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-149">Knowledge Base article [952996](https://mbs2.microsoft.com/Knowledgebase/kbdisplay.aspx?WTNTZSMNWUKNTMMYXUPYZQPOUXNXSPSYOQQYYMLUQLOYYMWP) discusses additional scenarios related to mentioned error message.</span></span>  

### <a name="scenario-ii-posting-date-on-adjustment-value-entry-versus-posting-date-on-entry-causing-the-adjustment-such-as-revaluation-or-item-charge"></a><span data-ttu-id="4fdd0-150">Szenario II: Buchungsdatum auf Wertposten mit Buchungsdatum des Postens, der dem Ausgleich wie Neubewertung oder Artikel Zu-/Abschlag zugeordnet wird</span><span class="sxs-lookup"><span data-stu-id="4fdd0-150">Scenario II: Posting Date on Adjustment Value Entry versus Posting Date on entry causing the adjustment such as Revaluation or Item charge.</span></span>  

### <a name="revaluation-scenario"></a><span data-ttu-id="4fdd0-151">Neubewertungsszenario:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-151">Revaluation scenario:</span></span>  
 <span data-ttu-id="4fdd0-152">Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-152">Prerequisites:</span></span>  

 <span data-ttu-id="4fdd0-153">Lagereinrichtung:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-153">Inventory setup:</span></span>  

-   <span data-ttu-id="4fdd0-154">Automatische Lagerbuchung = Ja</span><span class="sxs-lookup"><span data-stu-id="4fdd0-154">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="4fdd0-155">Automatische Lagerregulierung = Immer</span><span class="sxs-lookup"><span data-stu-id="4fdd0-155">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="4fdd0-156">Einst.-Pr.(durchschn.)Ber.-Art = Artikel</span><span class="sxs-lookup"><span data-stu-id="4fdd0-156">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="4fdd0-157">Durchschnittskostenperiode= Tag</span><span class="sxs-lookup"><span data-stu-id="4fdd0-157">Average Cost Period=Day</span></span>  

 <span data-ttu-id="4fdd0-158">Finanzbuchhaltungs-Einrichtung:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-158">General Ledger Setup:</span></span>  

-   <span data-ttu-id="4fdd0-159">Zulassen Buchung von = am 1. Januar 2014</span><span class="sxs-lookup"><span data-stu-id="4fdd0-159">Allow Posting From = January 1st, 2014</span></span>  

-   <span data-ttu-id="4fdd0-160">Anlagenbuchungen zugel. bis= leer</span><span class="sxs-lookup"><span data-stu-id="4fdd0-160">Allow Posting To = empty</span></span>  

 <span data-ttu-id="4fdd0-161">Benutzereinrichtung:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-161">User Setup:</span></span>  

-   <span data-ttu-id="4fdd0-162">Zulassen Buchung von = 1. Dezember 2013.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-162">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="4fdd0-163">Anlagenbuchungen zugel. bis= leer</span><span class="sxs-lookup"><span data-stu-id="4fdd0-163">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="4fdd0-164">So führen Sie ein Testszenario aus</span><span class="sxs-lookup"><span data-stu-id="4fdd0-164">To test the scenario</span></span>  

1.  <span data-ttu-id="4fdd0-165">Artikel TEST erstellen:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-165">Create item TEST:</span></span>  

     <span data-ttu-id="4fdd0-166">Basismaßeinheit = PCS</span><span class="sxs-lookup"><span data-stu-id="4fdd0-166">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="4fdd0-167">Kostenberechnungsmethode = Durchschnitt</span><span class="sxs-lookup"><span data-stu-id="4fdd0-167">Costing Method = Average</span></span>  

     <span data-ttu-id="4fdd0-168">Wählen Sie Buchungsgruppen optional aus.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-168">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="4fdd0-169">Buch.-Blatt öffnen und eine Zeile wie folgt erstellen und buchen:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-169">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="4fdd0-170">Buchungsdatum =  15. Dezember 2013</span><span class="sxs-lookup"><span data-stu-id="4fdd0-170">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="4fdd0-171">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="4fdd0-171">Item = TEST</span></span>  

     <span data-ttu-id="4fdd0-172">Eink.-Posten ausgleichen = Einkauf</span><span class="sxs-lookup"><span data-stu-id="4fdd0-172">Entry Type = Purchase</span></span>  

     <span data-ttu-id="4fdd0-173">Menge = 100</span><span class="sxs-lookup"><span data-stu-id="4fdd0-173">Quantity = 100</span></span>  

     <span data-ttu-id="4fdd0-174">Stückpreis = 10</span><span class="sxs-lookup"><span data-stu-id="4fdd0-174">Unit Amount = 10</span></span>  

3.  <span data-ttu-id="4fdd0-175">Buch.-Blatt öffnen und eine Zeile wie folgt erstellen und buchen:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-175">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="4fdd0-176">Datum = 20. Dezember 2013</span><span class="sxs-lookup"><span data-stu-id="4fdd0-176">Date = December 20th, 2013</span></span>  

     <span data-ttu-id="4fdd0-177">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="4fdd0-177">Item = TEST</span></span>  

     <span data-ttu-id="4fdd0-178">Eingangsart = Negative Anpassung</span><span class="sxs-lookup"><span data-stu-id="4fdd0-178">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="4fdd0-179">Menge = 2</span><span class="sxs-lookup"><span data-stu-id="4fdd0-179">Quantity = 2</span></span>  

4.  <span data-ttu-id="4fdd0-180">Buch.-Blatt öffnen und eine Zeile wie folgt erstellen und buchen:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-180">Open Item Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="4fdd0-181">Datum = 15. Januar 2014</span><span class="sxs-lookup"><span data-stu-id="4fdd0-181">Date = January 15th, 2014</span></span>  

     <span data-ttu-id="4fdd0-182">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="4fdd0-182">Item = TEST</span></span>  

     <span data-ttu-id="4fdd0-183">Eingangsart = Negative Anpassung</span><span class="sxs-lookup"><span data-stu-id="4fdd0-183">Entry Type = Negative Adjustment</span></span>  

     <span data-ttu-id="4fdd0-184">Menge = 3</span><span class="sxs-lookup"><span data-stu-id="4fdd0-184">Quantity = 3</span></span>  

5.  <span data-ttu-id="4fdd0-185">Buch.-Blatt Neubewertung öffnen und eine Zeile wie folgt erstellen und buchen:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-185">Open Revaluation Journal, create and post a line as follows:</span></span>  

     <span data-ttu-id="4fdd0-186">Artikel = TEST</span><span class="sxs-lookup"><span data-stu-id="4fdd0-186">Item = TEST</span></span>  

     <span data-ttu-id="4fdd0-187">Auf Eintrag anwenden = Einkaufsposten auswählen, der unter Schritt 2 gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-187">Applies-to Entry = select Purchase entry posted at step 2.</span></span> <span data-ttu-id="4fdd0-188">Das Buchungsdatum der Neubewertung ist derselbe, wie der Posten, der angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-188">The Posting Date of the revaluation will be the same as the entry it adjusts.</span></span>  

     <span data-ttu-id="4fdd0-189">Einstandspreis neu bewertet = 40</span><span class="sxs-lookup"><span data-stu-id="4fdd0-189">Unit Cost Revalued = 40</span></span>  

 <span data-ttu-id="4fdd0-190">Die folgenden Artikel- und Wertposten wurden gebucht:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-190">The following Item Ledger and Value Entries have been posted:</span></span>  

<span data-ttu-id="4fdd0-191">![Kosten anpassen; Artikeleingabedaten](media/helene/TechArticleAdjustcost9.png "TechArticleAdjustcos9")</span><span class="sxs-lookup"><span data-stu-id="4fdd0-191">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost9.png "TechArticleAdjustcost9")</span></span>

 <span data-ttu-id="4fdd0-192">![Kosten anpassen; Artikeleingabedaten](media/helene/TechArticleAdjustcost10.png "TechArticleAdjustcos10")</span><span class="sxs-lookup"><span data-stu-id="4fdd0-192">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost10.png "TechArticleAdjustcost10")</span></span>

 <span data-ttu-id="4fdd0-193">Die Stapelverarbeitung Lagerreg hat eine Änderung der Kosten realisiert und die negative Anpassung vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-193">The Adjust Cost – Item entries batch job has recognized a change in cost and adjusted the Negative Adjustments.</span></span>  

 <span data-ttu-id="4fdd0-194">**Überprüfung Buchungsdatum des erstellten Ausgleichs-Wertposten:** Der früheste zugelassene Buchungszeitraum, den die Stapelverarbeitung Lagerreg verknüpft, ist am 1. Januar 2014, wie in der Finanzbuchhaltungs-Einrichtung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-194">**Review of Posting Dates on created Adjustment Value Entries:** The earliest allowed Posting Date the Adjust Cost - Item Entries batch job has to relate to is January 1st, 2014 as stated in the General Ledger Setup.</span></span>  

 <span data-ttu-id="4fdd0-195">**Negative Anpassung in Schritt 3:** zugewiesenes Buchungsdatum ist am 1. Januar, wie von der  Finanzbuchhaltung eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-195">**Negative Adjustment in step 3:** assigned Posting Date is January 1st, provided by General Ledger Setup.</span></span> <span data-ttu-id="4fdd0-196">Das Buchungsdatum des Wertpostens im Bereich für Ausgleich ist am 20. Dezember 2013.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-196">The Posting Date of the Value Entry in scope for adjustment is December 20, 2013.</span></span> <span data-ttu-id="4fdd0-197">Entsprechend der Finanzbuchhaltungseinrichtung ist das Datum nicht innerhalb des Bereichs des zugelassenen Buchungszeitraums.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-197">According to General Ledger Setup the date is not within allowed posting date range.</span></span> <span data-ttu-id="4fdd0-198">Daher werden die Buchungsdaten, die im Feld Buchungen zulassen in der Finanzbuchhaltungs-Einrichtung festgelegt sind, den Ausgleichs-Wertposten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-198">Therefore the Posting Date stated in the Allow Posting From field in the General Ledger Setup is assigned to the Adjustment Value Entry.</span></span>  

 <span data-ttu-id="4fdd0-199">**Abgang in Schritt 4:** weist Buchungsdatum 15. Januar auf.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-199">**Negative Adjustment in step 4:** assigned Posting Date is January 15th.</span></span> <span data-ttu-id="4fdd0-200">Der Wertposten im Bereich des Ausgleichs hat Buchungsdatum am 15. Januar, das innerhalb des Bereichs des zugelassenen Buchungszeitraums entsprechend der Finanzbuchhaltungseinrichtung ist.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-200">The Value Entry in scope of adjustment has Posting Date January 15th, which is within the allowed posting date range according to General Ledger Setup.</span></span>  

 <span data-ttu-id="4fdd0-201">Der Ausgleich, der für den Abgang in Schritt 3 geändert wird, verursacht Diskussionen.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-201">The adjustment made for the Negative Adjustment in step 3 causes discussion.</span></span> <span data-ttu-id="4fdd0-202">Das bevorzugte Buchungsdatum für den Ausgleichs-Wertposten wäre am 20. Dezember oder mindestens im Dezember während die Neubewertung eine Änderung im Lagerverbrauch verursacht, der im Dezember gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-202">The favorable Posting Date for the Adjustment Value Entry would have been December 20th or at least within December as the revaluation causing the change in COGS was posted in December.</span></span>  

 <span data-ttu-id="4fdd0-203">Um den Ausgleich im Dezember im Feld Abgang in Schritt 3 zu erzielen, gestattet die Finanzbuchhaltungseinrichtung die Buchung aus dem Feld und es muss ein Datum im Dezember angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-203">To achieve adjustment in December of the Negative Adjustment in step 3, the General Ledger Setup, Allow Posting From field, need to state a date in December.</span></span>  

 <span data-ttu-id="4fdd0-204">**Schlussfolgerung:**</span><span class="sxs-lookup"><span data-stu-id="4fdd0-204">**Conclusion:**</span></span>  

 <span data-ttu-id="4fdd0-205">Mit den Erfahrungen aus diesem Szenarien, ziehen Sie die geeignetsten Einstellungen des Bereichs des zugelassenen Buchungszeitraums für ein Unternehmen in betrachtend. Folgendes kann hilfreich sein: Solange Veränderungen des Lagerwerts zulässig sind und in einer Periode gebucht werden können, in diesem Fall im Dezember, sollte die Einrichtung, die das Unternehmen für das Buchen von Buchungszeiträumen nutzt, mit diesem Entscheid übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-205">With the experiences from this scenario, considering most suitable setup of allowed posting date range for a company, the following might be useful: As long as changes in inventory value is allowed to be posted in a period, December in this case, the setup the company uses for allowed posting date ranges should be aligned with this decision.</span></span> <span data-ttu-id="4fdd0-206">Buchung von zulassen in der Finanzbuchhaltungs-Einrichtung, in diesem Fall der 1. Dezember, würde die Neubewertung ermöglichen, die im Dezember erfolgte und an betroffene ausgehenden Posten in derselben Periode weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-206">The Allow Posting From in the General Ledger Setup, stating December 1st  would allow the revaluation made in December to be forwarded to affected outbound entries in the same period.</span></span>  

 <span data-ttu-id="4fdd0-207">Die Benutzergruppen, die nicht erlaubt sind, um im Dezember gebucht zu werden, sondern im Januar, sind wahrscheinlich durch die Finanzbuchhaltungseinrichtung in diesem Szenario beschränkt und sollten stattdessen über die Benutzereinrichtung adressiert werden.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-207">User groups not allowed to post in December but in January, which was probably intended to be limited by the General Ledger Setup in this scenario, should instead be addressed via the User setup.</span></span>  

### <a name="item-charge-scenario"></a><span data-ttu-id="4fdd0-208">Artikel-Zu-/Abschlagszuweisung</span><span class="sxs-lookup"><span data-stu-id="4fdd0-208">Item charge scenario:</span></span>  
 <span data-ttu-id="4fdd0-209">Voraussetzungen:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-209">Prerequisites:</span></span>  

 <span data-ttu-id="4fdd0-210">Lagereinrichtung:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-210">Inventory setup:</span></span>  

-   <span data-ttu-id="4fdd0-211">Automatische Lagerbuchung = Ja</span><span class="sxs-lookup"><span data-stu-id="4fdd0-211">Automatic Cost Posting = Yes</span></span>  

-   <span data-ttu-id="4fdd0-212">Automatische Lagerregulierung = Immer</span><span class="sxs-lookup"><span data-stu-id="4fdd0-212">Automatic Cost Adjustment=Always</span></span>  

-   <span data-ttu-id="4fdd0-213">Einst.-Pr.(durchschn.)Ber.-Art = Artikel</span><span class="sxs-lookup"><span data-stu-id="4fdd0-213">Average Cost Calc. Type=item</span></span>  

-   <span data-ttu-id="4fdd0-214">Durchschnittskostenperiode= Tag</span><span class="sxs-lookup"><span data-stu-id="4fdd0-214">Average Cost Period=Day</span></span>  

 <span data-ttu-id="4fdd0-215">Finanzbuchhaltungs-Einrichtung:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-215">General Ledger Setup:</span></span>  

-   <span data-ttu-id="4fdd0-216">Zulassen Buchung von = 1. Dezember 2013.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-216">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="4fdd0-217">Anlagenbuchungen zugel. bis= leer</span><span class="sxs-lookup"><span data-stu-id="4fdd0-217">Allow Posting To = empty</span></span>  

 <span data-ttu-id="4fdd0-218">Benutzereinrichtung:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-218">User Setup:</span></span>  

-   <span data-ttu-id="4fdd0-219">Zulassen Buchung von = 1. Dezember 2013.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-219">Allow Posting From = December 1st, 2013.</span></span>  

-   <span data-ttu-id="4fdd0-220">Anlagenbuchungen zugel. bis= leer</span><span class="sxs-lookup"><span data-stu-id="4fdd0-220">Allow Posting to = empty</span></span>  

##### <a name="to-test-the-scenario"></a><span data-ttu-id="4fdd0-221">So führen Sie ein Testszenario aus</span><span class="sxs-lookup"><span data-stu-id="4fdd0-221">To test the scenario</span></span>  

1.  <span data-ttu-id="4fdd0-222">Artikel Zu-/Abschläge erstellen:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-222">Create item charge:</span></span>  

     <span data-ttu-id="4fdd0-223">Basismaßeinheit = PCS</span><span class="sxs-lookup"><span data-stu-id="4fdd0-223">Base unit of measure = PCS</span></span>  

     <span data-ttu-id="4fdd0-224">Kostenberechnungsmethode = Durchschnitt</span><span class="sxs-lookup"><span data-stu-id="4fdd0-224">Costing Method = Average</span></span>  

     <span data-ttu-id="4fdd0-225">Wählen Sie Buchungsgruppen optional aus.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-225">Select optional posting groups.</span></span>  

2.  <span data-ttu-id="4fdd0-226">Neue Bestellung erstellen</span><span class="sxs-lookup"><span data-stu-id="4fdd0-226">Create new purchase order</span></span>  

     <span data-ttu-id="4fdd0-227">Eink. von Kred.-Nr.: 10000</span><span class="sxs-lookup"><span data-stu-id="4fdd0-227">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="4fdd0-228">Buchungsdatum =  15. Dezember 2013</span><span class="sxs-lookup"><span data-stu-id="4fdd0-228">Posting Date = December 15th, 2013</span></span>  

     <span data-ttu-id="4fdd0-229">Kred.-Rechnungsnr.: 1234</span><span class="sxs-lookup"><span data-stu-id="4fdd0-229">Vendor Invoice No.: 1234</span></span>  

     <span data-ttu-id="4fdd0-230">Lagerdurchlaufzeit der Einkaufsbestellung:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-230">On the purchase order line:</span></span>  

     <span data-ttu-id="4fdd0-231">Artikel = ABSCHLAG</span><span class="sxs-lookup"><span data-stu-id="4fdd0-231">Item = CHARGE</span></span>  

     <span data-ttu-id="4fdd0-232">Menge = 1</span><span class="sxs-lookup"><span data-stu-id="4fdd0-232">Quantity = 1</span></span>  

     <span data-ttu-id="4fdd0-233">Direkte Einheitskosten = 100</span><span class="sxs-lookup"><span data-stu-id="4fdd0-233">Direct Unit Cost = 100</span></span>  

     <span data-ttu-id="4fdd0-234">Lieferung und Rechnung buchen.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-234">Post Receive and Invoice.</span></span>  

3.  <span data-ttu-id="4fdd0-235">Einen neuen Verkaufsauftrag erstellen:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-235">Create new sales order:</span></span>  

     <span data-ttu-id="4fdd0-236">Verk. an Deb.-Nr.: 10000</span><span class="sxs-lookup"><span data-stu-id="4fdd0-236">Sell-to Customer No.: 10000</span></span>  

     <span data-ttu-id="4fdd0-237">Buchungsdatum =  16. Dezember 2013</span><span class="sxs-lookup"><span data-stu-id="4fdd0-237">Posting Date = December 16th, 2013</span></span>  

     <span data-ttu-id="4fdd0-238">Lagerdurchlaufzeit der Einkaufsbestellung:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-238">On the sales order line:</span></span>  

     <span data-ttu-id="4fdd0-239">Artikel = ABSCHLAG</span><span class="sxs-lookup"><span data-stu-id="4fdd0-239">Item = CHARGE</span></span>  

     <span data-ttu-id="4fdd0-240">Menge = 1</span><span class="sxs-lookup"><span data-stu-id="4fdd0-240">Quantity = 1</span></span>  

     <span data-ttu-id="4fdd0-241">Einheitspreis = 135</span><span class="sxs-lookup"><span data-stu-id="4fdd0-241">Unit Price = 135</span></span>  

     <span data-ttu-id="4fdd0-242">Liefernung und Rechnung buchen.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-242">Post Ship and Invoice.</span></span>  

4.  <span data-ttu-id="4fdd0-243">Finanzbuchhaltungs-Einrichtung:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-243">General Ledger Setup:</span></span>  

     <span data-ttu-id="4fdd0-244">Zulassen Buchung von = am 1. Januar 2014</span><span class="sxs-lookup"><span data-stu-id="4fdd0-244">Allow Posting From = January 1st, 2014</span></span>  

     <span data-ttu-id="4fdd0-245">Anlagenbuchungen zugel. bis = leer</span><span class="sxs-lookup"><span data-stu-id="4fdd0-245">Allow Posting To = blank</span></span>  

5.  <span data-ttu-id="4fdd0-246">Neue Bestellung erstellen:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-246">Create new purchase order:</span></span>  

     <span data-ttu-id="4fdd0-247">Eink. von Kred.-Nr.: 10000</span><span class="sxs-lookup"><span data-stu-id="4fdd0-247">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="4fdd0-248">Buchungsdatum = 2. Januar 2014</span><span class="sxs-lookup"><span data-stu-id="4fdd0-248">Posting Date = January 2nd, 2014</span></span>  

     <span data-ttu-id="4fdd0-249">Kred.-Rechnungsnr.: 2345</span><span class="sxs-lookup"><span data-stu-id="4fdd0-249">Vendor Invoice No.: 2345</span></span>  

     <span data-ttu-id="4fdd0-250">Lagerdurchlaufzeit der Einkaufsbestellung:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-250">On the purchase order line:</span></span>  

     <span data-ttu-id="4fdd0-251">Artikelkosten = FRACHT</span><span class="sxs-lookup"><span data-stu-id="4fdd0-251">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="4fdd0-252">Menge = 1</span><span class="sxs-lookup"><span data-stu-id="4fdd0-252">Quantity = 1</span></span>  

     <span data-ttu-id="4fdd0-253">Direkte Einheitskosten = 3</span><span class="sxs-lookup"><span data-stu-id="4fdd0-253">Direct Unit Cost = 3</span></span>  

     <span data-ttu-id="4fdd0-254">Weisen Sie Artikeln Artikel-Zu-/Abschläge in die Einkaufslieferung von Schritt 2 zu.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-254">Assign Item Charge to Purchase Receipt from step 2.</span></span>  

     <span data-ttu-id="4fdd0-255">Empfang und Rechnung buchen.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-255">Post Receipt and Invoice.</span></span>  

     <span data-ttu-id="4fdd0-256">![Kosten anpassen; Artikeleingabedaten](media/helene/TechArticleAdjustcost11.png "TechArticleAdjustcos11")</span><span class="sxs-lookup"><span data-stu-id="4fdd0-256">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost11.png "TechArticleAdjustcost11")</span></span>

6.  <span data-ttu-id="4fdd0-257">Am Arbeitsdatum vom 3. Januar geht eine Einkaufsrechnung ein, die eine zusätzliche Belastung für den in Schritt 2 getätigten Einkauf enthält.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-257">On work date January 3rd a purchase invoice arrives, containing an additional item charge to the purchase made in step 2.</span></span> <span data-ttu-id="4fdd0-258">Diese Rechnung hat ein Belegdatum vom 30. Dezember und wird daher mit Buchungsdatum am 30. Dezember 2013 gebucht.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-258">This invoice has document date December 30th and is therefore posted with Posting Date December 30th, 2013.</span></span>  

     <span data-ttu-id="4fdd0-259">Neue Bestellung erstellen:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-259">Create new purchase order:</span></span>  

     <span data-ttu-id="4fdd0-260">Eink. von Kred.-Nr.: 10000</span><span class="sxs-lookup"><span data-stu-id="4fdd0-260">Buy-from Vendor No.: 10000</span></span>  

     <span data-ttu-id="4fdd0-261">Buchungsdatum =  30. Dezember 2013</span><span class="sxs-lookup"><span data-stu-id="4fdd0-261">Posting Date = December 30th, 2013</span></span>  

     <span data-ttu-id="4fdd0-262">Kred.-Rechnungsnr.: 3456</span><span class="sxs-lookup"><span data-stu-id="4fdd0-262">Vendor Invoice No.: 3456</span></span>  

     <span data-ttu-id="4fdd0-263">Lagerdurchlaufzeit der Einkaufsbestellung:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-263">On the purchase order line:</span></span>  

     <span data-ttu-id="4fdd0-264">Artikelkosten = FRACHT</span><span class="sxs-lookup"><span data-stu-id="4fdd0-264">Item Charge = JB-FREIGHT</span></span>  

     <span data-ttu-id="4fdd0-265">Menge = 1</span><span class="sxs-lookup"><span data-stu-id="4fdd0-265">Quantity = 1</span></span>  

     <span data-ttu-id="4fdd0-266">Direkte Einheitskosten = 2</span><span class="sxs-lookup"><span data-stu-id="4fdd0-266">Direct Unit Cost = 2</span></span>  

     <span data-ttu-id="4fdd0-267">Weisen Sie Artikeln Artikel-Zu-/Abschläge in die Einkaufslieferung von Schritt 2 zu.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-267">Assign Item Charge to Purchase Receipt from step 2</span></span>  

     <span data-ttu-id="4fdd0-268">Empfang und Rechnung buchen.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-268">Post Receipt and Invoice.</span></span>  

   <span data-ttu-id="4fdd0-269">![Kosten anpassen; Artikeleingabedaten](media/helene/TechArticleAdjustcost12.png "TechArticleAdjustcos12")</span><span class="sxs-lookup"><span data-stu-id="4fdd0-269">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost12.png "TechArticleAdjustcost12")</span></span>

 <span data-ttu-id="4fdd0-270">Lager-Bewertungsbericht wird mit 31. Dezember 2013 gedruckt</span><span class="sxs-lookup"><span data-stu-id="4fdd0-270">Inventory Valuation report is printed as of Date December 31st , 2013</span></span>  

<span data-ttu-id="4fdd0-271">![Kosten anpassen; Artikeleingabedaten](media/helene/TechArticleAdjustcost13.png "TechArticleAdjustcos13")</span><span class="sxs-lookup"><span data-stu-id="4fdd0-271">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost13.png "TechArticleAdjustcost13")</span></span>

 <span data-ttu-id="4fdd0-272">**Zusammenfassung des Szenarios:**</span><span class="sxs-lookup"><span data-stu-id="4fdd0-272">**Summary of scenario:**</span></span>  

 <span data-ttu-id="4fdd0-273">Das oben beschriebene Szenario endet mit einem Lager-Bewertungsbericht und zeigt Menge = 0 an, während der Wert = 2 beträgt.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-273">The described scenario ends up with an Inventory Valuation report demonstrating Quantity = 0 while the Value = 2.</span></span> <span data-ttu-id="4fdd0-274">Der Artikelzuschlag, der in Schritt 11 gebucht wird, ist ein Teil des Lagerzugangswerts vom Dezember, wohingegen der Lagerabgang derselben Periode nicht berücksichtigt wird.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-274">The Item charge posted in step 11 is part of the Inventory Increase value of December while the Inventory Decrease of the same period is not affected.</span></span>  

 <span data-ttu-id="4fdd0-275">Der Finanzbuchhaltungs-Einrichtung angeben, Buchungen ab dem 1. Januar zuzulassen, war für den ersten Artikel-Zu/Abschlag gut.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-275">Having the General Ledger Setup stating Allow Posting From January 1st was a good thing for the first Item charge.</span></span> <span data-ttu-id="4fdd0-276">Die Kosten des Lagerzugangs und des Feldes Abgang wurden in derselben Periode erfasst.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-276">The costs of the Inventory Increase and Decrease was recorded in the same period.</span></span> <span data-ttu-id="4fdd0-277">Für den zweiten Artikel-Zu-/Abschlag verursachte die Finanzbuchhaltungseinrichtung jedoch die Änderung im Lagerverbrauch, der in der Periode danach erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-277">For the second Item charge however, the General Ledger Setup causes the change in COGS to be recognized in the period after.</span></span>  

 <span data-ttu-id="4fdd0-278">**Schlussfolgerung:**</span><span class="sxs-lookup"><span data-stu-id="4fdd0-278">**Conclusion:**</span></span>  

 <span data-ttu-id="4fdd0-279">Es ist eine Herausforderung, den Bestandbewertungsbericht zu haben, um Menge = O anzuzeigen, während der Wert<> Wert 0 ist.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-279">It’s a challenge to have the Inventory Valuation report to demonstrate Quantity = 0 while the Value <> 0.</span></span> <span data-ttu-id="4fdd0-280">In diesem Fall ist es ebenfalls schwieriger, die optimalen Einstellungen zu finden, da Verkaufsrechnungen am gleichen Tag ankommen, jedoch verschiedene Perioden oder sogar Geschäftsjahre adressieren.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-280">In this case it’s also more difficult to express the optimal settings, having purchase invoices arriving the same day but addressing different periods or even fiscal years.</span></span> <span data-ttu-id="4fdd0-281">Das Eindringen in ein neues Geschäftsjahr erfordert normalerweise eine Absatzplanung ist Teil der Einblicke der Stapelverarbeitung Lagerreg Artikelposten und muss berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-281">Crossing to a new fiscal year usually requires some planning and as part of that the insight of Adjust Cost – Item entries process, recognizing COGS, is to be considered.</span></span>  

 <span data-ttu-id="4fdd0-282">In diesem Szenario könnte eine Option sein, die Finanzbuchhaltung so einzurichten, dass das Feld Buchung zulassen von ein Datum im Dezember für einige Tage mehr definiert und die Buchung des  Zuschlages des ersten Artikelpostens zurückgestellt wird, um die Kosten für die vorherige Periode/das vorherige Finanzjahr für die Periode zu ermöglichen, um alle Kosten dort zuzuweisen, wo sie zuerst erkannt wurden und dann die erlaubten Buchungsdaten in die neue Periode des \/ Steuerjahrs zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-282">In this scenario one option could have been to have the General Ledger Setup, field Allow Posting From, stating a date in December for a couple of more days and the posting of the first item charge postponed to allow all costs for the previous period/fiscal year to be recognized for the period they belong to first, having the Adjust Cost – Item entries batch job run and thereafter move the allowed posting date to the new period\/fiscal year.</span></span> <span data-ttu-id="4fdd0-283">Die Kosten des ersten Artikelpostens mit Buchungsdatum am 2. Januar dann gebucht werden.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-283">The first item charge with posting date January 2nd could then be posted.</span></span>  

## <a name="history-of-adjust-cost--item-entries-batch-job"></a><span data-ttu-id="4fdd0-284">Führen Sie die Stapelverarbeitung Lagerreg. fakt. Einst. Preise aus.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-284">History of Adjust Cost – Item entries batch job</span></span>  
 <span data-ttu-id="4fdd0-285">Unten finden Sie eine Zusammenfassung des Begriffs, der Buchungsdaten den Ausgleichs-Wertposten durch die Kostenanpassung Stapelverarbeitung seit Version 3.0 zuweist.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-285">Below is a summary of the concept assigning Posting Dates to Adjustment Value Entries by the Adjust Cost – Item entries batch job since version 3.0.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="4fdd0-286">Ab Version 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="4fdd0-286">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="4fdd0-287">Im Anforderungsformular der Stapelverarbeitung Lagerreg muss vom Benutzer ein Buchungsdatum eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-287">In the request form of the Adjust Cost - Item Entries batch job there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="4fdd0-288">Die Stapelverarbeitung wird durch alle erforderlichen Änderungen vorgenommen und erstellt Wertposten mit dem Buchungsdatum, das in das Anforderungsfenster eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-288">The batch job runs through all necessary changes and creates value entries with the posting date entered in the request form.</span></span> <span data-ttu-id="4fdd0-289">Das vorgeschlagene Buchungsdatum verwendet das heutige Datum.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-289">Suggested posting date to use is today’s date.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="4fdd0-290">Version 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="4fdd0-290">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="4fdd0-291">Im Anforderungsformular der Stapelverarbeitung Lagerreg muss vom Benutzer ein Buchungsdatum eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-291">In the request form of the Adjust Cost - Item Entries batch job there is a Closed Period Entry Posting Date to be entered by the user.</span></span> <span data-ttu-id="4fdd0-292">Die Stapelverarbeitung wird durch alle erforderlichen Änderungen vorgenommen und erstellt Wertposten mit dem Buchungsdatum des übergeordneten Artikels (Warenausgangsdatum des Verkaufs, das die Anpassung adressiert).</span><span class="sxs-lookup"><span data-stu-id="4fdd0-292">The batch job runs through all necessary changes and creates value entries with the posting date of the parent item ledger entry (shipment date of the sale that the adjustment address).</span></span> <span data-ttu-id="4fdd0-293">Wenn das Buchungsdatum des übergeordneten Artikels nicht innerhalb des Bereichs des zugelassenen Buchungszeitraums ist, wird das Buchungsdatum, das in Perioden-Posten-Buchungsdatum angegeben wird, den Wertposten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-293">If the posting date of the parent item ledger entry is not within allowed posting date range the posting date stated as Closed Period Entry Posting Date will be assigned the Adjustment Value Entry.</span></span> <span data-ttu-id="4fdd0-294">Ein Datum wird als in einer geschlossenen Periode angeschaut, wenn es vor dem Datum des Feldes  Buchungen zugel in der Finanzbuchhaltung liegt.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-294">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span>  

### <a name="from-version-50"></a><span data-ttu-id="4fdd0-295">Ab Version 5.0:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-295">From version 5.0:</span></span>  
 <span data-ttu-id="4fdd0-296">Es gibt kein Buchungsdatum mehr, das im Anforderungsformular der Stapelverarbeitung Lagerreg angegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-296">There is no longer a posting date to be stated in the request form of the Adjust Cost - Item entries batch job.</span></span> <span data-ttu-id="4fdd0-297">Die Stapelverarbeitung wird durch alle erforderlichen Änderungen vorgenommen und erstellt Wertposten mit dem Buchungsdatum, das in das Anforderungsfenster eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-297">The batch job runs through all necessary changes and creates value entries with the posting date of the value entry it adjusts.</span></span> <span data-ttu-id="4fdd0-298">Zuweisung des Buchungdatums; wenn das ursprüngliche Buchungsdatum nicht innerhalb des Bereichs des zugelassenen Buchungszeitraums liegt, wird die Stapelverarbeitung ein zulässiges Buchungsdatum aus entweder Finanzbuchhaltungseinrichtung oder Lagerbuchungsperiode zuweisen.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-298">If the posting date is not within allowed posting date range the posting date in the Allow Posting From field in the General Ledger Setup, OR if the Inventory periods are used, the later date of the two will be used.</span></span> <span data-ttu-id="4fdd0-299">vgl. Beschreibung des Konzepts oben.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-299">See described concept above.</span></span>  

## <a name="history-of-post-inventory-cost-to-gl-batch-job"></a><span data-ttu-id="4fdd0-300">Verlauf der Lagerkostenbuchung auf den Stapelverarbeitungseintrag</span><span class="sxs-lookup"><span data-stu-id="4fdd0-300">History of Post Inventory cost to G/L batch job</span></span>  
 <span data-ttu-id="4fdd0-301">Die Stapelverarbeitung "Lagerregulierung buchen" ist mit der Stapelverarbeitung Lagerreg eng verwandt, warum die Historie dieser Stapelverarbeitung auch hier zusammengefasst und freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-301">The Post Inventory Cost to G/L batch job is closely related to the Adjust Cost – Item entries batch job why the history of this batch job is summarized and shared here as well.</span></span>  

### <a name="from-version-30370a"></a><span data-ttu-id="4fdd0-302">Ab Version 3.0..3.70.A</span><span class="sxs-lookup"><span data-stu-id="4fdd0-302">From version 3.0..3.70.A</span></span>  
 <span data-ttu-id="4fdd0-303">Im Anforderungsformular der Stapelverarbeitung Lagerreg muss vom Benutzer ein Buchungsdatum eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-303">In the request form of the Post Inventory Cost to G/L there is a Posting Date to be entered by the user.</span></span> <span data-ttu-id="4fdd0-304">Die Stapelverarbeitung wird durch alle erforderlichen Änderungen vorgenommen und erstellt Wertposten mit dem Buchungsdatum, das in das Anforderungsfenster eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-304">The batch job runs through all value entries within the filter, if any, and creates General Ledger Entries with Posting Date entered in the request form.</span></span>  

### <a name="version-370b40"></a><span data-ttu-id="4fdd0-305">Version 3.70.B..4.0</span><span class="sxs-lookup"><span data-stu-id="4fdd0-305">Version 3.70.B..4.0</span></span>  
 <span data-ttu-id="4fdd0-306">Im Anforderungsformular der Stapelverarbeitung Lagerreg muss vom Benutzer ein Buchungsdatum eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-306">In the request form of the Post Inventory Cost to G/L the Closed Period Entry Posting Date field is available.</span></span> <span data-ttu-id="4fdd0-307">Die Anwendung verwendet das Datum, das Sie eingeben, wie auch das Buchungsdatum für die Sachposten für Wertposten, deren Buchungsdatum in abgeschlossenen Buchhaltungsperioden liegt.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-307">The program uses the date you enter in this field as the posting date for the general ledger entries it creates for value entries whose posting dates are in closed accounting periods.</span></span> <span data-ttu-id="4fdd0-308">Das Buchungsdatum der Sachposten ist das gleiche wie für die zugehörigen Wertposten.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-308">Otherwise, the general ledger entries will have the same posting date as the original value entries.</span></span> <span data-ttu-id="4fdd0-309">Ein Datum wird als in einer geschlossenen Periode angeschaut, wenn es vor dem Datum des Feldes  Buchungen zugel in der Finanzbuchhaltung liegt.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-309">A date is considered to be in a closed period when it is earlier than the date in the Allow Posting From field in the General Ledger Setup.</span></span> <span data-ttu-id="4fdd0-310">Wenn Sie GL\/pro Buchungsgruppe buchen, haben die Sachposten das Buchungsdatum, das Sie in dem Feld "Buchungsdatum" des Anforderungsformulars angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-310">If posting to G\/L Per Posting Group, the general ledger entries will have the posting date that is specified in the Posting Date field in the request form.</span></span>  

 <span data-ttu-id="4fdd0-311">In Version 3 und 4 scannt die Stapelverarbeitung alle Wertposteneinträge, um zu erkennen, ob es Wertposten gibt, bei denen der Kostenbetrag (tatsächl) von den gebuchten Kosten in der Finanzbuchhaltung abweicht.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-311">In version 3 and 4 the batch job scans all value entries to detect if there are any value entries where Cost Amount (Actual) differs from Cost Posted to G/L.</span></span> <span data-ttu-id="4fdd0-312">Wenn eine Differenz erkannt wird, wird der Unterschied in einem Sachposten gebucht.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-312">If there is a difference detected the differing amount will be posted in a G/L entry.</span></span> <span data-ttu-id="4fdd0-313">Wenn die erwartete Kostenbuchung verwendet wird, werden die entsprechenden Felder gleich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-313">If expected cost posting is used corresponding fields are processed in the same way.</span></span>  

<span data-ttu-id="4fdd0-314">![Kosten anpassen; Artikeleingabedaten](media/helene/TechArticleAdjustcost14.png "TechArticleAdjustcos14")</span><span class="sxs-lookup"><span data-stu-id="4fdd0-314">![Adjust cost &#45;Item entries data](media/helene/TechArticleAdjustcost14.png "TechArticleAdjustcost14")</span></span>

### <a name="from-version-50"></a><span data-ttu-id="4fdd0-315">Ab Version 5.0:</span><span class="sxs-lookup"><span data-stu-id="4fdd0-315">From version 5.0:</span></span>  
 <span data-ttu-id="4fdd0-316">Es gibt kein Buchungsdatum mehr, das im Anforderungsformular der Stapelverarbeitung Lagerreg angegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-316">There is no longer a posting date to be stated in the request form of the Post Inventory Cost to G/L batch job.</span></span> <span data-ttu-id="4fdd0-317">Die Sachposten werden mit dem gleichen Buchungsdatum wie der verwandter Wertposten erstellt.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-317">The G/L entry is created with the same Posting Date as the related value entry.</span></span> <span data-ttu-id="4fdd0-318">Um die Stapelverarbeitung auszuführen, muss der mittlere des zugelassenen Buchungszeitraums das Buchungsdatum des erstellten Sachpostens erlauben.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-318">In order to complete the batch job the allowed posting date range must allow the Posting Date of the created G/L entry.</span></span> <span data-ttu-id="4fdd0-319">Wenn nicht, muss sich der Standort des zugelassenen Buchungszeitraums durch das Ändern oder Entfernen des festgelegten Datumsfilters Buchungen zugel und aus den Feldern der Finanzbuchhaltungseinrichtung vorübergehend erneut geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-319">If not, the allowed posting date range must be temporarily re-opened by changing or removing the dates in the Allow Posting From and To fields in the General Ledger Setup.</span></span> <span data-ttu-id="4fdd0-320">Um Abstimmungsprobleme zu vermeiden ist es notwendig, dass das Buchungsdatum des Sachpostens zum Buchungsdatum des Wertpostens entspricht.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-320">To avoid reconciliation issues it is required that Posting Date of the G/L Entry corresponds to the Posting Date of the Value Entry.</span></span>  

 <span data-ttu-id="4fdd0-321">Die Stapelverarbeitungsscans scannt Tabelle 5811 - Buchen von Wertposten mit Sachkonten, um die Wertposten im Bereich für die Buchung auf das Sachkonto zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-321">The batch job scans Table 5811 - Post Value Entry to G/L, to identify the Value Entries in scope for posting to General Ledger.</span></span> <span data-ttu-id="4fdd0-322">Nach erfolgreicher Ausführung wird die Tabelle geleert.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-322">After successful run the table is emptied.</span></span>  

 <span data-ttu-id="4fdd0-323">Jedes möglicher Feedback zur weiteren Entwicklung der Prozesse und Dokumentation sind äußerst willkommen.</span><span class="sxs-lookup"><span data-stu-id="4fdd0-323">Any feedback to how this process and documentation can be further developed is very welcome.</span></span>  

 <span data-ttu-id="4fdd0-324">Helene Holmin</span><span class="sxs-lookup"><span data-stu-id="4fdd0-324">Helene Holmin</span></span>  

 <span data-ttu-id="4fdd0-325">Dynamics NAV Eskalations-Ingenieur</span><span class="sxs-lookup"><span data-stu-id="4fdd0-325">Dynamics NAV Escalation Engineer</span></span>  

## <a name="see-also"></a><span data-ttu-id="4fdd0-326">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fdd0-326">See Also</span></span>  
[<span data-ttu-id="4fdd0-327">Designdetails: Lagerkostenberechnung</span><span class="sxs-lookup"><span data-stu-id="4fdd0-327">Design Details: Inventory Costing</span></span>](design-details-inventory-costing.md)  
[<span data-ttu-id="4fdd0-328">Designdetails: Artikelausgleich</span><span class="sxs-lookup"><span data-stu-id="4fdd0-328">Design Details: Item Application</span></span>](design-details-item-application.md)  

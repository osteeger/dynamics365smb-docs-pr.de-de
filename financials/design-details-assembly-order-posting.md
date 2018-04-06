---
title: 'Designdetails: Montageauftragsbuchung | Microsoft Docs'
description: "Die Montageauftragsbuchung basiert auf demselben Prinzip wie das Buchen ähnlicher Aktivitäten von Verkaufsaufträgen und von Produktionsverbrauch/-aushabe. Die Prinzipien werden jedoch insofern kombiniert, als Montageaufträge ihre eigene Buchungsbenutzeroberfläche, wie für Verkaufsaufträge, haben, während die tatsächliche Postenbuchung im Hintergrund als direkte Artikel- und Ressourcen Buch.-Blattbuchung, wie für den Fertigungsverbrauch, Ausgabe und Kapazität geschieht."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 66590eb8ce7749658bad1fc3c9e54c1dff538abd
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="design-details-assembly-order-posting"></a><span data-ttu-id="5523b-104">Designdetails: Montageauftragsbuchung</span><span class="sxs-lookup"><span data-stu-id="5523b-104">Design Details: Assembly Order Posting</span></span>
<span data-ttu-id="5523b-105">Die Montageauftragsbuchung basiert auf demselben Prinzip wie das Buchen ähnlicher Aktivitäten von Verkaufsaufträgen und von Produktionsverbrauch/-aushabe.</span><span class="sxs-lookup"><span data-stu-id="5523b-105">Assembly order posting is based on the same principles as when posting the similar activities of sales orders and production consumption/output.</span></span> <span data-ttu-id="5523b-106">Die Prinzipien werden jedoch insofern kombiniert, als Montageaufträge ihre eigene Buchungsbenutzeroberfläche, wie für Verkaufsaufträge, haben, während die tatsächliche Postenbuchung im Hintergrund als direkte Artikel- und Ressourcen Buch.-Blattbuchung, wie für den Fertigungsverbrauch, Ausgabe und Kapazität geschieht.</span><span class="sxs-lookup"><span data-stu-id="5523b-106">However, the principles are combined in that assembly orders have their own posting UI, like that for sales orders, while the actual entry posting happens in the background as direct item and resource journal postings, like that for production consumption, output, and capacity.</span></span>  

<span data-ttu-id="5523b-107">Ähnlich wie bei der Fertigungsauftragsbuchung werden die verbrauchten Komponenten und die verwendeten Ressourcen konvertiert und als Montageartikel ausgegeben, wenn der Montageauftrag gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="5523b-107">Similarly to production order posting, the consumed components and the used resources are converted and output as the assembly item when the assembly order is posted.</span></span> <span data-ttu-id="5523b-108">Weitere Informationen finden Sie unter [Designdetails: Produktionsauftragsbuchung](design-details-production-order-posting.md).</span><span class="sxs-lookup"><span data-stu-id="5523b-108">For more information, see [Design Details: Production Order Posting](design-details-production-order-posting.md).</span></span> <span data-ttu-id="5523b-109">Der Kostenfluss für Montageaufträge ist jedoch weniger Komplex, insbesondere da die Buchung der Montagekosten nur einmal geschieht und daher keinen WIP-Bestand generiert.</span><span class="sxs-lookup"><span data-stu-id="5523b-109">However, the cost flow for assembly orders is less complex, especially because assembly cost posting only occurs once and therefore does not generate work-in-process inventory.</span></span>  

<span data-ttu-id="5523b-110">Die folgenden Buch.-Blattbuchungen treten während der Montageauftragsbuchung auf:</span><span class="sxs-lookup"><span data-stu-id="5523b-110">The following journal postings occur during assembly order posting:</span></span>  

-   <span data-ttu-id="5523b-111">Das Artikel Buch.-Blatt bucht die positiven Artikelposten, die Ausgabe des Montageartikels repräsentieren, aus dem Montageauftragskopf.</span><span class="sxs-lookup"><span data-stu-id="5523b-111">The item journal posts positive item ledger entries, representing output of the assembly item, from the assembly order header</span></span>  
-   <span data-ttu-id="5523b-112">Das Artikel Buch.-Blatt bucht die negativen Artikelposten, die den Verbrauch von Montagekomponenten repräsentieren, aus Montageauftragszeilen.</span><span class="sxs-lookup"><span data-stu-id="5523b-112">The item journal posts negative item ledger entries, representing consumption of assembly components, from the assembly order lines.</span></span>  
-   <span data-ttu-id="5523b-113">Das Ressourcen-Buch.-Blatt bucht den Verbrauch von Montageressourcen (Zeiteinheiten) aus den Montageauftragszeilen.</span><span class="sxs-lookup"><span data-stu-id="5523b-113">The resource journal posts usage of assembly resources (time units), from the assembly order lines.</span></span>  
-   <span data-ttu-id="5523b-114">Das Kapazitäts Buch.-Blatt bucht Wertposten bezüglich des Ressourcenverbrauchs, aus den Montageauftragszeilen.</span><span class="sxs-lookup"><span data-stu-id="5523b-114">The capacity journal posts value entries relating to the resource usage, from the assembly order lines.</span></span>  

<span data-ttu-id="5523b-115">Das folgende Diagramm zeigt die Struktur von Artikel- und Ressourcenposten, die aus der Montageauftragsbuchung resultieren.</span><span class="sxs-lookup"><span data-stu-id="5523b-115">The following diagram shows the structure of item and resource ledger entries that result from assembly order posting.</span></span>  

<span data-ttu-id="5523b-116">![Ressource und Kapazitätskosten](media/design_details_assembly_posting_1.png "design_details_assembly_posting_1")</span><span class="sxs-lookup"><span data-stu-id="5523b-116">![Resource and capacity costs](media/design_details_assembly_posting_1.png "design_details_assembly_posting_1")</span></span>  

> [!NOTE]  
>  <span data-ttu-id="5523b-117">Arbeitsplätze und Arbeitsplatzgruppen sind enthalten, um zu veranschaulichen, dass Kapazitätsposten aus der Produktion sowie aus der Montage erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="5523b-117">Machine and work centers are included to illustrate that capacity ledger entries are created from both production and assembly.</span></span>  

<span data-ttu-id="5523b-118">Die folgenden Diagramm zeigt, wie Montagedaten bei der Buchung in Buchungsposten eingehen.</span><span class="sxs-lookup"><span data-stu-id="5523b-118">The following diagram shows how assembly data flows into ledger entries during posting:</span></span>  

<span data-ttu-id="5523b-119">![Datenfluss beim Buchen](media/design_details_assembly_posting_2.png "design_details_assembly_posting_2")</span><span class="sxs-lookup"><span data-stu-id="5523b-119">![Data flow during posting](media/design_details_assembly_posting_2.png "design_details_assembly_posting_2")</span></span>  

## <a name="posting-sequence"></a><span data-ttu-id="5523b-120">Buchen der Sequenz</span><span class="sxs-lookup"><span data-stu-id="5523b-120">Posting Sequence</span></span>  
<span data-ttu-id="5523b-121">Die Buchung eines Montageauftrags erfolgt in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="5523b-121">The posting of an assembly order occurs in the following order:</span></span>  

1.  <span data-ttu-id="5523b-122">Die Montageauftragszeilen werden gebucht.</span><span class="sxs-lookup"><span data-stu-id="5523b-122">The assembly order lines are posted.</span></span>  
2.  <span data-ttu-id="5523b-123">Der Montageauftragskopf wird gebucht.</span><span class="sxs-lookup"><span data-stu-id="5523b-123">The assembly order header is posted.</span></span>  

<span data-ttu-id="5523b-124">In der folgenden Tabelle wird die Aktionsfolge illustriert.</span><span class="sxs-lookup"><span data-stu-id="5523b-124">The following table outlines the sequence of actions.</span></span>  

|<span data-ttu-id="5523b-125">Aktion</span><span class="sxs-lookup"><span data-stu-id="5523b-125">Action</span></span>|<span data-ttu-id="5523b-126">Description</span><span class="sxs-lookup"><span data-stu-id="5523b-126">Description</span></span>|  
|------------|-----------------|  
|<span data-ttu-id="5523b-127">Buchung initialisieren</span><span class="sxs-lookup"><span data-stu-id="5523b-127">Initialize Posting</span></span>|<span data-ttu-id="5523b-128">1.  Führen Sie Vorprüfungen durch.</span><span class="sxs-lookup"><span data-stu-id="5523b-128">1.  Make preliminary checks.</span></span><br /><span data-ttu-id="5523b-129">2.  Fügen Sie die Buchungsnummer hinzu, und ändern Sie den Montageauftragskopf.</span><span class="sxs-lookup"><span data-stu-id="5523b-129">2.  Add posting number and modify the assembly order header.</span></span><br /><span data-ttu-id="5523b-130">3.  Geben Sie den Montageauftrag frei.</span><span class="sxs-lookup"><span data-stu-id="5523b-130">3.  Release the assembly order.</span></span>|  
|<span data-ttu-id="5523b-131">Buchung</span><span class="sxs-lookup"><span data-stu-id="5523b-131">Post</span></span>|<ol><li><span data-ttu-id="5523b-132">Erstellen Sie den gebuchten Montageauftragskopf.</span><span class="sxs-lookup"><span data-stu-id="5523b-132">Create the posted assembly order header.</span></span></li><li><span data-ttu-id="5523b-133">Kommentarzeilen kopieren.</span><span class="sxs-lookup"><span data-stu-id="5523b-133">Copy comment lines.</span></span></li><li><span data-ttu-id="5523b-134">Beitragsmontageauftragszeilen (Verbrauch):</span><span class="sxs-lookup"><span data-stu-id="5523b-134">Post assembly order lines (consumption):</span></span><br /><br /> <ol><li><span data-ttu-id="5523b-135">Erstellen Sie ein Statusfenster, um den Montageverbrauch zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="5523b-135">Create a status window to calculate assembly consumption.</span></span></li><li><span data-ttu-id="5523b-136">Erhalten Sie die Restmenge, auf der die Artikel Buch.-Blattzeile basiert.</span><span class="sxs-lookup"><span data-stu-id="5523b-136">Get the remaining quantity on which the item journal line will be based.</span></span></li><li><span data-ttu-id="5523b-137">Setzen Sie die verbrauchten und die verbleibenden Mengen zurück.</span><span class="sxs-lookup"><span data-stu-id="5523b-137">Reset the consumed and remaining quantities.</span></span></li><li><span data-ttu-id="5523b-138">Für Montageauftragszeilen des Typs Artikel:</span><span class="sxs-lookup"><span data-stu-id="5523b-138">For assembly order lines of type Item:</span></span><br /><br /> <ol><li><span data-ttu-id="5523b-139">Füllen Sie die Felder in der Buch.-Blattzeile aus.</span><span class="sxs-lookup"><span data-stu-id="5523b-139">Populate fields on the item journal line.</span></span></li><li><span data-ttu-id="5523b-140">Übertragen Sie Reservierungen die Artikel Buch.-Blattzeile.</span><span class="sxs-lookup"><span data-stu-id="5523b-140">Transfer reservations to the item journal line.</span></span></li><li><span data-ttu-id="5523b-141">Buchen Sie die Artikel Buch.-Blattzeilen, um die Artikelposten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5523b-141">Post the item journal line to create the item ledger entries.</span></span></li><li><span data-ttu-id="5523b-142">Erstellen Sie Logistik Buch.-Blattzeilen, und buchen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="5523b-142">Create warehouse journal lines and post them.</span></span></li></ol></li><li><span data-ttu-id="5523b-143">Für Montageauftragszeilen des Typs Ressource:</span><span class="sxs-lookup"><span data-stu-id="5523b-143">For assembly order lines of type Resource:</span></span><br /><br /> <ol><li><span data-ttu-id="5523b-144">Füllen Sie die Felder in der Buch.-Blattzeile aus.</span><span class="sxs-lookup"><span data-stu-id="5523b-144">Populate fields on the item journal line.</span></span></li><li><span data-ttu-id="5523b-145">Buchen des Artikels Buch.-Blattzeile.</span><span class="sxs-lookup"><span data-stu-id="5523b-145">Post the item journal line.</span></span> <span data-ttu-id="5523b-146">Dies erstellt Kapazitätsposten.</span><span class="sxs-lookup"><span data-stu-id="5523b-146">This creates capacity ledger entries.</span></span></li><li><span data-ttu-id="5523b-147">Erstellen und buchen Sie Ressourcen-Buch.-Blattzeilen.</span><span class="sxs-lookup"><span data-stu-id="5523b-147">Create and post resource journal line.</span></span></li></ol></li><li><span data-ttu-id="5523b-148">Übertragen Sie Feldwerte aus der Montageauftragszeile in eine neu erstellte gebuchte Montageauftragszeile.</span><span class="sxs-lookup"><span data-stu-id="5523b-148">Transfer field values from the assembly order line into a newly created posted assembly order line.</span></span></li></ol></li><li><span data-ttu-id="5523b-149">Buchen Sie den Montageauftragskop (Ausgang):</span><span class="sxs-lookup"><span data-stu-id="5523b-149">Post the assembly order header (output):</span></span><br /><br /> <ol><li><span data-ttu-id="5523b-150">Füllen Sie die Felder in der Buch.-Blattzeile aus.</span><span class="sxs-lookup"><span data-stu-id="5523b-150">Populate fields on the item journal line.</span></span></li><li><span data-ttu-id="5523b-151">Übertragen Sie Reservierungen die Artikel Buch.-Blattzeile.</span><span class="sxs-lookup"><span data-stu-id="5523b-151">Transfer reservations to the item journal line.</span></span></li><li><span data-ttu-id="5523b-152">Buchen Sie die Artikel Buch.-Blattzeilen, um die Artikelposten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5523b-152">Post the item journal line to create the item ledger entries.</span></span></li><li><span data-ttu-id="5523b-153">Erstellen Sie Logistik Buch.-Blattzeilen, und buchen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="5523b-153">Create warehouse journal lines and post them.</span></span></li><li><span data-ttu-id="5523b-154">Setzen Sie die Montagemengen und die verbleibenden Mengen zurück.</span><span class="sxs-lookup"><span data-stu-id="5523b-154">Reset the assembly quantities and remaining quantities.</span></span></li></ol></li></ol>|  

> [!IMPORTANT]  
>  <span data-ttu-id="5523b-155">Anders als für fertiggestellte Artikel, die zu den Soll-Kosten gebucht werden, wird Montageausstoß zu den Ist-Kosten gebucht.</span><span class="sxs-lookup"><span data-stu-id="5523b-155">Unlike for production output, which is posted at expected cost, assembly output is posted at actual cost.</span></span>  

## <a name="cost-adjustment"></a><span data-ttu-id="5523b-156">Regulierung Kosten</span><span class="sxs-lookup"><span data-stu-id="5523b-156">Cost Adjustment</span></span>  
 <span data-ttu-id="5523b-157">Sobald ein Montageauftrag gebucht wird, in der Bedeutung, dass Komponenten (Material) und Ressourcen in einen neuen Artikel montiert werden, soll die Bestimmung der Ist-Kosten dieses Montageartikels und die Kosten des aktuellen Lagerstatus der betroffenen Komponenten möglich sein.</span><span class="sxs-lookup"><span data-stu-id="5523b-157">Once an assembly order is posted, meaning that components (material) and resources are assembled into a new item, then it should be possible to determine the actual cost of that assembly item, and the actual inventory cost of the components involved.</span></span> <span data-ttu-id="5523b-158">Dies wird durch Weiterleitung von Kosten von den gebuchten Posten der Quelle (den Komponenten und Ressourcen) an die gebuchten Posten des Ziels (die Montageartikel) erreicht.</span><span class="sxs-lookup"><span data-stu-id="5523b-158">This is achieved by forwarding costs from the posted entries of the source (the components and resources) to the posted entries of the destination (the assembly item).</span></span> <span data-ttu-id="5523b-159">Die Weiterleitung der Kosten wird ausgeführt, indem neue Posten berechnet und generiert werden; diese werden als Regulierungsposten bezeichnet und den Zielposten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="5523b-159">The forwarding of costs is done by calculating and generating new entries, called adjustment entries that become associated with the destination entries.</span></span>  

 <span data-ttu-id="5523b-160">Die weiterzuleitenden Montagekosten werden mithilfe des Auftragsebenenerkennungsmechanismus erkannt.</span><span class="sxs-lookup"><span data-stu-id="5523b-160">The assembly costs to be forwarded are detected with the Order Level detection mechanism.</span></span> <span data-ttu-id="5523b-161">Informationen über andere Ausgleichserkennungsmechanismen, siehe [Designdetails: Kostenanpassung](design-details-cost-adjustment.md)</span><span class="sxs-lookup"><span data-stu-id="5523b-161">For information about other adjustment detection mechanisms, see [Design Details: Cost Adjustment](design-details-cost-adjustment.md).</span></span>  

### <a name="detecting-the-adjustment"></a><span data-ttu-id="5523b-162">Erkennen der Regulierung</span><span class="sxs-lookup"><span data-stu-id="5523b-162">Detecting the Adjustment</span></span>  
<span data-ttu-id="5523b-163">Die Entdeckungsfunktion auf Auftragsebene wird in Konvertierungsszenarien, der Produktion und bei der Montage verwendet.</span><span class="sxs-lookup"><span data-stu-id="5523b-163">The order Level detection function is used in conversion scenarios, production and assembly.</span></span> <span data-ttu-id="5523b-164">Die Feldfunktionen funktionieren wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5523b-164">The function works as follows:</span></span>  

-   <span data-ttu-id="5523b-165">Kostenregulierung wird erkannt, indem der Auftrag markiert wird, sobald eine Ressource oder ein Werkstoff als verbraucht/verwendet gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="5523b-165">Cost adjustment is detected by marking the order whenever a material/resource is posted as consumed/used.</span></span>  
-   <span data-ttu-id="5523b-166">Die Kostenweiterleitung entsteht durch Anwenden der Kosten aus dem Werkstoff oder der Ressource auf die Ausstoßposten, die mit dem Auftrag verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="5523b-166">Cost is forwarding by applying the costs from material/resource to the output entries associated with the same order.</span></span>  

<span data-ttu-id="5523b-167">Die folgende Grafik zeigt die Regulierungspostenstruktur und die Regulierung der Montagekosten.</span><span class="sxs-lookup"><span data-stu-id="5523b-167">The following graphic shows the adjustment entry structure and how assembly costs are adjusted.</span></span>  

<span data-ttu-id="5523b-168">![Berichtigungseintragstruktur](media/design_details_assembly_posting_3.png "design_details_assembly_posting_3")</span><span class="sxs-lookup"><span data-stu-id="5523b-168">![Adjustment entry structure](media/design_details_assembly_posting_3.png "design_details_assembly_posting_3")</span></span>  

### <a name="performing-the-adjustment"></a><span data-ttu-id="5523b-169">Preiskorrektur durchführen</span><span class="sxs-lookup"><span data-stu-id="5523b-169">Performing the Adjustment</span></span>  
<span data-ttu-id="5523b-170">Die Verteilung erkannter Regulierungen von Material- und Ressourcenkosten zu den Montageausgabeposten geschieht durch die Stapelverarbeitung **Lagerreg. fakt. Einst. Preise**.</span><span class="sxs-lookup"><span data-stu-id="5523b-170">The spreading of detected adjustments from material and resource costs onto the assembly output entries is performed by the **Adjust Cost – Item Entries** batch job.</span></span> <span data-ttu-id="5523b-171">Enthält die Funktion „Mehrstufiger Ausgleich“, die aus den folgenden zwei Elementen besteht:</span><span class="sxs-lookup"><span data-stu-id="5523b-171">It contains the Make Multilevel Adjustment function, which consists of the following two elements:</span></span>  

-   <span data-ttu-id="5523b-172">Nehmen Sie einen Montageauftrags-Ausgleich vor, welcher die Kosten aus dem Material- und Ressourcenverbrauch an den Montageausgangsposten weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="5523b-172">Make Assembly Order Adjustment – which forwards cost from material and resource usage to the assembly output entry.</span></span> <span data-ttu-id="5523b-173">Zeilen 5 und 6 im nachstehenden Algorithmus sind dafür zuständig.</span><span class="sxs-lookup"><span data-stu-id="5523b-173">Lines 5 and 6 in the algorithm below are responsible for that.</span></span>  
-   <span data-ttu-id="5523b-174">Nehmen Sie Ein-Niveau-Anpassungen vor, welche die Kosten für einzelne Artikel mithilfe ihrer Lagerabgangsmethode weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="5523b-174">Make Single Level Adjustments – which forwards costs for individual items using their costing method.</span></span> <span data-ttu-id="5523b-175">Rubriken 9 und 10 im nachstehenden Algorithmus sind für dafür zuständig.</span><span class="sxs-lookup"><span data-stu-id="5523b-175">Lines 9 and 10 in the algorithm below are responsible for that.</span></span>  

<span data-ttu-id="5523b-176">![Montage-Ausgleichsalgorithmus](media/design_details_assembly_posting_4.jpg "design_details_assembly_posting_4")</span><span class="sxs-lookup"><span data-stu-id="5523b-176">![Assembly adjustment algorithm](media/design_details_assembly_posting_4.jpg "design_details_assembly_posting_4")</span></span>  

> [!NOTE]  
>  <span data-ttu-id="5523b-177">Das Element „WIP-Regulierungen“ auf den Zeilen 7 und 8 ist für die Weiterleitung von Produktionsmaterial und Kapazitätsnutzung an die Ausgabe nicht abgeschlossener Fertigungsaufträge verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="5523b-177">The Make WIP Adjustments element, in lines 7 and 8, is responsible for forwarding production material and capacity usage to the output of unfinished production orders.</span></span> <span data-ttu-id="5523b-178">Dies wird nicht verwendet, wenn Montageauftragskosten reguliert werden, da der Begriff WIP nicht auf Montage angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="5523b-178">This is not used when adjusting assembly order costs as the concept of WIP does not apply to assembly.</span></span>  

<span data-ttu-id="5523b-179">Weitere Informationen darüber, wie Kosten aus der Montage und aus der Produktion in der Finanzbuchhaltung gebucht werden, finden Sie unter [Designdetails: Bestandesbuchung](design-details-inventory-posting.md).</span><span class="sxs-lookup"><span data-stu-id="5523b-179">For information about how costs from assembly and production are posted to the general ledger, see [Design Details: Inventory Posting](design-details-inventory-posting.md).</span></span>  

## <a name="assembly-costs-are-always-actual"></a><span data-ttu-id="5523b-180">Montagekosten sind immer Ist-Kosten</span><span class="sxs-lookup"><span data-stu-id="5523b-180">Assembly Costs are Always Actual</span></span>  
 <span data-ttu-id="5523b-181">Das Umlaufbestand- (WIP) Konzept gilt nicht in der Montageauftragsbuchung.</span><span class="sxs-lookup"><span data-stu-id="5523b-181">The concept of work in process (WIP) does not apply in assembly order posting.</span></span> <span data-ttu-id="5523b-182">Montagekosten werden nur als Ist-Kosten gebucht, nie als erwartete Kosten.</span><span class="sxs-lookup"><span data-stu-id="5523b-182">Assembly costs are only posted as actual cost, never as expected cost.</span></span> <span data-ttu-id="5523b-183">Weitere Informationen finden Sie unter [Designdetails: Erwartete Kostenbuchung](design-details-expected-cost-posting.md).</span><span class="sxs-lookup"><span data-stu-id="5523b-183">For more information, see [Design Details: Expected Cost Posting](design-details-expected-cost-posting.md).</span></span>  

<span data-ttu-id="5523b-184">Dies wird durch die folgende Datenstruktur ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5523b-184">This is enabled by the following data structure.</span></span>  

-   <span data-ttu-id="5523b-185">Im Feld **Art** der Artikel Buch.-Blattzeilen in den Tabellen **Kapazitätsposten** und **Wertposten** Tabellen, wird *Ressource* verwendet, um Montageressourcenposten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5523b-185">In the **Type** field on item journal lines, in the **Capacity Ledger Entry** and **Value Entry** tables, *Resource* is used to identify assembly resource entries.</span></span>  
-   <span data-ttu-id="5523b-186">Im Feld **Artikelpostenart** der Artikel Buch.-Blattzeilen, in den Tabellen **Kapazitätsposten** und **Wertposten** Tabellen, werden *Montageausgabe* und *Montageverbrauch* verwendet, um die Ausgabemontageartikelposten und verbrauchte Montagekomponentenposten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5523b-186">In the **Item Ledger Entry Type** field on item journal lines, in the **Capacity Ledger Entry** and **Value Entry** tables, *Assembly Output* and *Assembly Consumption* are used to identify the output assembly item entries and the consumed assembly component entries respectively.</span></span>  

<span data-ttu-id="5523b-187">Darüber hinaus werden Produktbuchungsgruppen im Montageauftragskopf und in den Montageauftragszeilen standardmäßig wie folgt ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="5523b-187">In addition, posting group fields on the assembly order header and assembly order lines are populated by default as follows.</span></span>  

|<span data-ttu-id="5523b-188">Einheit</span><span class="sxs-lookup"><span data-stu-id="5523b-188">Entity</span></span>|<span data-ttu-id="5523b-189">Typ</span><span class="sxs-lookup"><span data-stu-id="5523b-189">Type</span></span>|<span data-ttu-id="5523b-190">Buchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5523b-190">Posting Group</span></span>|<span data-ttu-id="5523b-191">Produktbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5523b-191">Gen. Prod. Posting Group</span></span>|  
|------------|----------|-------------------|------------------------------|  
|<span data-ttu-id="5523b-192">Montageauftragskopf</span><span class="sxs-lookup"><span data-stu-id="5523b-192">Assembly Order Header</span></span>|<span data-ttu-id="5523b-193">Artikel</span><span class="sxs-lookup"><span data-stu-id="5523b-193">Item</span></span>|<span data-ttu-id="5523b-194">Lagerbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5523b-194">Inventory Posting Group</span></span>|<span data-ttu-id="5523b-195">Produktbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5523b-195">Gen. Prod. Posting Group</span></span>|  
|<span data-ttu-id="5523b-196">Montageauftragszeile</span><span class="sxs-lookup"><span data-stu-id="5523b-196">Assembly Order Line</span></span>|<span data-ttu-id="5523b-197">Artikel</span><span class="sxs-lookup"><span data-stu-id="5523b-197">Item</span></span>|<span data-ttu-id="5523b-198">Lagerbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5523b-198">Inventory Posting Group</span></span>|<span data-ttu-id="5523b-199">Produktbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5523b-199">Gen. Prod. Posting Group</span></span>|  
|<span data-ttu-id="5523b-200">Montageauftragszeile</span><span class="sxs-lookup"><span data-stu-id="5523b-200">Assembly Order Line</span></span>|<span data-ttu-id="5523b-201">Ressource</span><span class="sxs-lookup"><span data-stu-id="5523b-201">Resource</span></span>||<span data-ttu-id="5523b-202">Produktbuchungsgruppe</span><span class="sxs-lookup"><span data-stu-id="5523b-202">Gen. Prod. Posting Group</span></span>|  

<span data-ttu-id="5523b-203">Entsprechend werden nur Ist-Kosten in der Finanzbuchhaltung gebucht, und keine Interimskonten werden aus der Montageauftragsbuchung eingegeben.</span><span class="sxs-lookup"><span data-stu-id="5523b-203">Accordingly, only actual costs are posted to the general ledger, and no interim accounts are populated from assembly order posting.</span></span> <span data-ttu-id="5523b-204">Weitere Informationen finden Sie unter [Designdetails: Konten in der Finanzbuchhaltung](design-details-accounts-in-the-general-ledger.md).</span><span class="sxs-lookup"><span data-stu-id="5523b-204">For more information, see [Design Details: Accounts in the General Ledger](design-details-accounts-in-the-general-ledger.md)</span></span>  

## <a name="assemble-to-order"></a><span data-ttu-id="5523b-205">Auftragsmontage</span><span class="sxs-lookup"><span data-stu-id="5523b-205">Assemble to Order</span></span>  
<span data-ttu-id="5523b-206">Der Artikelposten, der aus der Buchung eines Auftragsmontageverkaufs resultiert, wurde für den entsprechenden Artikelposten für die Montageausgabe fest angewendet.</span><span class="sxs-lookup"><span data-stu-id="5523b-206">The item ledger entry that results from posting an assemble-to-order sale is fixed applied to the related item ledger entry for the assembly output.</span></span> <span data-ttu-id="5523b-207">Entsprechend werden die Kosten eines Auftragsmontageverkaufs aus dem Montageauftrag abgeleitet, mit dem er verknüpft wurde.</span><span class="sxs-lookup"><span data-stu-id="5523b-207">Accordingly, the cost of an assemble-to-order sale is derived from the assembly order that it was linked to.</span></span>  

<span data-ttu-id="5523b-208">Artikelposten des Typs Verkauf, die aus dem Buchen von Auftragsmontagemengen resultieren, werden mit **Ja** im Feld **Auftragsmontage** markiert.</span><span class="sxs-lookup"><span data-stu-id="5523b-208">Item ledger entries of type Sale that result from posting assemble-to-order quantities are marked with **Yes** in the **Assemble to Order** field.</span></span>  

<span data-ttu-id="5523b-209">Das Buchen von Verkaufsauftragszeilen, bei denen ein Teil eine Lagermenge und ein anderer Teil eine Auftragsmontagemenge darstellt, führt zu separaten Artikelposten, einer für die Lagermenge und einer für die Auftragsmontagemenge.</span><span class="sxs-lookup"><span data-stu-id="5523b-209">Posting sales order lines where a part is inventory quantity and another part is assemble-to-order quantity results in separate item ledger entries, one for the inventory quantity and one for the assemble-to-order quantity.</span></span>  

## <a name="see-also"></a><span data-ttu-id="5523b-210">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5523b-210">See Also</span></span>  
 <span data-ttu-id="5523b-211">[Designdetails: Lagerkostenberechnung](design-details-inventory-costing.md) </span><span class="sxs-lookup"><span data-stu-id="5523b-211">[Design Details: Inventory Costing](design-details-inventory-costing.md) </span></span>  
 <span data-ttu-id="5523b-212">[Designdetails: Fertigungsauftragsbuchung](design-details-production-order-posting.md) </span><span class="sxs-lookup"><span data-stu-id="5523b-212">[Design Details: Production Order Posting](design-details-production-order-posting.md) </span></span>  
 [<span data-ttu-id="5523b-213">Designdetails: Kostenberechnungsmethoden</span><span class="sxs-lookup"><span data-stu-id="5523b-213">Design Details: Costing Methods</span></span>](design-details-costing-methods.md)  
 [<span data-ttu-id="5523b-214">Verwalten der Lagerregulierung</span><span class="sxs-lookup"><span data-stu-id="5523b-214">Managing Inventory Costs</span></span>](finance-manage-inventory-costs.md)  
 [<span data-ttu-id="5523b-215">Finanzen</span><span class="sxs-lookup"><span data-stu-id="5523b-215">Finance</span></span>](finance.md)  
 <span data-ttu-id="5523b-216">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="5523b-216">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

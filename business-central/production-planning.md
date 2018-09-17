---
title: Lieferkettenplanung | Microsoft Docs
description: "Vorbereiten eines ausführlichen ausführbaren Plan und der Montageplan für Verkäufe und Produktionsbedarf."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/14/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2286b728a464943841b192031cfea13644441013
ms.openlocfilehash: f16c959334e26a54ff0a899512f2b76331643dea
ms.contentlocale: de-de
ms.lasthandoff: 06/28/2018

---
# <a name="planning"></a><span data-ttu-id="ea288-103">Planung</span><span class="sxs-lookup"><span data-stu-id="ea288-103">Planning</span></span>
<span data-ttu-id="ea288-104">Die Produktionsschritte, die ausgeführt werden müssen, um das Ausgangsmaterial zu Fertigerzeugnissen zu verarbeiten, müssen – abhängig von Volumen und Art der Produkte – täglich oder wöchentlich geplant werden.</span><span class="sxs-lookup"><span data-stu-id="ea288-104">The production operations required to transform inputs into finished goods must be planned daily or weekly depending on the volume and nature of the products.</span></span> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="ea288-105"> verfügt über Features zum Erfüllen des erwarteten und tatsächlichen Bedarfs von Verkauf und Produktion sowie über Verteilungsplanungsfeatures, die die Verwendung von Lagerhaltungsdaten und Umlagerungen zwischen Lagerorten ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="ea288-105"> offers features to supply for anticipated and actual demand from sale, assembly, and production as well as features for distribution planning using stockkeeping units and location transfers.</span></span>

> [!NOTE]
> <span data-ttu-id="ea288-106">Dieses Thema beschreibt die Planung für Unternehmen, die mit der Fertigung oder Montageverwaltung zu tun haben, wenn die resultierenden Beschaffungsaufträge entweder Produktion, Montage, Umlagerung oder Einkaufsbestellungen sein können.</span><span class="sxs-lookup"><span data-stu-id="ea288-106">This topic mainly describes planning for companies involved in manufacturing or assembly management where the resulting supply orders can be either production, assembly, transfer, or purchase orders.</span></span> <span data-ttu-id="ea288-107">Die Hauptschnittstelle für diese Planungsarbeiten ist das Fenster **Planungsvorschlag**</span><span class="sxs-lookup"><span data-stu-id="ea288-107">The main interface for this planning work is the **Planning Worksheet** window.</span></span>

> [!INCLUDE[d365fin](includes/d365fin_md.md)]<span data-ttu-id="ea288-108"> unterstützt auch Beschaffungsplanung für Großhandelsmandanten, in denen Beschaffungsaufträge und die resultierende Umlagerung nur Einkaufsbestellungen sein können.</span><span class="sxs-lookup"><span data-stu-id="ea288-108"> also supports supply planning for wholesale companies where the resulting supply orders can only be transfer and purchase orders.</span></span> <span data-ttu-id="ea288-109">Die für diese Hauptschnittstelle Planungsarbeiten ist das **Bestellvorschlag** Fenster, die indirekt in diesem Thema beschrieben wird, während die meisten Planungsfunktionalität auf beide Vorschläge gehört.</span><span class="sxs-lookup"><span data-stu-id="ea288-109">The main interface for this planning work is the **Requisition Worksheet** window, which is described indirectly in this topic as most planning functionality applies to both worksheets.</span></span>

<span data-ttu-id="ea288-110">Bevor Sie Produktionsaufträge planen und ausführen können, müssen Sie die Fertigungskapazitäten konfigurieren, wie Erstellung von Betriebskalendern, Arbeitsplänen, Produktionsstücklisten und Maschinencentren.</span><span class="sxs-lookup"><span data-stu-id="ea288-110">Before you can plan and execute production orders, you must configure production capacities, such as creating shop calendars, routings, production BOMs, and machine centers.</span></span> <span data-ttu-id="ea288-111">Weitere Informationen finden Sie unter [Einrichten von Produktion](production-configure-production-processes.md).</span><span class="sxs-lookup"><span data-stu-id="ea288-111">For more information, see [Setting Up Manufacturing](production-configure-production-processes.md).</span></span>

<span data-ttu-id="ea288-112">Planung kann als die Vorbereitung der erforderlichen Beschaffungsaufträge in den Montage- oder Fertigungsabteilungen zur Erfüllung des Bedarfs angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="ea288-112">Planning can be seen as the preparation required supply orders in the assembly or manufacturing departments to fulfill demand.</span></span> <span data-ttu-id="ea288-113">Weitere Informationen finden Sie unter [Montageverwaltung](assembly-assemble-items.md) und [Produktion](production-manage-manufacturing.md).</span><span class="sxs-lookup"><span data-stu-id="ea288-113">For more information, see [Assembly Management](assembly-assemble-items.md) and [Manufacturing](production-manage-manufacturing.md).</span></span>

<span data-ttu-id="ea288-114">In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.</span><span class="sxs-lookup"><span data-stu-id="ea288-114">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>   

|<span data-ttu-id="ea288-115">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="ea288-115">**To**</span></span>|<span data-ttu-id="ea288-116">**Siehe**</span><span class="sxs-lookup"><span data-stu-id="ea288-116">**See**</span></span>|  
|------------|-------------|  
|<span data-ttu-id="ea288-117">Erhalten einer kurzen Einführung, wie das Planungssystem verwendet werden kann, um Nachfrage zu erkennen und zu priorisieren und einen ausgewogenen Beschaffungsplan vorzuschlagen,.</span><span class="sxs-lookup"><span data-stu-id="ea288-117">Get a brief introduction to how the planning system can be used to detect and prioritize demand and suggest a balanced supply plan.</span></span>|[<span data-ttu-id="ea288-118">Info zu Planungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="ea288-118">About Planning Functionality</span></span>](production-about-planning-functionality.md)|
|<span data-ttu-id="ea288-119">Erläutert, wie das Planungssystem arbeitet und wie die Algorithmen angepasst werden, um Planungsbedingungen in verschiedenen Umgebungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="ea288-119">Understand how all aspects of the planning system works and how to adjust the algorithms to meet planning requirements in different environments.</span></span>|[<span data-ttu-id="ea288-120">Designdetails: Vorratsplanung</span><span class="sxs-lookup"><span data-stu-id="ea288-120">Design Details: Supply Planning</span></span>](design-details-supply-planning.md)|
|<span data-ttu-id="ea288-121">Erhalten von Informationen zur Planungslogikabweichung zwischen dem Bedarf an Lagerplätzen gemäß den Einstellungen der Lagerhaltungsdaten und dem Bedarf ohne Lagerortcodes</span><span class="sxs-lookup"><span data-stu-id="ea288-121">Learn how the planning logic differentiates between demand at locations according to the SKU setup and demand without location codes.</span></span>|<span data-ttu-id="ea288-122">Siehe [Planung mit/ohne Lagerortcodes](production-planning-with-without-locations.md).</span><span class="sxs-lookup"><span data-stu-id="ea288-122">[Planning With or Without Locations](production-planning-with-without-locations.md)</span></span>|
|<span data-ttu-id="ea288-123">Prognostizieren den Fertigungsbedarf, der durch erwartete Verkaufs- und Fertigungsaufträge dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ea288-123">Forecast production demand presented by expected sales and production orders.</span></span>|[<span data-ttu-id="ea288-124">Produktionsplanung erstellen</span><span class="sxs-lookup"><span data-stu-id="ea288-124">Create a Production Forecast</span></span>](production-how-to-create-a-forecast.md)|  
|<span data-ttu-id="ea288-125">Automatisches exaktes Erstellen von Fertigungsaufträgen auf der Grundlage von Aufträgen, um den exakten Bedarf der Auftragszeile abzudecken</span><span class="sxs-lookup"><span data-stu-id="ea288-125">Create one-to-one production orders automatically from a sales order to cover the exact demand of that sales order line.</span></span>|[<span data-ttu-id="ea288-126">Fertigungsaufträge aus Verkaufsaufträgen zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="ea288-126">Create Production Orders from Sales Orders</span></span>](production-how-to-create-production-orders-from-sales-orders.md)|
|<span data-ttu-id="ea288-127">Direktes Erstellen eines Projektfertigungsauftrags auf der Grundlage eines mehrzeiligen Auftrags, bei dem es sich um Fertigungsprojekt handelt</span><span class="sxs-lookup"><span data-stu-id="ea288-127">Create a project production order directly from a multiline sales order representing a production project.</span></span>|[<span data-ttu-id="ea288-128">Projektaufträge planen</span><span class="sxs-lookup"><span data-stu-id="ea288-128">Plan Project Orders</span></span>](production-how-to-plan-project-orders.md)|
|<span data-ttu-id="ea288-129">Manuelles Planen für Verkaufs- oder Fertigungsbedarf pro einzelner Stücklistenebene mithilfe des Fensters **Auftragsplanung**</span><span class="sxs-lookup"><span data-stu-id="ea288-129">Use the **Order Planning** window to manually plan for sales or production demand one production BOM level at a time.</span></span>|[<span data-ttu-id="ea288-130">Planung der Bestellung eines neuen Bedarfs von Auftrag</span><span class="sxs-lookup"><span data-stu-id="ea288-130">Plan for New Demand Order by Order</span></span>](production-how-to-plan-for-new-demand.md)|
|<span data-ttu-id="ea288-131">Verwenden Sie das Fenster **Planungsvorschlag**, um die Felder Prod.-Programmplanung und Nettobedarfsoptionen auszuführen, einen oder ausführlichen Beschaffungsplans auf hoher Ebene in allen Artikelebenen automatisch zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ea288-131">Use the **Planning Worksheet** window to run both the MPS and MRP options to automatically create either a high-level or detailed supply plan at all item levels.</span></span>|[<span data-ttu-id="ea288-132">Führen Sie eine vollständige Planung, Prod.-Programmplanung oder Nettobedarf aus</span><span class="sxs-lookup"><span data-stu-id="ea288-132">Run Full Planning, MPS or MRP</span></span>](production-how-to-run-mps-and-mrp.md)|
|<span data-ttu-id="ea288-133">Ausführen des Bestellvorschlags zum automatischen Erstellen eines ausführlichen Beschaffungsplans, um den Bedarf für Artikel zu decken, die ausschließlich per Einkauf oder Umlagerung beschafft werden</span><span class="sxs-lookup"><span data-stu-id="ea288-133">Run the requisition worksheet to automatically create a detailed supply plan to cover demand for items that are replenished by purchase or transfer only.</span></span>|<span data-ttu-id="ea288-134">**Bestellvorschlag** Seite</span><span class="sxs-lookup"><span data-stu-id="ea288-134">**Requisition Worksheet** page</span></span>|  
|<span data-ttu-id="ea288-135">Initiieren oder Aktualisieren eines Fertigungsauftrags in Form grobterminierter Arbeitsgänge im Produktionsplan</span><span class="sxs-lookup"><span data-stu-id="ea288-135">Initiate or update a production order as rough-scheduled operations in the master production schedule.</span></span>|[<span data-ttu-id="ea288-136">Neugestaltungs- oder direkt Aktualisierung von Fertigungsaufträgen</span><span class="sxs-lookup"><span data-stu-id="ea288-136">Replan or Refresh Production Orders Directly</span></span>](production-how-to-replan-refresh-production-orders.md)|
|<span data-ttu-id="ea288-137">Berechnen Sie Arbeits- oder Arbeitsplatzkalender aufgrund von Planungsänderungen.</span><span class="sxs-lookup"><span data-stu-id="ea288-137">Recalculate work or machine center calendars due to planning changes.</span></span>|<span data-ttu-id="ea288-138">"Berechnen eines Arbeitsplatzgruppenkalender-Abschnitt in [Richten Sie Betriebskalender ein](production-how-to-create-work-center-calendars.md)</span><span class="sxs-lookup"><span data-stu-id="ea288-138">"To calculate a work center calendar" section in [Set Up Shop Calendars](production-how-to-create-work-center-calendars.md)</span></span>|
|<span data-ttu-id="ea288-139">Verfolgen des Auftragsbedarfs (Menge mit Bedarfsverursacher), der Absatzplanung, des Rahmenauftrags oder der Planungsparameter (Menge ohne Bedarfsverursacher), auf den bzw. auf die die betreffende Planungszeile zurückzuführen ist</span><span class="sxs-lookup"><span data-stu-id="ea288-139">Track the order demand (tracked quantity), forecast, blanket sales order, or planning parameter (untracked quantity) that has given rise to the planning line in question.</span></span>|[<span data-ttu-id="ea288-140">Nachverfolgen von Beziehungen zwischen Bedarf und Vorrat.</span><span class="sxs-lookup"><span data-stu-id="ea288-140">Track Relations Between Demand and Supply</span></span>](production-how-track-demand-supply.md)|
|<span data-ttu-id="ea288-141">Anzeigen des voraussichtlich verfügbaren Lagerbestands eines Artikels in verschiedenen Ansichten und Anzeigen des beeinflussenden Bruttobedarfs sowie der beeinflussenden geplanten Auftragseingänge und anderer Ereignisse im Laufe der Zeit</span><span class="sxs-lookup"><span data-stu-id="ea288-141">View an item's projected available inventory by different views and see which gross requirements, planned order receipts, and other events influence it over time.</span></span>|[<span data-ttu-id="ea288-142">Artikelverfügbarkeit anzeigen</span><span class="sxs-lookup"><span data-stu-id="ea288-142">View the Availability of Items</span></span>](inventory-how-availability-overview.md)|  
|<span data-ttu-id="ea288-143">Wählen Sie Planungsaktivitäten wie ändern oder hinzufügen von Planungsvorschlagszeilen, in einer grafischen Ansicht des Beschaffungsplans aus.</span><span class="sxs-lookup"><span data-stu-id="ea288-143">Perform selected planning activities, such as changing or adding planning worksheet lines, in a graphical view of the supply plan.</span></span>|[<span data-ttu-id="ea288-144">Ändern von Planungsvorschlägen in einer grafischen Ansicht</span><span class="sxs-lookup"><span data-stu-id="ea288-144">Modify Planning Suggestions in a Graphical View</span></span>](production-how-to-modify-planning-suggestions-in-a-graphical-view.md)|

## <a name="see-also"></a><span data-ttu-id="ea288-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea288-145">See Also</span></span>
[<span data-ttu-id="ea288-146">Produktion einrichten</span><span class="sxs-lookup"><span data-stu-id="ea288-146">Setting Up Manufacturing</span></span>](production-configure-production-processes.md)  
<span data-ttu-id="ea288-147">[Produktion](production-manage-manufacturing.md)  </span><span class="sxs-lookup"><span data-stu-id="ea288-147">[Manufacturing](production-manage-manufacturing.md)  </span></span>  
[<span data-ttu-id="ea288-148">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="ea288-148">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="ea288-149">Einkauf</span><span class="sxs-lookup"><span data-stu-id="ea288-149">Purchasing</span></span>](purchasing-manage-purchasing.md)  
<span data-ttu-id="ea288-150">[Designdetails: Vorratsplanung](design-details-supply-planning.md) </span><span class="sxs-lookup"><span data-stu-id="ea288-150">[Design Details: Supply Planning](design-details-supply-planning.md) </span></span>  
[<span data-ttu-id="ea288-151">Bewährte Einrichtungsmethoden: Beschaffungsplanung</span><span class="sxs-lookup"><span data-stu-id="ea288-151">Setup Best Practices: Supply Planning</span></span>](setup-best-practices-supply-planning.md)  
<span data-ttu-id="ea288-152">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="ea288-152">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  
 

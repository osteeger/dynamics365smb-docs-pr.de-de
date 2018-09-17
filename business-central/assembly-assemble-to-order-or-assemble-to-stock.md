---
title: Auftragsmontage und Lagermontage verstehen | Microsoft Docs
description: "Montageartikeln können angegeben werden entweder, indem sie zusammengestellt werden, wenn sie bestellt oder montiert werden oder indem sie im Lager gehalten werden, bis diese Anforderung eines Verkaufsauftrags sind."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: kit, kitting
ms.date: 08/15/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 4bc9199b879c23115082b07a81d6da5a0b46e60d
ms.openlocfilehash: 3e24dd898bf427ab386c5c052b035d1192f84e9f
ms.contentlocale: de-de
ms.lasthandoff: 05/31/2018

---
# <a name="understanding-assemble-to-order-and-assemble-to-stock"></a><span data-ttu-id="1b1f6-103">Auftragsmontage und Lagermontage verstehen</span><span class="sxs-lookup"><span data-stu-id="1b1f6-103">Understanding Assemble to Order and Assemble to Stock</span></span>
<span data-ttu-id="1b1f6-104">Montageartikel können in den beiden folgenden Prozessen geliefert werden:</span><span class="sxs-lookup"><span data-stu-id="1b1f6-104">Assembly items can be supplied in the following two processes:</span></span>  

-   <span data-ttu-id="1b1f6-105">Auftragsmontage</span><span class="sxs-lookup"><span data-stu-id="1b1f6-105">Assemble to order.</span></span>  
-   <span data-ttu-id="1b1f6-106">Lagermontage</span><span class="sxs-lookup"><span data-stu-id="1b1f6-106">Assemble to stock.</span></span>  

## <a name="assemble-to-order"></a><span data-ttu-id="1b1f6-107">Auftragsmontage</span><span class="sxs-lookup"><span data-stu-id="1b1f6-107">Assemble to Order</span></span>  
<span data-ttu-id="1b1f6-108">In der Regel nutzen Sie die *Auftragsmontage* für Artikel, die Sie nicht auf Lager haben möchten, da Sie erwarten, dass diese für Debitorenanfragen angepasst werden müssen, oder weil Sie die Lagerkosten minimieren möchten.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-108">You typically use *assemble to order* for items that you do not want to stock because you expect to customize them to customer requests or because you want to minimize the inventory carrying cost.</span></span> <span data-ttu-id="1b1f6-109">Die unterstützenden Funktionen umfassen:</span><span class="sxs-lookup"><span data-stu-id="1b1f6-109">The supporting functionality includes:</span></span>  

-   <span data-ttu-id="1b1f6-110">Möglichkeit, Montageartikel anzupassen, wenn ein Verkaufsauftrag entgegengenommen wird.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-110">Ability to customize assembly items when taking a sales order.</span></span>  
-   <span data-ttu-id="1b1f6-111">Übersicht der Verfügbarkeit des Montageartikels und seiner Komponenten.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-111">Overview of availability of the assembly item and its components.</span></span>  
-   <span data-ttu-id="1b1f6-112">Möglichkeit, Montagekomponenten sofort zu reservieren, um die Auftragserfüllung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-112">Ability to reserve assembly components immediately to guarantee order fulfillment.</span></span>  
-   <span data-ttu-id="1b1f6-113">Funktion, um die Profitabilität des angepassten Auftrags durch Berechnen des Preises und der Kosten zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-113">Function to determine profitability of the customized order by rolling up price and cost.</span></span>  
-   <span data-ttu-id="1b1f6-114">Fibuintegration für das Lager, um die Montage und das Versenden zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-114">Integration to the warehouse to make assembly and shipping easier.</span></span>  
-   <span data-ttu-id="1b1f6-115">Möglichkeit der Auftragsmontage im Augenblick der Erstellung eines Verkaufsangebots oder eines Rahmenauftrags.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-115">Ability to assemble to order at the point of making a sales quote or a blanket sales order.</span></span>  
-   <span data-ttu-id="1b1f6-116">Möglichkeit, Lagermengen mit Auftragsmontagemengen zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-116">Ability to combine inventory quantities with assemble-to-order quantities.</span></span>  

<span data-ttu-id="1b1f6-117">Im Auftragsmontageprozess wird der Artikel als Reaktion auf einen Verkaufsauftrag und mit einer direkten Verknüpfung zwischen Montageauftrag und Verkaufsauftrag montiert.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-117">In the assemble-to-order process, the item is assembled in response to a sales order and with a one-to-one link between the assembly order and the sales order.</span></span>  

<span data-ttu-id="1b1f6-118">Wenn Sie einen Auftragsmontageartikel in eine Verkaufszeile eingeben, wird automatisch ein Montageauftrag mit einem Kopf erstellt, der auf der Verkaufszeile basiert und Zeilen enthält, die anhand der Montagestückliste des Artikels durch Multiplikation mit der Bestellmenge erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-118">When you enter an assemble-to-order item on a sales line, an assembly order is automatically created with a header that is based on the sales line and with lines that are based on the item’s assembly BOM multiplied by the order quantity.</span></span> <span data-ttu-id="1b1f6-119">Sie können das Fenster **Auftragsmontagezeilen** verwenden, um die Zeilen des verknüpften Montageauftrags anzuzeigen und den Montageartikel und das Lieferdatum, das auf der Komponentenverfügbarkeit basiert, anzupassen.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-119">You can use the **Assemble-to-Order Lines** window to see the linked assembly order lines to support you in customizing the assembly item and in a delivery date that is based on component availability information.</span></span> <span data-ttu-id="1b1f6-120">Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="1b1f6-120">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1b1f6-121">Obwohl es nicht Teil des Standardprozesses ist, können Sie Lagerbestandsmengen mit den Auftragsmontagemengen verkaufen.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-121">Although it is not part of the default process, you can sell inventory quantities with the assemble-to-order quantities.</span></span> <span data-ttu-id="1b1f6-122">Weitere Informationen finden Sie unter [Verkaufen von Lagerartikeln in Programmfertigungs-Flow](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md)</span><span class="sxs-lookup"><span data-stu-id="1b1f6-122">For more information, see [Sell Inventory Items in Assemble-to-Order Flows](assembly-how-to-sell-inventory-items-in-assemble-to-order-flows.md).</span></span>  

 <span data-ttu-id="1b1f6-123">Um dieses Verfahren auszuführen, muss für das Feld **Montagerichtlinie** auf der Artikelkarte **Auftragsmontage** aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-123">To enable this process, the **Assembly Policy** field on the item card must be **Assemble-to-Order**.</span></span>  

## <a name="assemble-to-stock"></a><span data-ttu-id="1b1f6-124">Lagermontage</span><span class="sxs-lookup"><span data-stu-id="1b1f6-124">Assemble to Stock</span></span>  
 <span data-ttu-id="1b1f6-125">In der Regel nutzen Sie *Lagerfertigung* für Artikel, die Sie vor dem Verkauf montieren möchten - wie zur Vorbereitung einer Kit-Kampagne - und auf Lager zu halten, bis sie bestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-125">You typically use *assemble to stock* for items that you want to assemble ahead of sales, such as to prepare for a kit campaign, and keep in stock until they are ordered.</span></span> <span data-ttu-id="1b1f6-126">Diese Artikel sind normalerweise Standardartikel, wie gepackte Kits, die Sie nicht an Debitorenanfragen anpassen.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-126">These items are usually standard items such as packaged kits that you do not offer to customize to customer requests.</span></span>  

 <span data-ttu-id="1b1f6-127">Im Lagerfertigungsvorgang wird der Artikel ohne sofortigen Verkaufsbedarf montiert und ist im Lager als Lagerartikel für den späteren Verkauf oder Verbrauch als Unterbaugruppe verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-127">In the assemble-to-stock process, the item is assembled without an immediate sales demand and is stocked in the warehouse as an inventory item for later sale or consumption as a subassembly.</span></span> <span data-ttu-id="1b1f6-128">Weitere Informationen finden Sie unter [Entnahme von Artikeln](assembly-how-to-assemble-items.md).</span><span class="sxs-lookup"><span data-stu-id="1b1f6-128">For more information, see [Assemble Items](assembly-how-to-assemble-items.md).</span></span> <span data-ttu-id="1b1f6-129">Ab diesem Punkt kann der Artikel als einzelner Artikel kommissioniert und verarbeitet werden und wird wie ein gefertigter Artikel behandelt.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-129">From this point, the item is picked and processed as a single item and is treated like a finished production item.</span></span>  

 <span data-ttu-id="1b1f6-130">Wenn Sie einen Lagerfertigungsartikel in eine Verkaufszeile eingeben, sieht die Zeile wie jeder andere Zeile eines aus dem Lagerbestand verkauften Artikels aus.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-130">When you enter an assemble-to-stock item on a sales line, the line like any other item sold from inventory.</span></span> <span data-ttu-id="1b1f6-131">Beispielsweise wird die Verfügbarkeit nur für den Montageartikel geprüft.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-131">For example, availability is checked for the assembly item only.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="1b1f6-132">Obwohl es nicht Teil des Standardprozesses ist, können Sie einen Artikel für einen Auftrag montieren, auch wenn für diesen die Lagermontage eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-132">Although it is not part of the default process, you can assemble an item to order even if it is set up to be assembled to stock.</span></span> <span data-ttu-id="1b1f6-133">Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln und Lagerartikeln zusammen](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md)</span><span class="sxs-lookup"><span data-stu-id="1b1f6-133">For more information, see [Sell Assemble-to-Order Items and Inventory Items Together](assembly-how-to-sell-assemble-to-order-items-and-inventory-items-together.md).</span></span>  

 <span data-ttu-id="1b1f6-134">Um dieses Verfahren auszuführen, muss für das Feld **Montagerichtlinie** auf der Artikelkarte **Lagermontage** aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-134">To enable this process, the **Assembly Policy** field on the item card must be **Assemble-to-Stock**.</span></span>  

## <a name="combination-scenarios"></a><span data-ttu-id="1b1f6-135">Kombinierte Szenarien</span><span class="sxs-lookup"><span data-stu-id="1b1f6-135">Combination Scenarios</span></span>  
 <span data-ttu-id="1b1f6-136">Ein allgemeines Prinzip der Montageverwaltung ist, dass Auftragsmontagemengen, wenn sie in einer Verkaufsauftragszeile zusammengefasst sind, vor Lagermengen ausgeliefert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-136">A general principle in Assembly Management is that when combined on a sales order line, assemble-to-order quantities must be shipped before inventory quantities.</span></span>  

 <span data-ttu-id="1b1f6-137">Wenn ein Montageauftrag mit einer Verkaufsauftragszeile verknüpft ist, wird der Wert im Feld **Menge für Auftragsmontage** der Verkaufsauftragszeile über das Feld **Montagemenge** im Montageauftragskopf in das Feld **Menge** kopiert.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-137">If an assembly order is linked to a sales order line, then the value in the **Qty. to Assemble to Order** field on the sales order line is copied to the **Quantity to Assemble** field, via the **Quantity** field on the assembly order header.</span></span> <span data-ttu-id="1b1f6-138">Weitere Informationen finden Sie unter [Verkaufen von Auftragsmontageartikeln](assembly-how-to-sell-items-assembled-to-order.md).</span><span class="sxs-lookup"><span data-stu-id="1b1f6-138">For more information, see [Sell Items Assembled to Order](assembly-how-to-sell-items-assembled-to-order.md).</span></span>  

 <span data-ttu-id="1b1f6-139">Darüber hinaus wird der Wert im Feld **Menge für Montage** mit dem Feld **Zu liefern** in der Verkaufsauftragszeile verknüpft. Diese Verknüpfung verwaltet die Lieferung von Teil- und vollständigen Montageauftragsmengen.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-139">In addition, the value in the **Quantity to Assemble** field is related to the **Qty. to Ship** field on the sales order line, and this relation manages the shipping of assemble-to-order quantities, both partially and completely.</span></span> <span data-ttu-id="1b1f6-140">Dies ist erfüllt, wenn die gesamte Verkaufszeilenmenge für einen Auftrag montiert wird und, in kombinierten Szenarien, wenn ein Teil der Verkaufszeilenmenge montiert und ein anderer Teil aus dem Lager geliefert wird.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-140">This is true both when the full sales line quantity is assembled to order and in combination scenarios where one part of the sales line quantity is assembled to order and another part is shipped from inventory.</span></span> <span data-ttu-id="1b1f6-141">In kombinierten Szenarien haben Sie jedoch bei der Teillieferung zusätzliche Flexibilität, indem Sie das Feld **Menge für Montage** innerhalb der vordefinierten Regeln ändern können, um anzugeben, wie viele Einheiten der Teillieferung aus dem Lagerbestand geliefert werden und wie viele durch Auftragsmontage geliefert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-141">However, in the combination scenario, you have additional flexibility when shipping partially in that you can modify the **Quantity to Assemble** field, within predefined rules, to specify how many units to ship partially from inventory and how many to ship partially by assembling to order.</span></span>  

 <span data-ttu-id="1b1f6-142">Wenn die vollständige Verkaufszeilenmenge nach Auftrag montiert und versendet werden muss, wird der Wert im Feld **Menge für Versand** in das Feld **Menge für Montage** im verknüpften Montageauftrag kopiert, wenn Sie die zu liefernde Menge ändern.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-142">If the full sales line quantity must be assembled to order and shipped, then the value in the **Qty. to Ship** field is copied to **Quantity to Assemble** field on the linked assembly order when you change the quantity to ship.</span></span> <span data-ttu-id="1b1f6-143">Dadurch ist sichergestellt, dass die Menge, die ausgeliefert wird, vollständig von der Auftragsmontagemenge geliefert wird.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-143">This ensures that the quantity being shipped is fully supplied by the assemble-to-order quantity.</span></span>  

 <span data-ttu-id="1b1f6-144">In den kombinierten Szenarien wird der Gesamtwert in **Menge für Versand** jedoch nicht in das Feld **Menge für Montage** im Montageauftragskopf kopiert.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-144">However, in combination scenarios, the full value in the **Qty. to Ship** is not copied to the **Quantity to Assemble** field on the assembly order header.</span></span> <span data-ttu-id="1b1f6-145">Stattdessen wird der Standardwert in das Feld **Menge für Montage** eingefügt, der entsprechend einer vordefinierten Regel, die sicherstellt, dass Auftragsmontagemengen zuerst geliefert werden, aus dem Feld **Zu liefern** berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-145">Instead, a default value is inserted in the **Quantity to Assemble** field that is calculated from the **Qty. to Ship** field according to a predefined rule that ensures shipment of assemble-to-order quantities first.</span></span>  

 <span data-ttu-id="1b1f6-146">Wenn Sie von diesem Standard abweichen möchten, weil Sie beispielsweise mehr oder weniger zusammenbauen möchten, als die Menge im Feld ,**Menge für Montage** können Sie das Feld **Menge für Montage** ändern, allerdings nur innerhalb der vordefinierten Regeln, wie unten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-146">If you want to deviate from this default, for example because you only want to assemble more or less of the quantity in the **Qty. to Ship** field, then you can modify the **Quantity to Assemble** field, but only within predefined rules, as illustrated below</span></span>  

 <span data-ttu-id="1b1f6-147">Ein Beispiel, warum Sie die zu montierende Menge ggf. ändern wollen, wäre, dass Sie Liefer- von Lagermengen teilweise buchen möchten, bevor der Montageausstoß geliefert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-147">An example why you would want to modify the quantity to assemble is that you want to partially post shipment of inventory quantities before the assembly output can be shipped.</span></span>  

 <span data-ttu-id="1b1f6-148">Im Folgenden werden die Regeln erläutert, die die minimalen und maximalen Werte festlegen, die Sie in **Menge für Montage** manuell eingeben können, um in einem kombinierten Szenario vom Standardwert abzuweichen.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-148">The following explains the rules that define the minimum and maximum values that you can enter manually in the **Quantity to Assemble** to deviate from the default value in a combination scenario.</span></span> <span data-ttu-id="1b1f6-149">Die Tabelle zeigt ein kombiniertes Szenario, in dem das Feld **Menge für Montage** der verknüpften Verkaufsauftragszeile von 7 in 4 geändert wird, weshalb **Menge für Montage** den Standardwert 4 annimmt.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-149">The table shows a combination scenario where the **Qty. to Ship** field on the linked sales order line is changed from 7 to 4, and the **Quantity to Assemble** is therefore defaulted to 4.</span></span>  

||<span data-ttu-id="1b1f6-150">Verkaufszeile</span><span class="sxs-lookup"><span data-stu-id="1b1f6-150">Sales Order Line</span></span>|<span data-ttu-id="1b1f6-151">Montageauftragskopf</span><span class="sxs-lookup"><span data-stu-id="1b1f6-151">Assembly Order Hheader</span></span>|  
|-|----------------------|---------------------------|  
||<span data-ttu-id="1b1f6-152">**Menge**</span><span class="sxs-lookup"><span data-stu-id="1b1f6-152">**Quantity**</span></span>|<span data-ttu-id="1b1f6-153">**Zu liefern**</span><span class="sxs-lookup"><span data-stu-id="1b1f6-153">**Qty. to Ship**</span></span>|<span data-ttu-id="1b1f6-154">**Menge für Auftragsmontage**</span><span class="sxs-lookup"><span data-stu-id="1b1f6-154">**Qty. to Assemble to Order**</span></span>|<span data-ttu-id="1b1f6-155">**Menge geliefert**</span><span class="sxs-lookup"><span data-stu-id="1b1f6-155">**Quantity Shipped**</span></span>|<span data-ttu-id="1b1f6-156">**Menge**</span><span class="sxs-lookup"><span data-stu-id="1b1f6-156">**Quantity**</span></span>|<span data-ttu-id="1b1f6-157">**Menge für Montage**</span><span class="sxs-lookup"><span data-stu-id="1b1f6-157">**Quantity to Assemble**</span></span>|<span data-ttu-id="1b1f6-158">**Zusammengesetzte Menge**</span><span class="sxs-lookup"><span data-stu-id="1b1f6-158">**Assembled Quantity**</span></span>|<span data-ttu-id="1b1f6-159">**Restmenge**</span><span class="sxs-lookup"><span data-stu-id="1b1f6-159">**Remaining Quantity**</span></span>|  
|<span data-ttu-id="1b1f6-160">Anfang</span><span class="sxs-lookup"><span data-stu-id="1b1f6-160">Initial</span></span>|<span data-ttu-id="1b1f6-161">10</span><span class="sxs-lookup"><span data-stu-id="1b1f6-161">10</span></span>|<span data-ttu-id="1b1f6-162">7</span><span class="sxs-lookup"><span data-stu-id="1b1f6-162">7</span></span>|<span data-ttu-id="1b1f6-163">7</span><span class="sxs-lookup"><span data-stu-id="1b1f6-163">7</span></span>|<span data-ttu-id="1b1f6-164">0</span><span class="sxs-lookup"><span data-stu-id="1b1f6-164">0</span></span>|<span data-ttu-id="1b1f6-165">7</span><span class="sxs-lookup"><span data-stu-id="1b1f6-165">7</span></span>|<span data-ttu-id="1b1f6-166">7</span><span class="sxs-lookup"><span data-stu-id="1b1f6-166">7</span></span>|<span data-ttu-id="1b1f6-167">0</span><span class="sxs-lookup"><span data-stu-id="1b1f6-167">0</span></span>|<span data-ttu-id="1b1f6-168">7</span><span class="sxs-lookup"><span data-stu-id="1b1f6-168">7</span></span>|  
|<span data-ttu-id="1b1f6-169">Ändern</span><span class="sxs-lookup"><span data-stu-id="1b1f6-169">Change</span></span>||<span data-ttu-id="1b1f6-170">4</span><span class="sxs-lookup"><span data-stu-id="1b1f6-170">4</span></span>||||<span data-ttu-id="1b1f6-171">4 (standardmäßig eingefügt)</span><span class="sxs-lookup"><span data-stu-id="1b1f6-171">4 (inserted by default)</span></span>|||  

 <span data-ttu-id="1b1f6-172">Basierend auf der obigen Situation können Sie nur das Feld **Menge für Montage** wie folgt ändern:</span><span class="sxs-lookup"><span data-stu-id="1b1f6-172">Based on the above situation, you can only modify the **Quantity to Assemble** field as follows:</span></span>  

-   <span data-ttu-id="1b1f6-173">Die Mindestmenge, die Sie eingeben können, ist 1.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-173">The minimum quantity that you can enter is 1.</span></span> <span data-ttu-id="1b1f6-174">Die Mindestmenge, die Sie eingeben können, ist 1. Dies liegt daran, dass Sie mindestens eine Einheit zusammenbauen müssen, damit Sie die vier Einheiten verkaufen können, wenn davon ausgegangen wird, dass die verbleibenden drei im Lager verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-174">This is because you must at least assemble one unit to be able to sell the four units, assuming that the remaining three are available in the inventory.</span></span>  
-   <span data-ttu-id="1b1f6-175">Die Höchstmenge, die Sie eingeben können, ist 4.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-175">The maximum quantity that you can enter is 4.</span></span> <span data-ttu-id="1b1f6-176">Damit wird sichergestellt, dass Sie nicht mehr als diese Auftragsmontageartikel zusammenbauen, die im Verkauf benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="1b1f6-176">This is to ensure that you do not assemble more of this assemble-to-order item than what is needed on the sale.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1b1f6-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b1f6-177">See Also</span></span>  
[<span data-ttu-id="1b1f6-178">Montageverwaltung</span><span class="sxs-lookup"><span data-stu-id="1b1f6-178">Assembly Management</span></span>](assembly-assemble-items.md)  
[<span data-ttu-id="1b1f6-179">Mit Fertigungsstücklisten arbeiten</span><span class="sxs-lookup"><span data-stu-id="1b1f6-179">Work with Bills of Material</span></span>](inventory-how-work-BOMs.md)  
[<span data-ttu-id="1b1f6-180">Lagerbest</span><span class="sxs-lookup"><span data-stu-id="1b1f6-180">Inventory</span></span>](inventory-manage-inventory.md)  
[<span data-ttu-id="1b1f6-181">Designdetails: Logistik</span><span class="sxs-lookup"><span data-stu-id="1b1f6-181">Design Details: Warehouse Management</span></span>](design-details-warehouse-management.md)  
<span data-ttu-id="1b1f6-182">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="1b1f6-182">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

---
title: "Vorgehensweise: Konvertieren von Serviceverträgen | Microsoft Docs"
description: "Da das Werkzeug zum Ändern des MwSt.-Satzes keine Serviceverträge konvertieren, müssen diese Verträge manuell konvertiert werden. In diesem Thema werden mehrere alternative Methoden beschrieben, die Sie für die Servicevertragkonvertierung verwenden können."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/08/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 29023e68808935b49aba663d994bac756d037615
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="convert-service-contracts-that-include-vat-amounts"></a><span data-ttu-id="2247f-104">Konvertieren von Serviceverträgen, die MwSt.-Beträge enthalten</span><span class="sxs-lookup"><span data-stu-id="2247f-104">Convert Service Contracts that Include VAT Amounts</span></span>
<span data-ttu-id="2247f-105">Da das Werkzeug zum Ändern des MwSt.-Satzes keine Serviceverträge konvertieren, müssen diese Verträge manuell konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="2247f-105">Because the VAT rate change tool cannot convert service contracts, these contracts must be converted manually.</span></span> <span data-ttu-id="2247f-106">In diesem Thema werden mehrere alternative Methoden beschrieben, die Sie für die Servicevertragkonvertierung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="2247f-106">This topic describes several alternative methods that you can use for service contract conversion.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2247f-107">Dieses Thema stellt einen High-Level-Workflow bereit.</span><span class="sxs-lookup"><span data-stu-id="2247f-107">This topic provides a high-level workflow.</span></span>  

 <span data-ttu-id="2247f-108">Nachfolgend wird beschrieben, wie eine Rechnung für einen vorausbezahlten Service-Vertrag korrigiert wird, die ein Jahr im Voraus erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="2247f-108">The following procedure describes how to correct an invoice for a prepaid service contract that has been created a year in advance.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2247f-109">Für dieses Beispiel müssen Sie Ihr Arbeitsdatum in 01.01.2017 ändern.</span><span class="sxs-lookup"><span data-stu-id="2247f-109">For this example, you must change your work date to 01.01.2017.</span></span>  

### <a name="to-correct-an-invoice-for-a-prepaid-service-contract"></a><span data-ttu-id="2247f-110">So korrigieren Sie eine Rechnung für einen vorausbezahlten Servicevertrag</span><span class="sxs-lookup"><span data-stu-id="2247f-110">To correct an invoice for a prepaid service contract</span></span>  
1. <span data-ttu-id="2247f-111">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Vertragsverwaltung** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="2247f-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Contract Management**, and then choose the related link.</span></span>  
2. <span data-ttu-id="2247f-112">Wählen Sie unter **Listen** die Option **Serviceverträge** aus.</span><span class="sxs-lookup"><span data-stu-id="2247f-112">Under **Lists**, choose **Service Contracts**.</span></span>  
3. <span data-ttu-id="2247f-113">Erstellen Sie eines neuen vorausbezahlten Servicevertrags.</span><span class="sxs-lookup"><span data-stu-id="2247f-113">Create a new prepaid service contract.</span></span> <span data-ttu-id="2247f-114">Geben Sie als Startdatum **01.01.2017** und als Fakturierungsjahr für Debitor **20000** ein.</span><span class="sxs-lookup"><span data-stu-id="2247f-114">Enter a start date of **01.01.2017** and an invoice period year for customer **20000**.</span></span>  
4. <span data-ttu-id="2247f-115">Dieser Vertrag muss signiert werden.</span><span class="sxs-lookup"><span data-stu-id="2247f-115">This contract must be signed.</span></span> <span data-ttu-id="2247f-116">Wählen Sie auf der Registerkarte **Start** in der Gruppe **Vorgang** die Option **Vertrag unterzeichnen** aus.</span><span class="sxs-lookup"><span data-stu-id="2247f-116">On the **Home** tab, in the **Process** group, choose **Sign Contract**.</span></span>  
5. <span data-ttu-id="2247f-117">Erstellen Sie eine Servicerechnung.</span><span class="sxs-lookup"><span data-stu-id="2247f-117">Create a service invoice.</span></span>
6. <span data-ttu-id="2247f-118">Die Rechnung wird als nicht gebuchte Servicerechnung aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="2247f-118">The invoice is listed as an unposted service invoice.</span></span> <span data-ttu-id="2247f-119">Um die Servicerechnung einzusehen, wählen Sie **Service**, **Vertragsverwaltung** und dann **Servicerechnungen** aus.</span><span class="sxs-lookup"><span data-stu-id="2247f-119">To view the service invoice, choose **Service**, choose **Contract Management**, and then choose **Service Invoices**.</span></span>  
7. <span data-ttu-id="2247f-120">Buchen Sie die Servicerechnung.</span><span class="sxs-lookup"><span data-stu-id="2247f-120">Post the service invoice.</span></span>  

> [!NOTE]  
>  <span data-ttu-id="2247f-121">Ändern Sie nicht die nicht gebuchte Servicerechnung.</span><span class="sxs-lookup"><span data-stu-id="2247f-121">Do not change the unposted service invoice.</span></span> <span data-ttu-id="2247f-122">Da die Serviceposten erstellt werden, wenn die Rechnung erstellt wird, ändert eine Änderung in der nicht gebuchten Rechnung nicht die bereits erstellten Serviceposten.</span><span class="sxs-lookup"><span data-stu-id="2247f-122">Since the service ledger entries are created when the invoice is created, a change in the unposted invoice will not change the already created service ledger entries.</span></span> <span data-ttu-id="2247f-123">Die MwSt.-Posten werden allerdings erstellt, wenn die Rechnung gebucht wird.</span><span class="sxs-lookup"><span data-stu-id="2247f-123">However, the VAT entries are created when the invoice is posted.</span></span> <span data-ttu-id="2247f-124">So können Sie die allgemeine Produktbuchungsgruppe und die GSP-Produktbuchungsgruppe auf der nicht gebuchten Servicerechnung ändern.</span><span class="sxs-lookup"><span data-stu-id="2247f-124">This lets you change the general product posting group and the GSP product posting group on the unposted service invoice.</span></span>  

### <a name="to-create-a-credit-memo-for-vat-difference"></a><span data-ttu-id="2247f-125">So erstellen Sie eine Gutschrift für MwSt.-Differenzen</span><span class="sxs-lookup"><span data-stu-id="2247f-125">To create a credit memo for VAT difference</span></span>  
<span data-ttu-id="2247f-126">Nachfolgend wird beschrieben, wie eine Gutschrift erstellt wird, die nur die MwSt.-Differenz für die bereits fakturierte Periode enthält, die am **01.07.2017** beginnt.</span><span class="sxs-lookup"><span data-stu-id="2247f-126">The following procedure describes how to create a credit memo that only includes the VAT difference for the already invoiced period starting on **01.07.2017**.</span></span> <span data-ttu-id="2247f-127">In diesem Beispiel wird der MwSt.-Betrag nur auf das Finanzmanagement-Modul gebucht, nicht auf das Service-Modul.</span><span class="sxs-lookup"><span data-stu-id="2247f-127">In this example, the VAT amount is only posted to the Financial Management module, not to the Service Management module.</span></span> <span data-ttu-id="2247f-128">Die MwSt.-Posten, die mit dem Serviceposten verknüpft sind, werden nicht korrigiert.</span><span class="sxs-lookup"><span data-stu-id="2247f-128">The VAT entries that are linked to the service ledger entry will not be corrected.</span></span>  

1. <span data-ttu-id="2247f-129">Erstellen Sie ein neues Sachkonto für die MwSt.-Differenz.</span><span class="sxs-lookup"><span data-stu-id="2247f-129">Create a new general ledger account for the VAT difference.</span></span> <span data-ttu-id="2247f-130">Dieses Konto wird für die direkte Buchung der MwSt.-Korrektur verwendet.</span><span class="sxs-lookup"><span data-stu-id="2247f-130">This account will be used for direct posting of the VAT correction.</span></span>  
2. <span data-ttu-id="2247f-131">Fügen Sie der MwSt.-Buchung eine neue Zeile hinzu.</span><span class="sxs-lookup"><span data-stu-id="2247f-131">Add a new line to the VAT posting setup.</span></span>  

### <a name="to-create-contract-expiration-dates-in-contract-lines"></a><span data-ttu-id="2247f-132">So erstellen Sie Vertragsablaufdaten in Vertragszeilen</span><span class="sxs-lookup"><span data-stu-id="2247f-132">To create contract expiration dates in contract lines</span></span>  
<span data-ttu-id="2247f-133">Die folgende Vorgehensweise beschreibt, wie Sie neue Verträge erstellen, indem sie in Servicevertragszeilen mit Kontaktablaufdaten arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2247f-133">The following procedure describes how to create new contracts by working with contract expiration dates in service contract lines.</span></span>  

1. <span data-ttu-id="2247f-134">Im Fenster **Servicevertag** legen Sie das Vertragsablaufdatum auf **30.06.2017** fest.</span><span class="sxs-lookup"><span data-stu-id="2247f-134">In the **Service Contract** window, set the contract expiration date to **30.06.2017**.</span></span>  
2. <span data-ttu-id="2247f-135">Wählen Sie die Aktionen **Verkaufsgutschrift erstellen** aus, um automatisch eine Gutschrift für Juli 2017 bis Dezember 2017 zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2247f-135">Choose the **Create Credit Memo** action to automatically create a credit memo for July 2017 to December 2017.</span></span>  
3. <span data-ttu-id="2247f-136">Da der Vertrag abgelaufen ist, müssen Sie einen neuen Vertrag für die Periode mit dem neuen Mehrwertsteuersatz für 1. Juli 2017 bis 31. Dezember 2017 erstellen.</span><span class="sxs-lookup"><span data-stu-id="2247f-136">Because the contract has expired, you need to create a new contract for the period with the new VAT rate for July 1, 2017 to December 31, 2017.</span></span>  

### <a name="to-create-a-new-credit-memo"></a><span data-ttu-id="2247f-137">Eine neue Gutschrift erstellen:</span><span class="sxs-lookup"><span data-stu-id="2247f-137">To create a new credit memo</span></span>  
<span data-ttu-id="2247f-138">Nachfolgend wird beschrieben, wie eine neue Gutschrift mithilfe des Batchauftrags **Vorausbez. Vertragsposten holen** erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2247f-138">The following procedure describes how to create a new credit memo using the **Get Prepaid Contract Entries** batch job.</span></span> <span data-ttu-id="2247f-139">Posten, die Sie nicht von Januar 2017 bis Juni 2017 korrigieren möchten, werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="2247f-139">Entries that you do not want to correct from January 2017 to June 2017 will be deleted.</span></span>  

1. <span data-ttu-id="2247f-140">Führen Sie das Werkzeug zum Ändern des MwSt.-Satzes am 1. Juli 2017 aus.</span><span class="sxs-lookup"><span data-stu-id="2247f-140">Run the VAT rate change tool on July 1, 2017.</span></span> <span data-ttu-id="2247f-141">Die allgemeine Produktbuchungsgruppe oder die MwSt-Produktbuchungsgruppe werden geändert.</span><span class="sxs-lookup"><span data-stu-id="2247f-141">The general product posting group or the VAT product posting group is changed.</span></span> <span data-ttu-id="2247f-142">Weitere Informationen Sie unter [Arbeiten mit MwSt im Verkauf und Einkauf](finance-work-with-vat.md).</span><span class="sxs-lookup"><span data-stu-id="2247f-142">For more information, see [Work with VAT on Sales and Purchases](finance-work-with-vat.md).</span></span>  
2. <span data-ttu-id="2247f-143">Nachdem Sie das Werkzeug zum Ändern des MwSt.-Satzes ausgeführt haben, können Sie ein Vertragsablaufdatum für den Servicevertrag eingeben.</span><span class="sxs-lookup"><span data-stu-id="2247f-143">After running the VAT rate change tool, enter a contract expiration date for the service contract.</span></span> <span data-ttu-id="2247f-144">Sie können die Servicevertragszeile jetzt löschen und eine neue Zeile erstellen, die mit der alten identisch ist.</span><span class="sxs-lookup"><span data-stu-id="2247f-144">You can now delete the service contract line and create a new line that is identical to the old one.</span></span>  
3. <span data-ttu-id="2247f-145">Erstellen Sie eine neue Rechnung für die Periode von Januar 2017 bis Dezember 2012 unter Verwendung des neuen Mehrwertsteuersatzes.</span><span class="sxs-lookup"><span data-stu-id="2247f-145">Create a new invoice for the period of January 2017 to December 2012 using the new VAT rate.</span></span>  
4. <span data-ttu-id="2247f-146">Um eine andere Gutschrift zu erstellen, wählen Sie im Fenster **Servicegutschriften** die Option **Neu** aus, um eine neue Servicegutschrift zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2247f-146">To create another credit memo, in the **Service Credit Memos** window, choose **New** to create a new service credit memo.</span></span>  
5. <span data-ttu-id="2247f-147">Wählen Sie die **Vorausbez. Vertragsposten holen** Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="2247f-147">Choose the **Get Prepaid Contract Entries** action.</span></span>  
6. <span data-ttu-id="2247f-148">Nachdem die Konvertierung abgeschlossen ist, sind MwSt.- und Serviceposten korrekt.</span><span class="sxs-lookup"><span data-stu-id="2247f-148">After the conversion is complete, VAT and service ledger entries will be correct.</span></span>  

## <a name="see-also"></a><span data-ttu-id="2247f-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2247f-149">See Also</span></span>  
[<span data-ttu-id="2247f-150">Arbeiten mit Serviceverträgen und Servicevertragsangeboten</span><span class="sxs-lookup"><span data-stu-id="2247f-150">Work with Service Contracts and Service Contract Quotes</span></span>](service-how-to-create-service-contracts-and-service-contract-quotes.md)  
[<span data-ttu-id="2247f-151">Finanzen</span><span class="sxs-lookup"><span data-stu-id="2247f-151">Finance</span></span>](finance.md)  
[<span data-ttu-id="2247f-152">Melden von MwSt. an die Steuerbehörden</span><span class="sxs-lookup"><span data-stu-id="2247f-152">Report VAT to Tax Authorities</span></span>](finance-how-report-vat.md)  
[<span data-ttu-id="2247f-153">Arbeiten mit MwSt im Verkauf und Einkauf</span><span class="sxs-lookup"><span data-stu-id="2247f-153">Work with VAT on Sales and Purchases</span></span>](finance-work-with-vat.md)  

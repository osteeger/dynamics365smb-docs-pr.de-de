---
title: Verwenden Sie die Zahlungsvorschlag-Stapelverarbeitung| Microsoft Docs
description: "Sie können Kreditorenzahlungseinstellungen festlegen, um Vorschläge zu erhalten oder damit für Zahlungen, die in Kürze fällig sind, oder denen ein Rabatt verfügbar ist."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: vendor payment, creditor, debt, balance due, AP
ms.date: 05/15/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: eb17659fc78865acae6c7cb969adf715eb858882
ms.openlocfilehash: 442f19dadefe01f9df2402bb5dc6ad0f4a3cb786
ms.contentlocale: de-de
ms.lasthandoff: 09/17/2018

---
# <a name="suggest-vendor-payments"></a><span data-ttu-id="8581f-103">Zahlungsvorschlag</span><span class="sxs-lookup"><span data-stu-id="8581f-103">Suggest Vendor Payments</span></span>
<span data-ttu-id="8581f-104">Im Fenster **Zahlungsjournal** können Sie die Stapelverarbeitung **Zahlungsvorschlag** verwenden, um Zahlungspositionen vorzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="8581f-104">In the **Payment Journal** window, you can use the **Suggest Vendor Payments** batch job to suggest payment lines.</span></span> <span data-ttu-id="8581f-105">Zeilen für Elemente wie Zahlungen, die in Kürze fällig sind oder Zahlungen, bei denen ein Rabatt verfügbar ist, werden entsprechend Ihren Einstellungen vorgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="8581f-105">Lines for payments that are due soon or payments where a payment discount is available are suggested based on your settings.</span></span>

<span data-ttu-id="8581f-106">Um aus vorgeschlagenen Zeilen voll zu profitieren, müssen Sie zuerst die Kreditoren priorisieren.</span><span class="sxs-lookup"><span data-stu-id="8581f-106">To benefit fully from payment suggestions, you must first prioritize your vendors.</span></span> <span data-ttu-id="8581f-107">Weitere Informationen finden Sie unter [Priorisieren von Kreditoren](purchasing-how-prioritize-vendors.md).</span><span class="sxs-lookup"><span data-stu-id="8581f-107">For more information, see [Prioritize Vendors](purchasing-how-prioritize-vendors.md).</span></span>  

> [!NOTE]  
> <span data-ttu-id="8581f-108">In die Stapelverarbeitung werden nur die Kreditorenposten einbezogen, bei denen das Feld **Abwarten** nicht markiert ist.</span><span class="sxs-lookup"><span data-stu-id="8581f-108">Vendor ledger entries that are **On Hold** are not included in the batch job.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="8581f-109">Wenn Sie Skonti nutzen möchten und einen verfügbaren Betrag eingegeben haben, wird der Rechnungsrabatt verwendet für:</span><span class="sxs-lookup"><span data-stu-id="8581f-109">If you want to take advantage of payment discounts, and have entered an available amount, the amount will be used for:</span></span>  
    * <span data-ttu-id="8581f-110">Priorisierte überfällige Kreditorenposten nach der Priorität.</span><span class="sxs-lookup"><span data-stu-id="8581f-110">Prioritized overdue vendor entries first in order of priority.</span></span>   
    * <span data-ttu-id="8581f-111">Überfällige Kreditorenposten, die nicht berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="8581f-111">Overdue vendor entries that are not prioritized.</span></span>  
    * <span data-ttu-id="8581f-112">Öffnen Sie die Kreditorenposten, die sich für Rabatte qualifizieren, angeordnet nach Kreditorennummer.</span><span class="sxs-lookup"><span data-stu-id="8581f-112">Open vendor entries that qualify for payment discounts, arranged by vendor number.</span></span>  

## <a name="to-use-the-suggest-vendor-payments-function"></a><span data-ttu-id="8581f-113">Die Zahlungsvorschlagfunktion verwenden</span><span class="sxs-lookup"><span data-stu-id="8581f-113">To use the Suggest Vendor Payments function</span></span>
1. <span data-ttu-id="8581f-114">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Zahlungs-Buchblatt** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="8581f-114">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Journals**, and then choose the related link.</span></span>  
2. <span data-ttu-id="8581f-115">Öffnen Sie das relevante Buch.-Blatt, und klicken Sie dann auf die Aktion **Zahlungsvorschlag**.</span><span class="sxs-lookup"><span data-stu-id="8581f-115">Open the relevant journal, and then choose the **Suggest Vendor Payments** action.</span></span>  
3. <span data-ttu-id="8581f-116">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="8581f-116">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. <span data-ttu-id="8581f-117">Wählen Sie die Schaltfläche **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="8581f-117">Choose the **OK** button.</span></span>  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines"></a><span data-ttu-id="8581f-118">Einfügen des Fälligkeitsdatum als Buchungsdatum auf Zahlungsausgangs Buch.-Blattzeilen</span><span class="sxs-lookup"><span data-stu-id="8581f-118">To insert the due date as posting date on payment journal lines</span></span>
<span data-ttu-id="8581f-119">Wenn Sie die Stapelverarbeitung **Zahlungsvorschlag** verwenden, um Zahlungszeilen für Ihre Kreditoren zu erstellen, können Sie zwei Felder ausfüllen, um sicherzustellen, dass die erzeugten Zeilen das Fälligkeitsdatum verwenden, um das Buchungsdatum zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="8581f-119">When you use the **Suggest Vendor Payments** batch job to create payment lines for your vendors, you can fill two special fields to make sure that the generated lines use the due date to calculate the posting date.</span></span> <span data-ttu-id="8581f-120">Diese Felder sind **Buchungsdatum von Fälligkeitsdatum für Ausgleich mit Beleg berechnen** und **Offset für Fälligkeitsdatum für Ausgleich mit Beleg**.</span><span class="sxs-lookup"><span data-stu-id="8581f-120">These fields are **Calculate Posting Date from Applies-to-Doc Due Date** and **Applies-to-Doc Due Date Offset**.</span></span>  

> [!IMPORTANT]  
>   <span data-ttu-id="8581f-121">Sie können das Feld **Buchungsdatum von Fälligkeitsdatum für Ausgleich mit Beleg berechnen** nicht zusammen mit den Feldern **Skonto finden** oder **Pro Kreditor summieren** verwenden.</span><span class="sxs-lookup"><span data-stu-id="8581f-121">You cannot use the **Calculate Posting Date from Applies-to-Doc Due Date** field together with the **Find Payment Discounts** field or the **Summarize per Vendor** field.</span></span> <span data-ttu-id="8581f-122">Der Grund besteht darin, dass, wenn das Buchungsdatum auf dem Fälligkeitsdatum liegt, einige Zahlungsrabatte nicht korrekt berechnet werden, da das Buchungsdatum nach dem Zahlungsrabattdatum liegen kann.</span><span class="sxs-lookup"><span data-stu-id="8581f-122">If the posting date is based on the due date, some payment discounts may not calculate correctly because the posting date is after the payment discount date.</span></span>  

<span data-ttu-id="8581f-123">Wenn das berechnete Buchungsdatum also in der Vergangenheit liegt, wird das Buchungsdatum auf das Arbeitsdatum verschoben, und eine Warnung wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8581f-123">Also, if the calculated posting date is in the past, then the posting date is moved up to the work date, and a warning is displayed.</span></span>  

<span data-ttu-id="8581f-124">Alternativ können Sie Zahlungspositionen mithilfe des Fälligkeitsdatums manuell generieren, um das Buchungsdatum zu berechnen</span><span class="sxs-lookup"><span data-stu-id="8581f-124">Alternatively, you can manually create payment lines using the due date to calculate the posting date.</span></span> <span data-ttu-id="8581f-125">Nachdem Sie Kreditorenposten ausgleichen, können Sie die Aktion **Buchungsdatum berechnen** verwenden, um das Buchungsdatum der Buch.-Blattzeile mit dem Fälligkeitsdatum der zugehörigen Einkaufsrechnung zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8581f-125">After you apply vendor ledger entries, you can use the **Calculate Posting Date** action to update the posting date on the journal line with the due date of the related purchase invoice.</span></span> <span data-ttu-id="8581f-126">Weitere Informationen finden Sie unter [Einkaufstransaktionen manuell ausgleichen](payables-how-apply-purchase-transactions-manually.md).</span><span class="sxs-lookup"><span data-stu-id="8581f-126">For more information, see [Apply Purchase Transactions Manually](payables-how-apply-purchase-transactions-manually.md).</span></span>  

> [!NOTE]  
>   <span data-ttu-id="8581f-127">Wenn die Einkaufsrechnung überfällig ist, wird das Buchungsdatum auf das Arbeitsdatum festgelegt, und die Schrift auf der Zeile wird in roter Farbe angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8581f-127">If the purchase invoice is overdue, the posting date is set to the work date, and the font on the line becomes red.</span></span>  

## <a name="see-also"></a><span data-ttu-id="8581f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8581f-128">See Also</span></span>
[<span data-ttu-id="8581f-129">Verwalten von Verbindlichkeiten</span><span class="sxs-lookup"><span data-stu-id="8581f-129">Managing Payables</span></span>](payables-manage-payables.md)  
[<span data-ttu-id="8581f-130">Zahlungen vornehmen</span><span class="sxs-lookup"><span data-stu-id="8581f-130">Making Payments</span></span>](payables-make-payments.md)  
[<span data-ttu-id="8581f-131">Arbeiten mit Fibu Buch.-Blättern</span><span class="sxs-lookup"><span data-stu-id="8581f-131">Working with General Journals</span></span>](ui-work-general-journals.md)  
<span data-ttu-id="8581f-132">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="8581f-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>  

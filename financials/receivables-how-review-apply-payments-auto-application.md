---
title: "Prüfen Sie automatisch übernommene Zahlungen, und wenden Sie Zahlungen manuell erneut an | Microsoft Docs"
description: "Nachdem Zahlungen automatisch ausgeglichen sind, können Sie alle Posten für eine Zahlung manuell überprüfen und diejenigen erneut ausgleichen, die fehlerhaft ausgeglichen wurden."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, reconcile payment, expenses, cash receipts
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: 745766657fe7e993aaa689f0074c4f4a41e0090c
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="review-or-apply-payments-manually-after-automatic-application"></a><span data-ttu-id="c2e85-103">Zahlungen manuell zuordnen oder überprüfen nach der automatischen Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="c2e85-103">Review or Apply Payments Manually After Automatic Application</span></span>
<span data-ttu-id="c2e85-104">Für jede Buch.-Blattzeile, die ein Zahlung im Fenster **Zahlungsabstimmungsbuch.-Blatt** darstellt, können Sie das Fenster **Zahlungsanwendung** öffnen, um alle offenen Kandidatenposten für die Zahlung anzuzeigen und detaillierte Informationen für jeden Posten zum Datenabgleich anzuzeigen, auf denen eine Zahlungsanwendung basiert.</span><span class="sxs-lookup"><span data-stu-id="c2e85-104">For each journal line representing a payment in the **Payment Reconciliation Journal** window, you can open the **Payment Application** window to see all candidate open entries for the payment and view detailed information for each entry about the data matching that a payment application is based on.</span></span> <span data-ttu-id="c2e85-105">Hier können Sie manuell Zahlungen ausgleichen, oder Zahlungen erneut ausgleichen, die automatisch auf einen falschen offenen Posten angewendet wurden,.</span><span class="sxs-lookup"><span data-stu-id="c2e85-105">Here, you can manually apply payments or reapply payments that were applied automatically to a wrong entry.</span></span> <span data-ttu-id="c2e85-106">Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).</span><span class="sxs-lookup"><span data-stu-id="c2e85-106">For more information about automatic application, see [Reconcile Payments Using Automatic Application](receivables-how-reconcile-payments-auto-application.md).</span></span>

> [!IMPORTANT]  
>   <span data-ttu-id="c2e85-107">Wenn das Bankkonto, für das Sie Zahlungen abstimmen, für die Mandantenwährung eingerichtet ist, zeigt das Fenster **Zahlungsanwendung** alle offenen Posten in Mandantenwährung, einschließlich offener Posten für Belege, die ursprünglich in Fremdwährungen fakturiert wurden.</span><span class="sxs-lookup"><span data-stu-id="c2e85-107">When the bank account that you are reconciling payments for is set up for the local currency, then the **Payment Application** window will show all open entries in the local currency, including open entries for documents that were originally invoiced in foreign currencies.</span></span> <span data-ttu-id="c2e85-108">Zahlungen, die mit Posten mit umgerechneten Währungen ausgeglichen wurden, werden daher aufgrund von möglicherweise verschiedenen Wechselkursen, die von der Bank bzw. [!INCLUDE[d365fin](includes/d365fin_md.md)] verwendet werden, möglicherweise mit anderen Beträgen als im ursprünglichen Beleg gebucht.</span><span class="sxs-lookup"><span data-stu-id="c2e85-108">Payments applied to entries with converted currencies may therefore be posted with different amounts than on the original document because of the potentially different exchange rates used by the bank and [!INCLUDE[d365fin](includes/d365fin_md.md)] respectively.</span></span>

<span data-ttu-id="c2e85-109">Daher empfiehlt es sich, dass Sie nach Fremdwährungscodes im Feld **Fremdwährungscode** im Fenster **Zahlungsanwendung** suchen, um zu überprüfen, ob Anwendungen auf umgerechneten Währungen basieren.</span><span class="sxs-lookup"><span data-stu-id="c2e85-109">Therefore, we recommend that you look for foreign currency codes in the **Currency Code** field in the **Payment Application** window to check if applications are based on converted currencies.</span></span> <span data-ttu-id="c2e85-110">Um den Originaldokumentbetrag in Fremdwährung zu überprüfen und den verwendeten Wechselkurs anzuzeigen, aktivieren Sie das Feld **Auf Eintragsnr. anwenden** und wählen dann das Dropdown-Menü, um **Debitorenposen** oder **Kreditorenposten** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="c2e85-110">To review the original document amount in the foreign currency and to see the exchange rate used, choose the **Applies-to Entry No.** field, and then, on the shortcut menu, choose the drilldown button to open the **Customer Ledger Entries** or **Vendor Ledger Entries** window.</span></span>

<span data-ttu-id="c2e85-111">Gewinn-und-Verlust-Ausgleich, der aufgrund der Fakturierung des Projekts erforderlich ist, wird nicht automatisch durch [!INCLUDE[d365fin](includes/d365fin_md.md)]verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c2e85-111">Any gains-and-loss adjustment required due to currency conversions is not handled automatically by [!INCLUDE[d365fin](includes/d365fin_md.md)].</span></span>

> [!NOTE]  
>   <span data-ttu-id="c2e85-112">Sie können Posten mit einem anderen Vorzeichen als dem Vorzeichen der Zahlung nicht ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="c2e85-112">You cannot apply entries with a different sign than the sign on the payment.</span></span> <span data-ttu-id="c2e85-113">Um beispielsweise sowohl eine Gutschrift mit negativem Vorzeichen als auch die zugehörige Rechnung mit positivem Vorzeichen abzuschließen, müssen Sie zuerst die Gutschrift mit der Rechnung ausgleichen und dann die Zahlung mit der Rechnung mit dem reduzierten Restbetrag ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="c2e85-113">For example, to close both a negative-sign credit memo and its related positive-sign invoice, you must first apply the credit memo to the invoice, and then apply the payment to the invoice with the reduced remaining amount.</span></span>

> [!WARNING]  
>   <span data-ttu-id="c2e85-114">**Warnung:** Falls Sie Rechnungsrabatte verwenden, und wenn das Fälligkeitsdatum vor dem Zahlungsfälligkeitsdatum ist, wird das Feld Verbleibender Betrag inkl. Rabatt im Fenster **Zahlungsanwendung** verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2e85-114">If you use payment discounts, and if the payment date is before the payment due date, then the **Remaining Amt. Incl. Discount** field in the **Payment Application** window will be used for matching.</span></span> <span data-ttu-id="c2e85-115">Ansonsten wird der Wert aus dem Feld **Verbleibender Betrag** verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2e85-115">Otherwise, the value in the **Remaining Amount** field will be used.</span></span> <span data-ttu-id="c2e85-116">Wenn die Zahlung mit einem verbilligten Betrag nach dem Zahlungsfälligkeitsdatum geleistet wurde oder der Totalbetrag bezahlt wurde, aber ein Skonto gewährt wurde, wird der Betrag nicht abgeglichen.</span><span class="sxs-lookup"><span data-stu-id="c2e85-116">If the payment was made with a discounted amount after the payment due date, or the full amount was paid but a discount was granted, then the amount will not be matched.</span></span>

> [!NOTE]  
>   <span data-ttu-id="c2e85-117">Sie können eine Zahlung nur mit einem Konto ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="c2e85-117">You can only apply a payment to one account.</span></span> <span data-ttu-id="c2e85-118">Wenn die Anwendung auf mehrere offene Posten aufteilen möchten, zum Beispiel, um eine Pauschalzahlung auszugleichen, müssen die offenen Posten für das gleiche Konto sein.</span><span class="sxs-lookup"><span data-stu-id="c2e85-118">If you want to split the application on multiple open entries, for example to apply a lump-sum payment, then the open entries must be for the same account.</span></span> <span data-ttu-id="c2e85-119">Weitere Informationen finden Sie in den Schritten 7 und 8 dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="c2e85-119">For more information, see steps 7 and 8 in the procedure in this topic.</span></span>

## <a name="to-review-or-apply-payments-after-automatic-application"></a><span data-ttu-id="c2e85-120">Vorgehensweise: Überprüfen oder Ausgleichen von Zahlungen nach automatischer Anwendung</span><span class="sxs-lookup"><span data-stu-id="c2e85-120">To review or apply payments after automatic application</span></span>
1. <span data-ttu-id="c2e85-121">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Zahlungsabstimmungsbuch.-Blatt** ein und wählen den zugehörenden Link aus.</span><span class="sxs-lookup"><span data-stu-id="c2e85-121">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Payment Reconciliation Journals**, and then choose the related link.</span></span>
2. <span data-ttu-id="c2e85-122">Öffnen Sie das Zahlungsabstimmungsbuch.-Blatt für ein Bankkonto, für das Sie Zahlungen abstimmen möchten.</span><span class="sxs-lookup"><span data-stu-id="c2e85-122">Open the payment reconciliation journal for a bank account that you want to reconcile payments for.</span></span> <span data-ttu-id="c2e85-123">Weitere Informationen finden Sie unter [Abstimmen von Zahlungen mithilfe der automatischen Anwendung](receivables-how-reconcile-payments-auto-application.md).</span><span class="sxs-lookup"><span data-stu-id="c2e85-123">For more information, see [Reconcile Payments Using Automatic Application](receivables-how-reconcile-payments-auto-application.md).</span></span>
3. <span data-ttu-id="c2e85-124">Im Fenster **Zahlungsabstimmungsbuch.-Blatt** wählen Sie eine Zahlung, die Sie mit einem oder mehreren offenen Posten manuell anwenden oder überprüfen möchten und wählen dann **Manuell Anwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="c2e85-124">In the **Payment Reconciliation Journal** window, select a payment that you want to review or manually apply to one or more open entries, and then choose the **Apply Manually** action.</span></span>
4. <span data-ttu-id="c2e85-125">Aktivieren Sie das Kontrollkästchen **Angewendet** für die Position mit dem offenen Eintrag aus, auf den die Zahlung angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2e85-125">Select the **Applied** check box on the line for the open entry that you want to apply the payment to.</span></span>
5. <span data-ttu-id="c2e85-126">Der Zahlungsbetrag, der auch im Feld **Transaktionsbetrag** unter **Zahlungszuordnung** angezeigt wird, wird im Feld **Zugeordneter Betrag** angezeigt wird, aber Sie können das Feld bearbeiten, wenn Sie zum Beispiel den Betrag auf mehrere offene Posten anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="c2e85-126">The payment amount, which is also shown in the **Transaction Amount** field in the **Payment Application** window, is inserted in the **Applied Amount** field, but you can modify the field, for example if you want to apply the amount to several open entries.</span></span>
6. <span data-ttu-id="c2e85-127">Um einen Teil des bezahlten Betrag in einem anderen offenen Posten für das Konto auszugleichen, beispielsweise um eine Pauschalzahlung auszugleichen, aktivieren Sie das Kontrollkästchen **Zugeordnet** für die Position.</span><span class="sxs-lookup"><span data-stu-id="c2e85-127">To apply a part of the paid amount to another open entry for the account, for example to apply a lump-sum payment, select the **Applied** check box for the line.</span></span> <span data-ttu-id="c2e85-128">Der Ausgleichsbetrag wird automatisch von dem Transaktionsbetrag abgezogen, um die Verteilung in den beiden offenen Posten widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="c2e85-128">The applied amount is automatically deducted from the transactions amount to reflect the distribution on the two open entries.</span></span>
7. <span data-ttu-id="c2e85-129">Um einen Teil einer Zahlung mit einem oder mehreren offenen Posten zu übernehmen die nicht in der Datenbank vorhanden sind, erstellen Sie eine neue Zeile unter der Zeile für das gleiche Konto.</span><span class="sxs-lookup"><span data-stu-id="c2e85-129">To apply a part of a payment to one or more open entries that does not exist in the database, create a new line under the line for the same account.</span></span> <span data-ttu-id="c2e85-130">Geben Sie im Feld **Zugeordneter Betrag** den Betrag ein, der der neuen Zeile zugeordnet werden soll und passen Sie dann das Feld **Zugeordneter Betrag** auf der bestehenden Zeile an.</span><span class="sxs-lookup"><span data-stu-id="c2e85-130">In the **Applied Amount** field, enter the amount to apply on the new line, and then adjust the **Applied Amount** field on the existing line.</span></span>
8. <span data-ttu-id="c2e85-131">Wiederholen Sie Schritt 5, 6 oder 7 für andere offene Posten, auf die Sie einen vollständige Zahlung oder Teilzahlung anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="c2e85-131">Repeat steps 5, 6, or 7 for other open entries that you want to apply a full or partial payment amount to.</span></span>
9. <span data-ttu-id="c2e85-132">Wenn Sie eine Zahlungs-Anwendung überprüft oder manuell auf einen oder mehrere offene Posten angewendet haben, wählen **Anwendung akzeptieren** aus.</span><span class="sxs-lookup"><span data-stu-id="c2e85-132">When you have reviewed a payment application or manually applied to one or more open entries, choose the **Accept Application** action.</span></span>

<span data-ttu-id="c2e85-133">Das Fenster **Zugeordnete Zahlung** wird geschlossen und im Fenster **Zahlungsabstimmungsbuch.-Blatt** wird der Wert im Feld **Übereinstimmungsgenauigkeit** auf **Zugeordnet** geändert, um Ihnen mitzuteilen, dass Sie die Zahlung überprüft oder manuell angewendet haben.</span><span class="sxs-lookup"><span data-stu-id="c2e85-133">The **Payment Application** window  closes, and in the **Payment Reconciliation Journal** window, the value in the **Match Confidence** field is changed to **Accepted** to indicate to you that you have reviewed or manually applied the payment.</span></span>

## <a name="see-also"></a><span data-ttu-id="c2e85-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2e85-134">See Also</span></span>
[<span data-ttu-id="c2e85-135">Verwalten von Forderungen</span><span class="sxs-lookup"><span data-stu-id="c2e85-135">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="c2e85-136">Verkauf</span><span class="sxs-lookup"><span data-stu-id="c2e85-136">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="c2e85-137">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="c2e85-137">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

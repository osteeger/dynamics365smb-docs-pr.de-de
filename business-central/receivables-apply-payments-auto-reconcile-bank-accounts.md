---
title: Zahlungen automatisch vornehmen und Bankkonten abstimmen| Microsoft Docs
description: "Zeigt Aufgaben, um Ihre Bank, Verkaufs- und Kreditorensammelkonte, Beitragszahlungseingänge oder Kosten auszugleichen und gleicht Zahlungen automatisch aus."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: payment process, direct payment posting, reconcile payment, expenses, cash receipts
ms.date: 02/28/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 992e51f11d11b86685cf6de813e0b7610350a6a7
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="applying-payments-automatically-and-reconciling-bank-accounts"></a><span data-ttu-id="89d43-103">Zahlungen automatisch vornehmen und Bankkonten abstimmen</span><span class="sxs-lookup"><span data-stu-id="89d43-103">Applying Payments Automatically and Reconciling Bank Accounts</span></span>
<span data-ttu-id="89d43-104">Sie müssen Ihre Bank, Debitoren- und Kreditorensammelkonten routinemäßig abstimmen, indem Sie die Zahlungen, die in Ihrem Bankkonto aufgezeichnet sind, mit ihren entsprechenden unbezahlten Rechnungen und Gutschriften oder anderen offenen Posten im [!INCLUDE[d365fin](includes/d365fin_long_md.md)]ausgleichen.</span><span class="sxs-lookup"><span data-stu-id="89d43-104">You must regularly reconcile your bank, receivables, and payables accounts by applying payments recorded in the bank to their related unpaid invoices and credit memos or other open entries in [!INCLUDE[d365fin](includes/d365fin_long_md.md)].</span></span>  

<span data-ttu-id="89d43-105">Diese Aufgabe können Sie dann im Fenster **Zahlungs-Abstimmungs-Buch.-Blatt** ausführen, indem Sie eine Bankkontoauszugsdatei oder einen Feed importieren, um die Zahlungen schnell zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="89d43-105">You can perform this task in the **Payment Reconciliation Journal** window by importing a bank statement file or feed to quickly register the payments.</span></span> <span data-ttu-id="89d43-106">Die Zahlungen werden angewendet, um Debitoren- oder Kreditorenposten zu öffnen, indem passender Zahlungstext und Zahlungsinformationen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="89d43-106">Payments are applied to open customer or vendor ledger entries based on matches between payment text and entry information.</span></span> <span data-ttu-id="89d43-107">Sie können auch automatische Anwendungen überprüfen und ändern, bevor Sie das Blatt buchen.</span><span class="sxs-lookup"><span data-stu-id="89d43-107">You can review and change automatic applications before you post the journal.</span></span> <span data-ttu-id="89d43-108">Sie können die offenen Bankkontoposten für ausgeglichenen Posten schließen, wenn Sie das Buch.-Blatt buchen.</span><span class="sxs-lookup"><span data-stu-id="89d43-108">You can choose to close any open bank account ledger entries related to the applied ledger entries when you post the journal.</span></span> <span data-ttu-id="89d43-109">Das bedeutet, dass das Bankkonto automatisch abgestimmt wird, wenn alle Zahlungen ausgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="89d43-109">The bank account is automatically reconciled when all payments are applied.</span></span>

<span data-ttu-id="89d43-110">Sie können auch, Bankkonten abstimmen ohne Zahlungen gleichzeitig anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="89d43-110">You can also reconcile bank accounts without simultaneously applying payments.</span></span> <span data-ttu-id="89d43-111">Sie führen diese Arbeiten im Fenster **Bankkonto Abstimmen** aus.</span><span class="sxs-lookup"><span data-stu-id="89d43-111">You perform this work in the **Bank Acc. Reconciliation** window.</span></span> <span data-ttu-id="89d43-112">Weitere Informationen finden Sie unter [Vorgehensweise: Einrichten von Bankkonten](bank-how-reconcile-bank-accounts-separately.md).</span><span class="sxs-lookup"><span data-stu-id="89d43-112">For more information, see [Reconcile Bank Account Separately](bank-how-reconcile-bank-accounts-separately.md).</span></span>   

<span data-ttu-id="89d43-113">Um den Import von Bankkontoauszügen als Bankfeed zu aktivieren, müssen Sie den Bank-Feed-Service Envestnet Yodlee anlegen und aktivieren und dann Ihr Bankkonto mit den entsprechenden Online Bankkonten verbinden.</span><span class="sxs-lookup"><span data-stu-id="89d43-113">To import bank statements as a bank feed, you must first set up and enable the Envestnet Yodlee Bank Feed service, and then link your bank accounts to the related online bank accounts.</span></span> <span data-ttu-id="89d43-114">Für weitere Informationen, siehe [Einrichten des Envestnet Yodlee Bank-Feed-Service](bank-how-setup-bank-statement-service.md).</span><span class="sxs-lookup"><span data-stu-id="89d43-114">For more information, see [Set Up the Envestnet Yodlee Bank Feeds Service](bank-how-setup-bank-statement-service.md).</span></span>  

<span data-ttu-id="89d43-115">Sie können auch die Funktion für den Bankdatenkonvertierungsdienst verwenden, um eine Bankkontoauszugsdatei, die Sie von Ihrer Bank erhalten, in einen Datenstream zu konvertieren, den Sie in das [!INCLUDE[d365fin](includes/d365fin_long_md.md)] importieren können.</span><span class="sxs-lookup"><span data-stu-id="89d43-115">Alternatively, you can use the bank data conversion service to convert a bank statement file, from any format, to a data stream that you can import into [!INCLUDE[d365fin](includes/d365fin_long_md.md)].</span></span> <span data-ttu-id="89d43-116">Für weitere Informationen, siehe [Einrichten des Bankdaten-Konvertierungsdienst](bank-how-setup-bank-data-conversion-service.md).</span><span class="sxs-lookup"><span data-stu-id="89d43-116">For more information, see [Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md).</span></span>  

<span data-ttu-id="89d43-117">In der folgenden Tabelle wird eine Reihe von Aufgaben mit Verknüpfungen zu den beschriebenen Themen erläutert.</span><span class="sxs-lookup"><span data-stu-id="89d43-117">The following table describes a sequence of tasks, with links to the topics that describe them.</span></span>  

| <span data-ttu-id="89d43-118">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="89d43-118">To</span></span> | <span data-ttu-id="89d43-119">Siehe</span><span class="sxs-lookup"><span data-stu-id="89d43-119">See</span></span> |
| --- | --- |
| <span data-ttu-id="89d43-120">Zahlungen verwenden, um Debitoren- oder Kreditorenposten zu öffnen, indem Sie einen Bankkontoauszug importieren und das Bankkonto abstimmen, wenn alle Zahlungen ausgeglichen werden.</span><span class="sxs-lookup"><span data-stu-id="89d43-120">Apply payments to open customer or vendor ledger entries by importing a bank statement, and reconcile the bank account when all payments are applied.</span></span> |[<span data-ttu-id="89d43-121">Abstimmen von Zahlungen mithilfe der automatischen Anwendung</span><span class="sxs-lookup"><span data-stu-id="89d43-121">Reconcile Payments Using Automatic Application</span></span>](receivables-how-reconcile-payments-auto-application.md) |
| <span data-ttu-id="89d43-122">Gleichen Sie manuell Zahlungen aus, indem Sie detaillierte Informationen über zugeordnete Daten und Vorschläge für offene Kandidatenposten anzeigen, mit denen Zahlungen ausgeglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="89d43-122">Manually apply payments by viewing detailed information about matched data and suggestions for candidate open entries to apply payments to.</span></span> |[<span data-ttu-id="89d43-123">Überprüfen oder Ausgleichen von Zahlungen nach automatischer Anwendung</span><span class="sxs-lookup"><span data-stu-id="89d43-123">Review or Apply Payments After Automatic Application</span></span>](receivables-how-review-apply-payments-auto-application.md) |
| <span data-ttu-id="89d43-124">Lösen Sie Zahlungen auf, die nicht automatisch in die entsprechenden offenen Posten übernommen werden können.</span><span class="sxs-lookup"><span data-stu-id="89d43-124">Resolve payments that cannot be applied automatically to their related open ledger entries.</span></span> <span data-ttu-id="89d43-125">Beispielsweise weil die Beträge abweichen oder weil ein verwandter Posten vorhanden.</span><span class="sxs-lookup"><span data-stu-id="89d43-125">For example because the amounts differ, or because a related ledger entry does not exist.</span></span> |[<span data-ttu-id="89d43-126">Abstimmen von Zahlungen, die nicht automatisch übernommen werden können</span><span class="sxs-lookup"><span data-stu-id="89d43-126">Reconcile Payments That Cannot be Applied Automatically</span></span>](receivables-how-reconcile-payments-cannot-apply-auto.md) |
| <span data-ttu-id="89d43-127">Verknüpfen Sie Text auf Zahlungen mit bestimmten Debitoren-, Kreditoren- oder Sachkonten, um solche wiederkehrenden Zahlungseingänge oder Ausgaben immer auf diesen Konten als Zahlungen ohne zugehörige Belege zu buchen, wenn keine entsprechenden Belege vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="89d43-127">Link text on payments to specific customer, vendor, or general ledger accounts to always post recurring cash receipts or expenses to those accounts when no documents exist to apply to.</span></span> |[<span data-ttu-id="89d43-128">Zuordnen von Text auf sich wiederholenden Zahlungen an Konten für automatische Abstimmung</span><span class="sxs-lookup"><span data-stu-id="89d43-128">Map Text on Recurring Payments to Accounts for Automatic Reconciliation</span></span>](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md) |

## <a name="see-also"></a><span data-ttu-id="89d43-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89d43-129">See Also</span></span>
[<span data-ttu-id="89d43-130">Verwalten von Forderungen</span><span class="sxs-lookup"><span data-stu-id="89d43-130">Managing Receivables</span></span>](receivables-manage-receivables.md)  
[<span data-ttu-id="89d43-131">Verkauf</span><span class="sxs-lookup"><span data-stu-id="89d43-131">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="89d43-132">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="89d43-132">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

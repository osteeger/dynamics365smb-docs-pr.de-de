---
title: 'Gewusst wie: Zusammenfassende Meldung'
description: "Mit der zusammenfassenden Meldung können Sie Informationen zu Verkaufstransaktionen mit anderen Ländern oder Regionen innerhalb der Europäischen Union (EU) an das System der Zoll- und Steuerbehördenlisten übermitteln."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/02/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 56cd8aa034935ca37bd91bdbec76b4f7b7a4c1c8
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="declare-vat-vies-tax"></a><span data-ttu-id="1e8ec-103">MwSt-VIES-Steuer angeben</span><span class="sxs-lookup"><span data-stu-id="1e8ec-103">Declare VAT-VIES Tax</span></span>
[!INCLUDE[d365fin](../../includes/d365fin_md.md)]<span data-ttu-id="1e8ec-104"> enthält die zusammenfassende Meldung, mit der Sie Informationen zu Verkaufstransaktionen mit anderen Ländern oder Regionen innerhalb der Europäischen Union (EU) an das System der Zoll- und Steuerbehördenlisten übermitteln können.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-104"> includes the VAT-VIES declaration report, which you can use to submit information about sales transactions with other European Union (EU) countries/regions to the customs and tax authorities' list system.</span></span> <span data-ttu-id="1e8ec-105">Im Bericht werden Informationen in dem Format angezeigt, das auch in der Erklärungsliste der Zoll- und Steuerbehörden verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-105">The report displays information in the same format that is used in the customs and tax authorities' declaration list.</span></span>  

<span data-ttu-id="1e8ec-106">Abhängig vom Volumen der verkauften Waren oder Dienstleistungen an andere EU-Länder/Regionen, müssen Sie monatliche, zweimonatliche oder vierteljährliche Meldungen senden.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-106">Depending on the volume of sales of goods or services to other EU countries/regions, you must submit monthly, bi-monthly, or quarterly declarations.</span></span> <span data-ttu-id="1e8ec-107">Hat das Unternehmen Verkäufe von mehr als 100.000 Euro pro Quartal, müssen Sie eine monatliche Meldung senden.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-107">If your company has sales of more than 100,000 euros per quarter, you must submit a monthly declaration.</span></span> <span data-ttu-id="1e8ec-108">Hat das Unternehmen Verkäufe von weniger als 100.000 Euro pro Quartal, müssen Sie eine monatliche Meldung senden.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-108">If your company has sales of less than 100,000 euros per quarter, you must submit a quarterly declaration.</span></span> <span data-ttu-id="1e8ec-109">Weitere Informationen finden Sie unter  [BZSt-Website](http://go.microsoft.com/fwlink/?LinkId=204368).</span><span class="sxs-lookup"><span data-stu-id="1e8ec-109">For more information, see the [BZSt website](http://go.microsoft.com/fwlink/?LinkId=204368).</span></span>  

<span data-ttu-id="1e8ec-110">Der Bericht basiert auf Daten in der Tabelle "MwSt.-Posten".</span><span class="sxs-lookup"><span data-stu-id="1e8ec-110">The report is based on the VAT Entry table.</span></span>  

## <a name="to-declare-vat-vies-tax"></a><span data-ttu-id="1e8ec-111">So erstellen Sie eine zusammenfassende Meldung</span><span class="sxs-lookup"><span data-stu-id="1e8ec-111">To declare VAT-VIES tax</span></span>  

1.  <span data-ttu-id="1e8ec-112">Wählen Sie ![Nach Seite oder Bericht suchen](../../media/ui-search/search_small.png "Symbol nach Seite oder Bericht suchen") und geben **Zusammenf. Meldung - Formular** ein und wählen dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-112">Choose the ![Search for Page or Report](../../media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **VAT-Vies Declaration Tax – DE**, and then choose the related link.</span></span>  
2.  <span data-ttu-id="1e8ec-113">Füllen Sie im Fenster **Zusammenf. Meldung MwSt-Vies-Formular** im Inforegister **Optionen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-113">In the **VAT-Vies Declaration Tax – DE** window, on the **Options** FastTab, fill in the fields as described in the following table.</span></span>  

    |<span data-ttu-id="1e8ec-114">Feld</span><span class="sxs-lookup"><span data-stu-id="1e8ec-114">Field</span></span>|<span data-ttu-id="1e8ec-115">Description</span><span class="sxs-lookup"><span data-stu-id="1e8ec-115">Description</span></span>|  
    |---------------------------------|---------------------------------------|  
    |<span data-ttu-id="1e8ec-116">**Meldezeitraum**</span><span class="sxs-lookup"><span data-stu-id="1e8ec-116">**Reporting Period**</span></span>|<span data-ttu-id="1e8ec-117">Geben Sie den Zeitraum an, den der Bericht umfasst.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-117">Select the time period that the report applies to.</span></span> <span data-ttu-id="1e8ec-118">Dies kann ein Monat, eine zweimonatige Periode, ein Quartal oder das Kalenderjahr sein.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-118">This can be a month, a two-month period, a quarter, or the calendar year.</span></span>|  
    |<span data-ttu-id="1e8ec-119">**Datum der Unterschrift**</span><span class="sxs-lookup"><span data-stu-id="1e8ec-119">**Date of Signature**</span></span>|<span data-ttu-id="1e8ec-120">Dient zum Eingeben des Datums, an dem die MwSt-VIES-Erklärung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-120">Enter the date on which the VAT-VIES declaration is sent.</span></span>|  
    |<span data-ttu-id="1e8ec-121">**Berichtigte Anmeldung**</span><span class="sxs-lookup"><span data-stu-id="1e8ec-121">**Corrected Notification**</span></span>|<span data-ttu-id="1e8ec-122">Ein Häkchen im Kontrollkästchen bedeutet, dass es sich um eine korrigierte Fassung einer bereits abgegebenen zusammenfassenden MwSt-VIES-Erklärung handelt.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-122">If selected, this field indicates that this is a corrected version of an already delivered VAT-VIES declaration.</span></span>|  
    |<span data-ttu-id="1e8ec-123">**Beträge in Berichtswährung ausgeben**</span><span class="sxs-lookup"><span data-stu-id="1e8ec-123">**Show Amounts in Add. Reporting Currency**</span></span>|<span data-ttu-id="1e8ec-124">Gibt an, ob die ausgewerteten Beträge in der zusätzlichen Berichtswährung angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-124">If selected, the amounts of the report will be in the additional reporting currency.</span></span> <span data-ttu-id="1e8ec-125">Weitere Informationen finden Sie unter zusätzliche Berichtswährung.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-125">For more information, see Additional Reporting Currency.</span></span>|  
    |<span data-ttu-id="1e8ec-126">**Auf monatliche Meldung umstellen**</span><span class="sxs-lookup"><span data-stu-id="1e8ec-126">**Change to monthly reporting**</span></span>|<span data-ttu-id="1e8ec-127">Wenn es ausgewählt wird, hat Ihr Unternehmen Verkäufe von mehr als 100.000 Euro pro Quartal und Sie müssen von einem Quartalsbericht zu einem monatlichen Bericht migrieren.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-127">If selected, your company has sales of more than 100,000 euros per quarter and you must migrate from a quarterly report to a monthly report.</span></span> <span data-ttu-id="1e8ec-128">**Wichtig:** Wählen sie nur dieses Feld aus, wenn Sie zum ersten Mal einen monatlichen Bericht senden.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-128">**Important:**  Only select this field the first time that you submit a monthly report.</span></span>|  
    |<span data-ttu-id="1e8ec-129">**Monatliche Meldung widerrufen**</span><span class="sxs-lookup"><span data-stu-id="1e8ec-129">**Revoke monthly reporting**</span></span>|<span data-ttu-id="1e8ec-130">Wird dieses Kontrollkästchen aktiviert, wollen Sie vom monatlichen Bericht zu einem anderen Meldezeitraum wechseln.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-130">If selected, you want to switch from monthly reporting to another reporting period.</span></span><br /><br /> <span data-ttu-id="1e8ec-131">Wenn Sie beispielsweise zuvor monatliche Erklärungen eingereicht haben, aber die EU-Umsätze weniger als 100.000 Euro pro Quartal betragen, wählen Sie das Feld und wählen Sie anschließend eines der Quartale im **Meldezeitraum** aus.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-131">For example, if you have previously submitted monthly declarations but the EU sales are less than 100,000 euros per quarter, select this field and then select one of the quarters in the **Reporting Period** field.</span></span>|  

3.  <span data-ttu-id="1e8ec-132">Wählen Sie im Inforegister **MwSt.-Abrechnungszeile** die entsprechenden Filter aus.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-132">On the **VAT Entry** FastTab, select the appropriate filters.</span></span>  

    > [!NOTE]  
    >  <span data-ttu-id="1e8ec-133">Um diesen Bericht ausführen, müssen Sie das **Buchungsdatum** als Filter auswählen und den Wert des Buchungsdatums eingegeben.</span><span class="sxs-lookup"><span data-stu-id="1e8ec-133">In order to run this report, you must select the **Posting Date** as a filter, and enter the posting date value.</span></span>  

## <a name="see-also"></a><span data-ttu-id="1e8ec-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e8ec-134">See Also</span></span>  
[<span data-ttu-id="1e8ec-135">MwSt.-Abrechnung</span><span class="sxs-lookup"><span data-stu-id="1e8ec-135">VAT Reporting</span></span>](vat-reporting.md)

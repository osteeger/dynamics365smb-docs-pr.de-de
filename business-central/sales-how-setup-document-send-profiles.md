---
title: "Bevorzugte Methoden der Übermittlung von Verkaufsbelegen einrichten | Microsoft Docs"
description: "Beschreibt, wie Sie die gewünschte Methode jedes Debitors der Übermittlung von Verkaufsbelegen eingerichtet, z Buchen, PDF-Dateien, elektronischer Beleg, usw."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: email, PDF, electronic document
ms.date: 03/29/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 9c73a6ed721cd8deda48cd2fa8a3470733b9f672
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="set-up-document-sending-profiles"></a><span data-ttu-id="f5ef4-103">Belegsendeprofile einrichten</span><span class="sxs-lookup"><span data-stu-id="f5ef4-103">Set Up Document Sending Profiles</span></span>
<span data-ttu-id="f5ef4-104">Sie können jeden Debitor mit einer bevorzugten Methode der Übermittlung von Verkaufsbelegen einrichten, sodass Sie nicht jedes Mal eine Sendeoptionen auswählen müssen, wenn Sie die Schaltfläche **Buchen und senden** auswählen.</span><span class="sxs-lookup"><span data-stu-id="f5ef4-104">You can set each customer up with a preferred method of sending sales documents, so that you do not have to select a sending option every time you choose the **Post and Send** action.</span></span>

<span data-ttu-id="f5ef4-105">Im Fenster **Belegsendeprofile** richten Sie verschiedene **Dokumente-Sendeprofile** ein, die Sie aus dem Feld von einer Debitorenkarte auswählen können.</span><span class="sxs-lookup"><span data-stu-id="f5ef4-105">In the **Document Sending Profiles** window, you set up different sending profiles that you can select from in the **Document Sending Profile** field on a customer card.</span></span> <span data-ttu-id="f5ef4-106">Im Kontrollkästchen **Standard** geben Sie an, dass das Belegsendprofil das Standardprofil für alle Debitoren gilt, außer Debitoren, bei denen das Feld **Dokument-Sendeprofil** mit einem anderen Sendeprofil ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="f5ef4-106">You can select the **Default** check box to specify that the document sending profile is the default profile for all customers, except for customers where the **Document Sending Profile** field is filled with another sending profile.</span></span>

<span data-ttu-id="f5ef4-107">Wenn Sie die Schaltfläche **Buchen und senden** für einen Verkaufsbeleg auswählen, wird im Dialogfeld **Buchungs- und Sendebestätigung** das verwendete Sendeprofil angezeigt. Dabei handelt es sich entweder um das für den Debitor eingerichtete oder um Standardprofil für alle Debitoren.</span><span class="sxs-lookup"><span data-stu-id="f5ef4-107">When you choose the **Post and Send** action on a sales document, the **Post and Send Confirmation** dialog box shows the sending profile used, either the one set up for the customer or the default for all customers.</span></span> <span data-ttu-id="f5ef4-108">In diesem Dialogfeld können Sie das Sendeprofil für den Verkaufsbeleg ändern.</span><span class="sxs-lookup"><span data-stu-id="f5ef4-108">In the dialog box, you can change the sending profile for the sales document.</span></span> <span data-ttu-id="f5ef4-109">Weitere Informationen finden Sie unter [Verkaufsrechnungen](sales-how-invoice-sales.md).</span><span class="sxs-lookup"><span data-stu-id="f5ef4-109">For more information, see [Invoice Sales](sales-how-invoice-sales.md).</span></span>

## <a name="to-set-up-a-document-sending-profile"></a><span data-ttu-id="f5ef4-110">Einrichten von Belegsendeprofilen</span><span class="sxs-lookup"><span data-stu-id="f5ef4-110">To set up a document sending profile</span></span>
1. <span data-ttu-id="f5ef4-111">Wählen Sie das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Dokumentsendeprofil** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="f5ef4-111">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Document Sending Profiles**, and then choose the related link.</span></span>
2. <span data-ttu-id="f5ef4-112">Im Feld **Dokumentsendeprofile** wählen Sie die Aktion **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="f5ef4-112">In the **Document Sending Profiles** window, choose the **New** action.</span></span>
3. <span data-ttu-id="f5ef4-113">Füllen Sie die Felder je nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="f5ef4-113">Fill in the fields as necessary.</span></span> [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-specify-a-sending-profile-on-a-customer-card"></a><span data-ttu-id="f5ef4-114">Sendeprofil für eine Debitorenkarte festlegen</span><span class="sxs-lookup"><span data-stu-id="f5ef4-114">To specify a sending profile on a customer card</span></span>
1. <span data-ttu-id="f5ef4-115">Wählen Sie in der rechten oberen Ecke das Symbol ![Nach Seite oder Bericht suchen](media/ui-search/search_small.png "Nach Seite oder Bericht suchen") und geben **Kunden** ein. Wählen Sie dann den zugehörigen Link aus.</span><span class="sxs-lookup"><span data-stu-id="f5ef4-115">Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers**, and then choose the related link.</span></span>
2. <span data-ttu-id="f5ef4-116">Öffnen Sie die Karte des Debitors, für den ein Sendeprofil eingerichtet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5ef4-116">Open the card of the customer who you want to set up a sending profile for.</span></span>
3. <span data-ttu-id="f5ef4-117">Wählen Sie im Inforegister **Belegsendeprofil** ein Profil aus, das sie eingerichtet haben wie im vorigen Verfahren beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f5ef4-117">In the **Document Sending Profile** field, select a profile that you have set up as described in the previous procedure.</span></span>

## <a name="see-also"></a><span data-ttu-id="f5ef4-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5ef4-118">See Also</span></span>
[<span data-ttu-id="f5ef4-119">Einrichten von Verkäufen</span><span class="sxs-lookup"><span data-stu-id="f5ef4-119">Setting Up Sales</span></span>](sales-setup-sales.md)  
[<span data-ttu-id="f5ef4-120">Verkauf</span><span class="sxs-lookup"><span data-stu-id="f5ef4-120">Sales</span></span>](sales-manage-sales.md)  
<span data-ttu-id="f5ef4-121">[Arbeiten mit [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span><span class="sxs-lookup"><span data-stu-id="f5ef4-121">[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)</span></span>

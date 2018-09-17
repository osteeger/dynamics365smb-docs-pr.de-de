---
title: "Überwachen von Segmenten und zugehörigen Aktivitäten| Microsoft Docs"
description: "Erhalten von Informationen zum Erstellen von Segmenten, um Kontaktgruppen zu definieren und Festlegen von Aktivitäten für Segmente."
services: project-madeira
documentationcenter: 
author: jswymer
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: relationship, prospect
ms.date: 06/06/2017
ms.author: jswymer
ms.translationtype: HT
ms.sourcegitcommit: e3917573a912a4e51416c4e926443c87513728fe
ms.openlocfilehash: 1962bd9d74f7b4d9600de11f85d1e312f6fb8c09
ms.contentlocale: de-de
ms.lasthandoff: 06/01/2018

---
# <a name="managing-interactions-for-segments"></a><span data-ttu-id="2f949-103">Verwalten von Aktivitäten für Segmente</span><span class="sxs-lookup"><span data-stu-id="2f949-103">Managing Interactions for Segments</span></span>
<span data-ttu-id="2f949-104">Das Fenster **Segment** ist ein Arbeitsschein, in dem Sie folgende Aufgaben ausführen können:</span><span class="sxs-lookup"><span data-stu-id="2f949-104">The **Segment** window is a type of worksheet where you can:</span></span>

* <span data-ttu-id="2f949-105">Segmente erstellen</span><span class="sxs-lookup"><span data-stu-id="2f949-105">Create segments.</span></span>
* <span data-ttu-id="2f949-106">Speichern Sie die Segmentierungskriterien, die Sie bei der Auswahl von Kontakten verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="2f949-106">Save the segmentation criteria you have used to select contacts.</span></span>
* <span data-ttu-id="2f949-107">Protokolliert das Segment und zeichnet Aktivitäten auf, die Sie mit Kontakten in dem Segment durchführen.</span><span class="sxs-lookup"><span data-stu-id="2f949-107">Log the segment and record interactions involving the contacts within the segment.</span></span>

## <a name="segmenting"></a><span data-ttu-id="2f949-108">Segmentieren</span><span class="sxs-lookup"><span data-stu-id="2f949-108">Segmenting</span></span>
<span data-ttu-id="2f949-109">Es gibt verschiedene Arten, Segmente zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="2f949-109">There are several ways to create segments:</span></span>

* <span data-ttu-id="2f949-110">Sie können Kontakte manuell in die Segmentszeilen eingeben.</span><span class="sxs-lookup"><span data-stu-id="2f949-110">You can manually enter the contacts you want to include in the segment in the segment lines.</span></span>
* <span data-ttu-id="2f949-111">Sie können Kontakte auswählen.</span><span class="sxs-lookup"><span data-stu-id="2f949-111">You can select contacts.</span></span>
* <span data-ttu-id="2f949-112">Sie können ein protokolliertes Segment wiederverwenden, um ein neues zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="2f949-112">You can reuse a logged segment as the basis to create a new one.</span></span>
* <span data-ttu-id="2f949-113">Sie können gespeicherte Segmentierungskriterien wiederverwenden.</span><span class="sxs-lookup"><span data-stu-id="2f949-113">You can reuse saved segmentation criteria.</span></span>

## <a name="interactions"></a><span data-ttu-id="2f949-114">Aktivitäten</span><span class="sxs-lookup"><span data-stu-id="2f949-114">Interactions</span></span>
<span data-ttu-id="2f949-115">In dem Fenster **Segment** können Sie Aktivitäten für mehrere Kontakte gleichzeitig erstellen.</span><span class="sxs-lookup"><span data-stu-id="2f949-115">In the **Segment** window, you can create interactions for several contacts simultaneously.</span></span> <span data-ttu-id="2f949-116">Sie können z. B. ein Segment mit einem Microsoft Word Dokument verbinden, sodass Sie einen Brief an alle Kontakte in dem Segment verschicken können.</span><span class="sxs-lookup"><span data-stu-id="2f949-116">For example, you can merge a segment with a Microsoft Word document, so that you can send a letter to all the contacts in the segment.</span></span>

<span data-ttu-id="2f949-117">Sie können Informationen über die Aktivität für das Segment im **Segmentkopf** festlegen.</span><span class="sxs-lookup"><span data-stu-id="2f949-117">You can specify information about the interaction for the segment on the **Segment** header.</span></span> <span data-ttu-id="2f949-118">Sie können z. B. entscheiden, welche Aktivitätenvorlage Sie für alle Kontakte verwenden möchten, Sie eine Beschreibung oder eine Korrespondenzart festlegen usw.</span><span class="sxs-lookup"><span data-stu-id="2f949-118">For example, you can decide which interaction template you want to use for all the contacts, specify a description, a correspondence type, and so on.</span></span> <span data-ttu-id="2f949-119">Sie können diese Informationen in der Segmentszeile für jeden einzelnen Kontakt verändern, z. B., indem Sie eine andere Beschreibung eingeben.</span><span class="sxs-lookup"><span data-stu-id="2f949-119">However, you can modify this information in the segment line for each particular contact, for example, by specifying another description for one contact.</span></span> <span data-ttu-id="2f949-120">Wenn Sie ein Segment mit einem Dokument in Microsoft Word verknüpfen, können Sie das Dokument für einen oder mehrere Kontakte des Segments personalisieren, indem Sie dem Dokument z. B. individuelle Kommentare hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="2f949-120">If you are merging a segment with a Microsoft Word document, you can personalize the document to be sent for one or several of the contacts within the segment, for example, by adding individualized comments to the document.</span></span>

## <a name="logging"></a><span data-ttu-id="2f949-121">Protokollieren</span><span class="sxs-lookup"><span data-stu-id="2f949-121">Logging</span></span>
<span data-ttu-id="2f949-122">Wenn Sie in dem Fenster **Segment** **Protokoll** wählen, werden alle Aktivitäten im Fenster **Aktivitätenprotokollposten** gespeichert und das Segment wird protokolliert.</span><span class="sxs-lookup"><span data-stu-id="2f949-122">In the **Segment** window, when you choose **Log**, the application records the interactions in the **Interaction Log Entry** window, and logs the segment.</span></span> <span data-ttu-id="2f949-123">Nachdem Sie das Segment protokolliert haben, finden Sie es nur in dem Fenster **Protokollierte Segmente**.</span><span class="sxs-lookup"><span data-stu-id="2f949-123">After you have logged the segment, you can only find it in the **Logged Segments** window.</span></span>

<span data-ttu-id="2f949-124">Im Fenster **Protokollierte Segmente** können Sie ein Anschluss-Segment mit den gleichen Kontakten wie das protokollierte Segment erstellen.</span><span class="sxs-lookup"><span data-stu-id="2f949-124">In the **Logged Segments** window, you can decide to create a follow-up segment containing the same contacts as the segment you have logged.</span></span>

## <a name="see-also"></a><span data-ttu-id="2f949-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2f949-125">See Also</span></span>
[<span data-ttu-id="2f949-126">Segmente erstellen</span><span class="sxs-lookup"><span data-stu-id="2f949-126">Create Segments</span></span>](marketing-how-create-segment.md)  
[<span data-ttu-id="2f949-127">Aktivitäten für Segmente erstellen</span><span class="sxs-lookup"><span data-stu-id="2f949-127">Create Interactions for Segments</span></span>](marketing-how-create-interactions.md)  
[<span data-ttu-id="2f949-128">Verwalten von Segmenten</span><span class="sxs-lookup"><span data-stu-id="2f949-128">Managing Segments</span></span>](marketing-segments.md)  
[<span data-ttu-id="2f949-129">Aufzeichnen von Aktivitäten mit Kontakten</span><span class="sxs-lookup"><span data-stu-id="2f949-129">Recording Interactions With Contacts</span></span>](marketing-interactions.md)  
[<span data-ttu-id="2f949-130">Verkaufschancen verwalten</span><span class="sxs-lookup"><span data-stu-id="2f949-130">Managing Sales Opportunities</span></span>](marketing-manage-sales-opportunities.md)  
[<span data-ttu-id="2f949-131">Erstellen und Verwalten von Kontakten</span><span class="sxs-lookup"><span data-stu-id="2f949-131">Creating and Managing Contacts</span></span>](marketing-contacts.md)  
[<span data-ttu-id="2f949-132">Arbeiten mit  Business Central</span><span class="sxs-lookup"><span data-stu-id="2f949-132">Working with Business Central</span></span>](ui-work-product.md)

---
title: "Feldzuordnung für den Export von Bankzahlungsdateien | Microsoft Docs"
description: "Wenn Sie Zahlungsdateien exportieren, indem Sie die Bankdaten-Konvertierungsdienst-Funktion verwenden, werden die Daten, die Sie exportieren, dem Anbieter des Bankdaten-Konvertierungsdienstes zur Verfügung gestellt."
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 08/18/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: bec0619be0a65e3625759e13d2866ac615d7513c
ms.openlocfilehash: aa3569037e79f79b0a644511361901d0844e58a3
ms.contentlocale: de-de
ms.lasthandoff: 03/22/2018

---
# <a name="field-mapping-when-exporting-payment-files-using-bank-data-conversion-service"></a><span data-ttu-id="e059a-103">Feld-Zuordnung beim Exportieren von Zahlungsdateien unter Verwendung von Bankdaten-Konvertierungsdienst</span><span class="sxs-lookup"><span data-stu-id="e059a-103">Field Mapping When Exporting Payment Files Using Bank Data Conversion Service</span></span>
<span data-ttu-id="e059a-104">Wenn Sie Zahlungsdateien exportieren, indem Sie die Bankdaten-Konvertierungsdienst-Funktion verwenden, werden die Daten, die Sie exportieren, dem Anbieter des Bankdaten-Konvertierungsdienstes zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="e059a-104">When you export payment files using the Bank Data Conversion Service feature, the data that you export is exposed to the provider of the bank data conversion service.</span></span> <span data-ttu-id="e059a-105">Der Dienstanbieter ist für den Schutz dieser Daten verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="e059a-105">The service provider is responsible for the privacy of this data.</span></span> <span data-ttu-id="e059a-106">Weitere Informationen darüber, wie die Bankdaten-Konvertierungsdienst-Funktion arbeitet, finden Sie unter [Datenaustausch-Framework](across-about-the-data-exchange-framework.md).</span><span class="sxs-lookup"><span data-stu-id="e059a-106">For more information about how the Bank Data Conversion Service feature works, see [About the Data Exchange Framework](across-about-the-data-exchange-framework.md).</span></span>  

> [!CAUTION]  
>  <span data-ttu-id="e059a-107">Wenn Sie Zahlungsdateien exportieren, indem Sie die Bankdaten-Konvertierungsdienst-Funktion verwenden, werden einige Ihrer Daten dem Anbieter des Services zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="e059a-107">When you export payment files by using the Bank Data Conversion Service feature, some of your business data will be exposed to the provider of the service.</span></span> <span data-ttu-id="e059a-108">Der Dienstanbieter, AMC Consult A/S, ist für den Schutz dieser Daten verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="e059a-108">The service provider, AMC Consult A/S, is responsible for the privacy of this data.</span></span> <span data-ttu-id="e059a-109">Weitere Informationen finden Sie unter [AMC-Datenschutzrichtlinie.](http://go.microsoft.com/fwlink/?LinkId=510158)</span><span class="sxs-lookup"><span data-stu-id="e059a-109">For more information, see [AMC Privacy Policy](http://go.microsoft.com/fwlink/?LinkId=510158).</span></span>  

<span data-ttu-id="e059a-110">In der folgenden Tabelle sind die Felder in [!INCLUDE[d365fin](includes/d365fin_md.md)] ausgefüllt, aus denen Daten zu dem Dienstanbieter exportiert werden können.</span><span class="sxs-lookup"><span data-stu-id="e059a-110">The following table lists the fields in [!INCLUDE[d365fin](includes/d365fin_md.md)] from which data can be exported to the service provider.</span></span>  

|<span data-ttu-id="e059a-111">Zugeordnetes Feld</span><span class="sxs-lookup"><span data-stu-id="e059a-111">Mapped Field</span></span>|<span data-ttu-id="e059a-112">Feld in Tabelle</span><span class="sxs-lookup"><span data-stu-id="e059a-112">Field in Table</span></span>|<span data-ttu-id="e059a-113">Tisch</span><span class="sxs-lookup"><span data-stu-id="e059a-113">Table</span></span>|<span data-ttu-id="e059a-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e059a-114">Description</span></span>|  
|------------------|--------------------|-----------|---------------------------------------|  
|<span data-ttu-id="e059a-115">Gläubiger-Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e059a-115">Creditor No.</span></span>|<span data-ttu-id="e059a-116">Gläubiger-Identifikationsnummer</span><span class="sxs-lookup"><span data-stu-id="e059a-116">Creditor No.</span></span>|<span data-ttu-id="e059a-117">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-117">Bank Account</span></span>|<span data-ttu-id="e059a-118">Die Identifikationsnummer, die Ihrem Unternehmen von Ihrer Bank zugeordnet wurde, um Zahlungen zu erfassen</span><span class="sxs-lookup"><span data-stu-id="e059a-118">The identifier assigned to your company by your bank to collect payments</span></span>|  
|<span data-ttu-id="e059a-119">Bankkontonr. des Absenders</span><span class="sxs-lookup"><span data-stu-id="e059a-119">Sender Bank Account No.</span></span>|<span data-ttu-id="e059a-120">Bankkontonummer/IBAN</span><span class="sxs-lookup"><span data-stu-id="e059a-120">Bank Account No./IBAN</span></span>|<span data-ttu-id="e059a-121">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-121">Bank Account</span></span>|<span data-ttu-id="e059a-122">Die Bankkontonummer (IBAN oder sonstige) Ihres Unternehmens, die auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-122">Your company's bank account number (IBAN or other) that is specified on the bank account card</span></span>|  
|<span data-ttu-id="e059a-123">Absenderbank-Clearing-Standard</span><span class="sxs-lookup"><span data-stu-id="e059a-123">Sender Bank Clearing Standard</span></span>|<span data-ttu-id="e059a-124">Bank-Clearing-Standard</span><span class="sxs-lookup"><span data-stu-id="e059a-124">Bank Clearing Standard</span></span>|<span data-ttu-id="e059a-125">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-125">Bank Account</span></span>|<span data-ttu-id="e059a-126">Das Nationale Register der Banknamen für das Bankkonto des Absenders</span><span class="sxs-lookup"><span data-stu-id="e059a-126">The national bank names register used for the sender bank account</span></span>|  
|<span data-ttu-id="e059a-127">Clearing-Code Absenderbank</span><span class="sxs-lookup"><span data-stu-id="e059a-127">Sender Bank Clearing Code</span></span>|<span data-ttu-id="e059a-128">Bank-Clearing-Code</span><span class="sxs-lookup"><span data-stu-id="e059a-128">Bank Clearing Code</span></span>|<span data-ttu-id="e059a-129">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-129">Bank Account</span></span>|<span data-ttu-id="e059a-130">Die Identifikationsnummer Bank des Absenders in Bezug auf das Bankadressenregister, das verwendet wird</span><span class="sxs-lookup"><span data-stu-id="e059a-130">The identifier of the sender's bank in relation to the bank names register used</span></span>|  
|<span data-ttu-id="e059a-131">BIC Absenderbank</span><span class="sxs-lookup"><span data-stu-id="e059a-131">Sender Bank BIC</span></span>|<span data-ttu-id="e059a-132">SWIFT-Code</span><span class="sxs-lookup"><span data-stu-id="e059a-132">SWIFT Code</span></span>|<span data-ttu-id="e059a-133">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-133">Bank Account</span></span>|<span data-ttu-id="e059a-134">Die SWIFT-Kennung des Absenderbankkontos.</span><span class="sxs-lookup"><span data-stu-id="e059a-134">The SWIFT identifier of the sender bank account</span></span>|  
|<span data-ttu-id="e059a-135">Kontowährung der Absenderbank</span><span class="sxs-lookup"><span data-stu-id="e059a-135">Sender Bank Account Currency</span></span>|<span data-ttu-id="e059a-136">Währungscode</span><span class="sxs-lookup"><span data-stu-id="e059a-136">Currency Code</span></span>|<span data-ttu-id="e059a-137">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-137">Bank Account</span></span>|<span data-ttu-id="e059a-138">Der Währungscode der Absenderbank</span><span class="sxs-lookup"><span data-stu-id="e059a-138">The sender bank account Currency Code</span></span>|  
|<span data-ttu-id="e059a-139">Belegnr.</span><span class="sxs-lookup"><span data-stu-id="e059a-139">Document No.</span></span>|<span data-ttu-id="e059a-140">Belegnr.</span><span class="sxs-lookup"><span data-stu-id="e059a-140">Document No.</span></span>|<span data-ttu-id="e059a-141">Fibu Buch.-Blattzeile</span><span class="sxs-lookup"><span data-stu-id="e059a-141">General Journal Line</span></span>|<span data-ttu-id="e059a-142">Die Belegnummer der Zahlungszeile</span><span class="sxs-lookup"><span data-stu-id="e059a-142">The document number of the payment line</span></span>|  
|<span data-ttu-id="e059a-143">Ausgleich ext. Belegnr.</span><span class="sxs-lookup"><span data-stu-id="e059a-143">Applies-to Ext. Doc. No.</span></span>|<span data-ttu-id="e059a-144">Ausgleich ext. Belegnr.</span><span class="sxs-lookup"><span data-stu-id="e059a-144">Applies-to Ext. Doc. No.</span></span>|<span data-ttu-id="e059a-145">Fibu Buch.-Blattzeile</span><span class="sxs-lookup"><span data-stu-id="e059a-145">General Journal Line</span></span>|<span data-ttu-id="e059a-146">Die Nummer des externen Belegs, der Rechnung oder Gutschrift, mit der die Zahlungszeile ausgeglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e059a-146">The external document number of the invoice or credit memo that the payment line is applied to</span></span>|  
|<span data-ttu-id="e059a-147">Empfänger-ID</span><span class="sxs-lookup"><span data-stu-id="e059a-147">Recipient ID</span></span>|<span data-ttu-id="e059a-148">Kontonummer</span><span class="sxs-lookup"><span data-stu-id="e059a-148">Account No.</span></span>|<span data-ttu-id="e059a-149">Fibu Buch.-Blattzeile</span><span class="sxs-lookup"><span data-stu-id="e059a-149">General Journal Line</span></span>|<span data-ttu-id="e059a-150">Die Nummer des Debitors oder Kreditors, die auf der Zahlungszeile angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-150">The customer or vendor number that is specified on the payment line</span></span>|  
|<span data-ttu-id="e059a-151">Zahlungsart</span><span class="sxs-lookup"><span data-stu-id="e059a-151">Payment Type</span></span>|<span data-ttu-id="e059a-152">Zahlungstyp Bankdatenkonvertierung</span><span class="sxs-lookup"><span data-stu-id="e059a-152">Bank Data Conversion Pmt. Type</span></span>|<span data-ttu-id="e059a-153">Zahlungsform</span><span class="sxs-lookup"><span data-stu-id="e059a-153">Payment Method</span></span>|<span data-ttu-id="e059a-154">Die Art des Banktransfers, wie Inland oder International</span><span class="sxs-lookup"><span data-stu-id="e059a-154">The type of bank transfer, such as domestic or international</span></span>|  
|<span data-ttu-id="e059a-155">Zahlungsreferenz</span><span class="sxs-lookup"><span data-stu-id="e059a-155">Payment Reference</span></span>|<span data-ttu-id="e059a-156">Zahlungsreferenz</span><span class="sxs-lookup"><span data-stu-id="e059a-156">Payment Reference</span></span>|<span data-ttu-id="e059a-157">Fibu Buch.-Blattzeile</span><span class="sxs-lookup"><span data-stu-id="e059a-157">General Journal Line</span></span>|<span data-ttu-id="e059a-158">Die Zahlungsreferenz der Zahlungszeile</span><span class="sxs-lookup"><span data-stu-id="e059a-158">The payment reference of the payment line</span></span>|  
|<span data-ttu-id="e059a-159">Adresse des Empfängers</span><span class="sxs-lookup"><span data-stu-id="e059a-159">Recipient Address</span></span>|<span data-ttu-id="e059a-160">Adresse</span><span class="sxs-lookup"><span data-stu-id="e059a-160">Address</span></span>|<span data-ttu-id="e059a-161">Debitor/Kreditor</span><span class="sxs-lookup"><span data-stu-id="e059a-161">Customer/Vendor</span></span>|<span data-ttu-id="e059a-162">Die Empfängeradresse, die auf der Debitoren- oder Kreditorenkarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-162">The recipient address that is specified on the customer or vendor card</span></span>|  
|<span data-ttu-id="e059a-163">Ort des Empfängers</span><span class="sxs-lookup"><span data-stu-id="e059a-163">Recipient City</span></span>|<span data-ttu-id="e059a-164">Ort</span><span class="sxs-lookup"><span data-stu-id="e059a-164">City</span></span>|<span data-ttu-id="e059a-165">Debitor/Kreditor</span><span class="sxs-lookup"><span data-stu-id="e059a-165">Customer/Vendor</span></span>|<span data-ttu-id="e059a-166">Die Stadt, die auf der Debitoren- oder Kreditorenkarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-166">The recipient city that is specified on the customer or vendor card</span></span>|  
|<span data-ttu-id="e059a-167">Name des Empfängers</span><span class="sxs-lookup"><span data-stu-id="e059a-167">Recipient Name</span></span>|<span data-ttu-id="e059a-168">Name</span><span class="sxs-lookup"><span data-stu-id="e059a-168">Name</span></span>|<span data-ttu-id="e059a-169">Debitor/Kreditor</span><span class="sxs-lookup"><span data-stu-id="e059a-169">Customer/Vendor</span></span>|<span data-ttu-id="e059a-170">Die Empfängername, der auf der Debitoren- oder Kreditorenkarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-170">The recipient name that is specified on the customer or vendor card</span></span>|  
|<span data-ttu-id="e059a-171">Landes-/Regionscode Empfänger</span><span class="sxs-lookup"><span data-stu-id="e059a-171">Recipient Country/Region Code</span></span>|<span data-ttu-id="e059a-172">Länder-/Regionscode</span><span class="sxs-lookup"><span data-stu-id="e059a-172">Country/Region Code</span></span>|<span data-ttu-id="e059a-173">Debitor/Kreditor</span><span class="sxs-lookup"><span data-stu-id="e059a-173">Customer/Vendor</span></span>|<span data-ttu-id="e059a-174">Der Länder-/Regionencode des Bankkontos des Empfängers, der auf der Debitoren- oder auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-174">The recipient country/region code that is specified on the customer or vendor card</span></span>|  
|<span data-ttu-id="e059a-175">PLZ-Code Empfänger</span><span class="sxs-lookup"><span data-stu-id="e059a-175">Recipient Post Code</span></span>|<span data-ttu-id="e059a-176">PLZ-Code</span><span class="sxs-lookup"><span data-stu-id="e059a-176">Post Code</span></span>|<span data-ttu-id="e059a-177">Debitor/Kreditor</span><span class="sxs-lookup"><span data-stu-id="e059a-177">Customer/Vendor</span></span>|<span data-ttu-id="e059a-178">Die Postleitzahl des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-178">The recipient post code that is specified on the customer or vendor card</span></span>|  
|<span data-ttu-id="e059a-179">Bankkontonr. Empfänger</span><span class="sxs-lookup"><span data-stu-id="e059a-179">Recipient Bank Acc. No.</span></span>|<span data-ttu-id="e059a-180">Bankkontonummer/IBAN</span><span class="sxs-lookup"><span data-stu-id="e059a-180">Bank Account No./IBAN</span></span>|<span data-ttu-id="e059a-181">Debitorenbankkonto/Kreditorenbankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-181">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="e059a-182">Die Nummer (IBAN oder sonstige) des Bankkontos des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-182">The recipient bank account number (IBAN or other) that is specified on the customer or vendor bank account card</span></span>|  
|<span data-ttu-id="e059a-183">Clearing-Code Empfängerbank</span><span class="sxs-lookup"><span data-stu-id="e059a-183">Recipient Bank Clearing Code</span></span>|<span data-ttu-id="e059a-184">Bank-Clearing-Standard</span><span class="sxs-lookup"><span data-stu-id="e059a-184">Bank Clearing Standard</span></span>|<span data-ttu-id="e059a-185">Debitorenbankkonto/Kreditorenbankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-185">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="e059a-186">Das Nationale Register der Banknamen für das Bankkonto des Empfängers</span><span class="sxs-lookup"><span data-stu-id="e059a-186">The national bank names register used for the recipient bank account</span></span>|  
|<span data-ttu-id="e059a-187">Clearing-Standard Empfängerbank</span><span class="sxs-lookup"><span data-stu-id="e059a-187">Recipient Bank Clearing Std.</span></span>|<span data-ttu-id="e059a-188">Bank-Clearing-Code</span><span class="sxs-lookup"><span data-stu-id="e059a-188">Bank Clearing Code</span></span>|<span data-ttu-id="e059a-189">Debitorenbankkonto/Kreditorenbankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-189">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="e059a-190">Die Identifikationsnummer des Empfänger-Bankkontos in Bezug auf das Bankadressenregister, das verwendet wird</span><span class="sxs-lookup"><span data-stu-id="e059a-190">The identifier of the recipient bank account in relation to the bank names register that is used</span></span>|  
|<span data-ttu-id="e059a-191">E-Mail-Adresse Empfänger</span><span class="sxs-lookup"><span data-stu-id="e059a-191">Recipient Email Address</span></span>|<span data-ttu-id="e059a-192">E-Mail</span><span class="sxs-lookup"><span data-stu-id="e059a-192">E-Mail</span></span>|<span data-ttu-id="e059a-193">Debitor/Kreditor</span><span class="sxs-lookup"><span data-stu-id="e059a-193">Customer/Vendor</span></span>|<span data-ttu-id="e059a-194">Die E-Mail-Adresse des Empfängers.</span><span class="sxs-lookup"><span data-stu-id="e059a-194">The email address of the recipient</span></span>|  
|<span data-ttu-id="e059a-195">Nachricht an Empfänger 1</span><span class="sxs-lookup"><span data-stu-id="e059a-195">Message To Recipient 1</span></span>|<span data-ttu-id="e059a-196">Nachricht an Empfänger</span><span class="sxs-lookup"><span data-stu-id="e059a-196">Message to Recipient</span></span>|<span data-ttu-id="e059a-197">Fibu Buch.-Blattzeile</span><span class="sxs-lookup"><span data-stu-id="e059a-197">General Journal Line</span></span>|<span data-ttu-id="e059a-198">Die Meldung an den Empfänger, die in der Zahlungszeile angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-198">The message to recipient that is specified on the payment line</span></span>|  
|<span data-ttu-id="e059a-199">Betrag</span><span class="sxs-lookup"><span data-stu-id="e059a-199">Amount</span></span>|<span data-ttu-id="e059a-200">Betrag</span><span class="sxs-lookup"><span data-stu-id="e059a-200">Amount</span></span>|<span data-ttu-id="e059a-201">Fibu Buch.-Blattzeile</span><span class="sxs-lookup"><span data-stu-id="e059a-201">General Journal Line</span></span>|<span data-ttu-id="e059a-202">Der Betrag auf der Zahlungszeile</span><span class="sxs-lookup"><span data-stu-id="e059a-202">The amount on the payment line</span></span>|  
|<span data-ttu-id="e059a-203">Währungscode</span><span class="sxs-lookup"><span data-stu-id="e059a-203">Currency Code</span></span>|<span data-ttu-id="e059a-204">Währungscode</span><span class="sxs-lookup"><span data-stu-id="e059a-204">Currency Code</span></span>|<span data-ttu-id="e059a-205">Fibu Buch.-Blattzeile</span><span class="sxs-lookup"><span data-stu-id="e059a-205">General Journal Line</span></span>|<span data-ttu-id="e059a-206">Der Währungscode auf der Zahlungszeile.</span><span class="sxs-lookup"><span data-stu-id="e059a-206">The currency code on the payment line</span></span>|  
|<span data-ttu-id="e059a-207">Lastschriftdatum</span><span class="sxs-lookup"><span data-stu-id="e059a-207">Transfer Date</span></span>|<span data-ttu-id="e059a-208">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="e059a-208">Posting Date</span></span>|<span data-ttu-id="e059a-209">Fibu Buch.-Blattzeile</span><span class="sxs-lookup"><span data-stu-id="e059a-209">General Journal Line</span></span>|<span data-ttu-id="e059a-210">Das Buchungsdatum der Zahlungsposition.</span><span class="sxs-lookup"><span data-stu-id="e059a-210">The posting date of the payment line</span></span>|  
|<span data-ttu-id="e059a-211">Rechnungsbetrag</span><span class="sxs-lookup"><span data-stu-id="e059a-211">Invoice Amount</span></span>|<span data-ttu-id="e059a-212">Ursprungsbetrag</span><span class="sxs-lookup"><span data-stu-id="e059a-212">Original Amount</span></span>|<span data-ttu-id="e059a-213">Debitoren-/Kreditorenposten</span><span class="sxs-lookup"><span data-stu-id="e059a-213">Customer/Vendor Ledger Entry</span></span>|<span data-ttu-id="e059a-214">Der Betrag in dem Eintrag, auf den die Zahlung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e059a-214">The amount on the entry that the payment is applied to</span></span>|  
|<span data-ttu-id="e059a-215">Rechnungsdatum</span><span class="sxs-lookup"><span data-stu-id="e059a-215">Invoice Date</span></span>|<span data-ttu-id="e059a-216">Belegdatum</span><span class="sxs-lookup"><span data-stu-id="e059a-216">Document Date</span></span>|<span data-ttu-id="e059a-217">Debitoren-/Kreditorenposten</span><span class="sxs-lookup"><span data-stu-id="e059a-217">Customer/Vendor Ledger Entry</span></span>|<span data-ttu-id="e059a-218">Der Rechnungsbetrag in dem Eintrag, auf den die Zahlung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e059a-218">The invoice date on the entry that the payment is applied to</span></span>|  
|<span data-ttu-id="e059a-219">Adresse Empfängerbank</span><span class="sxs-lookup"><span data-stu-id="e059a-219">Recipient Bank Address</span></span>|<span data-ttu-id="e059a-220">Adresse</span><span class="sxs-lookup"><span data-stu-id="e059a-220">Address</span></span>|<span data-ttu-id="e059a-221">Debitorenbankkonto/Kreditorenbankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-221">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="e059a-222">Die Bankkontoadresse des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-222">The recipient bank account address that is specified on the customer or vendor bank account card</span></span>|  
|<span data-ttu-id="e059a-223">Die Bankkontoadresse des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-223">The recipient bank account address that is specified on the customer or vendor bank account card</span></span>|<span data-ttu-id="e059a-224">Ort</span><span class="sxs-lookup"><span data-stu-id="e059a-224">City</span></span>|<span data-ttu-id="e059a-225">Debitorenbankkonto/Kreditorenbankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-225">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="e059a-226">Die Stadt des Bankkontos des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-226">The recipient bank account city that is specified on the customer or vendor bank account card</span></span>|  
|<span data-ttu-id="e059a-227">Name Empfängerbank</span><span class="sxs-lookup"><span data-stu-id="e059a-227">Recipient Bank Name</span></span>|<span data-ttu-id="e059a-228">Name</span><span class="sxs-lookup"><span data-stu-id="e059a-228">Name</span></span>|<span data-ttu-id="e059a-229">Debitorenbankkonto/Kreditorenbankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-229">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="e059a-230">Der Name des Bankkontos des Empfängers, der auf der Debitoren- oder auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-230">The recipient bank account name that is specified on the customer or vendor bank account card</span></span>|  
|<span data-ttu-id="e059a-231">Land/Region Empfängerbank</span><span class="sxs-lookup"><span data-stu-id="e059a-231">Recipient Bank Country/Region</span></span>|<span data-ttu-id="e059a-232">Länder-/Regionscode</span><span class="sxs-lookup"><span data-stu-id="e059a-232">Country/Region Code</span></span>|<span data-ttu-id="e059a-233">Debitorenbankkonto/Kreditorenbankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-233">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="e059a-234">Das Land/Die Region des Bankkontos des Empfängers, das auf der Debitoren- oder auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-234">The recipient bank account country/region that is specified on the customer or vendor bank account card</span></span>|  
|<span data-ttu-id="e059a-235">PLZ-Code Empfängerbank</span><span class="sxs-lookup"><span data-stu-id="e059a-235">Recipient Bank Post Code</span></span>|<span data-ttu-id="e059a-236">PLZ-Code</span><span class="sxs-lookup"><span data-stu-id="e059a-236">Post Code</span></span>|<span data-ttu-id="e059a-237">Debitorenbankkonto/Kreditorenbankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-237">Customer Bank Account/Vendor Bank Account</span></span>|<span data-ttu-id="e059a-238">Die Postleitzahl des Bankkontos des Empfängers, die auf der Debitoren- oder auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-238">The recipient bank account post code that is specified on the customer or vendor bank account card</span></span>|  
|<span data-ttu-id="e059a-239">Adresse Absenderbank</span><span class="sxs-lookup"><span data-stu-id="e059a-239">Sender Bank Address</span></span>|<span data-ttu-id="e059a-240">Adresse</span><span class="sxs-lookup"><span data-stu-id="e059a-240">Address</span></span>|<span data-ttu-id="e059a-241">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-241">Bank Account</span></span>|<span data-ttu-id="e059a-242">Die Absenderbankkontoadresse, die auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-242">The sender bank account address that is specified on the bank account card</span></span>|  
|<span data-ttu-id="e059a-243">Ort Absenderbank</span><span class="sxs-lookup"><span data-stu-id="e059a-243">Sender Bank City</span></span>|<span data-ttu-id="e059a-244">Ort</span><span class="sxs-lookup"><span data-stu-id="e059a-244">City</span></span>|<span data-ttu-id="e059a-245">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-245">Bank Account</span></span>|<span data-ttu-id="e059a-246">Die Absenderbankkontostadt, die auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-246">The sender bank account city that is specified on the bank account card</span></span>|  
|<span data-ttu-id="e059a-247">Name der Absenderbank</span><span class="sxs-lookup"><span data-stu-id="e059a-247">Sender Bank Name</span></span>|<span data-ttu-id="e059a-248">Name</span><span class="sxs-lookup"><span data-stu-id="e059a-248">Name</span></span>|<span data-ttu-id="e059a-249">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-249">Bank Account</span></span>|<span data-ttu-id="e059a-250">Der Absenderbankkontoname, der auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-250">The sender bank account name that is specified on the bank account card</span></span>|  
|<span data-ttu-id="e059a-251">Land/Region Absenderbank</span><span class="sxs-lookup"><span data-stu-id="e059a-251">Sender Bank Country/Region</span></span>|<span data-ttu-id="e059a-252">Länder-/Regionscode</span><span class="sxs-lookup"><span data-stu-id="e059a-252">Country/Region Code</span></span>|<span data-ttu-id="e059a-253">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-253">Bank Account</span></span>|<span data-ttu-id="e059a-254">Das Land/Die Region des Absenderbankkontos, das/die auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-254">The sender bank account country/region that is specified on the bank account card</span></span>|  
|<span data-ttu-id="e059a-255">PLZ-Code Absenderbank</span><span class="sxs-lookup"><span data-stu-id="e059a-255">Sender Bank Post Code</span></span>|<span data-ttu-id="e059a-256">PLZ-Code</span><span class="sxs-lookup"><span data-stu-id="e059a-256">Post Code</span></span>|<span data-ttu-id="e059a-257">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-257">Bank Account</span></span>|<span data-ttu-id="e059a-258">Der Absenderbankkonto-PLZ-Code, der auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-258">The sender bank account post code that is specified on the bank account card</span></span>|  
|<span data-ttu-id="e059a-259">Fibu Buch.-Blattvorlage</span><span class="sxs-lookup"><span data-stu-id="e059a-259">General Journal Template</span></span>|<span data-ttu-id="e059a-260">Buch.-Blattvorlagenname</span><span class="sxs-lookup"><span data-stu-id="e059a-260">Journal Template Name</span></span>|<span data-ttu-id="e059a-261">Fibu Buch.-Blattzeile</span><span class="sxs-lookup"><span data-stu-id="e059a-261">General Journal Line</span></span>|<span data-ttu-id="e059a-262">Die Fibu Buch.-Blattvorlage, die für die Zahlungszeile verwendet wird</span><span class="sxs-lookup"><span data-stu-id="e059a-262">The general journal template that is used for the payment line</span></span>|  
|<span data-ttu-id="e059a-263">Fibu Buch.-Blattname</span><span class="sxs-lookup"><span data-stu-id="e059a-263">General Journal Batch Name</span></span>|<span data-ttu-id="e059a-264">Buch.-Blattname</span><span class="sxs-lookup"><span data-stu-id="e059a-264">Journal Batch Name</span></span>|<span data-ttu-id="e059a-265">Fibu Buch.-Blattzeile</span><span class="sxs-lookup"><span data-stu-id="e059a-265">General Journal Line</span></span>|<span data-ttu-id="e059a-266">Der Fibu Buch.-Blatt-Buch.-Blatt, das für die Zahlungszeile verwendet wird</span><span class="sxs-lookup"><span data-stu-id="e059a-266">The general journal batch name that is used for the payment line</span></span>|  
|<span data-ttu-id="e059a-267">Name der Absenderbank – Datenkonvertierung</span><span class="sxs-lookup"><span data-stu-id="e059a-267">Sender Bank Name - Data Conv.</span></span>|<span data-ttu-id="e059a-268">Bankname – Datenkonv.</span><span class="sxs-lookup"><span data-stu-id="e059a-268">Bank Name – Data Conv.</span></span>|<span data-ttu-id="e059a-269">Bankkonto</span><span class="sxs-lookup"><span data-stu-id="e059a-269">Bank Account</span></span>|<span data-ttu-id="e059a-270">Der Absenderbankkontoname, der avom Bankdatenkonvertierungs-Service angefordert wird und auf der Bankkontokarte angegeben ist</span><span class="sxs-lookup"><span data-stu-id="e059a-270">The sender bank account name that is requested by the bank data conversion service and specified on the bank account card</span></span>|  

## <a name="see-also"></a><span data-ttu-id="e059a-271">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e059a-271">See Also</span></span>  
[<span data-ttu-id="e059a-272">Einrichten eines Datenaustauschs</span><span class="sxs-lookup"><span data-stu-id="e059a-272">Setting Up Data Exchange</span></span>](across-set-up-data-exchange.md)  
<span data-ttu-id="e059a-273">[Daten elektronisch austauschen](across-data-exchange.md)
[Richten Sie den Bankdaten-Konvertierungsdienst ein](bank-how-setup-bank-data-conversion-service.md) </span><span class="sxs-lookup"><span data-stu-id="e059a-273">[Exchanging Data Electronically](across-data-exchange.md)
[Set Up the Bank Data Conversion Service](bank-how-setup-bank-data-conversion-service.md) </span></span>  
[<span data-ttu-id="e059a-274">Nehmen Sie Zahlungen mit dem Bank-Datenkonvertierungs-Service- oder einer SEPA-Banküberweisung vor</span><span class="sxs-lookup"><span data-stu-id="e059a-274">Make Payments with Bank Data Conversion Service or SEPA Credit Transfer</span></span>](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   

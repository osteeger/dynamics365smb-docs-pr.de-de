---
title: 'Gewusst wie: Druck von Listenberichten für Kreditorenzahlungen'
description: Die Liste Kreditorenzahlungen zeigt eine Liste von Zahlungen für jeden Kreditor an. Der Bericht kann Zahlungen chronologisch oder nach Kreditor gruppiert sortieren.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: ''
ms.date: 04/01/2020
ms.author: edupont
ms.openlocfilehash: d148e5b9d33359a3085e51ab73b6a88f27dd4064
ms.sourcegitcommit: a80afd4e5075018716efad76d82a54e158f1392d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "3779116"
---
# <a name="print-vendor-payments-list-reports"></a>Gewusst wie: Druck von Listenberichten für Kreditorenzahlungen
Die Liste **Kreditorenzahlungen** zeigt eine Liste von Zahlungen für jeden Kreditor an. Der Bericht kann Zahlungen chronologisch oder nach Kreditor gruppiert sortieren.  

## <a name="to-print-the-vendor-payments-list-report"></a>Gewusst wie: Druck von Listenberichten für Kreditorenzahlungen  

1.  Wählen Sie das Symbol ![Glühbirne, das die Funktion „Sie wünschen“ öffnet](../../media/ui-search/search_small.png "Sagen Sie mir, was Sie tun wollen") aus, geben Sie **Kreditorenzahlungsliste** ein, und wählen Sie dann den entsprechenden Link.  
2.  Füllen Sie im Inforegister **Optionen** die Felder gemäß der Beschreibung in der folgenden Tabelle aus.  

    |Feld|Description|  
    |---------------------------------|---------------------------------------|  
    |**Sortieren**|Gibt den sortierten Auftrag an. Sie können chronologisch oder nach Kreditor sortieren. Wenn Sie nach Kreditor sortieren, finden Sie eine Zwischensumme für jeden Kreditor. Wenn Sie chronologisch sortieren, finden Sie keine Zwischensummen.|  
    |**Layout**|Gibt die Nummer des Berichtslayouts an.<br /><br /> Die Ergebnisse können in den folgenden Layouts angezeigt werden:<br /><br /> **Standard**<br /> Zeigt die Kreditorennummer und den Kreditorennamen, zusammen mit den Buchungsdetails wie Dokumentennummer und den Betrag in lokaler Währung an.<br /><br /> **FCY-Beträge**<br /> Zeigt die Kreditorennummer, Kreditorennamen, Belegnummer, Zahlungsstatus (O für den Wert Offen, PP. für Teilzahlung und C für geschlossene) an.<br /><br /> **Buchungsinfo**<br /> Zeigt die Kreditorennummer, den Kreditorennamen, die Kostenstelle, das Kostenobjekt, die Benutzer-ID und den Zahlungsbetrag an.|  

 Am Ende des Berichts wir die Anzahl der verarbeiteten Zahlungen angezeigt.  

## <a name="see-also"></a>Siehe auch  
[Zahlungen vornehmen](../../payables-make-payments.md)

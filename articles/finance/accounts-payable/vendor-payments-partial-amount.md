---
title: Kreditora daļējas summas maksājumi
description: Reizēm jūs veicat kreditoram maksājumu, kas ir mazāks par rēķinā norādīto summu. Šajā rakstā ir aprakstītas dažādās opcijas, ko darīt šādās situācijās.
author: abruer
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1be00ef4bd432bc0252e0588a3108b5b0f570e4
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716302"
---
# <a name="vendor-payments-for-a-partial-amount"></a>Kreditoru maksājumi par daļēju summu

[!include [banner](../includes/banner.md)]

Reizēm jūs veicat kreditoram maksājumu, kas ir mazāks par rēķinā norādīto summu. Šajā rakstā ir aprakstītas dažādās opcijas, ko darīt šādās situācijās. Jums pieejamās opcijas ir atkarīgas no jūsu biznesa prasībām un konfigurācijas. 

## <a name="cash-discount-amounts"></a>Termiņatlaides summas

Varat piedāvāt kreditoram termiņatlaidi, ja rēķins tiek apmaksāts pirms apmaksas datuma. Piemēram, ja rēķins tiek apmaksāts 10 dienu laikā, jūs ievadiet rēķinu par summu 100,00, kurā norādīta 2 procentu termiņatlaide. Apmaksas termiņš ir 30 dienas. Ja maksājuma piedāvājumā kā rēķina atlases kritērijs ir izmantota termiņatlaide un ja priekšlikums ir spēkā termiņatlaides datumā vai pirms tā, tad šis rēķins tiek atlasīts apmaksai un maksājums tiek veikts par summu 98,00. Termiņatlaidi var piemērot arī vienreizējam maksājumam, kas ir izveidots manuāli.

## <a name="partial-payments-with-cash-discounts"></a>Daļēji maksājumi ar termiņatlaidēm
Ja tiek veikts daļējs maksājums, var ieplānot veikt papildu daļēju maksājumu, lai pilnībā segtu rēķinu. Lai daļējam maksājumam piemērotu termiņatlaidi, opcija **Aprēķināt daļēju maksājumu termiņatlaides** lapā **Debitoru moduļa parametri** ir jāiestata ar vērtību **Jā**. 

Piemēram, ja rēķins tiek apmaksāts 10 dienu laikā pēc tā izrakstīšanas, jums tiek piedāvāta 2 procentu termiņatlaide. Rēķins ir iegrāmatots par summu 100,00. Ja 10 dienu laikā veicat maksājumu par summu 49,00, maksājumu žurnālā ievadiet debeta summu 49,00. Kad daļējais maksājums tiek nosegts lapā **Nosegt atvērtās transakcijas**, laukā **Noņemamā termiņatlaides summa** tiek parādīta vērtība **1,00**. 

> [!NOTE] 
> Ja ievadāt daļēju maksājumu un atstājat pilnu rēķina summu laukā **Nosedzamā summa**, tad lauks **Ņemamā termiņatlaides summa** automātiski tiek pārrēķināts, kad grāmatojot transakcijas.

## <a name="credit-notes-with-cash-discounts"></a>Kredīta notas ar temiņatlaidēm
Jūs varat atgriezt dažas rēķinā iekļautās preces un saņemt kredīta notu. Ja termiņatlaide ir piemērota sākotnējam rēķinam, varat atņemt atlaides vērtību un saņemt pareizās summas atmaksu. Ja opcija **Aprēķināt kredīta notu termiņatlaides** lapā **Kreditoru moduļa parametri** ir iestatīta ar vērtību **Jā**, kredīta notai automātiski tiek aprēķināta atlaide. 

Piemēram, ja rēķins tiek apmaksāts 10 dienu laikā pēc tā izrakstīšanas, jums tiek piedāvāta 2 procentu termiņatlaide. Rēķins tiek iegrāmatots par summu 100,00. Ja tiek atgrieztas preces un saņemta kredīta nota, varat ievadīt kredīta notu par sākotnējā rēķina visu summu 100,00 kopā ar 2 procentu termiņatlaidi, kas arī ir norādīta kredītrēķinā.  Skatot kredīta notu lapā **Nosegt transakcijas**, summa **98,00** ir redzama laukā **Nosedzamā summa**, un summa **-2,00** ir redzama laukā **Termiņatlaides summa**. Atlaides summa tiek grāmatota uz termiņatlaides kontu.

## <a name="overpaymentunderpayment-amounts"></a>Pārmaksas/nepilnas samaksas summas
Ja vēl atlikusī nosedzamā summa ir ļoti neliela, varat veikt daļējo maksājumu. Piemēram, kreditora rēķins summa ir 1000,00, bet jūs veicat maksājumu par summu 999.90. Ja atlikusī summa ir mazāka par summu, kas norādīta pārmaksām vai nepilnām samaksām lapā **Kreditoru moduļa parametri**, starpība tiek automātiski grāmatota uz pārmaksas/nepilnas samaksas virsgrāmatas kontu.


Plašāku informāciju skatiet šeit: [Kreditora maksājumu pārskats](../cash-bank-management/tasks/vendor-payment-overview.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

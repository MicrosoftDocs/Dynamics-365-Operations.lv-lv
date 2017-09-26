---
title: "Kreditora daļējas summas maksājumi"
description: "Reizēm jūs veicat kreditoram maksājumu, kas ir mazāks par rēķinā norādīto summu. Šajā rakstā ir aprakstītas dažādās opcijas, ko darīt šādās situācijās. Jums pieejamās opcijas ir atkarīgas no jūsu biznesa prasībām un konfigurācijas."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: 191d1ee0b47da4930e10146ba164d601d038e81b
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2017

---

# <a name="vendor-payments-for-a-partial-amount"></a>Kreditora daļējas summas maksājumi

[!include[banner](../includes/banner.md)]


Reizēm jūs veicat kreditoram maksājumu, kas ir mazāks par rēķinā norādīto summu. Šajā rakstā ir aprakstītas dažādās opcijas, ko darīt šādās situācijās. Jums pieejamās opcijas ir atkarīgas no jūsu biznesa prasībām un konfigurācijas. 

<a name="cash-discount-amounts"></a>Termiņatlaides summas
---------------------

Varat piedāvāt kreditoram termiņatlaidi, ja rēķins tiek apmaksāts pirms apmaksas datuma. Piemēram, ja rēķins tiek apmaksāts 10 dienu laikā, jūs ievadiet rēķinu par summu 100,00, kurā norādīta 2 procentu termiņatlaide. Apmaksas termiņš ir 30 dienas. Ja maksājuma piedāvājumā kā rēķina atlases kritērijs ir izmantota termiņatlaide un ja priekšlikums ir spēkā termiņatlaides datumā vai pirms tā, tad šis rēķins tiek atlasīts apmaksai un maksājums tiek veikts par summu 98,00. Termiņatlaidi var piemērot arī vienreizējam maksājumam, kas ir izveidots manuāli.

## <a name="partial-payments-with-cash-discounts"></a>Daļēji maksājumi ar termiņatlaidēm
Ja tiek veikts daļējs maksājums, var ieplānot veikt papildu daļēju maksājumu, lai pilnībā segtu rēķinu. Lai termiņatlaidi piemērotu daļējam maksājumam, opcijai **Aprēķināt daļēju maksājumu termiņatlaides** lapā **Debitoru moduļa parametri** ir jāiestata vērtība **Jā**. 

Piemēram, ja rēķins tiek apmaksāts 10 dienu laikā pēc tā izrakstīšanas, jums tiek piedāvāta 2 procentu termiņatlaide. Rēķins ir iegrāmatots par summu 100,00. Ja 10 dienu laikā veicat maksājumu par summu 49,00, maksājumu žurnālā ievadiet debeta summu 49,00. Kad daļējais maksājums tiek nosegts lapā **Nosegt atvērtās transakcijas**, laukā **Noņemamā termiņatlaides summa** tiek parādīta vērtība **1,00**. 

> [!NOTE] 
> Ja ievadāt daļēju maksājumu un atstājat pilnu rēķina summu laukā **Nosedzamā summa**, tad lauks **Ņemamā termiņatlaides summa** automātiski tiek pārrēķināts, kad grāmatojot transakcijas.

## <a name="credit-notes-with-cash-discounts"></a>Kredīta notas ar temiņatlaidēm
Jūs varat atgriezt dažas rēķinā iekļautās preces un saņemt kredīta notu. Ja termiņatlaide ir piemērota sākotnējam rēķinam, varat atņemt atlaides vērtību un saņemt pareizās summas atmaksu. Ja opcijai **Aprēķināt kredīta notu termiņatlaides** lapā **Kreditoru moduļa parametri** ir iestatīta vērtība **Jā**, tad kredīta notai automātiski tiek aprēķināta atlaide. 

Piemēram, ja rēķins tiek apmaksāts 10 dienu laikā pēc tā izrakstīšanas, jums tiek piedāvāta 2 procentu termiņatlaide. Rēķins tiek iegrāmatots par summu 100,00. Ja tiek atgrieztas preces un saņemta kredīta nota, varat ievadīt kredīta notu par sākotnējā rēķina visu summu 100,00 kopā ar 2 procentu termiņatlaidi, kas arī ir norādīta kredītrēķinā.  Skatot kredīta notu lapā **Nosegt transakcijas**, summa **98,00** ir redzama laukā **Nosedzamā summa**, un summa **-2,00** ir redzama laukā **Termiņatlaides summa**. Atlaides summa tiek grāmatota uz termiņatlaides kontu.

## <a name="overpaymentunderpayment-amounts"></a>Pārmaksas/nepilnas samaksas summas
Ja vēl atlikusī nosedzamā summa ir ļoti neliela, varat veikt daļējo maksājumu. Piemēram, kreditora rēķins summa ir 1000,00, bet jūs veicat maksājumu par summu 999.90. Ja atlikusī summa ir mazāka par summu, kas norādīta pārmaksām vai nepilnām samaksām lapā **Kreditoru moduļa parametri**, starpība tiek automātiski grāmatota uz pārmaksas/nepilnas samaksas virsgrāmatas kontu.


Plašāku informāciju skatiet šeit: [Kreditora maksājumu pārskats](../cash-bank-management/tasks/vendor-payment-overview.md).


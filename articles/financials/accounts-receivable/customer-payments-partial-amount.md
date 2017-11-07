---
title: "Debitoru maksājumi daļējai summai"
description: "Reizēm debitori veic maksājumu, kas ir mazāks par rēķinā norādīto summu. Šajā rakstā ir aprakstītas dažādās opcijas, ko darīt šādās situācijās. Jums pieejamās opcijas ir atkarīgas no jūsu biznesa prasībām un konfigurācijas."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13011
ms.assetid: 20423a2d-6997-4e1c-a596-a77016600071
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6e4fac197e75b80609486be7ea7c50c4b48beeb7
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="customer-payments-for-a-partial-amount"></a>Debitoru maksājumi daļējai summai

[!include[banner](../includes/banner.md)]


Reizēm debitori veic maksājumu, kas ir mazāks par rēķinā norādīto summu. Šajā rakstā ir aprakstītas dažādās opcijas, ko darīt šādās situācijās. Jums pieejamās opcijas ir atkarīgas no jūsu biznesa prasībām un konfigurācijas.

<a name="partial-payment-with-no-discount"></a>Daļējs maksājums bez atlaides
--------------------------------

Klienti varētu veikt daļēju maksājumu, vienkārši tāpēc, ka nav pieejams pietiekami daudz naudas, lai apmaksātu rēķinu pilnā apmērā vai tāpēc, ka ir domstarpības par krājumu rēķinā. Šādā gadījumā rēķins var būt daļēji segts ar maksājumu. Rēķins paliks atvērts un rādīs bilanci.

## <a name="discount-amounts"></a>Atlaižu summas
Varat piedāvāt debitoriem termiņatlaidi, apmaksājot rēķinu pirms apmaksas datuma. Piemēram, jūs ievadiet rēķinu par summu 100,00, kas norāda 2 procentu termiņatlaidi, ja rēķins tiks samaksāts 10 dienu laikā. Apmaksas datuma termiņš ir 30 dienas. Ja saņemat maksājumu 98,00 10 dienu laikā, ievadiet maksājumu par summu 98,00. Pēc tam, kad rēķins ir atzīmēts nosegšanai, termiņatlaide tiek piemērota automātiski.

## <a name="partial-payments-with-cash-discounts"></a>Daļēji maksājumi ar termiņatlaidēm
Kad klienti veic daļēju maksājumu, iespējams, tie plāno veikt papildu daļēju maksājumu, lai pilnībā segtu rēķinu. Lai daļējam maksājumam izmantotu termiņatlaidi, lapā **Debitoru moduļa parametri** opcijai **Aprēķināt termiņatlaides daļējiem maksājumiem** ir jāiestata vērtība **Jā**. 

Piemēram, varat piedāvāt 2 procentu termiņatlaidi, ja rēķins tiek apmaksāts 10 dienu laikā pēc tā izrakstīšanas. Rēķins ir iegrāmatots par summu 100,00. Ja saņemat maksājumu 49,00 10 dienu laikā, ievadiet maksājumu žurnālā kredītu par summu 49,00. Kad iestatāt daļēju maksājumu lapā **Darbību segšana**, **1,00** parādās laukā **Ņemamā termiņatlaides summa**. Atlaides summa tiek grāmatota uz termiņatlaides kontu. 

> [!NOTE] 
> Ja ievadāt daļēju maksājumu un atstājat pilnu rēķina summu laukā **Nosedzamā summa**, tad lauks **Ņemamā termiņatlaides summa** automātiski tiek pārrēķināts, kad grāmatojot transakcijas.

## <a name="credit-notes-with-discounts"></a>Kredīta notas ar atlaidēm
Ja debitori atgriež dažus no krājumiem rēķinā, var izdot kredīta notu. Ja termiņatlaide tika izmantota sākotnējā rēķinā, kredītrēķinam klientam jābūt neto summai no termiņatlaides, ko izmantoja klients. Ja opcija **Aprēķināt termiņatlaides kredīta notām** ir iestatīta uz **Jā**, lapā **Debitoru moduļa parametri**, atlaide tiek automātiski aprēķināta kredīta notai. 

Piemēram, jūs piedāvājāt maksājuma nosacījumus ar 2 procentu termiņatlaidi, ja rēķins tiek apmaksāts 10 dienu laikā pēc tā izrakstīšanas. Tika iegrāmatots rēķins par summu 100,00, un debitors izmantoja termiņatlaidi. Ja debitors atgriež preces un jūs izsniedzat kredīta notu, varat ievadīt kredīta notu par summu -100,00. Skatot kredīta notu lapā **Nosegt atvērtās transakcijas**, summa **98,00** ir redzama laukā **Nosedzamā summa**, un summa **-2,00** ir redzama laukā **Termiņatlaides summa**. Atlaides summa tiek grāmatota uz termiņatlaides kontu.

## <a name="overpaymentunderpayment-amounts"></a>Pārmaksas/nepilnas samaksas summas
Kad klienti veic maksājumu, iespējams, ka būs ļoti neliela summa, kas paliks nenosegta. Piemēram, jūs klientam izrakstāt rēķinu par summu 1000,00, bet debitors apmaksā 999,90. Ja atlikusī summa ir mazāka par summu, kas norādīta pārmaksām vai nepilnām samaksām lapā **Debitoru moduļa parametri**, starpība tiek automātiski grāmatota uz pārmaksas/nepilnas samaksas virsgrāmatas kontu.

## <a name="full-settlement"></a>Pilnīga nosegšana
Klienti var veikt daļēju maksājumu, kur atlikusī summa netiks samaksāta, taču ir lielāka nekā nepilnas samaksas summa, kas norādīta lapā **Kreditoru moduļa parametri**. Ja rēķinu vēlaties atzīmēt kā pilnībā nosegtu, varat izmantot opciju **Pilnīga nosegšana** lapā **Nosegt transakciju**. (Jūs varat iespējot pilnīgas segšanas funkcionalitāti, izmantojot konfigurācijas atslēgu.) Piemēram, rēķins tiek iegrāmatots par summu 1000,00 un klients veic maksājumu 990,00. Jūs esat vienojušies, ka klientam nav jāmaksā atlikusī summa 10,00. Pēc rēķina atzīmēšanas segšanai varat arī atzīmēt vienumu **Pilnīga nosegšana**. Tad rēķins tiks uzskatīts par pilnībā nosegtu. 10,00 starpība tiek grāmatota uz termiņatlaides kontu kā papildu termiņatlaides summa.


Papildinformāciju skatiet šeit: [Debitora maksājumu depozīts](tasks/deposit-customer-payments.md).


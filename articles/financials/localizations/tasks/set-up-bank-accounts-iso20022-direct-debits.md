--- 
title: "Debitoru un debitoru bankas kontu iestatīšana ISO20022 tiešajiem debetiem"
description: "Šajā uzdevumā ir izklāstīts, kā iestatīt debitora bankas kontu un debitora tiešā debeta pilnvarojumu, kas ir nepieciešami, lai ģenerētu debitora maksājumu failu kā ISO20022 tiešo debetu."
author: mrolecki
manager: AnnBe
ms.date: 10/31/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 22fadf126dfa884520bc2fe6f94bc3fe3b612f77
ms.openlocfilehash: 86c3f62e17d4955c12d09b512624eb5f576a9cd3
ms.contentlocale: lv-lv
ms.lasthandoff: 10/31/2017

---
# <a name="set-up-customers-and-customer-bank-accounts-for-iso20022-direct-debits"></a>Debitoru un debitoru bankas kontu iestatīšana ISO20022 tiešajiem debetiem

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Šajā uzdevumā ir izklāstīts, kā iestatīt debitora bankas kontu un debitora tiešā debeta pilnvarojumu, kas ir nepieciešami, lai ģenerētu debitora maksājumu failu kā ISO20022 tiešo debetu. Atkarībā no iestatītajiem debitora maksājuma formātiem var būt nepieciešama šajā procedūras aprakstā nepieminēta papildinformācija par debitoru vai debitora bankas kontu. 

Šis uzdevums ir izveidots, izmantojot demonstrācijas uzņēmuma DEMF datus, norādot Vāciju kā juridiskās personas primārās adreses valsti.



Šis ir ceturtā no piecām procedūrām, kas demonstrē debitora maksājuma procesu, izmantojot elektronisko atskaišu konfigurācijas.


## <a name="set-up-a-customer-bank-account"></a>Debitora bankas konta iestatīšana
1. Pārejiet uz sadaļu Debitori > Debitori > Visi debitori.
2. Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus. Piemēram, filtrējiet pēc lauka Konts vērtības DE-010.
3. Sarakstā noklikšķiniet uz saites atlasītajā rindā.
4. Darbību rūtī noklikšķiniet uz Debitors.
5. Noklikšķiniet uz Banku konti.
6. Noklikšķiniet uz Jauns.
7. Ierakstiet vērtību laukā Bankas konts.
8. Laukā Nosaukums ierakstiet kādu vērtību.
    * Piemēram, ievadiet 'EUR banka'.  
9. Ievadiet vai atlasiet vērtību laukā Banku grupas.
10. Ievadiet vērtību laukā IBAN.
    * Piemēram, ievadiet 'DE36200400000628808808'.  
11. Ierakstiet vērtību laukā SWIFT kods.
    * Piemēram, ievadiet COBADEFFXXX.  Lūdzu, ņemiet vērā, ka SWIFT\BIC nav nepieciešami daudziem maksājumu formātiem, tomēr ir ieteicams reģistrēt to bankas kontam.  
12. Noklikšķiniet uz Saglabāt.
13. Aizvērt lapu.
14. Noklikšķiniet uz Rediģēt.
15. Izvērsiet Maksāšanas noklusējuma sadaļu.
16. Ievadiet vai atlasiet vērtību laukā Bankas konts.

## <a name="add-a-direct-debit-mandate"></a>Tiešā debeta pilnvarojuma pievienošana
1. Izvērsiet sadaļu Tiešā debeta pilnvarojumi.
2. Noklikšķiniet uz Pievienot.
3. Laukā Kreditora bankas konts, ievadiet vai atlasiet kādu vērtību.
    * Piemēram, atlasiet DEMF OPER.  
4. Ievadiet datumu laukā Parakstīšanas datums.
5. Noklikšķiniet uz Jā, lai apstiprinātu datuma atjaunināšanu.
6. Ievadiet vai atlasiet vērtību laukā Parakstīšanas vieta.
7. Ievadiet skaitli laukā Sagaidāmais maksājumu skaits.
8. Noklikšķiniet uz OK.
9. Noklikšķiniet uz Saglabāt.



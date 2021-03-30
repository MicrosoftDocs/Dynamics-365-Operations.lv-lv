---
title: Kreditora maksājumu papildu maksu definēšana
description: Iestatiet kreditoru maksājumu papildmaksas.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0705cdae069b687a141b0a85280eaed0fa207a89
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227260"
---
# <a name="define-vendor-payment-fees"></a>Kreditora maksājumu papildu maksu definēšana

[!include [banner](../../includes/banner.md)]

Iestatiet kreditoru maksājumu papildmaksas. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Pārejiet uz sadaļu Kreditori > Maksājuma iestatījumi > Komisijas maksa.
2. Noklikšķiniet uz Jauns.
3. Ierakstiet vērtību laukā Papildmaksas ID.
    * Papildmaksas ID ir jānorāda, kad šī papildmaksa tiks izmantota, piemēram, "EFT_Fee".  
4. Laukā Nosaukums ierakstiet kādu vērtību.
5. Ierakstiet vērtību laukā Papildmaksas apraksts.
    * Pievienojiet aprakstu, kas sniedz vairāk informācijas par gadījumiem, kad šī papildmaksa tiek noteikta.  
6. Laukā Maksa atlasiet Kreditors vai Virsgrāmata.
    * Ja papildmaksu sedz jūsu organizācija, tiek izmantota Virsgrāmata.  Ja papildmaksa tiek noteikta kreditoram, tiek izmantota vērtība Kreditors.  
7. Ievadiet galveno kontu, kurā papildmaksa tiks iekļauta.
    * Šī opcija ir pieejama tikai tad, kad maksas opcijā izvēlēta Virsgrāmata.  
8. Atlasiet žurnālu, kurā šī papildmaksa var tikt izmantota. 
    * Kreditora maksājuma papildmaksai jāatlasa žurnāls Kreditoru rēķinu apmaksa.  
9. Noklikšķiniet uz Saglabāt.
10. Noklikšķiniet uz Maksāšanas papildmaksu iestatījumi.
    * Dodieties uz papildmaksu iestatījumiem, lai definētu, kad atlasītajam žurnālam pēc noklusējuma jāizmanto papildmaksa.  
11. Atlasiet Tabula, Grupa vai Visi.
    * Tabula tiek izmantota, lai atlasītu vienu bankas kontu, Grupa tiek izmantota, lai atlasītu banku grupu, bet vērtība Visi tiek izmantota, lai šo papildmaksu iestatījumus izmantotu visiem bankas kontiem.  
12. Atlasiet banku grupu vai bankas kontu.
    * Ja atlasījāt Grupa, uzmeklēšanā tiks parādītas banku grupas, ja atlasījāt Tabula, uzmeklēšanā tiks parādīti bankas konti.  
13. Atlasiet maksāšanas metodi, kurai noteikt šo papildmaksu.
14. Atlasiet maksājuma specifikāciju atlasītajai maksāšanas metodei.
    * Maksājuma specifikācija tiek izmantota maksāšanas metodēm, kas attiecināmas uz elektronisko līdzekļu pārsūtīšanu.  
15. Atlasiet, vai papildmaksa ir procenti, summa vai intervāls.
16. Ievadiet papildmaksas procentuālo daļu vai summu.
    * Ja papildmaksa ir procentuāla daļa, ievadiet procentuālo daļu. Ja papildmaksa ir summa, ievadiet papildmaksas summu. Ja papildmaksa ir intervāls, pa pakāpēm sadalītu papildmaksu definēšanai izmantojiet cilni Intervāls.  
17. Laukā Papildmaksas valūta atlasiet valūtu, kurā papildmaksa tiek noteikta.
    * Šī valūta attiecas uz papildmaksu. Apmaksas valūta tiek izmantota, lai definētu to, kad papildmaksas kārtula ir jānovērtē, pamatojoties uz maksājuma valūtu. Piemēram, jūsu banka var iekasēt komisijas maksu, kad maksājums tiek veikts EUR, bet citiem maksājumiem komisijas maksa netiek noteikta.  
18. Noklikšķiniet uz Saglabāt.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
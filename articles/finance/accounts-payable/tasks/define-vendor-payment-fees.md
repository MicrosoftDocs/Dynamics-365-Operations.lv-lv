---
title: Kreditora maksājumu papildu maksu definēšana
description: Iestatiet kreditoru maksājumu papildmaksas.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendPaymFee, VendPaymModeFee, BankAccountTableLookUp
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c490bb4d15fa03742b12f337046f26976ab70d29
ms.sourcegitcommit: 3105642fca2392edef574b60b4748a82cda0a386
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/12/2022
ms.locfileid: "8109835"
---
# <a name="define-vendor-payment-fees"></a>Kreditora maksājumu papildu maksu definēšana

[!include [banner](../../includes/banner.md)]

Iestatiet kreditoru maksājumu papildmaksas. Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.

1. Pārejiet uz **sadaļu > Kreditori, lai > maksājumu nodevas**.
2. Klikšķiniet **Jauns**.
3. Laukā **Maksas ID** ievadiet vērtību.
    * Maksas **ID ir** jāapraksta, kad tiks izmantota šī maksa, piemēram, "EFT_Fee".  
4. Laukā **Nosaukums** ierakstiet kādu vērtību.
5. Laukā **Papildmaksas** apraksts ievadiet vērtību.
    * Pievienojiet aprakstu, kas sniedz vairāk informācijas par gadījumiem, kad šī papildmaksa tiek noteikta.  
6. Laukā **Maksas atlasiet Kreditoru vai** Virsgrāmatu **·** **.**
    * **Virsgrāmata** tiek izmantota, kad maksa tiks izdevumiem jūsu uzņēmumam. **Kreditors** tiek izmantots, kad maksa tiks novērtēta kreditoram.  
7. Ievadiet galveno kontu, kurā papildmaksa tiks iekļauta.
    * Šī opcija ir pieejama tikai tad, ja virsgrāmata **ir** atlasīta kā **opcija** Maksa.  
8. Atlasiet žurnālu, kurā šī papildmaksa var tikt izmantota. 
    * Kreditora maksājuma papildmaksai jāatlasa žurnāls Kreditoru rēķinu apmaksa.  
9. Noklikšķiniet uz **Saglabāt**.
10. Noklikšķiniet uz **Komisijas maksas iestatīšana**.
    * Turpiniet ar maksājuma **papildmaksas iestatījumu,** lai definētu, kad pēc noklusējuma maksa jāiekļauj atlasītajā žurnālā.  
11. Atlasiet **Tabulu**, Grupu **vai** **Visus**.
    * **Tabula** tiek izmantota, lai atlasītu atsevišķu bankas kontu, **grupa** tiek izmantota banku grupas atlasei, **bet** Visi lieto šos papildu maksas iestatījumus visiem bankas kontiem.  
12. Atlasiet banku grupu vai bankas kontu.
    * Ja atlasījāt Grupa, pārlūks parādīs banku **grupu un** rādīs bankas kontus, ja atlasījāt **Tabula**.  
13. Atlasiet maksāšanas metodi, kurai noteikt šo papildmaksu.
14. **Atlasiet maksājuma specifikāciju** atlasītajai maksājuma metodei.
    * Maksājuma **specifikācija tiek** izmantota ar elektronisko līdzekļu pārsūtīšanas maksājuma metodēm.  
15. Atlasiet, vai papildmaksa ir procenti, summa vai intervāls.
16. Ievadiet papildmaksas procentuālo daļu vai summu.
    * Ja papildu **maksa** ir izteikta procentos, ievadiet procentus. **Ja papildu** maksa ir summa, ievadiet papildmaksas summu. Ja maksa **ir** intervāls, izmantojiet cilni **Intervāls**, lai definētu pakāpju maksas.  
17. Laukā **Papildmaksas** valūta atlasiet valūtu, kurā tiks novērtēts maksājums.
    * Šī valūta attiecas uz papildmaksu. Apmaksas valūta tiek izmantota, lai definētu to, kad papildmaksas kārtula ir jānovērtē, pamatojoties uz maksājuma valūtu. Piemēram, jūsu banka var iekasēt komisijas maksu, kad maksājums tiek veikts EUR, bet citiem maksājumiem komisijas maksa netiek noteikta.  
18. Noklikšķiniet uz **Saglabāt**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

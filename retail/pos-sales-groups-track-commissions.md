---
title: "POS komisijas maksu izsekošana, izmantojot pārdošanas grupas"
description: "Mazumtirdzniecībā bieži lietota prakse ir pārdošanas darbību izsekošana pēc darbinieka, kurš strādā ar debitoru, sniedzot palīdzību, veicot papildu pārdošanu un šķērspārdošanu un apstrādājot transakciju."
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core, UnifiedOperations
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611, Retail Version
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 31f57519aa55a06256d2b31cc64d4a964d889555
ms.contentlocale: lv-lv
ms.lasthandoff: 05/25/2017


---

# <a name="track-commissions-in-pos-using-sales-groups"></a>POS komisijas maksu izsekošana, izmantojot pārdošanas grupas

[!include[banner](includes/banner.md)]


Mazumtirdzniecībā bieži lietota prakse ir pārdošanas darbību izsekošana pēc darbinieka, kurš strādā ar debitoru, sniedzot palīdzību, veicot papildu pārdošanu un šķērspārdošanu un apstrādājot transakciju.

Pārdošanas darbību izsekošana pēc tirdzniecības pārstāvja ir darbinieka pārdošanas spēju mērs, bet pārdošanas darbību izsekošana pēc kasiera ir ātruma un efektivitātes mērs. Pārdošanas darbību izsekošana pēc tirdzniecības pārstāvja bieži vien tiek izmantota komisijas maksu vai citu prēmiju aprēķinam.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Nodarbinātā konfigurēšana POS kā tirdzniecības pārstāvi
Kad nodarbinātais tiek pievienots pārdošanas grupai, viņš kļūst piemērots komisijas maksas saņemšanai un viņu sistēmā var norādīt kā tirdzniecības pārstāvi. Nodarbinātais, kurš nav ietverts pārdošanas grupā, nav piemērots komisijas maksu saņemšanai un pārdošanas punkta (POS) lietojumprogrammā nav norādīts kā tirdzniecības pārstāvis. POS tirdzniecības pārstāvju saraksts tiek veidots, izmantojot visas pārdošanas grupas, kurās ir vismaz viens nodarbinātais, kurš ir piešķirts konkrētajam veikalam. Saraksts POS tiek rādīts pārdošanas grupas ID un nosaukuma (ID: nosaukums) kombinācijas formātā. Nodarbinātajiem var piešķirt noklusējuma pārdošanas grupu, lai nodrošinātu scenārijus, kuros mazumtirgotājs izvēlas automātiski iestatīt tirdzniecības pārstāvi POS rindās. Lietotāji var izvēlēties nodarbināt no jebkuras pārdošanas grupas, kurā viņš ir ietverts.

## <a name="functionality-profile-settings"></a>Funkcionalitātes profila iestatījumi
Ir pieejami vairāki veikala funkcionalitātes profila iestatījumi, kas nosaka POS plūsmu un procesus, kuri ir saistīti ar tirdzniecības pārstāvjiem.

|                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Profils**                           | **Apraksts**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Pēc noklusējuma: kasierim, ja pieejams** | Ja ir atlasīta šī opcija, POS transakciju rindas tiek automātiski aizpildītas ar pašreizējā kasiera noklusējuma pārdošanas grupas datiem. Ja kasierim nav norādīta noklusējuma pārdošanas grupa, vērtība netiek iestatīta. Lietotājs joprojām var manuāli iestatīt pārdošanas grupu, izmantojot POS pogu režģa pogu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Rādīt tirdzniecības pārstāvja uzvedni**   | Šai opcijai ir pieejamas trīs vērtības. **Nē** — ja ir atlasīta šī opcija, lietotājam netiek parādīta uzvedne ar aicinājumu atlasīt pārdošanas grupu. Vērtību joprojām var iestatīt, izmantojot kasiera noklusējuma pārdošanas grupu, vai arī to var iestatīt manuāli, izmantojot POS pogu režģa pogu. **Transakcijas sākums** — ja ir atlasīta šī opcija un nav iespējota opcija **Pēc noklusējuma: kasierim, ja pieejams** vai pašreizējam kasierim nav norādīta noklusējuma pārdošanas grupa, lietotajam katras transakcijas sākumā tiek parādīta uzvedne ar aicinājumu atlasīt pārdošanas grupu. Šajā uzvednē atlasītā pārdošanas grupa tiek iestatīta kā visu nākamo pārdošanas rindu noklusējuma pārdošanas grupa. Lietotājs joprojām var manuāli iestatīt pārdošanas grupu, izmantojot POS pogu režģa pogu. **Visām rindām** — ja ir atlasīta šī opcija un nav iespējota opcija **Pēc noklusējuma: kasierim, ja pieejams** vai pašreizējam kasierim nav norādīta noklusējuma pārdošanas grupa, lietotajam pēc katras rindas pievienošanas tiek parādīta uzvedne ar aicinājumu atlasīt pārdošanas grupu. Lietotājs joprojām var manuāli iestatīt pārdošanas grupu, izmantojot POS pogu režģa pogu. |
| **Nepieciešams**                           | Šī opcija tiek lietota tikai tas, ja POS ir konfigurēts tirdzniecības pārstāvja uzvednes rādīšanai. Ja tā ir iespējota, lietotājam pirms turpināšanas obligāti ir jāizvēlas pārdošanas grupa. Pretējā gadījumā lietotājam tiek parādīta uzvedne, taču viņš var atcelt un turpināt, neveicot atlasi. Pēc rindas pievienošanas lietotājs, kuram ir pietiekamas atļaujas, joprojām var noņemt no rindas pārdošanas grupu. Šādā gadījumā netiek piespiedu kārtā lietots iestatījums Nepieciešams tirdzniecības pārstāvis.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Tirdzniecības pārstāvja informācijas rādīšana POS transakciju ekrānā
POS transakciju ekrāna izkārtojumu un saturu var konfigurēt, izmantojot ekrāna izkārtojuma dizaineru un veikaliem, kases sistēmām vai nodarbinātajiem piešķirtos ekrāna izkārtojumus. Rūts Kvīts cilnē Rindas var pievienot lauku **Tirdzniecības pārstāvis**.  Tādējādi transakciju ekrānā tiek rādīts katrai rindai norādītās pārdošanas grupas ID.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Tirdzniecības pārstāvja operāciju pievienošana POS pogu režģiem
POS sniedz lietotājiem iespēju konfigurēt pogu režģus, kas tiek ietverti ekrāna izkārtojumos, lai nodrošinātu piekļuvi POS operācijām. Pogu režģa pogām var piešķirt tālāk norādītās ar tirdzniecības pārstāvjiem saistītās POS operācijas.

|                                           |                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Operācija**                             | **Apraksts**                                                                                                                                                                                                                                                                              |
| Iestatīt rindas pārdošanas pārstāvi          | Izmantojot šo POS operāciju, tiek parādīts veikalam pieejamo pārdošanas grupu saraksts (ID: nosaukums). Atlasot pārdošanas grupu šajā sarakstā, tiek iestatīta vērtība pašreizējā transakcijas rindā.                                                                                                            |
| Notīrīt rindā norādīto tirdzniecības pārstāvi        | Izmantojot šo POS operāciju, var noņemt pašreizējo pārdošanas grupas vērtību no pašreizējās transakcijas rindas.                                                                                                                                                                                                  |
| Iestatīt transakcijas tirdzniecības pārstāvi   | Izmantojot šo POS operāciju, tiek parādīts veikalam pieejamo pārdošanas grupu saraksts (ID: nosaukums). Atlasot pārdošanas grupu šajā sarakstā, tiek iestatīta pašreizējās transakcijas noklusējuma vērtība. Tiek iestatītas visas esošās rindas, kam nav piešķirta pārdošanas grupa, kā arī visas vēlāk pievienotās rindas. |
| Noņemt transakcijas pārdošanas pārstāvi | Izmantojot šo POS operāciju, tiek noņemta pašreizējās transakcijas pašreizējā noklusējuma pārdošanas grupas vērtība. Tas neietekmē nevienu jau esošo transakcijas rindu.                                                                                                                             |

## <a name="calculating-commissions"></a>Komisijas maksu aprēķins
Norādītajā pārdošanas grupā ietverto darbinieku komisijas maksa tiek aprēķināta izraksta vai pārdošanas pasūtījuma grāmatošanas laikā. Komisijas maksas summa tiek noteikta, pamatojoties uz nodarbinātā komisijas daļu, kas ir definēta pārdošanas grupai, ar to saistītajiem debitora komisijas maksas aprēķina iestatījumiem un/vai transakcijā ietvertajām precēm.





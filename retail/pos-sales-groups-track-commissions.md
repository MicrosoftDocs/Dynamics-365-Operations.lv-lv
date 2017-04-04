---
title: "Komisijas pārdošanas grupām, izmantojot POS izsekot"
description: "Tas ir kopējā mazumtirdzniecības prakse, lai izsekotu pārdošanas asociētajā uzņēmumā, kurš strādā ar klientu, — sniedzot palīdzību augšuppār-došanu, šķērspārdošanu un izskatī anas termiņu darījumu."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: dfefdede8f3bc884b230109d6c915127a1361ecd
ms.lasthandoff: 03/31/2017


---

# <a name="track-commissions-in-pos-using-sales-groups"></a>Komisijas pārdošanas grupām, izmantojot POS izsekot

Tas ir kopējā mazumtirdzniecības prakse, lai izsekotu pārdošanas asociētajā uzņēmumā, kurš strādā ar klientu, — sniedzot palīdzību augšuppār-došanu, šķērspārdošanu un izskatī anas termiņu darījumu.

Izsekošanai pārdošanas, pārdošanas pārstāvis ir sabiedroto spējas pārdot pasākums, kamēr pārdošanas, kasieris ir pasākums, ātrumu un efektivitāti. Pārdošanas, izsekoti pārdošanas pārstāvis arī bieži tiek izmantotas, lai aprēķinātu komisijas naudu vai citus stimulus.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Darbinieks ir pārdošanas pārstāvis, POS konfigurēšana
Ja darba ņēmējs tiek pievienota pārdošanas grupai, tie kļūst pretendēt uz Komisiju un var kvalificēt kā tirdzniecības pārstāvis sistēmā. Darba ņēmējs, kurš nav pārdošanas grupā nav pretendēt uz Komisiju un nav uzskaitīti kā tirdzniecības pārstāvis, sale (POS) piemērošanas punktā. POS, tirdzniecības pārstāvju saraksts iegūst visas pārdošanas grupas, kurās ir vismaz viens darbinieks, kas piešķirts uz veikalu. Saraksts tiek rādīts kā pārdošanas grupas kods un nosaukums, apvienojot POS (ID: vārds). Noklusējuma pārdošanas grupai var piešķirt darba ņēmēju atbalstam, ja mazumtirgotājs izvēlas automātiski uzstādīt POS rindās tirdzniecības pārstāvi scenārijiem. Lietotāji var izvēlēties no pārdošanas grupai, ka darba ņēmējs ir biedrs.

## <a name="functionality-profile-settings"></a>Funkcionalitātes profila iestatījumus
Ir vairāki funkcionalitātes profila iestatījumus veikalu, kas noteiks plūsmu un procesu POS, kas ietver pārdošanas pārstāvjiem.

|                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Profile**                           | **Description**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Default to cashier when available** | Ja šī opcija ir iespējota, POS automātiski aizpildīt darbības rindas ar pašreizējo kasiera noklusējuma pārdošanas grupu. Ja kase nav norādīts noklusētais pārdošanas grupa, vērtība nav iestatīta. Lietotājs varētu joprojām manuāli iestatīt pārdošanas grupas, izmantojot POS režģa poga.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Prompt for sales representative**   | Šim variantam ir trīs iespējamās vērtības: * * Nr * *-ja ir atlasīta šī opcija, lietotājam netiks piedāvāts atlasīt pārdošanas grupu. Vērtību, izmantojot kasiera noklusējuma pārdošanas grupa joprojām jānosaka vai manuāli, izmantojot POS pogu režģa pogu. **Darbības sākumu** – ja ir atlasīta šī opcija, un vai nu **, noklusētā kase** opcija nav iespējota vai pašreizējā kase nav noklusējuma pārdošanas grupai, lietotājam tiks pieprasīts atlasīt pārdošanas grupu sākumā katra darījuma. Pārdošanas grupas atlasi no šīs uzvednes noklusētā visām turpmākajām rindām pārdošanas grupas dalībniekus. Lietotājs varētu joprojām manuāli iestatīt pārdošanas grupas, izmantojot POS režģa poga. **Katrai rindai** – ja ir atlasīta šī opcija, un vai nu **, noklusētā kase** opcija nav iespējota vai pašreizējā kase nav noklusējuma pārdošanas grupai, lietotājam tiks pieprasīts atlasīt pārdošanas grupa pēc pievienošanas katrai rindai. Lietotājs varētu joprojām manuāli iestatīt pārdošanas grupas, izmantojot POS režģa poga. |
| **Nepieciešama**                           | Šī iespēja ir piemērojama, kad POS ir konfigurēta, lai prasītu tirdzniecības pārstāvi. Ja aktivizēta, lietotājam būs nepieciešams izvēlēties pārdošanas grupu, pirms turpināt. Pretējā gadījumā lietotājs tiks piedāvāts, bet var atcelt un turpināt neizdarot izvēli. Pēc tam, kad ir pievienota līnijai, lietotājs ar pietiekamām atļaujām joprojām varētu noņemt pārdošanas grupu no līnijas. Šajā situācijā nav izpildīts "Prasa pārdošanas pārstāvim".                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Ražotāju organizāciju darbības ekrānā parādīt pārdošanas pārstāvja informācija
POS darījumu ekrāna izkārtojumu un saturu var konfigurēt, izmantojot ekrāna izkārtojuma dizainers un piešķirtie ekrāna izkārtojumus, veikali, reģistri vai darbinieku. **Pārdošanas pārstāvis** lauku var pievienot cilnes rindas saņemšanas rūts.  Tas parādīsies ekrānā ID norādīto pārdošanas grupu katrai rindai darbību.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Pievienot pārdošanas pārstāvja darbību POS pogu režģi
POS ļauj lietotājiem konfigurēt poga elektrotīkliem, kas iekļauti ekrāna izkārtojumu, lai nodrošinātu piekļuvi POS operāciju. POS šādas darbības var tikt piešķirtas pogu režģa pogas, kas attiecas uz pārdošanas pārstāvjiem.

|                                           |                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Operācija**                             | **Description**                                                                                                                                                                                                                                                                              |
| Iestatīt rindas pārdošanas pārstāvi          | Šo POS operāciju parāda sarakstu ar atbilstīgo pārdošanas grupās (ID: vārds) veikalā. No šajā sarakstā atlasot pārdošanas grupu noteiks vērtību pašreizējā darbības rindā.                                                                                                            |
| Notīrīt rindā norādīto tirdzniecības pārstāvi        | Šo POS operāciju noņem pašreizējo pārdošanas grupai vērtību pašreizējai darbības rindai.                                                                                                                                                                                                  |
| Iestatīt tirdzniecības pārstāvi darbībai   | Šo POS operāciju parāda sarakstu ar atbilstīgo pārdošanas grupās (ID: vārds) veikalā. No šajā sarakstā atlasot pārdošanas grupu noteiks noklusējuma vērtību pašreizējai darbībai. Jebkuras esošās līnijas bez pārdošanas grupas, kam piešķirts būs kopā, kā arī tam pievienotās rindas. |
| Skaidri tirdzniecības pārstāvi darbībai | Šo POS operāciju noņem pašreizējo noklusējuma pārdošanas grupai vērtību pašreizējai darbībai. Tas neietekmē jau esošo darbību rindas.                                                                                                                             |

## <a name="calculating-commissions"></a>Komisijas aprēķināšanā
Komisija aprēķina noteiktā pārdošanas grupās strādājošo paziņojumu grāmatošanai vai pārdošanas pasūtījuma grāmatošanas laikā. Komisijas summa ir noteikta, pamatojoties uz darba ņēmēja Komisijas daļa, kā noteikts pārdošanas grupas un klientu un/vai produktu darbību saistītās Komisijas aprēķina iestatījumus.



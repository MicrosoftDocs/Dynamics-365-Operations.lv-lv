---
title: "Fiziskie un finanšu atjauninājumi"
description: "Šajā tēmā ir sniegts pārskats par to, kāda veida darbības palielina vai samazina krājumu daudzumu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d68006c756f6b29804cad1d05db9ced2bd33897d
ms.lasthandoff: 03/31/2017


---

# <a name="physical-and-financial-updates"></a>Fiziskie un finanšu atjauninājumi

Šajā tēmā ir sniegts pārskats par to, kāda veida darbības palielina vai samazina krājumu daudzumu. 

Krājumu darbības var fiziski atjaunināts un finansiāli atjaunināts programmā Microsoft Dynamics 365 operācijām. Dažu tipu fiziskās un finanšu transakcijas palielina daudzumu, bet citas daudzumu samazina.

## <a name="physical-increases"></a>Fizisks palielinājums
Kad fiziska transakcija tiek iegrāmatota, transakcijas ieraksta statuss ir **Saņemts**. Turpmāk minētās transakcijas tiek uzskatītas par fizisku palielinājumu:

-   Pirkšanas pasūtījuma ieejas plūsma
-   Pārdošanas pasūtījuma pavadzīmes atgriešana
-   Ražošanas pasūtījuma atzīmēšana kā pabeigta
-   Blakusprodukts ražošanas pasūtījuma izdošanas sarakstā

## <a name="financial-increases"></a>Finansiāls palielinājums
Kad finansiālas ieejas plūsmas transakcija tiek iegrāmatota, transakcijas ieraksta, kas palielina daudzumu, statuss ir **Nopirkts**. Turpmāk minētās transakcijas tiek uzskatītas par finansiālu palielinājumu:

-   Kreditora rēķins
-   Pārdošanas pasūtījuma rēķins par atgriešanu
-   Ražošanas pasūtījuma izmaksu aprēķināšana
-   Pozitīva daudzuma krājumu žurnāli, tādi kā pārvietošana, pelņa un zaudējumi, uzskaite, materiālu komplekti un pārsūtīšana

## <a name="transactions-that-increase-quantity"></a>Darbības, kas palielina daudzumu
Darbības, kas palielina daudzumu, tiek grāmatotas, norādot kārtējo vidējo pašizmaksu. Dinamika 365 operācijām aprēķina darbojas vidējās izmaksu cenas, kuras pamatā ir izmaksas par katru no šiem darījumiem katrai krājuma dimensijai, kas finansiāli tiek uzskaitīta. Informāciju par kārtējo vidējo pašizmaksu skatiet [Kārtējā vidējā pašizmaksa](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Darbības, kas samazina daudzumu
Dinamika 365 operācijām izmanto darbojas vidējā aprēķinātā izmaksu cena, grāmatojot transakciju, kuras samazina daudzumu, neatkarīgi no krājumu modelim, kas ir saistīts ar šo krājumu. Ir nepieciešams, lai transakcija, kas samazina daudzumu, pirms grāmatošanas nebūtu iepriekš atzīmēta citai transakcijai. Ja fiziskais rīcībā esošie krājumi kļūst negatīvs, Dynamics 365 operācijām izmanto preču pašizmaksu, kas definēta krājumam par **preces** lapā. **Piezīme:** ja ir iespējota vairākvietu funkcionalitāte, šīs izmaksas būs krājumu izmaksas, kas definētas vietai lapā **Pasūtījuma noklusējuma iestatījumi**.

## <a name="physical-issues-vs-financial-issues"></a>Fiziska izdošana un finansiāla izdošana
Kad fiziskas izejas plūsmas transakcija tiek iegrāmatota, transakcijas ieraksta statuss ir **Atskaitīts**. Turpmāk minētās transakcijas tiek uzskatītas par fiziskām izejas plūsmām:

-   Ražošanas pasūtījuma izdošanas saraksta žurnāls
-   Pārdošanas pasūtījuma pavadzīme
-   Pirkšanas pasūtījuma pavadzīmes atgriešana

Kad finansiāla transakcija tiek iegrāmatota, transakcijas ieraksta statuss ir **Pārdots**. Turpmāk minētās transakcijas tiek uzskatītas par finansiālām izejas plūsmām:

-   Ražošanas pasūtījuma pabeigšana
-   Pārdošanas pasūtījuma rēķins
-   Kreditora rēķina atgriešana
-   Negatīva daudzuma krājumu žurnāli, tādi kā pārvietošana, pelņa un zaudējumi, uzskaite, materiālu komplekti un pārsūtīšana

Darbības, kas samazina daudzumu, tiek grāmatotas, norādot pašreizējo vidējo pašizmaksu. Līdz ar to, lai izdošanas transakcijas segtu ar saņemšanas darbībām, pamatojoties uz katram krājumam piešķirto krājumu modeli, ir nepieciešama krājumu slēgšanas procedūra.



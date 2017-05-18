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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 1d20faab03a46e39077890a19ce16f6324982a29
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="physical-and-financial-updates"></a>Fiziskie un finanšu atjauninājumi

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegts pārskats par to, kāda veida darbības palielina vai samazina krājumu daudzumu. 

Krājumu transakcijas programmatūrā Microsoft Dynamics 365 for Operations var atjaunināt gan fiziski, gan finansiāli. Dažu tipu fiziskās un finanšu transakcijas palielina daudzumu, bet citas daudzumu samazina.

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
Darbības, kas palielina daudzumu, tiek grāmatotas, norādot kārtējo vidējo pašizmaksu. Programmatūrā Dynamics 365 for Operations tiek aprēķināta kārtējā vidējā pašizmaksa, pamatojoties uz katras transakcijas izmaksām par katru krājuma dimensiju, kas tiek finansiāli izsekota. Informāciju par kārtējo vidējo pašizmaksu skatiet [Kārtējā vidējā pašizmaksa](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Darbības, kas samazina daudzumu
Neatkarīgi no tā, kurš krājumu modelis ir saistīts ar attiecīgo krājumu, programmatūrā Dynamics 365 for Operations grāmatojot darbību, kas samazina daudzumu, tiek izmantota aprēķinātā kārtējā vidējā pašizmaksa. Ir nepieciešams, lai transakcija, kas samazina daudzumu, pirms grāmatošanas nebūtu iepriekš atzīmēta citai transakcijai. Ja fizisko rīcībā esošo krājumu daudzums kļūst negatīvs, programmatūrā Dynamics 365 for Operations tiek izmantotas krājuma izmaksas, kas šim krājumam ir definētas lapā **Krājums**. **Piezīme:** ja ir iespējota vairākvietu funkcionalitāte, šīs izmaksas būs krājumu izmaksas, kas definētas vietai lapā **Pasūtījuma noklusējuma iestatījumi**.

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





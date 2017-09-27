---
title: "Fiziskie un finanšu atjauninājumi"
description: "Šajā tēmā ir sniegts pārskats par to, kāda veida darbības palielina vai samazina krājumu daudzumu."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: a0eeb5a57f9b82150150752c64e89c2c91856889
ms.contentlocale: lv-lv
ms.lasthandoff: 06/13/2017

---

# <a name="physical-and-financial-updates"></a>Fiziskie un finanšu atjauninājumi

[!include[banner](../includes/banner.md)]


Šajā tēmā ir sniegts pārskats par to, kāda veida darbības palielina vai samazina krājumu daudzumu. 

Krājumu transakcijas programmatūrā Microsoft Dynamics 365 for Finance and Operations var atjaunināt gan fiziski, gan finansiāli. Dažu tipu fiziskās un finanšu transakcijas palielina daudzumu, bet citas daudzumu samazina.

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
Darbības, kas palielina daudzumu, tiek grāmatotas, norādot kārtējo vidējo pašizmaksu. Programmatūrā Finance and Operations tiek aprēķināta kārtējā vidējā pašizmaksa, pamatojoties uz katras transakcijas izmaksām par katru krājuma dimensiju, kas tiek finansiāli izsekota. Informāciju par kārtējo vidējo pašizmaksu skatiet [Kārtējā vidējā pašizmaksa](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Darbības, kas samazina daudzumu
Neatkarīgi no tā, kurš krājumu modelis ir saistīts ar attiecīgo krājumu, programmatūrā Finance and Operations grāmatojot transakciju, kas samazina daudzumu, tiek izmantota aprēķinātā kārtējā vidējā pašizmaksa. Ir nepieciešams, lai transakcija, kas samazina daudzumu, pirms grāmatošanas nebūtu iepriekš atzīmēta citai transakcijai. Ja fizisko rīcībā esošo krājumu daudzums kļūst negatīvs, programmatūrā Finance and Operations tiek izmantotas krājuma izmaksas, kas šim krājumam ir definētas lapā **Krājums**. **Piezīme:** ja ir iespējota vairākvietu funkcionalitāte, šīs izmaksas būs krājumu izmaksas, kas definētas vietai lapā **Pasūtījuma noklusējuma iestatījumi**.

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




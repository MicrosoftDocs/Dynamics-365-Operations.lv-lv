---
title: Fiziskie un finanšu atjauninājumi
description: Šajā tēmā ir sniegts pārskats par to, kāda veida darbības palielina vai samazina krājumu daudzumu.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88432b9a5e564f9e81892e0bb379f95ff40d6c9d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842157"
---
# <a name="physical-and-financial-updates"></a>Fiziskie un finanšu atjauninājumi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir sniegts pārskats par to, kāda veida darbības palielina vai samazina krājumu daudzumu. 

Programmā Dynamics 365 Supply Chain Management var fiziski un finansiāli atjaunināt krājumu transakcijas. Dažu tipu fiziskās un finanšu transakcijas palielina daudzumu, bet citas daudzumu samazina.

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
Darbības, kas palielina daudzumu, tiek grāmatotas, norādot kārtējo vidējo pašizmaksu. Aprēķinātā kārtējā vidējā pašizmaksa ir pamatota uz katras transakcijas maksu par katru krājuma dimensiju, kas tiek finansiāli izsekota. Informāciju par kārtējo vidējo pašizmaksu skatiet [Kārtējā vidējā pašizmaksa](running-average-cost-price.md).

## <a name="transactions-that-decrease-quantity"></a>Darbības, kas samazina daudzumu
Neatkarīgi no tā, kurš krājumu modelis ir saistīts ar attiecīgo krājumu, aprēķinātā kārtējā vidējā pašizmaksa tiek izmantota, grāmatojot darbību, kas samazina daudzumu. Ir nepieciešams, lai transakcija, kas samazina daudzumu, pirms grāmatošanas nebūtu iepriekš atzīmēta citai transakcijai. Ja fiziski rīcībā esošo krājumu daudzums kļūst par negatīvu skaitli, tiek izmantotas krājumu izmaksas, kas definētas krājumam formā **Krājums**. 

> [!NOTE]
> Ja ir iespējota vairākvietu funkcionalitāte, šīs izmaksas būs krājumu izmaksas, kas definētas vietai lapā **Pasūtījuma noklusējuma iestatījumi**.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Kvalitātes pārvaldības krājumu paraugu ņemšana
description: Šajā tēmā ir aprakstīts, kā iestatīt krājumu paraugu ņemšanu.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022232"
---
# <a name="quality-management-item-sampling"></a>Kvalitātes pārvaldības krājumu paraugu ņemšana

Krājumu paraugu ņemšana tiek izmantota kā daļa no kvalitātes saistības. Tas nosaka pašreizējā krājuma apjomu, kas jāpārbauda. Paraugu nodošana var būt balstīta uz fiksētiem daudzumiem, procentiem vai pilnu numura zīmi.

## <a name="set-up-item-sampling"></a>Krājuma paraugu izveides iestatīšana

Lai iestatītu krājuma paraugu ņemšanu, rīkojieties šādi.

1. Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Kvalitātes kontrole \> Krājumu iztveršana**.
1. Atlasiet **Jauns**.
1. Ievadiet vērtību laukā **Krājumu paraugu ņemšana**.
1. Laukā **Apraksts** ievadiet kādu vērtību.
1. Ievadiet skaitli laukā **Vērtība**. Šī vērtība attiecas uz daudzuma specifikācijas vērtību, kas atlasīta blakus esošajā laukā.
1. Sadaļā **Process** atzīmējiet izvēles rūtiņu **Pilna bloķēšana**, ja testa kļūmes gadījumā ir jābloķē viss partijas vai pasūtījuma rindas daudzums. Ja šī izvēles rūtiņa ir notīrīta, tikai krājumi kvalitātes pasūtījumā tiks bloķēti, ja tests nav izdevies.
1. Atlasiet **Saglabāt**.
1. Aizvērt lapu.

> [!NOTE]
> Funkcija *Kvalitātes pārvaldība noliktavas procesiem* nodrošina papildu krājumu paraugu ņemšanas iespējas. Tas pievieno *preču paraugu ņemšanas tvēruma* koncepciju un ļauj noteikt pilnu numura zīmi kā daudzuma specifikāciju. Ja esat ieslēdzis šo līdzekli, tad skatiet sadaļu [Kvalitātes pārvaldība noliktavas procesiem](quality-management-for-warehouses-processes.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

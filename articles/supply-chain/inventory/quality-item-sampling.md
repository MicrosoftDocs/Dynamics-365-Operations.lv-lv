---
title: Kvalitātes pārvaldības krājumu paraugu ņemšana
description: Šajā tēmā ir aprakstīts, kā iestatīt krājumu paraugu ņemšanu.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ea749c470ab1d80f1f3974596a2cd4a1f5b7b32d
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578492"
---
# <a name="quality-management-item-sampling"></a>Kvalitātes pārvaldības krājumu paraugu ņemšana

[!include [banner](../includes/banner.md)]

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

---
title: Logotipa pievienošana
description: Šajā tēmā aprakstīts, kā pievienot logotipu vietnei risinājumā Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d9e1cba6bd07e0c3d9ed7d741d87e10837d8021c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797603"
---
# <a name="add-a-logo"></a>Logotipa pievienošana

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā pievienot logotipu vietnei risinājumā Microsoft Dynamics 365 Commerce.

Veidojot vietni, viena no pirmajām lietām, ko jūs, iespējams, darīsiet, ir vietnes galvenē pievienosiet sava uzņēmuma vai zīmola logotipu. Tiešsaistes moduļu bibliotēka Dynamics 365 Commerce nodrošina moduli, kas atvieglo šo uzdevumu.

Logotipu var pievienot tieši veidnei, izkārtojumam vai lapai. Tādā veidā jūs varat viegli nomainīt logotipu, kas parādās konkrētās lapās vai lapu grupās. Tomēr šī tēma attiecas uz visbiežāk sastopamo scenāriju, kur jūs pievienojat savu logotipu galvenes fragmentam, ko var atkārtoti izmantot visās vietnes lapās.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu pievienot logotipu visām vietnes lapām, jums ir jāizpilda tālāk aprakstītie uzdevumi.

1. Savs logotipa augšupielāde multivides bibliotēkā.
1. izveidojiet galvenes fragmentu. Vairāk informācijas par fragmentu izveidi un izmantošanu skatiet sadaļā [Darbs ar fragmentiem](work-with-fragments.md).
1. Iekļaujiet veidnē galvenes fragmentu, kuru jūsu vietnes lapas izmanto izkārtojumu un moduļu opcijām. Vairāk informācijas par veidnēm skatiet sadaļā [Darbs ar veidnēm](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Logotipa pievienošana galvenes fragmentam

Lai pievienotu logotipu vietnes galvenes fragmentam, veiciet tālāk norādītās darbības.

1. Navigācijas rūtī kreisajā pusē atlasiet **Fragmenti**.
1. Atlasiet iepriekš izveidoto galvenes fragmentu un pēc tam izvēlieties **Rediģēt**.
1. Paplašiniet galvenes moduli.
1. Galvenes moduļa rekvizītu rūtī ir jānorāda logotipa attēls un saite. 
1. Saglabājiet galvenes fragmentu, pabeidziet to rediģēt un publicējiet to.

Pēc atjauninātā galvenes fragmenta publicēšanas visās vietņu lapās, kurās tiek izmantota veidne, kurā ir galvenes fragments, tiks parādīts jūsu logotips.

## <a name="additional-resources"></a>Papildu resursi

[Vietnes dizaina atlase](select-site-theme.md)

[Darbs ar CSS ignorēšanas failiem](css-override-files.md)

[Izlases ikonas pievienošana](add-favicon.md)

[Sveiciena ziņojuma pievienošana](add-welcome-message.md)

[Autortiesību paziņojuma pievienošana](add-copyright-notice.md)

[Valodu pievienošana vietnei](add-languages-to-site.md)

[Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

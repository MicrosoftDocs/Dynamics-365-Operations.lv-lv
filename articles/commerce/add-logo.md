---
title: Logotipa pievienošana
description: Šajā tēmā ir aprakstīts, kā pievienot logotipu savai vietnei programmā Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 5fc0673dcdcc8b761089be2c2d201c8488128865
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025713"
---
# <a name="add-a-logo"></a>Logotipa pievienošana


[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīts, kā pievienot logotipu savai vietnei programmā Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Pārskats

Veidojot vietni, viena no pirmajām lietām, ko jūs, iespējams, darīsiet, ir vietnes galvenē pievienosiet sava uzņēmuma vai zīmola logotipu. Dynamics 365 Commerce tiešsaistes sākuma komplekts nodrošina moduli, kas padara šo uzdevumu vieglu.

Logotipu var pievienot tieši veidnei, izkārtojumam vai lapai. Tādā veidā jūs varat viegli nomainīt logotipu, kas parādās konkrētās lapās vai lapu grupās. Tomēr šī tēma attiecas uz visbiežāk sastopamo scenāriju, kur jūs pievienojat savu logotipu galvenes fragmentam, ko var atkārtoti izmantot visās vietnes lapās.

## <a name="prerequisites"></a>Priekšnosacījumi

Lai varētu pievienot logotipu visām vietnes lapām, jums ir jāizpilda tālāk aprakstītie uzdevumi.

1. Savs logotipa augšupielāde multivides bibliotēkā.
1. izveidojiet galvenes fragmentu. Vairāk informācijas par fragmentu izveidi un izmantošanu skatiet sadaļā [Darbs ar fragmentiem](work-with-fragments.md).
1. Iekļaujiet veidnē galvenes fragmentu, kuru jūsu vietnes lapas izmanto izkārtojumu un moduļu opcijām. Vairāk informācijas par veidnēm skatiet sadaļā [Darbs ar veidnēm](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Logotipa pievienošana galvenes fragmentam

Lai pievienotu logotipu vietnes galvenes fragmentam, veiciet tālāk norādītās darbības.

1. Navigācijas rūtī kreisajā pusē atlasiet **Lapas fragments**.
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


---
title: Logotipa pievienošana
description: Šajā rakstā ir aprakstīts, kā pievienot logotipu jūsu vietnei Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 4bd47907791edfd0ab81282bd1e465ac54172cdf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278102"
---
# <a name="add-a-logo"></a>Logotipa pievienošana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā pievienot logotipu jūsu vietnei Microsoft Dynamics 365 Commerce.

Veidojot vietni, viena no pirmajām lietām, ko jūs, iespējams, darīsiet, ir vietnes galvenē pievienosiet sava uzņēmuma vai zīmola logotipu. Tiešsaistes moduļu bibliotēka Dynamics 365 Commerce nodrošina moduli, kas atvieglo šo uzdevumu.

Logotipu var pievienot tieši veidnei, izkārtojumam vai lapai. Tādā veidā jūs varat viegli nomainīt logotipu, kas parādās konkrētās lapās vai lapu grupās. Tomēr šajā rakstā ir apskatīts visbiežāk izmantotais scenārijs, kurā jūs pievienojat savu logotipu virsraksta fragmentam, ko var atkārtoti izmantot visās jūsu vietnes lapās.

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

[Autortiesību paziņojuma pievienošana](add-copyright-notice.md)

[Valodu pievienošana vietnei](add-languages-to-site.md)

[Skripta koda pievienošana vietnes lapām, lai atbalstītu telemetriju](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Līdzekļu skaitītāju automātiska atjaunināšana
description: Šajā tēmā aprakstīta automātiska līdzekļu skaitītāju atjaunināšana programmā Asset Management.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9a3814a575fbe4379b59723f269d83379a253ede71962c0c82b5f4cc55d36e6c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6738299"
---
# <a name="automatic-update-of-asset-counters"></a>Pamatlīdzekļu skaitītāju automātiska atjaunināšana

[!include [banner](../../includes/banner.md)]

Papildinformāciju par līdzekļu skaitītāju manuālu reģistrāciju skatiet tēmā [Līdzekļu skaitītāju manuāla atjaunināšana](../work-orders/manual-update-of-asset-counters.md). Informāciju par to, kā iestatīt līdzekļu skaitītājus, skatiet tēmā [Skaitītāji](../setup-for-objects/counters.md).

Skaitītāju vērtības var arī automātiski atjaunināt no produktu reģistrācijas, balstoties uz ražošanas stundām vai ražoto daudzumu (proti, daudzumu, kas ir saražots). Šis atjauninājums tiek veikts lapā **Atjaunināt līdzekļu skaitītājus**. Var atjaunināt vienu vai vairākus līdzekļus, iestatot vienu parametru **Datums no**. Šis parametrs norāda ražošanas reģistrāciju sākuma datumu (ražošanas stundas vai ražošanas daudzumu). Citiem vārdiem sakot, tas norāda datumu, no kura ir jāatjaunina skaitītāja vērtības.

Visi līdzekļi, kas saistīti ar resursu *un* kam ir līdzekļu skaitītāji, kas iestatīti atjaunošanai, balstoties uz ražošanas stundām vai saražoto daudzumu, tiks iekļauti automātiskā atjauninājumā. Tiks izveidotas jaunas skaitītāja vērtības.

Skaitītājiem, kas balstās uz saražoto daudzumu, skaits ietver gan derīgo, gan brāķa daudzumu, kas ir reģistrēts. Ja saražotā daudzuma reģistrācijai lietotā vienība atšķiras no skaitītajā izmantotās vienības, daudzums tiek pārveidots, lai atbilstu skaitītāja vienībai.

Kā minēts iepriekš, automātisko skaitītāju vērtības var arī atjaunināt no produktu reģistrācijas. Tādēļ līdzeklim, kam vēlaties automātiski atjaunināt skaitītājus, jābūt saistītam ar resursu (mašīnu). Kad saražotie daudzumi vai ražošanas stundas reģistrētas resursam, varat atjaunināt saistītos līdzekļu skaitītājus.

1. Atlasiet **Līdzekļu pārvaldība** > **Periodiski** > **Līdzekļi** > **Līdzekļu skaitītāju atjaunināšana**.

2. Laukā **No datums** atlasiet automātiskā atjauninājuma sākuma datumu.

    >[!NOTE]
    >Datums šajā laukā ir "notiek darbs" datums no **Maršruta darījumi** (**Ražošanas kontrole** > **Pieprasījumi un atskaites** > **Ražošana** > **Maršruta darījumi** > **Fiziskais datums** laukā).

3. Kopsavilkuma cilnē **Iekļaujamie ieraksti** varat atlasīt konkrētus līdzekļus, līdzekļu veidus vai resursus automātiskai atjaunināšanai. Atlasiet **Filtrēt** un veiciet atbilstošās atlases.

4. Ātrajā cilnē **Palaist fonā** jūs varat pēc vajadzības uzstādīt automātisko atjauninājumu kā pakešuzdevumu.

    Attēlā zemāk ir parādīts dialoglodziņš **Atjaunināt līdzekļu skaitītājus**.

    ![1. attēls.](media/12-work-orders.png)

5. Atlasiet **Labi**. 

Pēc automātiskās līdzekļu skaitītāja atjaunināšanas varat apskatīt skaitītāja reģistrācijas, kas saistītas ar līdzekli lapā **Līdzekļu skaitītāji**. Atlasiet **Līdzekļu pārvaldība** > **Vispārīgi** > **Līdzekļi** > **Visi līdzekļi**, atlasiet līdzekli un pēc tam darbību rūts cilnas **Līdzeklis** grupā **Profilaktiski** atlasiet **Skaitītāji**.

Lapā **Līdzekļu apkopotā vērtība** ir pārskats par jaunāko reģistrāciju, kas veikta visiem skaitītāju veidiem visiem līdzekļiem. Atlasiet **Līdzekļu pārvaldība** > **Pieprasījumi** > **Līdzekļi** > **Līdzekļu apkopotā vērtība**. Šī lapa ir līdzīga lapai **Līdzekļu skaitītāji**, taču jūs nevarat pievienot vai rediģēt reģistrācijas. Tā ir tikai pārskatam.

Attēlā zemāk ir parādīta lapa **Līdzekļu apkopotā vērtība**.

![2. attēls.](media/13-work-orders.png)

Ņemiet vērā šādus punktus:

- Joprojām varat veidot manuālas skaitītāja vērtības reģistrācijas skaitītāju veidiem, kas tiek automātiski atjaunināti. Papildinformāciju skatiet sadaļā [Manuāla līdzekļu skaitītāju atjaunināšana](../work-orders/manual-update-of-asset-counters.md).

- Varat iestatīt skaitītājus, kas ir saistīti ar citu skaitītāju. Šādā gadījumā, atjauninot skaitītāju, vienlaikus automātiski tiek atjaunināti saistītie skaitītāji. Papildinformāciju par to, kā iestatīt saistītos skaitītājus, skatiet tēmā [Skaitītāji](../setup-for-objects/counters.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
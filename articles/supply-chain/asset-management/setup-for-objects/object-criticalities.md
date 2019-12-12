---
title: Līdzekļu kritiskuma veidi
description: Tēmā ir paskaidrot līdzekļu kritiskuma veidi Līdzekļu pārvaldībā.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f96fcc7ebb8928c6d6b17b30465ad1625d9b5be4
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2571074"
---
# <a name="asset-criticality-types"></a>Līdzekļu kritiskuma veidi

[!include [banner](../../includes/banner.md)]

 

Tēmā ir paskaidrot līdzekļu kritiskuma veidi Līdzekļu pārvaldībā. Līdzekļu kritiskums ir saistīts ar līdzekļiem un tiek pārsūtīts uz darba pasūtījumiem. Darba pasūtījumā to mainīt nevar. Līdzekļu kritiskumu izmanto, lai darba pasūtījumu ieplānošanas laikā aprēķinātu darba pasūtījuma kritiskumu. Citiem vārdiem sakot, tas tiek izmantots, lai aprēķinātu, cik lielā mērā līdzekļa uzturēšanas darbs ietekmē ražošanas grafiku un produktivitāti jūsu uzņēmumā. Plašāku informāciju par iestatījumiem, kas ir saistīti ar vērtējuma rezultātu aprēķināšanu darba pasūtījumu plānošanai, skatiet nodaļā [Līdzekļu pārvaldības parametri](../setup-for-objects/enterprise-asset-management-parameters.md).

Lai iestatītu kritiskumu, vispirms izveidojiet kritiskuma veidus, kas jāizmanto līdzekļa iestatīšanā. Pēc tam iestatiet līdzekļa kritiskās vērtības.

## <a name="set-up-criticality-types"></a>Kritiskuma veidu iestatīšana

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļi** \> **Kritiskuma veidi**.
2. Atlasiet **Jauns**, lai izveidotu ierakstu.
3. Laukā **Kritiskums** ievadiet skaitli, kas norāda kritiskumu.
4. Laukā **Nosaukums** ievadiet kritiskuma veida nosaukumu.
5. Laukā **Koeficients** ievadiet koeficientu. Šis koeficients tiek izmantots darba pasūtījuma plānošanas aprēķināšanas laikā, lai noteiktu, kādu kritiskuma ierakstu izmantot. (Vienmēr tiek izmantots ieraksts, kuram ir augstākais koeficients.) Šis iestatījums ir atbilstošs, ja, kā parādīts nākamajā attēlā, tiek veidotas kritiskuma rindas, kurām ir tāda pati kritiskuma vērtība.

    ![Kritiskuma veidu lapa](media/23-setup-for-objects.png)

## <a name="set-up-asset-criticalities"></a>Līdzekļa kritisko vērtību iestatīšana

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļa kritiskās vērtības**.
2. Atlasiet **Jauns**, lai izveidotu ierakstu.
3. Atkarībā no līdzekļu kritiskuma nepieciešamā detalizācijas līmeņa veiciet atbilstīgu atlasi laukos **Funkcionālais novietojums**, **Līdzekļa veids**, **Ražotājs**, **Modelis**, **Līdzeklis**, **Darba veida kategorija**, **Darba veids**, **Darba veida variants** un **Darba vajadzība**.

    > [!NOTE]
    > Kad līdzekļa kritiskums ir atlasīts, Līdzekļu pārvaldība iziet cauri visiem līdzekļu kritiskuma ierakstiem, lai pārbaudītu iespējamo atbilstību. Tā vienmēr vispirms pārbauda visraksturīgāko kombināciju. Citiem vārdiem sakot, Līdzekļu pārvaldība vispirms pārbauda **Darba vajadzība**. Ja atbilstība netiek atrasta, tā pārbauda **Darba veida variantu**. Ja atbilstība netiek atrasta, tā pārbauda **Darba veidu** un tā tālāk. Kā jūs varat redzēt lapas izkārtojumā, šī uzvedība nozīmē, ka, lai atrastu visspecifiskāko kombināciju, Līdzekļu pārvaldība atbilstības meklēšanai pārbauda katru ierakstu no labās puses uz kreiso. Ja atbilstība netiek atrasta, tiek izmantots "noklusējuma" ieraksts, kam nav atlases iespēju.

4. Laukā **Kritiskums** atlasiet vienu no kritiskuma vērtībām, kuru izveidojāt iepriekšējā procedūrā.

### <a name="notes-about-criticality-setup"></a>Piezīmes par kritiskuma iestatīšanu

- Ja maināt līdzekļa kritiskumu šajā iestatījumā pēc tam, kad esat to jau izmantojis darba pasūtījumā, kritiskums darba pasūtījumā netiek attiecīgi atjaunināts.
- Kritiskums darba pasūtījumā tiek pārrēķināts katru reizi, kad darba pasūtījuma rinda tiek pievienota vai dzēsta darba pasūtījumā.
- Ja darba pasūtījumā ir vairāki darba pasūtījuma darbi, darba pasūtījumā vienmēr tiek izmantots augstākais kritiskums saskaņā ar lauku **Koeficients** lapā **Kritiskuma veidi**.
- Parasti līdzekļu kritiskums laika posmā var mainīties. Kritiskumu var ietekmēt jaunu iekārtu iegāde, atjaunošana un tā tālāk. Apsveriet iespēju regulāri no jauna izvērtēt savu līdzekļu kritiskās vērtības (piemēram, reizi gadā vai katru otro gadu), lai nodrošinātu, ka jūsu kritiskuma definīcijas atbilst aktuālajiem ražošanas iestatījumiem.
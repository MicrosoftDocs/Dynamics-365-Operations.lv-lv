---
title: Līdzekļu pakalpojumu līmeņi
description: Šajā tēmā ir paskaidroti līdzekļu pakalpojumu līmeņi Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 83b195add44927d847491e6394e72637323117b3
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021633"
---
# <a name="asset-service-levels"></a>Līdzekļu pakalpojumu līmeņi

[!include [banner](../../includes/banner.md)]

 

Šajā tēmā ir paskaidroti līdzekļu pakalpojumu līmeņi Līdzekļu pārvaldībā. Līdzekļu pakalpojumu līmeņi ir saistīti ar līdzekļiem, un tiek pārsūtīti uz uzturēšanas pieprasījumiem un darba pasūtījumiem. Tos izmanto, lai darba pasūtījumu plānošanas laikā aprēķinātu darba uzdevumu prioritāti. Līdzekļu pakalpojumu līmeni var mainīt, ja ir nepieciešamas izmaiņas.

Plašāku informāciju par iestatījumiem, kas ir saistīti ar vērtējuma rezultātu aprēķināšanu darba pasūtījumu plānošanai, skatiet nodaļā [Līdzekļu pārvaldības parametri](../setup-for-objects/enterprise-asset-management-parameters.md). Līdzekļu pakalpojumu līmenim jāiestata vismaz viens noklusējuma ieraksts. Šo noklusējuma ierakstu izmanto, ja darba pasūtījuma plānošanas laikā netiek atrasta neviena cita atbilstība.

**1. piemērs** : noklusējuma pakalpojumu līmenis, kas tiek izmantots, ja netiek atrasta neviena cita atbilstība. Šajā ierakstā atlasiet tikai pakalpojumu līmeni.

**2. piemērs** : augsts pakalpojumu līmenis, ko izmanto, lai plānotu darbus Volvo kravas automašīnas dzinējam. Šajā ierakstā atlasiet atbilstošo līdzekļa veidu **(piemēram, kravas automašīnas dzinēju**), ražotāju (**Volvo**) un pakalpojumu līmeni.

## <a name="set-up-asset-service-levels"></a>Līdzekļu pakalpojumu līmeņu iestatīšana

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļa pakalpojumu līmeņi**.
2. Atlasiet **Jauns**, lai izveidotu ierakstu.
3. Atkarībā no detalizācijas līmeņa, kas nepieciešams līdzekļu pakalpojumu līmenim, veiciet atbilstošo atlasi laukos **Funkcionālais novietojums**, **Līdzekļa veids**, **Ražotājs**, **Modelis**, **Līdzeklis**, **Darba pasūtījuma veids** un **Pakalpojumu līmenis**.

    > [!NOTE]
    > Ja līdzekļa pakalpojumu līmenis tiek izmantots uzturēšanas pieprasījumiem un darba pasūtījumiem, Līdzekļu pārvaldība iziet cauri visiem līdzekļu pakalpojumu līmeņu ierakstiem, lai pārbaudītu iespējamo atbilstību. Tā vienmēr vispirms pārbauda visraksturīgāko kombināciju. Citiem vārdiem sakot, Līdzekļu pārvaldība vispirms pārbauda atbilstību laukam **Darba pasūtījuma veids**. Ja atbilstība netiek atrasta, tā meklē atbilstību laukam **Līdzeklis** un tā tālāk. Kā jūs varat redzēt lapas **Līdzekļa pakalpojumu līmeņi** zkārtojumā, šī uzvedība nozīmē, ka, lai atrastu visspecifiskāko kombināciju, Līdzekļu pārvaldība atbilstības meklēšanai pārbauda katru ierakstu no labās puses uz kreiso. Ja atbilstība netiek atrasta, šajos laukos tiek izmantots "noklusējuma" ieraksts, kam nav atlases iespēju.

4. Laukā **Pakalpojumu līmenis** atlasiet skaitli, kas norāda pakalpojumu līmeni (prioritāti).


> [!NOTE]
> Ja maināt līdzekļu pakalpojumu līmeņa ierakstu lapā **Līdzekļu pakalpojumu līmeņi** pēc tam, kad esat to jau izmantojis darba pasūtījumā, pakalpojumu līmenis uzturēšanas pieprasījumiem un darba pasūtījumiem netiek atbilstoši atjaunināts.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
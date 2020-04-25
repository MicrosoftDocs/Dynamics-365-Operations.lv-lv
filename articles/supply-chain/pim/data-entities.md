---
title: Produkta datu elementi
description: Šajā tēmā ir sniegta informācija par dažādām entītijām, kuras var izmantot, lai importētu un eksportētu produktu datus.
author: cvocph
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: conradv
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2019-12-1
ms.openlocfilehash: 340cb33537c7ba07555e1f0b6437fa4a3458a11a
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208620"
---
# <a name="product-data-entities"></a>Produkta datu elementi

[!include [banner](../includes/banner.md)]

Izmantojiet datu elementus, lai importētu un eksportētu datus. Tabulā ir sniegta detalizēta informācija par datu entītijām, kas saistītas ar produktu, un aprakstīts katras entitījas nolūks.

| Elements | Lietojumprogrammas objektu koka (AOT) nosaukums (veids) | Piezīmes |
|--------|-------------------------------------------|-------|
| Preces V2 | EcoResProductV2Entity | Šo entītiju izmanto, lai importētu un eksportētu koplietojamos produktus-atšķirīgas preces un preču šablonus. Tas ļauj atjauninājumus. Tas neatbalsta kopās balstītas SQL operācijas. Tas ir iespējots atvērto datu protokolam (OData). |
| Izlaistās preces V2 | EcoResReleasedProductV2Entity | Šo entītiju izmanto, lai importētu un eksportētu izlaistoss produktus-atšķirīgas preces un preču šablonus. Tas ļauj atjauninājumus. Tam ir nepieciešams jau izveidota koplietojamā prece. Importējot jaunu izlaisto preci, rodas koplietotās preces laidiens. Pastāv arī atsevišķas entītijas, kuras var izmantot, lai importētu un eksportētu izlaisto preču šablonus un izlaistos atšķirīgos variantus. Šī entītija neatbalsta kopā balstītas SQL operācijas vai dzēšanas operācijas. Tā ir iespējota OData. |
| Izlaisto preču izveide V2 | EcoResReleasedProductCreationV2Entity | Šo entītiju izmanto, lai vienā darbībā importētu koplietojamos produktus un izlaistās preces. Lai gan tā atbalsta eksportu, tā izmantošana nav ieteicama, jo entītijas nolūks ir preces radīšana. Tā neatbalsta atjauninājumus. Tā atbalsta ierobežotu lauku kopu (lauki, kas ir pieejami preces izveides dialoglodziņā). Tas neatbalsta kopās balstītas SQL operācijas. Tā netiek rādīta ar OData. |
| Preces varianti | EcoResProductVariantEntity | Šo entītiju izmanto, lai importētu un eksportētu koplietojamos preču variantus. Tas ļauj atjauninājumus. Tam nepieciešamas jau izveidotas dimensiju vērtības. Integrācijas atslēga ir preces šablons ar preces dimensijām. Šī entitīja neatbalsta kopās balstītas SQL operācijas. Tā ir iespējota OData. Tā atbalsta dzēšanas operācijas. To nevar paplašināt, pievienojot jaunas preces dimensijas. |
| Preču varianti pēc preces numura identifikācijas | EcoResProductNumberIdentifiedProductVariantEntity | Šo entītiju izmanto, lai importētu un eksportētu koplietojamos preču variantus. Tas ļauj atjauninājumus. Tam nepieciešamas jau izveidotas dimensiju vērtības. Integrācijas atslēga ir preces numurs (bet entītijas **Preču varianti**integrācijas atslēga ir preces šablons ar preces dimensijām). |
| Izlaistie preces varianti | EcoResReleasedProductVariantEntity | Šo entītiju izmanto, lai importētu un eksportētu izlaistos preču variantus. Tas ļauj atjauninājumus. Tam ir nepieciešami jau izveidoti koplietotās preces varianti. Importējot jaunu izlaisto preces variantu, rodas koplietotās preces varianta laidiens. Šī entitīja neatbalsta kopās balstītas SQL operācijas. Tā ir iespējota OData. Lai gan tas atbalsta dzēšanas darbības, to izmantošana pašlaik izraisa datu sabojāšanu pašreizējās platformas kļūmes dēļ. Šo entitīju nevar paplašināt, pievienojot jaunas preces dimensijas. |
| Izlaistie preču varianti pēc preces numura identifikācijas | EcoResProductNumberIdentifiedReleasedProductVariantEntity | Šī entitīja ir līdzīga entitījai **Izlaistie produktu varianti**, taču integrācijas atslēga ir preces numurs nevis preces šablons ar preces dimensijām. To var paplašināt, pievienojot jaunas preces dimensijas. |
| Pārdodamas izlaistās preces | EcoResSellableReleasedProductEntity | Šī entītija tiek izmantota, lai eksportētu tikai pārdodamas preces. Pārdodamās preces ir preces, par kurām ir pieejama informācija, kas ir nepieciešama, lai tās varētu izmantot pārdošanas pasūtījumā. Tie paši noteikumi attiecas uz preces validāciju, izmantojot funkciju **Validēt** lapā **Izlaistās preces**. |
| Izlaistās atšķirīgās preces V2 | EcoResDistinctProductV2Entity | Šī entītija tiek izmantota, lai eksportētu atšķirīgas preces. Šīs atšķirīgās preces var būt preces, apakštipa preces un preču varianti. |
| Izlaisto preču šabloni V2 | EcoResProductMasterV2Entity | Šo entītiju izmanto, lai importētu un eksportētu preču šablonus. Tā nav iespējota datu pārvaldībai. |
| Krājums - svītrkods | EcoResProductBarcodeEntity | Šī entītija tiek izmantota, lai eksportētu preces un svītrkodus. |
| Preces dzīves cikla stāvokļi | EcoResProductLifecycleSateEntity | Šī entītija tiek izmantota, lai importētu un eksportētu dažādus preces dzīves cikla stāvokļus, kurus var piešķirt precei. |

> [!NOTE]
> Lai importētu produktus sistēmā, jūs varat izmantot datu elementu **Izlaistās preces V2** tikai tad, ja koplietotā prece jau ir izveidota. Pretējā gadījumā, lai importētu produktus sistēmā, jāizmanto datu elements **Produkta izveide**.

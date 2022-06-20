---
title: Funkcionālā novietojuma dzīves cikla stāvokļi
description: Šajā rakstā ir aprakstīts, kā iestatīt funkcionālos novietojumus un dzīves cikla modeļus sadaļā Līdzekļu pārvaldība.
author: johanhoffmann
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetFunctionalLocationLifecycleModel, EntAssetFunctionalLocationLifecycleState
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae56c2b734339343b134be95abe0ce40b70c8a0e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934731"
---
# <a name="functional-location-lifecycle-states"></a>Funkcionālā novietojuma dzīves cikla stāvokļi

[!include [banner](../../includes/banner.md)]

 

Šajā rakstā ir aprakstīts, kā iestatīt funkcionālo atrašanās vietas dzīves cikla valstu un dzīves cikla modeļus sadaļā Līdzekļu pārvaldība. Funkcionālā novietojuma dzīves cikla stāvokļi definē stāvokļus, kādi var būt funkcionālajam novietojumam, piemēram, izveidots, aktīvs un beidzies. Varat skatīt visus funkcionālos novietojumus neatkarīgi no to dzīves cikla stāvokļa saraksta lapā **Visas funkcionālie novietojumi**. Funkcionālā novietojuma stāvokli var mainīt, atlasot to saraksta lapā **Visi funkcionālie novietojumi** un atlasot vienumu **Atjaunināt funkcionālā novietojuma stāvokli**.

## <a name="set-up-functional-location-lifecycle-states"></a>Funkcionālā novietojuma dzīves cikla stāvokļu iestatīšana

1. Atlasiet **Līdzekļu pārvaldība** > **Iestatīšana** > **Funkcionālie novietojumi** > **Dzīves cikla stāvokļi**.
2. Atlasiet **Jauns**, lai izveidotu jaunu funkcionālā novietojuma stāvokli.
3. Ievietojiet stāvokļa ID laukā **Dzīves cikla stāvoklis** un funkcionālā novietojuma stāvokļa nosaukumu laukā **Nosaukums**. Laukā **Dzīves cikla modeļi** varat redzēt to funkcionālo novietojumu dzīves cikla modeļu skaitu, kuri izmanto funkcionālā novietojuma stāvokli.
4. Kopsavilkuma cilnē **Vispārīgi** atlasiet "Jā" uz pārslēgšanas pogas **Aktīvs**, ja funkcionālajam novietojumam vajadzētu būt aktīvam šajā stāvoklī.
5. Atlasiet "Jā" uz pārslēgšanas pogas **Izveidot līdzekļus**, ja vajadzētu būt iespējamam automātiski izveidot līdzekli ar tādu pašu nosaukumu kā funkcionālajam novietojumam un uzstādīt to funkcionālajā novietojumā šajā stāvoklī.  
>[!NOTE]
>Šī pārslēgšanas poga attiecas uz lauku **Līdzekļa veids** kopsavilkuma cilnē **Vispārīgi** veidlapā **Funkcionālo novietojumu veidi** (**Līdzekļu pārvaldība** > **Iestatīšana** > **Funkcionālie novietojumi** > **Funkcionālo novietojumu veidi**).

6. Atlasiet "Jā" uz pārslēgšanas pogas **Pārdēvēt atrašanās vietu**, ja vajadzētu būt iespējamam mainīt funkcionālā novietojuma nosaukumu šajā stāvoklī.
7. Atlasiet "Jā" uz pārslēgšanas pogas **Jaunas apakšvietas**, ja vajadzētu būt iespējamam pievienot jaunas apakšvietas funkcionālajam novietojumam šajā stāvoklī.
8. Atlasiet "Jā" uz pārslēgšanas pogas **Uzstādīt līdzekļus**, ja vajadzētu būt iespējamam uzstādīt līdzekļus funkcionālajā novietojumā šajā stāvoklī.
9. Atlasiet "Jā" uz pārslēgšanas pogas **Dzēst funkcionālo novietojumu**, ja vajadzētu būt iespējamam dzēst funkcionālo novietojumu šajā stāvoklī.
10. Atlasiet līdzekļa stāvokli laukā **Dzīves cikla stāvoklis**, ja vēlaties, lai līdzekļa dzīves cikla stāvoklis visiem līdzekļiem, kas uzstādīti funkcionālajā novietojumā, tiktu automātiski atjaunināts šajā stāvoklī. Piemērs: ja aizverat funkcionālo novietojumu un iestatāt funkcionālā novietojuma dzīves cikla stāvokli uz "Pabeigts", iespējams, vēlēsities automātiski mainīt šajā funkcionālajā novietojumā uzstādīto līdzekļu dzīves cikla stāvokli uz "Netiek lietots".


>[!NOTE]
>Funkcionālā novietojuma dzīves cikla stāvokļi, dzīves cikla modeļi un veidi ir saistīti un tiek izmantoti tādā pašā veidā kā darba pasūtījuma dzīves cikla stāvokļi, darba pasūtījuma dzīves cikla modeļi un darba pasūtījumu veidi. 

## <a name="set-up-functional-location-lifecycle-models"></a>Funkcionālā novietojuma dzīves cikla modeļu iestatīšana

Kad esat izveidojis dzīves cikla stāvokļus, kas nepieciešami jūsu funkcionālajam novietojumam, tos var iedalīt grupās. Tas tiek darīts, lai izveidotu dzīves cikla modeļu plūsmu, ko var izmantot dažādiem funkcionālo novietojumu veidiem. Jāizveido vismaz viens standarta funkcionālā novietojuma dzīves cikla modelis.

1. Atlasiet **Līdzekļu pārvaldība** > **Iestatīšana** > **Funkcionālie novietojumi** > **Dzīves cikla modeļi**.
2. Atlasiet **Jauns**, lai izveidotu dzīves cikla modeli.
3. Ievietojiet dzīves cikla modeļa ID laukā **Dzīves cikla modelis** un dzīves cikla modeļa nosaukumu laukā **Nosaukums**. Laukos **Funkcionālo novietojumu veidi** un **Dzīves cikla stāvokļi** varat redzēt to funkcionālo novietojumu veidu skaitu, kas izmanto dzīves cikla modeli, kā arī dzīves cikla modelī atlasīto stāvokļu skaitu.
4. Kopsavilkuma cilnē **Dzīves cikla stāvokļi** atlasiet stāvokļus, kuri būtu jāiekļauj modelī. Tas tiek darīts, noklikšķinot uzstāvokļa sadaļā **Atlikušie dzīves cikla stāvokļi** un noklikšķinot uz pogas ![bultiņa uz priekšu.](media/02-setup-for-functional-locations.png) poga.
5. Ja vēlaties atlasīt visus modelim pieejamos stāvokļus, noklikšķiniet uz pogas ![atlasīt visus pieejamos posmus.](media/03-setup-for-functional-locations.png) poga. Visi stāvokļi tiek nosūtīti uz sadaļu **Atlasītie dzīves cikla stāvokļi**.
6. Ja vēlaties modelima noņemt atlasīto stāvokli, atlasiet stāvokli sadaļā **Atlasītie dzīves cikla stāvokļi** un pēc tam atlasiet pogu ![bultiņa atpakaļ.](media/04-setup-for-functional-locations.png) poga.
7. Atlasiet **Dzīves cikla stāvokļa atjauninājumi**, lai definētu, kuri dzīves cikla stāvokļi var sekot atlasītajam stāvoklim.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: Līdzekļu dzīves cikla stāvokļi
description: Šajā tēmā ir paskaidroti līdzekļu dzīves cikla stāvokļi un dzīves cikla modeļi Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetLifecycleModelStateNext, EntAssetObjectLifecycleState, EntAssetLifecycleStateUpdate, EntAssetObjectLifecycleModel
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 55139c6458e569b15518f0f11f1c12c3a26cae2f26c6a2046a7ebdc1277cb144
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6722467"
---
# <a name="asset-lifecycle-states"></a>Līdzekļu dzīves cikla stāvokļi

[!include [banner](../../includes/banner.md)]

 

Šajā tēmā ir paskaidroti līdzekļu dzīves cikla stāvokļi un dzīves cikla modeļi Līdzekļu pārvaldībā. Līdzekļa dzīves cikla stāvokļi tiek izmantoti, lai definētu, vai līdzeklis ir aktīvs vai neaktīvs. Piemēram, varat iestatīt tādus līdzekļa dzīves cikla stāvokļus kā **Izveidots**, **Aktīvs** un **Izbeigts**.

> [!NOTE]
> - Pieprasījuma dzīves cikla stāvokļi ir saistīti ar līdzekļu dzīves cikla stāvokļiem. Tādēļ, kad pieprasījums tiek mainīts uz jaunu pieprasījuma dzīves cikla stāvokli, pieprasījumam pievienotais līdzeklis tiek mainīts uz jaunu līdzekļa dzīves cikla stāvokli. Piemēram, ja pieprasījuma dzīves cikla stāvoklis tiek nomainīts uz **Ienākošais**, pievienotā līdzekļa dzīves cikla stāvoklis tiek mainīts uz to dzīves cikla stāvokli, kas atlasīts lapas **Līdzekļa dzīves cikla stāvokļa modeļi** kopsavilkuma cilnes **Līdzekļa dzīves cikla stāvoklis** laukā **Ienākošais dzīves cikla stāvoklis**. 


Līdzekļa dzīves cikla stāvokļus var iestatīt līdzekļa dzīves cikla modeļos, kur var definēt nepieciešamos dzīves cikla stāvokļus dažādiem līdzekļu veidiem. Vispirms iestatiet dzīves cikla stāvokļus. Pēc tam izveidojiet dzīves cikla modeli un atlasiet tam dzīves cikla stāvokļus.

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļi** \> **Dzīves cikla stāvokļi**.
2. Atlasiet **Jauns**, lai izveidotu jaunu dzīves cikla stāvokli.
3. Laukā **Dzīves cikla stāvoklis** ievadiet dzīves cikla stāvokļa ID.
4. Laukā **Nosaukums** ievadiet aprakstu.

    Laukā **Dzīves cikla modeļi** ir parādīts to līdzekļu dzīves cikla modeļu skaits, kuri izmanto līdzekļa dzīves cikla stāvokli.

5. Iestatiet opciju **Aktīvs** uz **Jā**, ja šim dzīves cikla stāvoklim jābūt aktīvam dzīves cikla stāvoklim (citiem vārdiem, ja darba pasūtījumus var izveidot līdzekļiem, kas ir šajā dzīves cikla stāvoklī).
6. Iestatiet opciju **Dzēst atvērtās kalendāra rindas** uz **Jā**, ja atvērtās līdzekļu kalendāra rindas, kuru līdzekļa dzīves cikla stāvoklis ir **Izveidots**, ir jāizdzēš, kad tās ir šajā dzīves cikla stāvoklī. Šis iestatījums ir noderīgs, ja vēlaties notīrīt visus atvērtos uzturēšanas grafikus, kas vairs nav atbilstoši līdzeklim (piemēram, ja līdzeklis vairs nav aktīvs).

> [!NOTE]
> Līdzekļa dzīves cikla stāvokļi, līdzekļa dzīves cikla modeļi un līdzekļu veidi ir saistīti. Tos izmanto tādā pašā veidā kā darba pasūtījuma dzīves cikla stāvokļus, darba pasūtījuma dzīves cikla modeļus un darba pasūtījumu veidus. 


Kad esat izveidojis nepieciešamos līdzekļa dzīves cikla stāvokļus, varat iestatīt dzīves cikla stāvokļus līdzekļa dzīves cikla modeļos.

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļi** \> **Dzīves cikla modeļi**.
2. Atlasiet **Jauns**, lai izveidotu jaunu dzīves cikla modeli.
3. Laukā **Dzīves cikla modelis** ievadiet dzīves cikla modeļa ID.
4. Laukā **Nosaukums** ievadiet aprakstu.

    Laukā **Dzīves cikla stāvokļi** ir parādīts to līdzekļu dzīves cikla stāvokļu skaits, kuri ir atlasīti līdzekļa dzīves cikla modelī. Laukā **Līdzekļu veidi** ir parādīts to līdzekļu veidu skaits, kuri izmanto līdzekļa dzīves cikla modeli.

5. Kopsavilkuma cilnē **Dzīves cikla stāvokļi** atlasiet līdzekļa dzīves cikla stāvokļus, kuri būtu jāiekļauj līdzekļa dzīves cikla modelī:

    - Lai modelim izmantotu dzīves cikla stāvokli, atlasiet to sadaļā **Atlikušie dzīves cikla stāvokļi** un pēc tam atlasiet bultiņas pa labi pogu ![Bultiņa pa labi.](media/15-setup-for-objects.png) Lai pārvietotu to uz sadaļu **Atlasītie dzīves cikla stāvokļi**.
    - Lai modelim izmantotu visus pieejamos dzīves cikla stāvokļus, atlasiet pogu **Visi pieejamie dzīves cikla stāvokļi** ![Visi pieejamie dzīves cikla stāvokļi.](media/20-setup-for-objects.png). Visi dzīves cikla stāvokļi tiek nosūtīti uz sadaļu **Atlasītie dzīves cikla stāvokļi**.
    - Lai no modeļa noņemtu dzīves cikla stāvokli, atlasiet to sadaļā **atlasītie dzīves cikla stāvokļi** un pēc tam atlasiet bultiņas pa kreisi pogu ![Bultiņa pa kreisi.](media/16-setup-for-objects.png) Lai pārvietotu to uz sadaļu **Atlikušie dzīves cikla stāvokļi**.

6. Atlasiet **Dzīves cikla stāvokļa atjauninājumi**, lai definētu, kuri līdzekļa dzīves cikla stāvokļi var sekot atlasītajam dzīves cikla stāvoklim.
7. Izmantojiet kopsavilkuma cilni **Līdzekļa stāvoklis**, ja apstrādat līdzekļus, kurus saņemat remontam. Sadaļā **Ienākošais/Izejošais** varat atlasīt līdzekļa dzīves cikla stāvokļus, lai norādītu remontam saņemtā līdzekļa darbplūsmu. Ja piedāvājat patapinājuma līdzekļus debitoriem vai nodaļām, sadaļā **Patapinājums** varat atlasīt dzīves cikla stāvokļus patapinājuma līdzekļiem.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
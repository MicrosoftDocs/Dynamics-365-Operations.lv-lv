---
title: Līdzekļu dokumenti
description: Šajā rakstā skaidroti līdzekļu dokumenti Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectDocument
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a2e8d72dc938c43e266c6b7c39329f827c56607a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899474"
---
# <a name="asset-documents"></a>Līdzekļu dokumenti

[!include [banner](../../includes/banner.md)]

 

Šajā rakstā skaidroti līdzekļu dokumenti Līdzekļu pārvaldībā.

Līdzekļu pārvaldībā varat iestatīt dokumentus tā, lai tie tiktu automātiski saistīti, piemēram, ar darbu veidiem, līdzekļu ražotājiem, līdzekļu veidiem vai līdzekļiem. Šī funkcionalitāte tiek izmantota, kad tiek izlaistas atjauninātas dokumenta versijas. Šādā gadījumā jums vienkārši jāievieto atjauninātais dokuments standarta atrašanās vietā, ko izmantojat Supply Chain Management dokumentiem, un jāpievieno dokuments jūsu izveidotajam līdzekļu dokumenta ierakstam. Pēc tam atjauninātajam dokumentam var piekļūt no izvēlnes elementiem **Visi līdzekļi**, **Aktīvie līdzekļi**, **Mani aktīvie līdzekļi**, **Visi darba pasūtījumi** un **Aktīvie darba pasūtījuma darbi** . Dokumentu pievienošanas process līdzekļa dokumenta ierakstam izmanto standarta dokumentu apstrādes sistēmu.

**1. piemērs** : dokuments, kas saistīts ar darba veidu, var aprakstīt procedūru šim darba veidam.

**2. piemērs:** dokuments, kas ir saistīts ar līdzekļa veida, ražotāja un modeļa kombināciju, var būt standarta rokasgrāmata atlasītajam līdzekļu ražotāja modelim.

## <a name="create-asset-document-relation"></a>Līdzekļa dokumentu attiecību izveide

1. Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Līdzekļa dokumenti**.
2. Atlasiet **Jauns**, lai izveidotu līdzekļa dokumenta ierakstu.
3. Atkarībā no tā, cik konkrētas dokumentu attiecības vēlaties, veiciet atbilstīgu atlasi vienā vai vairākos šādos laukos: **Līdzekļa veids**, **Ražotājs**, **Modelis**, **Līdzeklis**, **Darba veida kategorija**, **Darba veids**, **Darba veida variants** un **Darba vajadzība**. Opcijas, kas pieejamas laukos **Darba veida variants** un **Darba vajadzība**, ir atkarīgas no atlases laukā **Darba veids**.

    > [!NOTE]
    > Kad sistēma meklē dokumentus, kas ir jāattiecina uz līdzekli vai darba pasūtījumu, Līdzekļu pārvaldība iziet cauri visiem līdzekļa dokumentu ierakstiem, lai pārbaudītu iespējamo sakritību. Tā vienmēr vispirms pārbauda visraksturīgāko kombināciju. Citiem vārdiem sakot, Līdzekļu pārvaldība vispirms pārbauda atbilstību laukam **Darba vajadzība**. Ja atbilstība netiek atrasta, tā meklē atbilstību laukam **Darba veida variants**. Ja atbilstība netiek atrasta, tā meklē atbilstību laukam **Darba veids** un tā tālāk. Kā jūs varat redzēt lapas **Līdzekļa dokumenti** zkārtojumā, šī uzvedība nozīmē, ka, lai atrastu visspecifiskāko kombināciju, Līdzekļu pārvaldība atbilstības meklēšanai pārbauda katru ierakstu no labās puses uz kreiso. Ar līdzekli vai darba pasūtījumu var būt saistīti vairāki dokumenti. Vajadzības gadījumā varat rediģēt pakalpojumu līmeni uzturēšanas pieprasījumā vai darba pasūtījumā.

4. Atlasiet **Pielikumi**. Tiek parādīta standarta lapa **Dokumentu apstrāde**.
5. Iestatiet dokumentus vai piezīmes, kas jāpievieno līdzekļa dokumenta ierakstam. Pēc dokumentu pievienošanas lauks **Pielikumi** parāda ar ierakstu saistīto dokumentu skaitu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
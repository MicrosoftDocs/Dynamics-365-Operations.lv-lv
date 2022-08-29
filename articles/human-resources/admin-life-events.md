---
title: Iestatīt administratora tiesības dzīves notikumiem
description: Šajā rakstā skaidrots, kā konfigurēt administratora tiesības dzīves notikumiem programmā Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9deed240977394667cee8b107397267b182d960b
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229990"
---
# <a name="set-administrator-rights-for-life-events"></a>Iestatīt administratora tiesības dzīves notikumiem

[!include [banner](../includes/preview-banner.md)]

Administratori var atjaunināt dzīves notikumu opcijas atkarībā no konfigurācijas iestatījumiem. Lapā Cilvēkresursu **parametri varat** konfigurēt parametrus, kas administratoriem ļauj veikt plāna atlases izmaiņas. Varat arī pilnībā ierobežot administratorus veikt izmaiņas.

Lapā Cilvēkresursu **parametri varat** iestatīt plāna izmaiņu ierobežojumus apstiprinātajiem plāniem un dzīves notikumu opcijām.

Ja ir **atlasīta opcija** Apstiprinātie plāni, izmaiņas var veikt tikai tad, ja reģistrācijas periods ir aktīvs. (Reģistrācijas periodu piemēri ietver atvērtos reģistrācijas periodus, jaunus reģistrācijas periodus un dzīves notikumu reģistrācijas periodus.) Ja šī opcija nav atlasīta, izmaiņas var tikt veiktas jebkurā laikā.

Ja ir **atlasīta opcija Dzīves** notikums, plāna izmaiņas dzīves notikuma laikā ierobežo dzīves notikuma opcijas, kas definētas plāna tipam. Ja nav atlasīta šī opcija, plāna atlasi var mainīt dzīves notikuma laikā.

## <a name="set-plan-change-restrictions"></a>Iestatīt plāna izmaiņu ierobežojumus

**Lapā Personāla vadības parametri** cilnē Atvieglojumu **pārvaldība** ir pieejami šādi lauki.

| Lauks | Apraksts |
|-------|-------------|
| Apstiprinātie plāni | Atlasiet šo opciju, ja plāna izmaiņas ir atļautas tikai tad, ja reģistrācijas periods ir aktīvs. Ja šī opcija nav atlasīta, izmaiņas var tikt veiktas jebkurā laikā. |
| Dzīves notikumu opcijas | Atlasiet šo opciju, ja plāna izmaiņas dzīves notikuma laikā ierobežo plāna tipam definētās dzīves notikuma opcijas. Ja nav atlasīta šī opcija, plāna atlasi var mainīt dzīves notikuma laikā. |

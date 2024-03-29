---
title: Ražošanas noviržu vispārējo iemeslu analīze
description: Šajā rakstā ir izskaidroti dažādi tipiski visu ražošanas noviržu veidu iemesli.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcVarianceTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b0f7a66c00540216887c7913e7f094c819b693a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/03/2022
ms.locfileid: "8674003"
---
# <a name="common-sources-of-production-variances"></a>Ražošanas noviržu vispārējo iemeslu analīze

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidroti dažādi tipiski visu ražošanas noviržu veidu iemesli. 

Tālāk norādīti daži tipiski **partijas lieluma** noviržu iemesli.

-   Preču daudzums ražošanas pasūtījumam atšķiras no aprēķina daudzuma, kas tiek izmantots standarta izmaksu aprēķinam. Daudzums nodrošina pamatojumu amortizēšanas konstantām izmaksām.
-   Konstanto izmaksu vērtība ražošanas pasūtījumā atšķiras no konstantām izmaksām, kas tiek izmantotas standarta izmaksu aprēķinā. Konstantas izmaksas ražošanas pasūtījumā var atšķirties dažādu iemeslu dēļ. Piemēram, konstantas izmaksas var norādīt uz tālāk minētajiem faktoriem.
    -   Manuāli veiktas izmaiņas ražošanas materiālu komplektā (MK) vai maršrutā
    -   Atšķirīgas MK vai maršruta versijas atlase, izveidojot ražošanas pasūtījumu
    -   Krājumam piešķirtās MK vai maršruta versijas plānotas tehnoloģiskas izmaiņas

Tālāk norādīti daži tipiski **ražošanas cenas** noviržu iemesli.

-   Izmaksu kategorija (un tās izmaksu kategorijas cena) maršrutēšanas operācijas ziņotajam patēriņam atšķiras no izmaksu kategorijas, ko izmanto standarta izmaksu aprēķinā.
-   Aktīvā izmaksa izmaksu kategorijas cenai atšķiras no izmaksu kategorijas cenas, ko izmanto standarta izmaksu aprēķinā.

Tālāk norādīti daži tipiski **ražošanas daudzuma** noviržu iemesli.

-   Materiāla komponenta pārmērīga vai nepietiekama izsniegšana.
-   Pārskatā norādīts pārsniegts vai nepietiekams maršrutēšanas operācijas laiks.
-   Pārmērīga vai nepietiekama pamata krājuma, kas saistītas ar pasūtījuma daudzumu, derīga daudzuma saņemšana. Tomēr komponenti tiek izsniegti un darbības tiek reģistrētas pilnībā atkarībā no ražošanas pasūtījumā noradītā pasūtījuma daudzuma.

Tālāk norādīti daži tipiski **ražošanas aizstāšanas** noviržu iemesli.

-   Tiek izdots materiāla komponents, kas nav ražošanas MK.
-   Ražošanas materiālu komplektam (MK) manuāli tiek pievienots komponents, reģistrējot to kā patērētu.
-   Krājums tiek reģistrēts kā patērēts, bet netiek manuāli pievienots ražošanas MK.
-   Operācija tiek manuāli pievienota ražošanas maršrutam, reģistrējot to kā par patērētu.
-   Izveidojot ražošanas pasūtījumu, tiek atlasīta MK versija, kas atšķiras no tās, ko izmanto standarta izmaksu aprēķinā.
-   Izveidojot ražošanas pasūtījumu, tiek atlasīta maršruta versija, kas atšķiras no tās, ko izmanto standarta izmaksu aprēķinā.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
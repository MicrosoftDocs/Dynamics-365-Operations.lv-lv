---
title: Finanšu dimensiju kopas
description: Šajā tēmā aprakstītas finanšu dimensiju kopas un sniegti daži padomi to lietošanas optimizēšanai.
author: yukonpeegs
ms.date: 03/07/2022
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: twheeloc
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: c583a2a89b45b59ea76ffd8e38b6206c9ca9ed41
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722581"
---
# <a name="financial-dimension-sets"></a>Finanšu dimensiju kopas

[!include [banner](../includes/banner.md)]

Šajā tēmā aprakstītas finanšu dimensiju kopas un sniegti daži padomi to lietošanas optimizēšanai.

Dimensiju kopa ir sakārtots finanšu dimensiju saraksts, ko var izmantot, lai apkopotu Virsgrāmatas datus lietotāja definētā veidā. Dimensiju kopu primārā izmantošana ir definēt apgrozījuma bilanci.

Vienīgā standarta dimensiju kopa ir dimensiju kopa, kas ietver tikai galveno kontu.

Lapa **Finanšu dimensiju kopas** tiek izmantota finanšu dimensiju kopu izveidošanai un pārvaldīšanai.

## <a name="dimension-set-balances"></a>Dimensiju kopas bilances

Dimensiju kopai var būt bilances, kas pamatotas uz tās finanšu dimensijām. Bilances pastāv Virsgrāmatā, un tās ir balstītas uz dimensiju kopas definīciju. Bilances tiek apkopotas no Virsgrāmatas datiem, lai palīdzētu uzlabot veiktspēju to izgūšanas laikā (piemēram, kad tiek ģenerēta apgrozījuma bilance).

## <a name="create-balances"></a>Izveidot bilances

Izmantojiet pogu **Izveidot bilances**, lai inicializētu bilances dimensiju kopai, kurai pašlaik nav bilances.

> [!NOTE]
> Ieteicams ierobežot to dimensiju kopu skaitu, kurām ir bilances, jo bilances atjauninājumi ietekmē visas Virsgrāmatas grāmatošanas darbības.

## <a name="update-balances"></a>Atjaunināt bilances

Izmantojiet pogu **Atjaunināt bilances**, lai bilancēs iekļautu pēdējo Virsgrāmatas grāmatošanas aktivitāti. Bilances atjauninājumi ir vieglas darbības. Tām ir jāapstrādā tikai Virsgrāmatas grāmatošanas aktivitāte, kas ir notikusi kopš pēdējās atjaunināšanas.

> [!NOTE]
> Rādot apgrozījuma bilanci, tiek veikta atjaunināšana, lai pārliecinātos, vai parādītās bilances ir aktuālas. Apsveriet iespēju izmantot periodisku pakešuzdevumu, lai jūsu visbiežāk izmantoto dimensiju kopu atjauninājumi būtu ātri. Šādā veidā jūs palīdzat samazināt laiku, kas apgrozījuma bilances lietotājiem ir jāgaida.

## <a name="rebuild-balances"></a>Atjaunot bilances

Izmantojiet pogu **Atjaunot bilances**, lai no jauna izveidotu bilances. Šādā veidā jūs palīdzat nodrošināt, lai tie atbilstu Virsgrāmatas datiem. Bilanču atjaunošanai ir vajadzīga liela pārstrāde, un parasti tā nav obligāta.

> [!NOTE]
> Ja ir scenārijs, kas regulāri pieprasa bilanču atjaunošanu, ieteicams sazināties ar klientu atbalsta dienestu. Klientu atbalsts var palīdzēt noteikt, kāpēc bilances neatbilst Virsgrāmatas datiem.

## <a name="clear-balances"></a>Notīrīt bilances

Izmantojiet pogu **Dzēst bilances**, lai noņemtu bilances un apturētu turpmākus atjauninājumus. Dimensiju kopa vairs neietekmēs Virsgrāmatas grāmatošanas aktivitātes.

## <a name="delete-a-dimension-set"></a>Dimensiju kopas dzēšana

Neizdzēsiet **un atkārtoti** izveidojiet dimensiju kopas kā nevienu darba veidu, lai atrisinātu potenciālās problēmas ar bilances datiem noteiktai dimensiju kopai. Dimensiju kopas atkārtota aprēķināšana ir dārga. Lai saņemtu palīdzību saistībā ar problēmām, sazinieties ar klientu atbalsta dienestu. 


Papildinformāciju skatiet tēmā [Finanšu dimensijas](financial-dimensions.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

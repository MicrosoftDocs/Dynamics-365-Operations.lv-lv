---
title: Pasūtījumu piegāde no cita veikala, izmantojot līdzekli Maksas nosūtīšana
description: Šajā tēmā ir aprakstīts līdzeklis Maksas nosūtīšana.
author: ashishmsft
manager: AnnBe
ms.date: 10/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2017-10-10
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 088f55e5605c99f69852b4d6811b5c5504f267a2
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/24/2019
ms.locfileid: "2019466"
---
# <a name="ship-orders-from-another-store-by-using-the-charge-send-feature"></a>Pasūtījumu piegāde no cita veikala, izmantojot līdzekli Maksas nosūtīšana

[!include [banner](includes/banner.md)]

Izmantojot programmas Retail līdzekli Maksas nosūtīšana, vienā veikalā veiktos debitoru pasūtījumus var nosūtīt no cita veikala.

Debitoru pasūtījumiem pārdošanas punkta (POS) klientā tiek atbalstītas vairākas izpildes opcijas. Tālāk ir norādīti daži izpildes opciju piemēri.

- Izdot tajā pašā veikalā citā datumā.
- Izdot citā veikalā tajā pašā vai citā datumā.
- Izdot no citas veikalam piešķirtās nosūtīšanas noliktavas un piegādāt noteiktā datumā.

Līdzeklim Maksas sūtīšana tiek izmantotas šādas POS operācijas: Nosūtīt visas preces un Nosūtīt atlasītās preces. Tas sniedz veikala darbiniekam iespēju atlasīt nosūtīšanas vietu, no kuras ir jāizpilda pasūtījums vai pasūtījuma rinda. Pēc noklusējuma kā nosūtīšanas vieta ir iestatīta ar veikalu saistītā nosūtīšanas noliktava. Taču veikala darbinieks var mainīt šo vietu un atlasīt jebkuru attiecīgajam veikalam piešķirtajā veikalu vietrāžu grupā definēto veikalu.

Tas neietekmē iespēju atlasīt piegādes adresi.

Pasūtījuma rindas izpildei izmantojamās piegādes metodes ir atkarīgas no precēm un adresēm konfigurētajiem derīgajiem piegādes veidiem. Tā kā piegādes veidu derīguma kārtulas tiek glabātas tikai modulī Mazumtirdzniecība (HQ), POS klientā tiek veikts reāllaika izsaukums, lai iegūtu informāciju par sūtīšanas rindai derīgajiem piegādes veidiem.

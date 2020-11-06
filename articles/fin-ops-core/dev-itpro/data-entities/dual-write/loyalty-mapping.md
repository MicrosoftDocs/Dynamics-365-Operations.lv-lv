---
title: Klientu lojalitātes programmas kartes un atlīdzības punkti
description: Šajā tēmā aprakstīta klientu lojalitātes programmu un atlīdzības karšu datu integrācija starp Finance and Operations programmām un Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 24ce08bb6cba9c74075151bafe0b07509fbdf73d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998018"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Klientu lojalitātes programmas kartes un atlīdzības punkti

[!include [banner](../../includes/banner.md)]



Uzņēmumi klasificē klientus un sniedz sarežģītus pakalpojumus, pamatojoties uz klientu iepirkšanās un izdevumu modeļiem. Programmas Microsoft Dynamics 365 programmu klāstā ir Dynamics 365 Commerce, kurai ir infrastruktūra un funkcijas, kas atvieglo un apstrādā klientu lojalitātes programmas kartes, atlīdzības punktus, lojalitātē balstītu cenu noteikšanu un atlīdzībā balstītu iepirkšanās pieredzi. Kad dati par klientu lojalitātes programmas kartēm un atlīdzības punktiem pakalpojumā Commerce ir sinhronizēti ar Common Data Service, Dynamics 365 modeļa vadītā programmas var šos datus izmantot. Piemēram, Dynamics 365 Customer Service lietotāji var izmantot datus, lai nodrošinātu tos pašus sarežģītos pakalpojumus, izmantojot palīdzības dienestu.

## <a name="templates"></a>Veidnes

| Finance and Operations programmas | Modeļa vadītas programmas programmā Dynamics 365 | apraksts |
|-----------------------------|-----------------------------------|-------------|
| Lojalitātes programmas karte                | msdyn\_loyaltycards               | Šī veidne sinhronizē informāciju par klientu lojalitātes programmu kartēm. |
| Lojalitātes programmas atlīdzības punkti       | msdyn\_loyaltyrewardpoints        | Šī veidne sinhronizē informāciju par klientu atlīdzības punktiem. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]

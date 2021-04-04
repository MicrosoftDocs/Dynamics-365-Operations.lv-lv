---
title: Klientu lojalitātes programmas kartes un atlīdzības punkti
description: Šajā tēmā aprakstīta klientu lojalitātes programmu un atlīdzības karšu datu integrācija duālā ierakstā.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 39e1d5b0a73b198b164e51a18222dbd985192070
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568032"
---
# <a name="customer-loyalty-cards-and-reward-points"></a>Debitoru lojalitātes programmas kartes un atlīdzības punkti

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Uzņēmumi klasificē klientus un sniedz sarežģītus pakalpojumus, pamatojoties uz klientu iepirkšanās un izdevumu modeļiem. Piemēram, Dynamics 365 Commerce ir infrastruktūra un funkcijas, kas atvieglo un apstrādā klientu lojalitātes programmas kartes, atlīdzības punktus, lojalitātē balstītu cenu noteikšanu un atlīdzībā balstītu iepirkšanās pieredzi. Kad dati par klientu lojalitātes programmas kartēm un atlīdzības punktiem pakalpojumā Commerce ir sinhronizēti ar Dataverse, klientu iesaistes programmas var šos datus izmantot. Piemēram, Dynamics 365 Customer Service lietotāji var izmantot datus, lai nodrošinātu tos pašus sarežģītos pakalpojumus, izmantojot palīdzības dienestu.

## <a name="templates"></a>Veidnes

| Finance and Operations programmas | Modeļa vadītas programmas programmā Dynamics 365 | apraksts |
|-----------------------------|-----------------------------------|-------------|
| Lojalitātes programmas karte                | msdyn\_loyaltycards               | Šī veidne sinhronizē informāciju par klientu lojalitātes programmu kartēm. |
| Lojalitātes programmas atlīdzības punkti       | msdyn\_loyaltyrewardpoints        | Šī veidne sinhronizē informāciju par klientu atlīdzības punktiem. |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
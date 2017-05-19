---
title: "Finanšu dimensijas un galvenie konti valodā ar rakstību no labās puses uz kreiso"
description: "Šajā tēmā ir aprakstīti daži no ieviešanas lēmumiem, ka ir jāņem vērā, kad programmatūrā Microsoft Dynamics 365 for Operations lietojat valodu ar rakstību no labās puses uz kreiso un ir jāiestata finanšu dimensijas un galvenie konti."
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 3ca0ece17111f50e48019f57a426820392efacab
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="financial-dimensions-and-main-accounts-in-a-right-to-left-language"></a>Finanšu dimensijas un galvenie konti valodā ar rakstību no labās puses uz kreiso

[!include[banner](../includes/banner.md)]


Šajā tēmā ir aprakstīti daži no ieviešanas lēmumiem, ka ir jāņem vērā, kad programmatūrā Microsoft Dynamics 365 for Operations lietojat valodu ar rakstību no labās puses uz kreiso un ir jāiestata finanšu dimensijas un galvenie konti.

Finanšu dimensijas un galvenie konti ir galvenie implementēšanas plānošanas fāzes komponenti. Kad sistēma ir izveidotas finanšu dimensijas un galvenie konti, tie tiek izmantoti lapās **Konfigurēt kontu struktūras**, **Detalizēto kārtulu struktūras** un **Finanšu dimensijas konfigurācija programmu integrēšanai**. Šajās lapas definētā secība sistēmā tiek izmantota datu ievadei un patēriņam. Noteiktās sistēmas vietās finanšu dimensijas un galvenie konti tiek rādīti atsevišķos laukos. Taču citviet, piemēram, žurnālos, finanšu dimensijas un galvenie konti tiek rādīti kā viena virkne.

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Finanšu dimensiju un galveno kontu iestatīšanas paraugprakse sistēmā ar rakstību no labās puses uz kreiso

-   Kad atlasāt norobežotāju kontu plāniem, atlasiet kādu no dubultajām norobežotāju opcijām: dubulto pārnesumzīmi (--), dubulto šķirtni (||) vai divpunkti (..), vai dubulto pasvītrojuma zīmi (\_\_).
-   Kad veidojat finanšu dimensijas un galvenā konta vērtības, izmantojiet tikai ciparus un rakstzīmes valodai ar rakstību no labās puses uz kreiso.
-   Atlasīto kontu plāna norobežotāju nelietojiet finanšu dimensijas un galveno kontu vērtībās.

Ievērojot šo paraugpraksi, jūs palīdzat garantēt konsekventu lietotāja definēto pasūtījumu attēlojumu visā sistēmā.





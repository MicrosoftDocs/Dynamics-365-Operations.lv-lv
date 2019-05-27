---
title: Finanšu dimensijas un galvenie konti valodām ar rakstību no labās uz kreiso pusi
description: Šajā tēmā ir aprakstīti daži no ieviešanas lēmumiem, kas ir jāņem vērā, kad lietojat valodu ar rakstību no labās puses uz kreiso un ir jāiestata finanšu dimensijas un galvenie konti.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 9609c052083dc3157618584da9311211ea036eba
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555598"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>Finanšu dimensijas un galvenie konti valodām ar rakstību no labās uz kreiso pusi

[!include [banner](../includes/banner.md)]

Šajā tēmā ir aprakstīti daži no ieviešanas lēmumiem, kas ir jāņem vērā, kad lietojat valodu ar rakstību no labās puses uz kreiso un ir jāiestata finanšu dimensijas un galvenie konti.

Finanšu dimensijas un galvenie konti ir galvenie implementēšanas plānošanas fāzes komponenti. Kad sistēma ir izveidotas finanšu dimensijas un galvenie konti, tie tiek izmantoti lapās **Konfigurēt kontu struktūras**, **Detalizēto kārtulu struktūras** un **Finanšu dimensijas konfigurācija programmu integrēšanai**. Šajās lapas definētā secība sistēmā tiek izmantota datu ievadei un patēriņam. Noteiktās sistēmas vietās finanšu dimensijas un galvenie konti tiek rādīti atsevišķos laukos. Taču citviet, piemēram, žurnālos, finanšu dimensijas un galvenie konti tiek rādīti kā viena virkne.

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Finanšu dimensiju un galveno kontu iestatīšanas paraugprakse sistēmā ar rakstību no labās puses uz kreiso

-   Kad atlasāt norobežotāju kontu plāniem, atlasiet kādu no dubultajām norobežotāju opcijām: dubulto pārnesumzīmi (--), dubulto šķirtni (||) vai divpunkti (..), vai dubulto pasvītrojuma zīmi (\_\_).
-   Kad veidojat finanšu dimensijas un galvenā konta vērtības, izmantojiet tikai ciparus un rakstzīmes valodai ar rakstību no labās puses uz kreiso.
-   Atlasīto kontu plāna norobežotāju nelietojiet finanšu dimensijas un galveno kontu vērtībās.

Ievērojot šo paraugpraksi, jūs palīdzat garantēt konsekventu lietotāja definēto pasūtījumu attēlojumu visā sistēmā.




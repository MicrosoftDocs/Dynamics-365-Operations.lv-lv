---
title: Finanšu dimensijas un galvenie konti valodām ar rakstību no labās uz kreiso pusi
description: Šajā rakstā ir aprakstīti lēmumi, kas jāveic, izmantojot valodu ar labās puses un kreiso pusi, un ir jāiestata finanšu dimensijas un galvenie konti.
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: rcarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b1e2c0ef5cd405232332847078c70af42f056e17
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866765"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>Finanšu dimensijas un galvenie konti valodām ar rakstību no labās uz kreiso pusi

[!include [banner](../includes/banner.md)]

Šajā rakstā aprakstīti daži ieviešanas noteikumi, kurus būtu jāņem vērā, kad izmantojat valodu no labās uz kreiso pusi, un ir jāiestata finanšu dimensijas un galvenie konti.

Finanšu dimensijas un galvenie konti ir galvenie implementēšanas plānošanas fāzes komponenti. Kad sistēma ir izveidotas finanšu dimensijas un galvenie konti, tie tiek izmantoti lapās **Konfigurēt kontu struktūras**, **Detalizēto kārtulu struktūras** un **Finanšu dimensijas konfigurācija programmu integrēšanai**. Šajās lapas definētā secība sistēmā tiek izmantota datu ievadei un patēriņam. Noteiktās sistēmas vietās finanšu dimensijas un galvenie konti tiek rādīti atsevišķos laukos. Citviet, piemēram, žurnālos, finanšu dimensijas un galvenie konti tiek rādīti kā viena virkne.

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Finanšu dimensiju un galveno kontu iestatīšanas paraugprakse sistēmā ar rakstību no labās puses uz kreiso

- Kad atlasāt norobežotāju kontu plāniem, atlasiet kādu no dubultajām norobežotāju opcijām: dubulto pārnesumzīmi (`--`), dubulto šķirtni (`||`) vai divpunkti (`..`), vai dubulto pasvītrojuma zīmi (`\\`).
- Kad veidojat finanšu dimensijas un galvenā konta vērtības, izmantojiet tikai ciparus un rakstzīmes valodai ar rakstību no labās puses uz kreiso.
- Atlasīto kontu plāna norobežotāju nelietojiet finanšu dimensijas un galveno kontu vērtībās.

Ievērojot šo paraugpraksi, jūs palīdzat garantēt konsekventu lietotāja definēto pasūtījumu attēlojumu visā sistēmā.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

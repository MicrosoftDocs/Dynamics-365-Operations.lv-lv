---
title: Preču kvalitātes pārbaude
description: Šajā rakstā ir aprakstīts, kā apstrādāt kvalitātes pasūtījumus.
author: yufeihuang
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eeb14a3b0a61f34819bdd8d524e65ac214a81c35
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857581"
---
# <a name="inspect-the-quality-of-goods"></a>Preču kvalitātes pārbaude

[!include [banner](../../includes/banner.md)]

Šajā rakstā ir aprakstīts, kā apstrādāt kvalitātes pasūtījumus. Kvalitātes pārbaudes parasti veic kvalitātes darbinieks.

Ja standarta demonstrācijas dati ir instalēti, varat izmantot to, lai veiktu procedūras šajā rakstā. Lai izmantotu demonstrācijas datus, atlasiet *USMF* juridisko personu. Pēc tam apstipriniet pirkšanas pasūtījumu *000016* un grāmatojiet produktu ieejas plūsmu. Kvalitātes pārbaudes pasūtījumus tiek ģenerēts automātiski.

## <a name="step-1-select-a-quality-order"></a>1. darbība: Atlasiet kvalitātes pārbaudes pasūtījumu

Lai atlasītu kvalitātes pārbaudes pasūtījumu, izpildiet tālāk aprakstītās darbības.

1. Dodieties uz **Krājumu pārvaldība \> Periodiskie uzdevumi \> Kvalitātes pārvaldība \> Kvalitātes pārbaudes pasūtījumi**.
1. Atlasiet kvalitātes pārbaudes pasūtījumu, kas tika ģenerēts pirms šīs procedūras uzsākšanas.

## <a name="step-2-record-test-results"></a>2. darbība: Testa rezultātu reģistrēšana

Lai ierakstītu testa rezultātus, sekojiet šiem darbībām.

1. Atlasiet **Rezultāti**.
1. Atlasiet **Rediģēt**.
1. Laukā **Rezultātu daudzums** ierakstiet skaitli.
1. Laukā **Rezultāts** atlasiet vēlamo ierakstu. Šajā piemērā rezultāta pamatā ir iepriekš definēts iznākums. Parasti tiek ierakstīts specifiskāks testa rezultāts, piemēram, izmērs vai cita dimensija.
1. Atlasiet **Saglabāt**.
1. Aizvērt lapu.

## <a name="step-3-validate-the-quality-order"></a>3. darbība: Pārbaudīt kvalitātes pasūtījumu

Lai pārbaudītu kvalitātes pārbaudes pasūtījumu, izpildiet tālāk aprakstītās darbības.

1. Atlasiet **Pārbaudīt**.
1. Laukā **Pārbaudīts pēc** atlasiet lietotāju, kas veic pārbaudi.
1. Atlasiet **Atlasīt**.
1. Atlasiet **Labi**.
1. Aizvērt lapu.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

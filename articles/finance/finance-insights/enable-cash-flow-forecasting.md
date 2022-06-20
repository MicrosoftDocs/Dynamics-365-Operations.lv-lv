---
title: Naudas plūsmas prognozēšanas iespējošana
description: Šajā rakstā ir izskaidrots, kā ieslēgt naudas plūsmas prognozes līdzekli Finanšu ieskatījumā.
author: ShivamPandey-msft
ms.date: 02/11/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 253e3ea9c1c44573b37503f167b4cb3860683c10
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859880"
---
# <a name="enable-cash-flow-forecasting"></a>Naudas plūsmas prognozēšanas iespējošana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir izskaidrots, kā ieslēgt naudas plūsmas prognozes līdzekli Finanšu ieskatījumā.

> [!NOTE]
> Lai izmantotu maksājumu prognozes skaidras naudas plūsmā, jāiestata debitora maksājumu prognožu līdzeklis, kā tas aprakstīts [Debitora maksājumu prognožu iespējošana](enable-cust-paymnt-prediction.md).
  
1. Atveriet darbvietu **Līdzekļu pārvaldība** un veiciet tālāk norādītās darbības.

    1. Atlasiet **Pārbaudīt atjauninājumus**.
    2. **Cilnē Viss** meklējiet naudas **plūsmas prognozes**. Ja šo līdzekli neatrod, meklējiet (priekšskatījums **) naudas plūsmas prognozes**. 
    3. Ieslēgt funkciju.

2. Dodieties uz **Skaidras naudas un bankas pārvaldība \> Skaidras naudas plūsmas prognozes iestatīšana** un pievienojiet likviditātes kontus, kas jāiekļauj prognozēs. Iestatiet arī likviditātes kontu maksājumiem cilnēs **Debitori** un **Parādi** kreditoriem. Noteikti pārrēķiniet naudas plūsmas prognozi.

    > [!NOTE]
    > Ja likviditātes konti nav iestatīti, skaidras naudas plūsmu nevar ģenerēt.
    >
    > Papildinformāciju par to, kā iestatīt naudas plūsmas prognozes, skatiet sadaļā Naudas [plūsmas prognozēšana](../cash-bank-management/cash-flow-forecasting.md).

3. Dodieties uz **Skaidras naudas un bankas pārvaldība \> Iestatīšana \> Finanšu ieskati (priekšskatījums) \> Skaidras naudas plūsmas prognozes (priekšskatījums)** un veiciet tālāk norādītās darbības.

    1. Cilnē **Skaidras naudas plūsmas prognoze** atlasiet **Iespējot līdzekli**.
    2. Atlasiet **Izveidot prognozēšanas modeli**.

> [!NOTE]
> Naudas **plūsmas prognozes modeļa** apmācībai nepieciešami dati ar 100 vai vairāk darbībām, kas aptver vairāk par vienu gadu. Ieteicams, lai jums būtu vismaz divi gadi datu ar vairāk nekā 1000 darbībām.

Plašāku informāciju par to, kā iestatīt skaidras naudas plūsmas prognozēšanas iespēju, skatiet [Skaidras naudas plūsmas prognozēšana](cash-flow-forecast-intro.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

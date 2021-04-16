---
title: Skaidras naudas plūsmas prognozēšanas iespējošana (priekšskatījums)
description: Šajā tēmā skaidrots, kā ieslēgt skaidras naudas plūsmas prognozēšanas līdzekli Finanšu ieskatos.
author: ShivamPandey-msft
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f7c06eaeb79c1a2aa319cfa3d2ad8255bf716cd0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818732"
---
# <a name="enable-cash-flow-forecasting-preview"></a>Skaidras naudas plūsmas prognozēšanas iespējošana (priekšskatījums)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Šajā tēmā skaidrots, kā ieslēgt skaidras naudas plūsmas prognozēšanas līdzekli Finanšu ieskatos.

> [!NOTE]
> Lai izmantotu maksājumu prognozes skaidras naudas plūsmā, jāiestata debitora maksājumu prognožu līdzeklis, kā tas aprakstīts [Debitora maksājumu prognožu iespējošana](enable-cust-paymnt-prediction.md).

1. Izmantojiet informāciju no vides lapas Microsoft Dynamics Lifecycle Services (LCS), lai izveidotu savienojumu ar Azure SQL primāro instanci šai videi. Palaidiet tālāk norādīto Transact-SQL (T-SQL) komandu, lai ieslēgtu ierobežotos līdzekļus smilškastes videi. (Iespējams, būs LCS jāieslēdz piekļuve savai IP adresei pirms varēsiet izveidot attilināto savienojumu ar programmas objektu serveri \[AOS\].)

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > Ja jūsu Microsoft Dynamics 365 Finance izvietošana ir Service Fabric izvietošana, varat izlaist šo darbību. Finanšu ieskatu grupai jau vajadzētu ieslēgt jums šo ierobežoto līdzekli. Ja neredzat līdzekļus darbvietā **Līdzekļu pārvaldība** vai ja rodas problēmas, mēģinot tos ieslēgt, sazinieties ar <fiap@microsoft.com>.
  
2. Atveriet darbvietu **Līdzekļu pārvaldība** un veiciet tālāk norādītās darbības.

    1. Atlasiet **Pārbaudīt atjauninājumus**.
    2. Ieslēdziet tālāk norādītos līdzekļus.

        - Jauna režģa vadīkla
        - Grupēšana režģos (priekšskatījums) 
        - Debitoru maksājumu prognozes (priekšskatījums)
        - Skaidras naudas plūsmas prognozēšana (priekšskatījums)

3. Dodieties uz **Skaidras naudas un bankas pārvaldība \> Skaidras naudas plūsmas prognozes iestatīšana** un pievienojiet likviditātes kontus, kas jāiekļauj prognozēs.

    > [!NOTE]
    > Ja likviditātes konti nav iestatīti, skaidras naudas plūsmu nevar ģenerēt.

4. Dodieties uz **Skaidras naudas un bankas pārvaldība \> Iestatīšana \> Finanšu ieskati (priekšskatījums) \> Skaidras naudas plūsmas prognozes (priekšskatījums)** un veiciet tālāk norādītās darbības.

    1. Cilnē **Skaidras naudas plūsmas prognoze** atlasiet **Iespējot līdzekli**.
    2. Atlasiet **Izveidot prognozēšanas modeli**.

Plašāku informāciju par to, kā iestatīt skaidras naudas plūsmas prognozēšanas iespēju, skatiet [Skaidras naudas plūsmas prognozēšana](cash-flow-forecast-intro.md).

## <a name="privacy-notice"></a>Paziņojums par konfidencialitāti

Priekšskatījumiem (1) var tikt izmantots mazāk konfidencialitātes un drošības pasākumu nekā pakalpojumam Dynamics 365 Finance and Operations, (2) tie nav ietverti pakalpojuma līmeņa līgumā par šo pakalpojumu, (3) tos nedrīkst izmantot personas datu vai citu tādu datu apstrādei, uz kuriem attiecas juridiskās vai normatīvās prasības, un (4) tiem tiek nodrošināts ierobežots atbalsts.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
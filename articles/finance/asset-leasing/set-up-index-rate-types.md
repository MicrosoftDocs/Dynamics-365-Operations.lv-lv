---
title: Indeksu likmju iestatīšana
description: Šajā tēmā ir paskaidrots, kā iestatīt indeksu likmes. Indeksu likmes ir nepieciešamas, ja jūsu organizācija piesaista nomas maksājumu summas ar indeksu likmju kopu.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseIndexRateType
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 40f230a9d69a142b18eb27a2d5e420dbadc600d2
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880964"
---
# <a name="set-up-index-rates"></a>Indeksu likmju iestatīšana

[!include [banner](../includes/banner.md)]

Ja nomas maksājumi ir atkarīgi no indeksa, indeksu likmes tipus sistēmā var pievienot un uzturēt. Lai pārvērtētu nomas maksājumus lapā **Indeksa likmes tips**, indeksa likmes pārvērtēšanas process izmanto visjaunāko indeksa likmi no pārvērtēšanas datuma.

Lai pievienotu indeksu likmju tipus un indeksu likmes, rīkojieties šādi.

1. Dodieties uz **Līdzekļu noma \> Iestatījumi \> Indeksa likmes tips**.
2. Atlasiet **Jauns**.
3. Atbilstošajos laukos ievadiet likmes tipu un indeksa likmes nosaukumu.
4. Lai pievienotu jaunu indeksa likmes vērtību, atlasiet indeksa likmes tipu un pēc tam atlasiet **Pievienot**.
5. Atlasiet spēkā stāšanas sākuma datumu un atlasiet likmes vērtību.

Kā indeksa likmes metode ir jāatlasa **Indeksa likmes vērtību starpība** vai **Indeksa likmes vērtība**.

- Atlasiet metodi **Indeksa likmes vērtību starpība**, lai aprēķinātu jaunu nomas maksājumu, pamatojoties uz starpību starp indeksa likmi sākuma datumā un visjaunāko indeksa likmi. Indeksa likme ir definēta laukā **Indeksa likme (%)**.
- Atlasiet metodi **Indeksa likmes vērtība**, lai aprēķinātu nomas maksājumu, izmantojot procentuālo vērtību, kas norādīta laukā **Indeksa likme (%)**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

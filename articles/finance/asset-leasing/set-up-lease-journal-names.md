---
title: Nomas žurnālu nosaukumu iestatīšana
description: Šajā tēmā skaidrots, kā definēt nomas žurnāla nosaukumus. Nomas žurnāla nosaukumi norāda žurnālus, kuros tiek grāmatoti ieraksti, kas radušies līdzekļu nomā.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: c139df124b249ec9dc5d16096e6f45f22d435456
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880890"
---
# <a name="set-up-lease-journal-names"></a>Nomas žurnālu nosaukumu iestatīšana

[!include [banner](../includes/banner.md)]

Nomas žurnāla nosaukumi norāda žurnālus, kuros tiek grāmatoti līdzekļu nomas darījumi. Tikai tie žurnālu nosaukumi, kas ir piešķirti žurnāla tipam **Līdzekļu noma**, tiek parādīti laukos **Sākotnējā atzīšana** un **Ikmēneša žurnāla nosaukums**, kas atrodas lapā **Līdzekļu nomas parametri**. Laukam **Rēķina žurnāla nosaukums** var piešķirt tikai žurnāla tipu **Kreditora žurnāla ieraksts**.

Lai konfigurētu nomas žurnālu nosaukumus, rīkojieties šādi.

1. Dodieties uz **Līdzekļu noma \> Iestatījumi \> Līdzekļu nomas parametri**.
2. Cilnes **Vispārīgi** laukā **Sākotnējais atzīšanas žurnāla nosaukums** atlasiet žurnālu. Visi sākotnējās atzīšanas žurnāla ieraksti tiks grāmatoti šajā žurnāla nosaukumā.
3. Laukā **Rēķina žurnāla nosaukums** atlasiet žurnālu. Ja opcija **Maksāt kreditoram** ir iestatīta uz **Jā** nomas grāmatai, nomas un izdevumu maksājumu rēķini tiks grāmatoti šajā žurnāla nosaukumā.
4. Laukā **Nomas žurnāla nosaukums** atlasiet žurnālu. Visi nolietojuma, procentu un īstermiņa pārklasificēšanas ieraksti tiks grāmatoti šajā žurnāla nosaukumā. Ja opcija **Maksāt kreditoram** ir iestatīta uz **Nē** nomas grāmatai, nomas maksājumu un izdevumu ieraksti arī tiks grāmatoti šajā žurnāla nosaukumā.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

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
ms.openlocfilehash: 1ea35ec40ddd459e1a9e7641557147e23fe45d3e
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343218"
---
# <a name="set-up-lease-journal-names"></a>Nomas žurnālu nosaukumu iestatīšana

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]


Nomas žurnāla nosaukumi norāda žurnālus, kuros tiek grāmatoti līdzekļu nomas darījumi. Tikai tie žurnālu nosaukumi, kas ir piešķirti žurnāla tipam **Līdzekļu noma**, tiek parādīti laukos **Sākotnējā atzīšana** un **Ikmēneša žurnāla nosaukums**, kas atrodas lapā **Līdzekļu nomas parametri**. Laukam **Rēķina žurnāla nosaukums** var piešķirt tikai žurnāla tipu **Kreditora žurnāla ieraksts**.

Sistēma bloķē noteiktus finanšu laukus, lai novērstu novirzes starp darbībām un grafikiem. Dažos bloķētos laukos ir iekļauts: **Konts**, **Summa**, **Finanšu dimensijas**, **Valūta** un **Darbības tips**. Turklāt nevarēsit pievienot vai dzēst žurnāla ierakstu rindas jebkurās Pamatlīdzekļu izlaižot žurnāla ierakstos, jo tas var izraisīt novirzes starp grafikiem un darbībām.


Lai konfigurētu nomas žurnālu nosaukumus, rīkojieties šādi.

1. Dodieties uz **Līdzekļu noma \> Iestatījumi \> Līdzekļu nomas parametri**.
2. Cilnes **Vispārīgi** laukā **Sākotnējais atzīšanas žurnāla nosaukums** atlasiet žurnālu. Visi sākotnējās atzīšanas žurnāla ieraksti tiks grāmatoti šajā žurnāla nosaukumā.
3. Laukā **Rēķina žurnāla nosaukums** atlasiet žurnālu. Ja opcija **Maksāt kreditoram** ir iestatīta uz **Jā** nomas grāmatai, nomas un izdevumu maksājumu rēķini tiks grāmatoti šajā žurnāla nosaukumā.
4. Laukā **Nomas žurnāla nosaukums** atlasiet žurnālu. Visi nolietojuma, procentu un īstermiņa pārklasificēšanas ieraksti tiks grāmatoti šajā žurnāla nosaukumā. Ja opcija **Maksāt kreditoram** ir iestatīta uz **Nē** nomas grāmatai, nomas maksājumu un izdevumu ieraksti arī tiks grāmatoti šajā žurnāla nosaukumā.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

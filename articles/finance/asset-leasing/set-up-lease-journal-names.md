---
title: Nomas žurnālu nosaukumu iestatīšana
description: Šajā tēmā skaidrots, kā definēt nomas žurnāla nosaukumus. Nomas žurnāla nosaukumi norāda žurnālus, kuros tiek grāmatoti ieraksti, kas radušies līdzekļu nomā.
author: moaamer
ms.date: 12/03/2021
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
ms.openlocfilehash: a92461e742f1675e4cfda89e6c80c5b087ff5bfb
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644902"
---
# <a name="set-up-lease-journal-names"></a>Nomas žurnālu nosaukumu iestatīšana

[!include [banner](../includes/banner.md)]


Nomas žurnāla nosaukumi norāda žurnālus, kuros tiek grāmatoti līdzekļu nomas darījumi. Tikai tie žurnālu nosaukumi, kas ir piešķirti žurnāla tipam **Līdzekļu noma**, tiek parādīti laukos **Sākotnējā atzīšana** un **Ikmēneša žurnāla nosaukums**, kas atrodas lapā **Līdzekļu nomas parametri**. Laukam **Rēķina žurnāla nosaukums** var piešķirt tikai žurnāla tipu **Kreditora žurnāla ieraksts**.

Sistēma bloķē noteiktus finanšu laukus, lai novērstu novirzes starp darbībām un grafikiem. Dažos bloķētos laukos ir iekļauts: **Konts**, **Summa**, **Finanšu dimensijas**, **Valūta** un **Darbības tips**. Turklāt nevarēsit pievienot vai dzēst žurnāla ierakstu rindas jebkurās Pamatlīdzekļu izlaižot žurnāla ierakstos, jo tas var izraisīt novirzes starp grafikiem un darbībām.


Lai konfigurētu nomas žurnālu nosaukumus, veiciet sekojošos soļus.

1. Dodieties uz **Līdzekļu noma \> Iestatījumi \> Līdzekļu nomas parametri**.
2. Cilnes **Vispārīgi** laukā **Sākotnējais atzīšanas žurnāla nosaukums** atlasiet žurnālu. Visi sākotnējās atzīšanas žurnāla ieraksti tiks grāmatoti šajā žurnāla nosaukumā.
3. Laukā **Rēķina žurnāla nosaukums** atlasiet žurnālu. Ja opcija **Maksāt kreditoram** ir iestatīta uz **Jā** nomas grāmatai, nomas un izdevumu maksājumu rēķini tiks grāmatoti šajā žurnāla nosaukumā.
4. Laukā **Nomas žurnāla nosaukums** atlasiet žurnālu. Visi nolietojuma, procentu un īstermiņa pārklasificēšanas ieraksti tiks grāmatoti šajā žurnāla nosaukumā. Ja opcija **Maksāt kreditoram** ir iestatīta uz **Nē** nomas grāmatai, nomas maksājumu un izdevumu ieraksti arī tiks grāmatoti šajā žurnāla nosaukumā.
5. Laukā **Nomas modifikāciju žurnāla** nosaukums atlasiet žurnālu. Nomas pielāgošanas, darba attiecību pārtraukšanas un pasliktināšanās darbības tiks grāmatotas šim žurnāla nosaukumam. Jūsu atlasītam žurnāla nosaukumam nedrīkst būt piešķirta darbplūsma vai apstiprinājums. Ja nomas modifikāciju žurnāla nosaukums nav definēts, nomas pielāgojuma, darba attiecību pārtraukšanas un pasliktināšanās darbības tiks grāmatotas žurnāla nosaukumā, **kas ir atlasīts laukā Nomas žurnāla** nosaukums. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

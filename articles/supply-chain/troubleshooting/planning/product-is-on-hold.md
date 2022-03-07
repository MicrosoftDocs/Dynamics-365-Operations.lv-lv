---
title: Prece ir aizturēta šāda veida darījumiem
description: Pēc plānošanas pasūtījumu apstiprināšanas tiek saņemts kļūdas ziņojums, kurā norādīts, ka krājums ir aizturēts darījumiem.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 8e012a65041c2f32e21d2631eda18eea488e28e35f6a53bbe9a67c08159765e1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6752614"
---
# <a name="product-is-on-hold-for-transactions"></a>Prece ir aizturēta šāda veida darījumiem

Kļūdas kods: SYS13295

## <a name="symptoms"></a>Simptomi

Pēc plānoto pasūtījumu apstiprināšanas saņemsit šādu kļūdas ziņojumu:

> Krājums %1 pašlaik ir aizturēts darbībām %2.

## <a name="cause"></a>Iemesls

Aprakstot bloķētos krājumus, sistēma lieto tādus savstarpēji aizvietojamus jēdzienus kā *bloķēti*, *apturēti* un *aizturēti*. Šī kļūda nozīmē, ka noklusējuma pasūtījuma iestatījumos krājums ir iestatīts kā **Apturēts**.

Ja krājums tiek bloķēts un jūs pievienojat to pirkšanas pasūtījuma vai pārdošanas pasūtījuma rindai, saņemat brīdinājuma ziņojumu. Kad krājums ir bloķēts, inventāra transakcijas, kas saistītas ar pirkšanas pasūtījumu vai pārdošanas pasūtījumu līniju, nevar modificēt (piemēram, gramatojot pavadzīmi vai rēķinu). Varat bloķēt iegādātu krājumu un vienlaicīgi pārdot šo krājumu. Tādā gadījumā izvēles rūtiņa **Apturēts** tiek atlasīta pirkšanas pasūtījumā, bet krājums nav bloķēts krājumos vai pārdošanas pasūtījumā.

Tālāk ir norādīti daži nosacījumi, kuru dēļ krājuma kods var tikt bloķēts pārdošanai:

- Krājums joprojām tiek izstrādāts vai ražots. Tādēļ nevēlaties to pārdot vai rezervēt.
- Jūs esat saņēmis daudzus bojātus krājumus, un defekti jāizlabo, pirms krājumu var pārdot.

Šāda veida gadījumos, jūs varat bloķēt šo krājumu līdz brīdim, kad problēma ir novērsta.

Ja krājums ir bloķēts un jūs izveidojat atgriešanas pasūtījuma rindu, jūs saņemat ziņojumu. Nevar bloķēt krājumu sēriju vai laidienu. Ja krājuma daļas ir jābloķē, var bloķēt tās, pārvietojot krājumu vai bloķējot pilnu krājumu tam periodam.

## <a name="resolution"></a>Novēršana

- Atveriet lapu **Noklusējuma pasūtījuma iestatījumi** un noņemiet izvēles rūtiņas **Apturēts** atzīmi.

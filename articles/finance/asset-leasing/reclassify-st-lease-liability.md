---
title: Īstermiņa nomas saistību pārklasificēšana
description: Šajā tēmā skaidrots, kā izveidot mēneša žurnāla ierakstu, lai pārklasificētu nomas saistību daļu kā īstermiņa.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 46bcd396c93bc1d2944241165d438f8ccc013e20
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445783"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Īstermiņa nomas saistību pārklasificēšana

[!include [banner](../includes/banner.md)]

Šajā tēmā skaidrots, kā izveidot mēneša žurnāla ierakstu, lai pārklasificētu nomas saistību daļu kā īstermiņa. Kad pakešuzdevuma procesā atlasītais grafiks ir **Īstermiņa nomas saistību pārklasificēšana**, tiek izveidots žurnāla ieraksts. Šo ierakstu izmanto, lai grāmatotu nomas saistību pašreizējo daļu mēneša pēdējā dienā. Tajā pašā laikā atgriešanas ieraksts tiek grāmatots no nākamā mēneša pirmās dienas.

Nomas saistību īstermiņa daļa tiek rādīta saistību amortizācijas grafikā. Kad žurnāla ieraksts ir iegrāmatots, kļūst pieejama kolonna **Izveidots saistību pārkvalificēšanas žurnāls**, un žurnāla ID tiek norādīts arī grafikā.

Lai izveidotu un grāmatotu īstermiņa saistību pārklasificēšanas žurnāla ierakstu, rīkojieties šādi.

1. Doties uz **Līdzekļa noma \> Periodisks \> Žurnāla izveide partijā**.
2. Dialoglodziņa **Žurnāla izveide partijā** laukā **Atlasīt grafiku** atlasiet **Īstermiņa nomas saistību pārklasificēšana**.
3. Laukā **Nomas grupa** atlasiet nomas grupu. Vai arī laukā **Grāmatas ID** atlasiet grāmatas ID.
4. Ieslēdziet parametru **Grāmatot**. Pretējā gadījumā, ja ieraksts ir jāizveido, bet nav jāgrāmato, atstājiet šo parametru izslēgtu.
5. Ieslēdziet parametru **Priekšskatīt pirms grāmatošanas**, lai skatītu ierakstu pirms tā grāmatošanas.
6. Atlasiet **Labi**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
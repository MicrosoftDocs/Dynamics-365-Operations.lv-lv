---
title: Īstermiņa nomas saistību pārklasificēšana
description: Šajā rakstā skaidrots, kā izveidot ikmēneša žurnāla ierakstu, lai pārklasificētu nomas saistību daļu kā īstermiņa.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Dialog
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 7c7c3f86aa5d24e9aeed89526a4b7317699e9a78
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886347"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a>Īstermiņa nomas saistību pārklasificēšana

[!include [banner](../includes/banner.md)]

Šajā rakstā skaidrots, kā izveidot ikmēneša žurnāla ierakstu, lai pārklasificētu nomas saistību daļu kā īstermiņa. Kad pakešuzdevuma procesā atlasītais grafiks ir **Īstermiņa nomas saistību pārklasificēšana**, tiek izveidots žurnāla ieraksts. Šo ierakstu izmanto, lai grāmatotu nomas saistību pašreizējo daļu mēneša pēdējā dienā. Tajā pašā laikā atgriešanas ieraksts tiek grāmatots no nākamā mēneša pirmās dienas.

Nomas saistību īstermiņa daļa tiek rādīta saistību amortizācijas grafikā. Kad žurnāla ieraksts ir iegrāmatots, kļūst pieejama kolonna **Izveidots saistību pārkvalificēšanas žurnāls**, un žurnāla ID tiek norādīts arī grafikā.

Lai izveidotu un grāmatotu īstermiņa saistību pārklasificēšanas žurnāla ierakstu, rīkojieties šādi.

1. Doties uz **Līdzekļa noma \> Periodisks \> Žurnāla izveide partijā**.
2. Dialoglodziņa **Žurnāla izveide partijā** laukā **Atlasīt grafiku** atlasiet **Īstermiņa nomas saistību pārklasificēšana**.
3. Laukā **Nomas grupa** atlasiet nomas grupu. Vai arī laukā **Grāmatas ID** atlasiet grāmatas ID.
4. Ieslēdziet parametru **Grāmatot**. Pretējā gadījumā, ja ieraksts ir jāizveido, bet nav jāgrāmato, atstājiet šo parametru izslēgtu.
5. Atlasiet **Labi**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

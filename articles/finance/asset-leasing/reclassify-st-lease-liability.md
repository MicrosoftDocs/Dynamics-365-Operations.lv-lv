---
title: Īstermiņa nomas saistību pārklasificēšana
description: Šajā tēmā skaidrots, kā izveidot mēneša žurnāla ierakstu, lai pārklasificētu nomas saistību daļu kā īstermiņa.
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
ms.openlocfilehash: 3a71b809b4bb16c2b918b7acd4fbb8bc49278ff6
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727739"
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
5. Atlasiet **Labi**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

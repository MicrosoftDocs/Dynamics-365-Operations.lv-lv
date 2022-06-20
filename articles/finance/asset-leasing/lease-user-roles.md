---
title: Nomas lietotāju lomu piešķiršana
description: Šajā rakstā ir aprakstītas drošības lomas, kas tiek izmantotas Izlaižot Pamatlīdzekļus. Izskaidrots arī, kā piešķirt lietotājiem šīs lomas.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 38c859d64742d582d0709506d83600ea26a21147
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8878136"
---
# <a name="assign-lease-user-roles"></a>Nomas lietotāju lomu piešķiršana

[!include [banner](../includes/banner.md)]

Šajā rakstā ir aprakstītas drošības lomas, kas tiek izmantotas Izlaižot Pamatlīdzekļus. Izskaidrots arī, kā piešķirt lietotājiem šīs lomas.

Trīs lietotāju lomas nodrošina atšķirīgu piekļuvi līdzekļu nomai. Viena loma ir piemērota nomu uzturēšanai, otra ir piemērota nomu skatīšanai, bet trešā ir piemērota nomas sekretāra pienākumu veikšanai. Katrai lomai ir noteiktas atļaujas visām nomas lapām, un katra no tām ļauj lietotājiem skatīt, izveidot, rediģēt vai dzēst nomu saskaņā ar darba pienākumiem.

| Loma           | Apraksts |
|----------------|-------------|
| Nomas uzturēšana | Lietotāji ar šo lomu var pievienot, rediģēt, dzēst un apskatīt nomu. Šī loma ir paredzēta ikdienas lietotājiem, kuru uzdevumi ir ikmēneša žurnāla ierakstu izveide un grāmatošana, kā arī jaunu nomu pievienošana. Šī loma sniedz piekļuvi visām līdzekļu nomas funkcionalitātēm. |
| Nomas skatīšana     | Lietotāji ar šo nomu var tikai skatīt nomas ierakstus, grafikus un palaist pārskatus. Viņi nevar izveidot jaunas nomas, rediģēt esošās nomas vai izveidot žurnāla ierakstus nomām. Loma ir paredzēta lietotājiem, kuriem ir tikai jāskata nomas, nomu grafiki un darījumi, kas notiek attiecībā saistība ar šīm nomām. |
| Nomas darbinieks    | Lietotāji ar šo lomu var tikai izveidot tikai jaunas nomas. Viņi nevar labot vai dzēst esošās nomas, skatīt nomu grafikus vai grāmatot nomu žurnālu ierakstus. Šī loma ir paredzēta lietotājiem, kuri strādā datu ievadē. |

Veiciet šīs darbības, lai piešķirtu lietotājus lomām, kas tiek izmantotas līdzekļu nomā.

1. Dodieties uz **Sistēmas administrēšana \> Drošība \> Piešķirt lomas lietotājiem**.
2. Atlasiet lomu **Nomas uzturēšana**, **Nomas darbinieks** vai **Nomas skatīšana** un pēc tam atlasiet **Manuāli piešķirt/izslēgt lietotājus**.
3. Atlasiet lietotāju, kuram piešķirt lomu, un pēc tam atlasiet **Piešķirt lomai**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Kreditoru transakciju saraksta lapa
description: "Šajā tēmā ir sniegta informācija par kreditora transakciju saraksta lapu sistēmai Microsoft Dynamics 365 for Finance and Operations."
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: 1ef7d97f059801f2fb2c0d451546b57055208f81
ms.contentlocale: lv-lv
ms.lasthandoff: 09/22/2018

---

# <a name="vendor-transaction-list-page"></a>Kreditoru transakciju saraksta lapa

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Skatīt nosegšanas darbības

Darbību rūts cilne **Skatīt segšanas** nodrošina ātru piekļuvi segšanas vēsturei un papildu informācijai par visu segšanas transakciju. Varat arī parādīt papildu transakcijas, kas ir saistītas ar atlasīto transakciju, vai nu tāpēc, ka tās ir šīs segšanas daļa, vai arī tie ir maksājumi, kas izveidoti tajā pašā maksājumu žurnālā.

1. Atlasiet cilni **Kreditori \> Visi kreditori**.
2. Atlasiet kreditoru, kuram ir transakcijas, un pēc tam atlasiet cilni **Kreditors \>Transakcija**.
3. Atlasiet meklējamo transakciju.
4. Atlasiet darbību rūts cilni **Skatīt segšanas**.

    Tiek atvērts dialoglodziņš **Skatīt segšanas**, kurā ir redzama atlasītā transakcija un visi dokumenti, kas to sedz. Šis dialoglodziņš līdzinās segšanas vēstures skatam, bet tas ietver visus saistītos dokumentus.

5. No šī dialoglodziņa var veikt dažādus uzdevumus. Atlasiet vienu vai vairākus vaučerus un pēc tam atlasiet vienu no tālāk norādītajām izvēlnēm.

   - **Skatīt uzskaiti** – tiek parādīti visi ar atlasītajiem dokumentiem saistītie vaučeri. Atlasiet **Aizvērt**, lai aizvērtu dialoglodziņu.
   - **Eksportēt** – eksportēt atlasītos vaučerus uz programmu Microsoft Excel.
   - **Skatīt saistītos maksājumus** – tiek parādītas visas maksājumu žurnāla transakcijas, kas tika izveidotas maksājumu žurnālā, kas ir saistīts ar atlasīto dokumentu. Turklāt tiek parādītas visas segšanas, kas ir saistītas ar šiem maksājumiem. Šīs izvēlnes marķējums arī tiek mainīts uz **Skatīt segšanas**. Atlasiet **Skatīt segšanas**, lai parādītu tikai tās transakcijas, kuras tika parādītas, kad pirmoreiz atvērāt dialoglodziņu **Skatīt segšanas**.
    - **Transakciju segšana** – šī izvēlne tiek parādīta, ja oriģinālais dokuments, kas tika atlasīts, netika pilnībā segts. To atlasot, tiek parādīts dialoglodziņš **Transakciju segšana**, kurā var atlasīt transakcijas segšanai.
    - **Transakciju atsaukšana** – šī izvēlne tiek parādīta, ja oriģinālais dokuments, kas tika atlasīts, tika pilnībā segts. To atlasot, tiek parādīts dialoglodziņš **Segšanu atsaukšana**, kurā var atsaukt segšanas darbības, kas tika veiktas šim dokumentam.


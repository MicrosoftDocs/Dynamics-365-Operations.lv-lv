---
title: Debitoru transakciju saraksta lapa
description: "Šajā tēmā ir sniegta informācija par debitora transakciju saraksta lapu programmai Microsoft Dynamics 365 for Finance and Operations."
author: mikefalkner
manager: aolson
ms.date: 08/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: 8.0.4
ms.translationtype: HT
ms.sourcegitcommit: 98ed3378ab05c0c69c9e5b2a82310113a81c2264
ms.openlocfilehash: e828cb292ad48bb4690117b41589b25edcdf28bc
ms.contentlocale: lv-lv
ms.lasthandoff: 09/22/2018

---

# <a name="customer-transaction-list-page"></a>Debitoru transakciju saraksta lapa

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a>Skatīt nosegšanas darbības

Darbību rūts cilne **Skatīt segšanas** nodrošina ātru piekļuvi segšanas vēsturei un papildu informācijai par visu segšanas transakciju. Varat arī parādīt papildu transakcijas, kas ir saistītas ar atlasīto transakciju, vai nu tāpēc, ka tās ir šīs segšanas daļa, vai arī tie ir maksājumi, kas izveidoti tajā pašā maksājumu žurnālā.

1. Atlasiet **Debitoru parādi \> Debitori**.
2. Atlasiet debitoru, kuram ir transakcijas, un pēc tam atlasiet cilni **Debitors \> Transakcija**.
3. Atlasiet meklējamo transakciju.
4. Atlasiet darbību rūts cilni **Skatīt segšanas**.

    Dialoglodziņa **Skatīt segšanas** ir redzama atlasītā transakcija un visi dokumenti, kas to sedz. Šis dialoglodziņš līdzinās segšanas vēstures skatam, bet tas ietver visus saistītos dokumentus. 

5. No šī dialoglodziņa var veikt dažādus uzdevumus. Atlasiet vienu vai vairākus vaučerus un pēc tam atlasiet vienu no tālāk norādītajām izvēlnēm.

   - **Skatīt uzskaiti** – tiek parādīti visi ar atlasītajiem dokumentiem saistītie vaučeri. Atlasiet **Aizvērt**, lai aizvērtu dialoglodziņu.
   - **Eksportēt** – eksportēt atlasītos vaučerus uz programmu Microsoft Excel.
   - **Skatīt saistītos maksājumus** – tiek parādītas visas maksājumu žurnāla transakcijas, kas tika izveidotas maksājumu žurnālā, kas ir saistīts ar atlasīto dokumentu. Turklāt tiek parādītas visas segšanas, kas ir saistītas ar šiem maksājumiem. Šīs izvēlnes marķējums arī tiek mainīts uz **Skatīt segšanas**. Atlasiet **Skatīt segšanas**, lai parādītu tikai tās transakcijas, kuras tika parādītas, kad pirmoreiz atvērāt dialoglodziņu **Skatīt segšanas**.
    - **Transakciju segšana** – šī izvēlne tiek parādīta, ja oriģinālais dokuments, kas tika atlasīts, netika pilnībā segts. To atlasot, tiek parādīts dialoglodziņš **Transakciju segšana**, kurā var atlasīt transakcijas segšanai.
    - **Transakciju atsaukšana** – šī izvēlne tiek parādīta, ja oriģinālais dokuments, kas tika atlasīts, tika pilnībā segts. To atlasot, tiek parādīts dialoglodziņš **Segšanu atsaukšana**, kurā var atsaukt segšanas darbības, kas tika veiktas šim dokumentam.
    


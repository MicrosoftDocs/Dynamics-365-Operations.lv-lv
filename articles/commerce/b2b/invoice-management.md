---
title: Rēķinu pārvaldība B2B e-komercijas tīmekļa vietnēm
description: Šajā tēmā aprakstītas rēķinu pārvaldības iespējas bizness-biznesam Microsoft Dynamics 365 Commerce (B2B) e-komercijas vietnes.
author: shajain
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 60cb0c8aaede4a0eaeed80cf5ebe41068da57836
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8686304"
---
# <a name="invoice-management-for-b2b-e-commerce-websites"></a>Rēķinu pārvaldība B2B e-komercijas tīmekļa vietnēm

[!include [banner](../../includes/banner.md)]

Šajā tēmā aprakstītas rēķinu pārvaldības iespējas bizness-biznesam Microsoft Dynamics 365 Commerce (B2B) e-komercijas vietnes.

Tā ir izplatīta prakse uzņēmumiem, kuri apstrādā B2B darbības, lai pieņemtu pasūtījumus debitora kredītā un pēc tam nosūtītu rēķinu debitoriem pēc pasūtījuma izpildes. Maksājuma nosacījumi ir noteikti debitoriem, un var būt dažas atlaides, lai motivāciju debitoriem maksāt laikā vai pirms laika. Lai palīdzētu palielināt iespējamību, ka maksājumi tiks saņemti laikā, B2B e-komercijas vietnes ļauj debitoriem skatīt visus rēķinus. Debitors var viegli filtrēt rēķinus, lai skatītu apmaksātos, neapmaksātos un daļēji apmaksātos rēķinus kopā ar apmaksas datumiem.

![Rēķinu lapa B2B vietnē.](../media/ViewInvoices.png)

> [!NOTE]
> Pierakstījies lietotājs var skatīt un apmaksāt tikai savus rēķinus. Ja organizācijas **konts** **ir** konfigurēts nolaižamajā izvēlnē Rēķina konts kopsavilkuma cilnē Rēķins un piegāde, kas atrodas programmas Commerce Headquarters debitora ierakstā, lietotājs varēs skatīt un apmaksāt rēķinus organizācijas kontam.

**B2B vietnes** rēķinu lapā lietotājs var atlasīt neapmaksātu vai daļēji apmaksātu rēķinu un pēc tam atlasīt Maksājumu **rēķinu**. Atlasītais rēķins tiek pievienots grozam, un lietotājs var turpināt maksājumu. Lietotājs pēc tam var izlemt, vai apmaksāt pilnu rēķina summu vai daļējo summu. Lietotājs nevar izmantot starpkonta maksājuma metodi, lai apmaksātu rēķinus.

> [!NOTE]
> Rēķinus grozam var pievienot tikai tad, ja tajā nav nevienas preces. Otrādi, preces var pievienot grozam tikai tad, ja tajā pašlaik nav rēķinu. Microsoft plāno noņemt šo ierobežojumu turpmākajos Commerce laidienos.

![Groza lapa B2B vietnē.](../media/PayInvoice.png)

**Lapā Rēķini** lietotājs var arī atlasīt līdzās **rēķinam** opciju Pieprasīt rēķinu. Šādā veidā lietotājs var pieprasīt detalizētu informāciju par rēķinu, kas tiek nosūtīts uz viņu reģistrēto e-pasta adresi.

![Pieprasījuma rēķina dialoglodziņš](../media/RequestInvoice2.png)

Pēc tam, kad lietotājs pieprasa rēķinu, pieprasījums tiek pārvietots uz **mana konta lapas sadaļu** **B2B** Pieprasījumi. Pēc tam pēc **P-0001** **un** Sinhronizējiet pasūtījumus un kanāla pieprasījumus tiek palaisti programmā Commerce Headquarters, rēķina e-pasta ziņojums tiek parādīts un B2B pieprasījuma statuss tiek atzīmēts kā pabeigts.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

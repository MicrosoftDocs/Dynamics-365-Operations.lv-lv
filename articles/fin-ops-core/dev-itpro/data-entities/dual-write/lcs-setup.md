---
title: Duālās rakstīšanas iestatījums no Lifecycle Services
description: Šajā tēmā skaidrots, kā iestatīt divu rakstīšanas savienojumu starp jaunu Finance and Operations vidi un jaunu Common Data Service vidi no Microsoft Dynamics Lifecycle Services (LCS).
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: c78752aa1544b12f61071fa06617af4ac2809233
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172996"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Duālās rakstīšanas iestatījums no Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Šajā tēmā skaidrots, kā iestatīt divu rakstīšanas savienojumu starp jaunu Finance and Operations vidi un jaunu Common Data Service vidi no Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Priekšnosacījumi

Jums ir jābūt administratoram, lai iestatītu duālās rakstīšanas savienojumu.

+ Jums ir nepieciešama piekļuve nomniekam.
+ Jums ir jābūt administratoram gan Finance and Operations, gan Common Data Service vidēs.

## <a name="set-up-a-dual-write-connection"></a>Izveidot duālās rakstīšanas savienojumu

Sekojiet šīm darbībām, lai iestatītu duālās rakstīšanas savienojumu.

1. Dodieties uz savu projektu portālā LCS.
2. Atlasiet **Konfigurēt**, lai izvietotu jaunu vidi.
3. Atlasiet versiju. 
4. Atlasiet topoloģiju. Ja ir pieejama tikai viena topoloģija, tā tiek automātiski atlasīta.
5. Pabeidziet pirmās darbības **Izvietošanas iestatījumu** vednī.
6. **Common Data Service** cilnē sekojiet šīm darbībām:

    - Ja Common Data Service vide jau ir nodrošināta jūsu nomniekam, varat to atlasīt.

        1. Iestatiet **Konfigurēt Common Data Service** opciju uz **Jā**.
        2. Laukā **Pieejamās vides** atlasiet vidi, ko integrēt ar jūsu Finance and Operations datiem. Saraksts ietver visas vides, kurās ir administratora privilēģijas.
        3. Atzīmējiet izvēles rūtiņu **Piekrītu**, lai norādītu, ka piekrītat noteikumiem un nosacījumiem.

        ![Common Data Service cilne, kad Common Data Service vide jau ir nodrošināta jūsu nomniekam](../dual-write/media/lcs_setup_1.png)

    - Ja nomniekam vēl nav Common Data Service vide, tiks nodrošināta jauna vide.

        1. Iestatiet **Konfigurēt Common Data Service** opciju uz **Jā**.
        2. Ievadiet Common Data Service vides nosaukumu.
        3. Atlasiet reģionu, kurā izvietot vidi.
        4. Atlasiet noklusējuma valodu un valūtu videi.

            > [!NOTE]
            > Vēlāk nevarēs mainīt valodu un valūtu.

        5. Atzīmējiet izvēles rūtiņu **Piekrītu**, lai norādītu, ka piekrītat noteikumiem un nosacījumiem.

        ![Common Data Service cilne, kad jūsu nomniekam vēl nav Common Data Service vides](../dual-write/media/lcs_setup_2.png)

7. Pabeidziet atlikušās darbības **Izvietošanas iestatījumu** vednī.
8. Pēc tam, kad vides statuss ir **Izvietots**, atveriet vides informācijas lapu. **Common Data Service vides informācijas** sadaļā ir redzami saistīto Finance and Operations vides un Common Data Service vides nosaukumi.

    ![Common Data Service vides informācijas sadaļa](../dual-write/media/lcs_setup_3.png)

9. Finance and Operations vides administratoram ir jāpiesakās portālā LCS un jāatlasa **Saite uz kompaktdiskiem lietojumprogrammām**, lai izveidotu saites. Vides informācijas lapa rāda administratora kontaktinformāciju.

    Pēc tam, kad saite ir pabeigta, statuss tiek atjaunināts uz **Vides saistīšana ir veiksmīgi pabeigta**.

10. Lai atvērtu **Datu integrācijas** darbvietu Finance and Operations vidē un kontrolētu pieejamās veidnes, izvēlieties **Saistīt ar kompaktdiskiem lietojumprogrammās**.

    ![¨Saite uz kompaktdiskiem lietojumprogrammām¨ poga Common Data Service vides informācijas sadaļā](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Jūs nevarat atsaistīt vides, izmantojot portālu LCS. Lai noņemtu saiti videi, atveriet **Datu integrācijas** darbvietu Finance and Operations vidē un pēc tam atlasiet **Noņemt saiti**.

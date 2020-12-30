---
title: Duālās rakstīšanas iestatījums no Lifecycle Services
description: Šajā tēmā skaidrots, kā iestatīt divu rakstīšanas savienojumu starp jaunu Finance and Operations vidi un jaunu Dataverse vidi no Microsoft Dynamics Lifecycle Services (LCS).
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 25db9c58c3d09e44dcf11b48cae1a9eda4241c35
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683529"
---
# <a name="dual-write-setup-from-lifecycle-services"></a>Duālās rakstīšanas iestatījums no Lifecycle Services

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā tēmā skaidrots, kā iestatīt divu rakstīšanas savienojumu starp jaunu Finance and Operations vidi un jaunu Dataverse vidi no Microsoft Dynamics Lifecycle Services (LCS).

## <a name="prerequisites"></a>Priekšnosacījumi

Jums ir jābūt administratoram, lai iestatītu duālās rakstīšanas savienojumu.

+ Jums ir nepieciešama piekļuve nomniekam.
+ Jums ir jābūt administratoram gan Finance and Operations, gan Dataverse vidēs.

## <a name="set-up-a-dual-write-connection"></a>Izveidot duālās rakstīšanas savienojumu

Sekojiet šīm darbībām, lai iestatītu duālās rakstīšanas savienojumu.

1. Dodieties uz savu projektu portālā LCS.
2. Atlasiet **Konfigurēt**, lai izvietotu jaunu vidi.
3. Atlasiet versiju. 
4. Atlasiet topoloģiju. Ja ir pieejama tikai viena topoloģija, tā tiek automātiski atlasīta.
5. Pabeidziet pirmās darbības **Izvietošanas iestatījumu** vednī.
6. **Dataverse** cilnē sekojiet šīm darbībām:

    - Ja Dataverse vide jau ir nodrošināta jūsu nomniekam, varat to atlasīt.

        1. Iestatiet **Konfigurēt Dataverse** opciju uz **Jā**.
        2. Laukā **Pieejamās vides** atlasiet vidi, ko integrēt ar jūsu Finance and Operations datiem. Saraksts ietver visas vides, kurās ir administratora privilēģijas.
        3. Atzīmējiet izvēles rūtiņu **Piekrītu**, lai norādītu, ka piekrītat noteikumiem un nosacījumiem.

        ![Dataverse cilne, kad Dataverse vide jau ir nodrošināta jūsu nomniekam](../dual-write/media/lcs_setup_1.png)

    - Ja nomniekam vēl nav Dataverse vide, tiks nodrošināta jauna vide.

        1. Iestatiet **Konfigurēt Dataverse** opciju uz **Jā**.
        2. Ievadiet Dataverse vides nosaukumu.
        3. Atlasiet reģionu, kurā izvietot vidi.
        4. Atlasiet noklusējuma valodu un valūtu videi.

            > [!NOTE]
            > Vēlāk nevarēs mainīt valodu un valūtu.

        5. Atzīmējiet izvēles rūtiņu **Piekrītu**, lai norādītu, ka piekrītat noteikumiem un nosacījumiem.

        ![Dataverse cilne, kad jūsu nomniekam vēl nav Dataverse vides](../dual-write/media/lcs_setup_2.png)

7. Pabeidziet atlikušās darbības **Izvietošanas iestatījumu** vednī.
8. Pēc tam, kad vides statuss ir **Izvietots**, atveriet vides informācijas lapu. **Dataverse vides informācijas** sadaļā ir redzami saistīto Finance and Operations vides un Dataverse vides nosaukumi.

    ![Dataverse vides informācijas sadaļa](../dual-write/media/lcs_setup_3.png)

9. Finance and Operations vides administratoram ir jāpiesakās portālā LCS un jāatlasa **Saite uz kompaktdiskiem lietojumprogrammām**, lai izveidotu saites. Vides informācijas lapa rāda administratora kontaktinformāciju.

    Pēc tam, kad saite ir pabeigta, statuss tiek atjaunināts uz **Vides saistīšana ir veiksmīgi pabeigta**.

10. Lai atvērtu **Datu integrācijas** darbvietu Finance and Operations vidē un kontrolētu pieejamās veidnes, izvēlieties **Saistīt ar kompaktdiskiem lietojumprogrammās**.

    ![¨Saite uz kompaktdiskiem lietojumprogrammām¨ poga Dataverse vides informācijas sadaļā](../dual-write/media/lcs_setup_4.png)

> [!NOTE]
> Jūs nevarat atsaistīt vides, izmantojot portālu LCS. Lai noņemtu saiti videi, atveriet **Datu integrācijas** darbvietu Finance and Operations vidē un pēc tam atlasiet **Noņemt saiti**.

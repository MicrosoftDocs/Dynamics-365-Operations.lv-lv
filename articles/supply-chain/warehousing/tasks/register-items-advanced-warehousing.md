---
title: Krājumu reģistrēšana uzlabotā noliktavā aktivizētam krājumam, izmantojot krājumu saņemšanas žurnālu
description: Šajā tēmā parādīts, kā reģistrēt krājumus, izmantojot krājumu saņemšanas žurnālu, ja izmantojat papildu noliktavas vadības procesus.
author: ShylaThompson
ms.date: 03/24/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSJournalTable, WMSJournalCreate, WHSLicensePlate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af427e8df2ac7a3a3b5a7fd6edb740400f6bbeaf
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358006"
---
# <a name="register-items-for-an-advanced-warehousing-enabled-item-using-an-item-arrival-journal"></a>Krājumu reģistrēšana uzlabotā noliktavā aktivizētam krājumam, izmantojot krājumu saņemšanas žurnālu

[!include [banner](../../includes/banner.md)]

Šajā tēmā parādīts, kā reģistrēt krājumus, izmantojot krājumu saņemšanas žurnālu, ja izmantojat papildu noliktavas vadības procesus. Tas parasti būtu jāveic saņemšanas darbiniekam.

## <a name="enable-sample-data"></a>Iespējot datu paraugu

Lai šajā scenārijā darbotos, izmantojot šajā tēmā norādītos parauga ierakstus un vērtības, ir jāizmanto sistēma, kurā ir instalēti standarta demonstrācijas dati, un pirms sākšanas ir jāatlasa *USMF* juridiskā persona.

Tā vietā varat strādāt šajā scenārijā, aizstājot vērtības no saviem datiem, ja vien jums ir pieejami šādi dati:

- Jums jābūt apstiprinātam pirkšanas pasūtījumam ar atvērtu pirkšanas pasūtījuma rindu.
- Rindas vienībai ir jābūt esošā krājumā. Tā nedrīkst izmantot preces variantus, un tai nedrīkst būt izsekošanas dimensijas.
- Krājuma vienībai jābūt saistītai ar noliktavas dimensijas grupu, kas iespējo noliktavas pārvaldības apstrādi.
- Izmantojamajai noliktavai ir jābūt iespējotiem noliktavas vadības procesiem un saņemšanai izmantojamajam novietojumam jānotiek numuru zīmju pārbaudei.

## <a name="create-an-item-arrival-journal-header-that-uses-warehouse-management"></a>Izveidot krājumu saņemšanas žurnāla virsrakstu, kas izmanto noliktavas pārvaldību

Šajā scenārijā parādīts, kā izveidot krājumu saņemšanas žurnāla virsrakstu, kas izmanto noliktavas pārvaldību:

1. Pārliecinieties, vai sistēmā ir apstiprināts pirkšanas pasūtījums, kas neatbilst iepriekšējā sadaļā aprakstītajām prasībām. Šis scenārijs izmanto pirkšanas pasūtījumu uzņēmumam *USMF*, kreditora kontam *1001*, noliktavai *51*, ar pasūtījuma rindu *10 PL* (10 paletes) ar krājumu numuru *M9200*.
1. Pierakstiet izmantojamo pirkuma pasūtījuma numuru.
1. Dodieties uz **Krājumu pārvaldība \> Žurnāla ieraksti \> Krājumu saņemšana \> Krājumu saņemšana**.
1. Atlasiet **Jauns** darbību rūtī.
1. Atveras dialoglodziņš **Izveidot noliktavas pārvaldības žurnālu**. Laukā **Nosaukums** atlasiet žurnāla nosaukumu.
    - Ja izmantojat uzņēmuma *USMF* paraugdatus, atlasiet *WHS*.
    - Ja izmantojat savus datus, izvēlei žurnālam **Pārbaudīt izdošanas vietu** jābūt iestatītam uz *Nē* un **Karantīnas pārvaldība** jāiestata uz *Nē*.
1. Iestatiet **Atsauci** *Pirkšanas pasūtījumam*.
1. Iestatiet **Konta numuru** uz *1001*.
1. Iestatiet **Numuru** pirkšanas pasūtījuma numuram, kuru esat identificējis šim uzdevumam.

    ![Krājumu saņemšanas žurnāls.](../media/item-arrival-journal-header.png "Krājumu saņemšanas žurnāls")

1. Atlasiet **Labi**, lai izveidotu žurnāla galveni.
1. Sadaļā **Žurnāla rindas** atlasiet **Pievienot rindu** un ievadiet šādus datus:
    - **Krājuma numurs** – iestatiet uz *M9200*. **Vieta**, **Noliktava** un **Daudzums** tiks iestatīti, pamatojoties uz krājumu darbības datiem 10 paletēm (1000 ea.).
    - **Novietojums** – iestatīts uz  *001*. Šis konkrētais novietojums neizseko numura zīmes.

    ![Krājumu saņemšanas žurnāla rinda.](../media/item-arrival-journal-line.png "Krājumu saņemšanas žurnāla rinda")

    > [!NOTE]
    > Lauks **Datums** nosaka datumu, kurā šī krājuma rīcībā esošais daudzums tiks reģistrēts krājumos.  
    >
    > **Laidiena ID** ierakstīs sistēma, ja tā varēs to unikāli identificēt no sniegtās informācijas. Pretējā gadījumā jums būs tas jāievada manuāli. Tas ir obligāts lauks, kas savieno šo reģistrāciju ar noteiktu pirmdokumenta rindu.  

1. Darbību rūtī atlasiet **Pārbaudīt**. Šādi tiek pārbaudīts, vai žurnāls ir gatavs grāmatošanai. Ja pārbaude neizdodas, jums būs jāatrisina kļūdas pirms žurnālu varēs grāmatot.  
1. Atveras dialoglodziņš **Pārbaudīt žurnālu**. Atlasiet **Labi**.
1. Pārskatīt ziņojuma joslu. Tajā vajadzētu būt ziņojumam par operācijas pabeigšanu.  
1. Darbību rūtī atlasiet **Grāmatot**.
1. Atveras dialoglodziņš **Grāmatot žurnālu**. Atlasiet **Labi**.
1. Pārskatīt ziņojuma joslu. Tajā vajadzētu būt ziņojumam par operācijas pabeigšanu.
1. Atlasiet **Funkcijas > Produktu saņemšana** darbību rūtī, lai atjauninātu pirkšanas pasūtījuma rindu un grāmatotu produktu saņemšanu.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: Veikala darbalaika izveide un atjaunināšana
description: Šajā tēmā ir aprakstīts, kā izveidot un atjaunināt darbalaiku programmā Commerce Headquarters.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 96ae5f33b1ab5fda98da4fc48b1fb883ca4d54b8
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3024482"
---
# <a name="create-and-update-store-hours"></a>Veikala darbalaika izveide un atjaunināšana

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a>Pārskats

Vienā vietā mazumtirgotāji var izveidot, uzturēt un pārvaldīt veikala darbalaiku dažādiem veikaliem visos ģeogrāfiskajos reģionos. Veikala darbalaiks var tikt rādīts pārdošanas punkta (POS) termināļos. Šādā veidā kasieri var koplietot veikala darbalaiku ar klientiem un labāk palīdzēt pircējiem, kas interesējas par krājumiem citos veikalos. Veikala darbalaiku var drukāt arī ieejas plūsmās, ja klienti vēlas atgriezties veikalā vēlāk.

Vairākus darbalaikus ir iespējams konfigurēt dažādos kanālos. Šie kanāli ietver fiziskus veikalus, zvanu centrus, mobilās ierīces un e-komercijas vietnes.

Ja klientam ir paņemšanas pasūtījums citam veikalam, kasieris var izvēlēties datumus, kad paņemšana būs pieejama šajā veikalā. Veikala uzmeklēšanā tiks sniegta atsauce uz datumiem un veikalu laikiem. Kasieris var atlasīt datumu un vietu, kā arī izdrukāt saņemšanas kvīti, kurā iekļauts veikala darbalaiks.

Šī funkcionalitāte ir pieejama tikai programmas Microsoft Dynamics 365 Retail versijā 8.1.2 un jaunākās.

## <a name="configure-store-hours"></a>Veikala darba laika konfigurēšana

Izpildiet tālāk norādītās darbības, lai konfigurētu veikala darbalaiku.

1. Pārejiet uz sadaļu**Retail un Commerce** \> **Kanāla iestatīšana** \> **Veikala darba laiks**.
2. Atlasiet **Jauns**, lai izveidotu jaunu veikala darbalaika veidni. Lai izmantotu esošu veidni, atlasiet veidni kreisajā rūtī.
3. Dialoglodziņā **Pievienot diapazonu** definējiet datuma diapazonu, veikala darbalaiku un nepieciešamās brīvdienas.

    - Ja veikala darbalaiks nemainās, atlasiet **Nekad nebeidzas** laukā **Beigu datums**.
    - Ja veikala darbalaiks ir noteikts mēnesis, nedēļa vai diena, iestatiet atbilstošos datumus laukos **Sākuma datums** un **Beigu datums**.

    > [!NOTE]
    > Varat izveidot vairākas veidnes, kuru sākuma un beigu datumi pārklājas. Tāpēc jūs, piemēram, varat noteikt veikala darbalaiku veikaliem dažādās laika joslās.

    ![Pievienot diapazona dialoglodziņu](../dev-itpro/media/Storehours1.png "Pievienot diapazona dialoglodziņu")

4. Saistiet veikals darbalaika veidni ar veikaliem, kur tā tiks izmantota. Dialoglodziņā **Izvēlēties organizācijas mezglus**, atlasiet veikalus, reģionus un organizācijas, ar kurām veidne jāsaista.

    - Ar katru veikalu var saistīt tikai vienu veikala darbalaika veidni.
    - Izmantojiet bulttaustiņus, lai atlasītu veikalus, reģionus vai organizācijas. Kalendārs būs pieejams veikaliem vai veikalu grupām, un tas atsaucei būs redzams pārdošanas punktos.

    ![Izvēlēties organizācijas zaru dialoglodziņu](../dev-itpro/media/Storehours2.png "Izvēlēties organizācijas zaru dialoglodziņu")

5. Lapā **Izplatīšanas grafiks** izpildiet uzdevumus **1070** un **1090**, lai veikala darbalaiks būtu redzams pārdošanas punktos.

## <a name="add-store-hours-to-printed-receipts"></a>Veikala darbalaika pievienošana drukātajām kvītīm

Veiciet šīs darbības, lai pievienotu veikala darbalaiku drukātajām pārdošanas punkta kvītīm.

1. Atveriet kvīšu noformētāju.
2. Atlasiet **Kājene** apakšējā kreisajā stūrī.
3. Velciet elementu **Veikala darbalaiks** no kreisās rūts līdz kājenei kvīts veidnes apakšā.
4. Jūs varat rediģēt noklusējuma etiķeti elementā **Veikala darbalaiks**, kā vēlaties.
5. Saglabājiet kvīti un aizveriet kvīšu noformētāju.
6. Lapā **Izplatīšanas grafiks** izpildiet uzdevumus **1070** un **1090**.
7. Pierakstieties pārdošanas punktā (POS).
8. Izpildiet pārdošanu un izdrukājiet kvīti.

Tagad pārdošanas punktu kvītis ietver veikala darbalaiku. Ja veidnē tika iekļautas brīvdienas, tās tiek parādītas kvītī.

![Saņemšanas piemērs](../dev-itpro/media/Storehours3.png "Saņemšanas piemērs")

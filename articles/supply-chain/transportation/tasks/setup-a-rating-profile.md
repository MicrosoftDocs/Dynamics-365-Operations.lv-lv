---
title: Novērtējuma profili
description: Šajā rakstā ir aprakstīts, kā iestatīt datus novērtēšanas profiliem.
author: Weijiesa
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRatingProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: weijiesa
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1f7408574187ddb099181bd2566c46c52307f603
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850481"
---
# <a name="rating-profiles"></a>Novērtējuma profili

[!include [banner](../../includes/banner.md)]

Novērtējuma profils atgādina loģistikas līgumu (bet ne juridisku līgumu). Tas tiek izmantots, lai noteiktu transportēšanas tarifus kravām. 

Katrs novērtējuma profils sūtījumu pārvadātājam ir unikāls. Novērtējuma profilā jūs saistāt sūtījumu pārvadātāju saistītu ar likmes šablonu. Likmes šablons definē likmes bāzes piešķiri un likmes bāzi. Likmes bāze nosaka pārvadātāja likmi.

Novērtējuma profilu varat iestatīt, izmantojot vispārīgo lapu, kas parāda pārskatu par visiem esošajiem novērtējuma profiliem. Alternatīvi, novērtējuma profilu varat arī iestatīt tieši no sūtījumu pārvadātāja. Abos gadījumos novērtējuma profilam iestatītā informācija ir tāda pati.

## <a name="create-or-edit-a-rating-profile-on-the-rating-profiles-page"></a>Izveidot vai rediģēt novērtējuma profilu lapā Novērtējuma profili

Lapā **Novērtējuma profili** varat pārskatīt visus pieejamos novērtējuma profilus. Varat arī rediģēt esošos profilus un izveidot jaunus profilus.

1. Dodieties uz **Transportēšanas pārvaldība \> Iestatīšana \> Vērtējums \> Novērtējuma profils**.
1. Darbības rūtī atlasiet **Jauns**, lai pievienotu jaunu novērtējuma profilu režģī vai atlasiet **Rediģēt**, lai rediģētu esošu profilu.
1. Jaunā vai esošā novērtējuma profila rindā iestatiet šādus laukus:

    - **Novērtējuma profils** – ievadiet unikālu novērtējuma profila identifikatoru (ID) un aprakstu.
    - **Nosaukums** - Ievadiet novērtējuma profila aprakstošu nosaukumu.
    - **Nosūtīšanas pārvadātājs** - atlasiet nosūtīšanas pārvadātāju. Novērtējuma profils, kuru iestatāt, tiks norādīts arī izvēlētā pārvadātāja lapā **Nosūtīšanas pārvadātāji**.
    - **Vietne** un **Noliktava** - atlasiet vietni un noliktavu.
    - **Likmes noteikšanas programma** - atlasiet likmes noteikšanas programmu novērtējuma profilam.
    - **Likmes šablons** - atlasiet likmes šablonu novērtējuma profilam. Varat izmantot šo likmes šablonu, lai definētu likmes bāzes tipu un likmes bāzi. Plašāku informāciju skatiet [Likmes šablonu iestatīšana](set-up-rate-masters.md).
    - **Pārvadājumu ilguma noteikšanas programma** - atlasiet pārvadājumu ilguma noteikšanas programmu novērtējuma profilam.
    - **Pārvadātāja degvielas rādītājs** – šim novērtējuma profilam atlasiet pārvadātāja degvielas rādītāju.
    - **Spēkā sākšanās datums un laiks**, kā arī **Derīguma beigu datums un laiks** - definējiet periodu, kad novērtējuma profilam ir jābūt aktīvam.

1. Darbību rūtī atlasiet **Saglabāt**.

## <a name="create-a-rating-profile-directly-on-the-shipping-carriers-page"></a>Izveidot novērtējuma profilu tieši lapā Nosūtīšanas pārvadātāji

1. Dodieties uz **Transportēšanas pārvaldība \> Iestatījumi \> Pārvadātāji \> Sūtījumu pārvadātāji**.
1. Sarakstā atlasiet nosūtīšanas pārvadātāju.
1. Kopsavilkuma cilnē **Novērtējuma profili** noklikšķiniet uz **Jauns**, lai izveidotu novērtējuma profilu.
1. Iestatiet laukus jaunajam novērtējuma profilam. Šie lauki atbilst laukiem novērtējuma profilu **lapā**, kā aprakstīts iepriekšējā šī raksta sadaļā.

> [!NOTE]
> Lapā **Nosūtīšanas pārvadātāji** izveidotie profili tiek parādīti arī lapā **Novērtējuma profili**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
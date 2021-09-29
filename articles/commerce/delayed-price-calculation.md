---
title: Precīzās cenas un atlaides aprēķina aizkavēšana uzlabotam sniegumam
description: Šajā tēmā aprakstīta aizkavētā cenu aprēķina iespēja, kura ir pieejama Microsoft Dynamics 365 Commerce pārdošanas punktā (POS) un zvanu centrā.
author: boycezhu
ms.date: 09/09/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: boycez
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 8c4264c3a4c71e6aab0e1ef8d7d8cfffad065a46
ms.sourcegitcommit: 7a2001e4d01b252f5231d94b50945fd31562b2bc
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/15/2021
ms.locfileid: "7488367"
---
# <a name="delay-exact-price-and-discount-calculation-for-improved-performance"></a>Precīzās cenas un atlaides aprēķina aizkavēšana uzlabotam sniegumam

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīta aizkavētā cenu aprēķina iespēja, kura ir pieejama Microsoft Dynamics 365 Commerce pārdošanas punktā (POS) un zvanu centrā.

Dynamics 365 Commerce atbalsta daudzrindu atlaižu izveidi, kuras tiek piemērotas, kad tiek apvienotas pārdošanas pasūtījuma vai pārdošanas piedāvājuma daudzrindu pārdošanas rindas. Šīs atlaides ietver komplekta piedāvājumu, robežvērtību un daudzuma atlaides.

Katru reizi, kad pasūtījumam pievieno jaunu rindu, Commerce cenu noteikšanas rīks izvērtē visu grozu, lai noteiktu, vai var piemērot kādu no šīm daudzrindu atlaidēm. Šīs atkārtotas aprēķināšanas dēļ jaunu rindu pievienošana var ietekmēt sniegumu, augot pārdošanas pasūtījumam.

Taču starpuzņēmumu (B2B) uzņēmumiem un dažiem "bizness-klientam" (B2C) uzņēmumiem bieži vien ir liela apjoma pasūtījumi. Tāpēc var paiet ilgs laiks, kamēr cenu noteikšanas rīks veic atkārtotu aprēķinu pēc tam, kad grozam ir pievienota katra prece. Turklāt lielu pasūtījumu gadījumā nav īpaši svarīgi, ka precīzu cenu un atlaidi rādītu katru reizi, kad grozam tiek pievienota prece. Svarīgāk ir tas, lai klienti preces varētu pievienot ātri. Iespēja aizkavēt precīzu cenas un atlaides aprēķinu, līdz to pieprasa lietotājs vai līdz tiek finalizēts pasūtījums, var ievērojami uzlabot sniegumu. Tādējādi var arī tikt samazināts laiks, kas vajadzīgs pasūtījuma veikšanas noslēgšanai.

Iespēja aizkavēt precīzu cenas un atlaides aprēķinu jau ilgi ir pieejama POS. No Commerce 10.0.22. versijas laidiena tā būs pieejama arī zvanu centram.

## <a name="enable-delayed-price-and-discount-calculation-for-pos"></a>Aizkavētā preču un atlaides aprēķina iespējošana POS

Lai aizkavētu cenu un atlaižu aprēķinu POS, izpildiet tālāk norādītās darbības.

1. Commerce galvenajā pārvaldē dodieties uz funkcionalitātes profilu, kas ir saistīts ar fizisko veikalu.
1. Kopsavilkuma cilnē **Skaits** iespējojiet konfigurāciju **Manuāli aprēķināt atlaides vairākām precēm**.
1. Atveriet reģistrācijas ekrāna izkārtojuma noformētāju, lai fiksētu, kur vajadzētu iespējot aizkavēto aprēķinu.
1. Pievienojiet operācijas **Aprēķināt kopsummu** pogu vēlamajam pogu režģim.
1. Palaidiet uzdevumus **1070** un **1090**.

Kad preces ir pievienotas transakcijai, daudzrindu atlaides netiek aprēķinātas, ja vien pārdevējs neatlasa pogu **Aprēķināt kopsummu**. Kad transakcijai ir atlasīta opcija **Aprēķināt kopsummu**, tai vienmēr tiks aprēķinātas daudzrindu atlaides. Pārdevējam nevajadzēs pogu atlasīt vēlreiz, pat, ja grozam tiks pievienotas papildu preces. Sistēma neļaus pārdevējam tvert maksājumu, kamēr nav atlasīta opcija **Aprēķināt kopsummu**.

## <a name="enable-delayed-price-and-discount-calculation-for-call-center"></a>Aizkavētā preču un atlaides aprēķina iespējošana zvanu centram

Lai aizkavētu cenu un atlaižu aprēķinu zvanu centram, izpildiet tālāk norādītās darbības.

1. Commerce galvenajā pārvaldībā dodieties uz **Darbvietas \> Līdzekļu pārvaldība**.
1. Iespējojiet līdzekli **Novērst neparedzētu cenu aprēķinu komercijas pasūtījumam**. Šis līdzeklis ir priekšnoteikums aizkavētā cenu un atlaižu aprēķina iespējai.

    > [!NOTE]
    > Jauniem izvietojumiem līdzeklis **Novērst neparedzētu cenu aprēķinu komercijas pasūtījumam** tiek iespējots pēc noklusējuma.

1. Dodieties uz **Commerce parametri \> Cenas un atlaides**.
1. Sadaļā **Dažādi** iespējojiet konfigurāciju **Manuāli aprēķināt daudzrindu cenas un atlaides**.

Kad pārdošanas pasūtījums vai piedāvājums tiek izveidots vai rediģēts zvanu centrā, precīzs cenas un atlaides aprēķins tam tiks aizkavēts. Cenu noteikšanas rīks ņems vērā tikai to pārdošanas rindu, kas tiek pievienota vai rediģēta, bet ignorēs visas pārējās. Preces neto summa ietver cenu aprēķinu un vienkāršās atlaides (atlaižu procenti vai summa no atsevišķas preces). Taču netiks piemērotas komplekta piedāvājuma, robežvērtību un daudzuma atlaides. Zvanu centru lietotāji, kuri vēlas skatīt precīzu cenu, tostarp visas atlaides, var atlasīt vienu no trim pogām **Pārrēķināt**, **Kopsummas** vai **Pabeigts**.

> [!NOTE]
> Zvanu centru pasūtījumiem sistēma rāda brīdinājuma ziņojumu, lai atgādinātu lietotājam, ka viņam ir jāatlasa poga **Pārrēķināt**, **Kopsumma** vai **Pabeigts**, lai tiktu veikts precīzs cenas un atlaides aprēķins. Pasūtījumiem, kuriem ir pieejama poga **Pabeigts**, zvanu centram nav iespējas izlaist precīzu cenas un atlaides aprēķinu, jo ir jāatlasa **Pabeigts**, lai pabeigtu pasūtījuma tveršanu. Pasūtījumiem, kuriem nav pieejama poga **Pabeigts**, nav darbības, kura norādītu uz pasūtījuma tveršanas pabeigšanu. Tāpēc zvanu centra lietotājs atbild par pogas **Pārrēķināt** vai **Kopsumma** atlasi, pirms tiek pabeigta pasūtījuma tveršana.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

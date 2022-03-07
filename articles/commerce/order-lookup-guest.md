---
title: Viesu izrakstīšanās pasūtījuma uzmeklēšanas iespējošana
description: Šajā tēmā aprakstīts, kā iespējot viesu izrakstīšanās pasūtījuma uzmeklēšanu pakalpojumā Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2021-08-15
ms.dyn365.ops.version: Release 10.0.22
ms.openlocfilehash: 639ee670b83198423425d03dad308306c9eed25c
ms.sourcegitcommit: 1707cf45217db6801df260ff60f4648bd9a4bb68
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/23/2021
ms.locfileid: "7674980"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>Viesu izrakstīšanās pasūtījuma uzmeklēšanas iespējošana

[!include [banner](includes/banner.md)]

Šajā tēmā aprakstīts, kā iespējot viesu izrakstīšanās pasūtījuma uzmeklēšanu pakalpojumā Microsoft Dynamics 365 Commerce.

Viesu izrakstīšanās līdzekļa pasūtījuma uzmeklēšana ļauj klientiem, kuri veic pirkumus kā viesi, uzmeklēt savus pasūtījumus. Pasūtījuma uzmeklēšanas iespēja ir noderīga, ja klienti vēlas veikt darbības, piemēram, pārbaudīt pasūtījuma preču izpildes statusu, pārbaudīt adresi, uz kuru ticis sūtīts pasūtījums, atkārtoti pasūtīt preci vai apstiprināt, kurā veikalā prece tiks saņemta.

Klienti, kuri veic pasūtījumus kā reģistrēti lietotāji, savu pasūtījuma informāciju var aplūkot piesakoties, taču klienti, kuri norēķinās kā viesi, to darīt nevar. Taču, ja ir iespējota viesu izrakstīšanās līdzekļa pasūtījumu uzmeklēšana, tiek nodrošināta veidlapa, kuru klienti var lietot, lai meklētu pasūtījumus, kurus tie veikuši kā viesi. Šajā veidlapā klienti ievada pasūtījuma apstiprinājuma ID un (pēc izvēles) e-pasta adresi, kuru tie norādījuši izrakstīšanās laikā.

Turklāt jebkuros ar pasūtījumu saistītos transakciju e-pasta ziņojumos var iekļaut saiti vai pogu, kura klientu novirza tieši uz viņu pasūtījuma informācijas lapu. Šī saite vai poga darbosies pasūtījumiem, kurus veic gan reģistrēti lietotāji, gan viesi.

## <a name="turn-on-necessary-features-in-commerce-headquarters"></a>Vajadzīgo līdzekļu iespējošana Commerce galvenajā pārvaldē

Lai iespējotu viesu norēķinu pasūtījumu uzmeklēšanu, ir jāieslēdz šādi līdzekļi, dodoties uz Commerce galvenās pārvaldes sadaļu **Darbvietas \> Līdzekļu pārvaldība**.

| Funkcija | Nolūks |
|---------|---------|
| Retail anonīmo lietotāju meklēšanas pasūtījuma informācijas izvēles līdzeklis | Šis līdzeklis parāda lietotāja saskarni Commerce parametros, kas ļauj iespējot pasūtījuma uzmeklēšanas API neautentificetiem lietotājiem un konfigurēt veidu, kādā tiek parādīta personas informācija. |
| Iespējot stiprāka kanāla atsauces ID ģenerēšanu | Šis līdzeklis ģenerē drošāku 12 rakstzīmju kanāla atsauces ID (pasūtījuma apstiprinājuma ID), kuru var padot vaicājuma virknē, kad tiek uzmeklēts pasūtījums. |
| Visiem kanāliem ģenerēt konsekventu kanāla atsauces ID formātu | Šis līdzeklis ģenerē droša kanāla atsauces ID pasūtījumiem, kuri tiek veikti, izmantojot e-komercijas vietni, mazumtirdzniecības pārdošanas punktu (POS) vai zvanu centru. Pirms šo līdzekli varat iespējot, ir jābūt iespējotam līdzeklim **Iespējot drošāka kanāla atsauces ID ģenerēšanu**. |

Pēc tam, kad ir iespējots līdzeklis **Mazumtirdzniecības anonīmā lietotāja meklēšanas pasūtījuma informācijas izvēles līdzeklis**, ir jāiespējo API, kas atbalsta neautentificētu pasūtījuma uzmeklēšanu Commerce galvenajā pārvaldē. Dodieties uz **Retail un Commerce \> Galvenās pārvaldes iestatījumi \> Parametri \> Klientu pasūtījumi**. Lapas **Klientu pasūtījumi** kopsavilkuma cilnē **Pasūtījuma meklēšana** iestatiet opciju **Iespējot neautentificētu pasūtījuma uzmeklēšanu** uz vērtību **Jā**, kā parādīts attēlā tālāk.

## <a name="manage-the-display-of-personal-data"></a>Parādāmās personas informācijas pārvaldība

Lapas **Klientu pasūtījumi** kopsavilkuma cilnē **Pasūtījuma meklēšana** Commerce galvenajā pārvaldē ir iekļauts lauks **Viesu pasūtījuma meklēšanā iekļaut personas informāciju**, kas ļauj noteikt, vai klientiem tiek rādīta personas informācija. Šī personas informācija ietver klienta piegādes adresi un klienta kredītkartes numura pēdējos četrus ciparus. Personas informācija pēc noklusējuma netiek rādīta klientiem, ja tiek iespējota neautentificēta pasūtījuma uzmeklēšana. Tālāk esoŠajā tabulā ir aprakstītas pieejamās opcijas.

| Opcija | Rezultāts |
|--------|--------|
| Nekad | Noklusējuma vērtība. Uzmeklēšanā netiek rādīta personas informācija. Ja reģistrēti un pierakstījušies lietotāji uzmeklē sevis veikto pasūtījumu, kamēr viņi ir pierakstījušies, viņi varēs skatīt savu personas informāciju. |
| Tikai viesu pasūtījumi | Personas informācija tiek rādīta pasūtījumu uzmeklēšanā par pasūtījumiem, kurus klienti ir veikuši kā viesi. Ja pasūtījumu veicis reģistrēts lietotājs, šim lietotājam ir jāpiesakās, lai skatītu personas informāciju. |
| Visi pasūtījumi | Personas informācija tiek rādīta visās pasūtījumu uzmeklēšanas instancēs. |

> [!NOTE]
> Šīs opcijas nosaka, kad personas dati, piemēram, klienta adrese un kredītkartes pēdējie četri cipari, tiek rādīti anonīmiem viesiem. Lai aizsargātu reģistrēto klientu privātumu, iesakām atlasīt opciju **Tikai viesu pasūtījumi**. Taču visdrošākā opcija ir **Nekad**.

Pēc tam, kad esat mainījuši lauka **Iekļaut personas datus viesu pasūtījuma uzmeklēšanā**, Commerce pārvaldē ir jāpalaiž darbs 1070 (**Kanāla konfigurācija**), dodoties uz **Retail un Commerce \> Retail un Commerce IT \> Sadalījuma grafiks**. 

## <a name="configure-the-order-lookup-module"></a>Pasūtījuma uzmeklēšanas moduļa konfigurēšana

Commerce moduļu krātuves pasūtījumu uzmeklēšanas moduli izmanto, lai atveidotu veidlapu, kuru viesi var izmantot, lai uzmeklētu pasūtījumus. Pasūtījumu uzmeklēšanas moduli var iekļaut jebkuras lapas pamattekstā, kurā nav vajadzīga klientu pierakstīšanās. Informāciju par moduļa konfigurēšanu skatiet sadaļā [Pasūtījuma uzmeklēšanas modulis](order-lookup-module.md).

## <a name="additional-resources"></a>Papildu resursi

[Pasūtījumu uzmeklēšanas modulis](order-lookup-module.md)

[E-pasta paziņojumu profila iestatīšana](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Viesu izrakstīšanās pasūtījuma uzmeklēšanas iespējošana
description: Šajā rakstā ir aprakstīts, kā iespējot pasūtījumu meklēšanu viesu reģistrēšanās laikā Microsoft Dynamics 365 Commerce.
author: stuharg
ms.date: 12/03/2021
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
ms.openlocfilehash: fe32bb59b6529dd9686ced92c1016f12a75a32d4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891991"
---
# <a name="enable-order-lookup-for-guest-checkouts"></a>Viesu izrakstīšanās pasūtījuma uzmeklēšanas iespējošana

[!include [banner](includes/banner.md)]

Šajā rakstā ir aprakstīts, kā iespējot pasūtījumu meklēšanu viesu reģistrēšanās laikā Microsoft Dynamics 365 Commerce.

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

**Pēc** tam, kad būsiet nomainījis vērtību lauka Iekļaut personas datus viesa pasūtījumu meklē meklēē, programmā Commerce Headquarters **darbs 1070 (** **kanāla konfigurācija) ir jāpalaiž, dodoties uz programmu Retail un Commerce \> Retail un Commerce IT \> Distribution grafiku**.

## <a name="configure-the-order-lookup-module"></a>Pasūtījuma uzmeklēšanas moduļa konfigurēšana

Commerce moduļu krātuves pasūtījumu uzmeklēšanas moduli izmanto, lai atveidotu veidlapu, kuru viesi var izmantot, lai uzmeklētu pasūtījumus. Pasūtījumu uzmeklēšanas moduli var iekļaut jebkuras lapas pamattekstā, kurā nav vajadzīga klientu pierakstīšanās. Informāciju par moduļa konfigurēšanu skatiet sadaļā [Pasūtījuma uzmeklēšanas modulis](order-lookup-module.md).

## <a name="configure-the-order-details-page"></a>Konfigurēt pasūtījuma detalizētas informācijas lapu

Pirms viesa pasūtījuma lietotāji var skatīt detalizētu informāciju par pasūtījumu, jūsu e-komercijas vietnē ir jākonfigurē pasūtījuma detalizētas informācijas lapa, lai tai nebūtu nepieciešama pierakstīšanās. Lai pasūtījuma detalizētas informācijas lapai izslēgtu pierakstīšanās prasību, atveriet lapu Commerce Site Builder, **koka skatā atlasiet noklusējuma lapas (obligāts)** slotu **un notīriet izvēles rūtiņu Nepieciešama pieteikšanās?**

## <a name="add-a-link-to-order-details-in-transactional-emails"></a>Pievienot saiti pasūtījuma informācijai darbību e-pasta ziņojumiem

Ar pasūtījumu saistītajos e-pasta ziņojumiem varat norādīt saiti vai pogu, kas klientus aizved uz pasūtījumu detalizētas informācijas lapu par to pasūtījumu. Lai pievienotu šo saiti vai pogu, izveidojiet HTML hipersaiti, kas norāda uz pasūtījuma detalizētas informācijas lapu jūsu e-komercijas vietnē, un padot pasūtījuma apstiprinājuma ID un debitora e-pasta adresi kā URL parametrus, kā parādīts šajā piemērā.

`<a href="https://[domain]/[orderdetailspage]?confirmationId=%orderconfirmationid%&propertyName=email&propertyValue=%customeremailaddress%" target="_blank">View my order status</a>`

## <a name="additional-resources"></a>Papildu resursi

[Pasūtījumu uzmeklēšanas modulis](order-lookup-module.md)

[E-pasta paziņojumu profila iestatīšana](email-notification-profiles.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

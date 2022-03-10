---
title: Migrēt potenciālo klientu uz kases datiem no datu integrētāja uz duālo rakstīšanas metodi
description: Šajā tēmā aprakstīts, kā migrēt potenciālo klientu uz skaidras naudas datiem no datu integrētāja uz duālo rakstīšanas metodi.
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: 82bfb768b0ecac04184f4b806527346d39584d64
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087272"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Migrēt potenciālo klientu uz kases datiem no datu integrētāja uz duālo rakstīšanas metodi

[!include [banner](../../includes/banner.md)]

Datu integratoram pieejamais risinājums Prospect to cash nav saderīgs ar duālo rakstīšanu. Iemesls tam ir konta tabulā esošais indekss msdynce_AccountNumber, kas tika iekļauts risinājumā Prospect to cash. Ja šis indekss pastāv, jūs nevarat izveidot vienu un to pašu klienta konta numuru divās dažādās juridiskās personām. Varat izvēlēties sākt no jauna ar divkāršu rakstīšanu, migrējot potenciālo klientu uz skaidras naudas datiem no datu integratora uz divkāršu rakstīšanu, vai arī varat instalēt pēdējo "neaktīvo" prospekta versiju skaidrā naudā. Šī tēma aptver abas šīs pieejas.

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>Instalējiet Datu integratora Prospect pēdējo "neaizsargāto" versiju skaidrā naudā

**P2C versija 15.0.0.2** tiek uzskatīta par datu integratora Prospect to cash risinājuma pēdējo "snaudošo" versiju. Jūs varat to lejupielādēt no [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C).

Jums tas jāinstalē manuāli. Pēc instalēšanas viss paliek tieši tāds pats, izņemot indeksu msdynce_AccountNumber ir noņemts.

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Darbības, lai migrētu Prospect uz skaidras naudas datiem no Data Integrator uz divkāršu rakstīšanu

Veiciet šīs darbības, lai migrētu potenciālo klientu uz skaidras naudas datiem no datu integrētāja uz duālo rakstīšanas metodi.

1. Palaidiet potenciālo klientu skaidras naudas datu integrētājam darbiem, lai izpildītu vienu pilnu sinhronizāciju. Tādā veidā jūs nodrošināsiet, ka abām sistēmām (programmām Finance and Operations un klientu iesaistes programmām) ir visi dati.
2. Lai palīdzētu novērst iespējamos datu zudumus, eksportējiet potenciālo klientu uz skaidras naudas datiem no Microsoft Dynamics 365 Sales uz Excel failu vai ar komatu atdalītu vērtību (CSV) failu. Eksportēt datus no šādām entītijām:

    - [Konts](#account-table)
    - [Kontaktpersona](#contact-table)
    - [Rēķins](#invoice-table)
    - Izrakstīt rēķinu par precēm
    - [Pasūtījums](#order-table)
    - [Pasūtīt preces](#order-products-table)
    - [Produkti](#products-table)
    - [Piedāvājums](#quote-and-quote-product-tables)
    - [Piedāvājuma preces](#quote-and-quote-product-tables)

3. Atinstalējiet risinājumu Potenciālais skaidras naudas klients no Sales vides. Šajā solī tiek noņemtas kolonnas un atbilstošie dati, kas ir iekļauts potenciālā klienta naudas risinājumā.
4. Instalējiet duālās rakstīšanas risinājumu.
5. Vienai vai vairākām juridiskajām personām izveidojiet divkāršas rakstīšanas savienojumu starp programmu Finance and Operations un klientu piesaistes programmu.
6. Iespējojiet dubultās rakstīšanas tabulas kartes un veiciet sākotnējo sinhronizāciju nepieciešamajiem atsauces datiem. (Plašāku informāciju skatiet [Sākotnējās sinhronizācijas apsvērumi](initial-sync-guidance.md).) Pieprasīto datu piemēri ietver debitoru grupas, maksājumu termiņus un maksājumu grafikus. Neiespējojiet dubultās rakstīšanas kartes tabulām, kurām nepieciešama inicializēšana, piemēram, kontam, piedāvājumam, piedāvājuma rindai, pasūtījuma un pasūtījuma rindu tabulām.
7. Debitoru aktivācijas programmā atveriet sadaļu **Papildu iestatījumi \> Sistēmas iestatījumi \> Datu pārvaldība \> Dublikātu noteikšanas kārtulas** un deaktivizējiet visas kārtulas.
8. Inicializējiet tabulas, kas uzskaitītas 2. darbībā. Lai iegūtu norādījumus, skatiet pārējās šīs tēmas sadaļas.
9. Atveriet programmu Finance and Operations un iespējojiet tabulas kartes, piemēram, kontu, piedāvājumu, piedāvājuma rindu, pasūtījumu un pasūtījumu rindu tabulas kartes. Palaidiet sākotnējo sinhronizāciju. (Papildinformāciju skatiet [Apsvērumi sākotnējai sinhronizācijai](initial-sync-guidance.md) .) Šajā procesā tiks sinhronizēta papildu informācija no programmas Finance and Operations, piemēram, apstrādes statuss, piegādes un norēķinu adreses, vietnes un noliktavas.

## <a name="account-table"></a>Kontu tabula

1. Kolonnā **Uzņēmums** ievadiet uzņēmuma nosaukumu, piemēram, **USMF**.
2. Slejā **Attiecību tips** ievadiet **Debitoru** kā statisku vērtību. Iespējams, ka nevēlaties klasificēt katru konta ierakstu kā debitoru biznesa loģikā.
3. Iekš **Klientu grupas ID** slejā ievadiet klientu grupas numuru no programmas Finance and Operations. Noklusējuma vērtība no potenciālā klienta uz skaidras naudas risinājumu ir **10**.
4. Ja izmantojat risinājumu Potenciālais klients, lai veiktu risinājumu skaidrā naudā, nepielāgojot **Konta numuru**, ievadiet **Konta numura vērtību** kolonnā **Puses numurs**. Ja ir pielāgojumi un jūs nezināt partijas numuru, izņemiet šo informāciju no programmas Finance and Operations.

## <a name="contact-table"></a>Kontaktpersonu tabula

1. Kolonnā **Uzņēmums** ievadiet uzņēmuma nosaukumu, piemēram, **USMF**.
2. Iestatiet tālāk norādītās kolonnas, pamatojoties uz **IsActiveCustomer** vērtību CSV failā:

    - Ja **IsActiveCustomer** CSV failā ir iestatīts uz **Jā**, iestatiet kolonnu **Pārdodams** uz **Jā**. Iekš **Klientu grupas ID** slejā ievadiet klientu grupas numuru no programmas Finance and Operations. Noklusējuma vērtība no potenciālā klienta uz skaidras naudas risinājumu ir **10**.
    - Ja **IsActiveCustomer** CSV failā ir iestatīts uz **Nē**, iestatiet kolonnu **Pārdodams** uz **Nē** un iestatiet kolonnu **Kontaktpersona** **Debitors**.

3. Ja izmantojat potenciālo klientu skaidras naudas risinājumu, nepielāgojot **Kontaktpersonas numuru**, iestatiet šādas kolonnas:

    - Migrēt kontaktpersonas numuru no CSV faila (**msdynce\_contactnumber**) kontaktpersonas numuram tabulā **Kontaktpersonas** (**msdndi\_contactnumber**).
    - Lietojiet **Kontaktpersonas numura** tabulas vērtības kolonnā **Puses numurs**.
    - Lietojiet **Kontaktpersonas numura** tabulas vērtības kolonnā **Konta numurs/Kontaktpersonas ID**.

## <a name="invoice-table"></a>Rēķinu tabula

Tā kā dati no **Rēķins** tabula ir izstrādāta tā, lai tā varētu plūst vienā virzienā no programmas Finance and Operations uz klientu piesaistes lietotni, inicializācija nav nepieciešama. Palaidiet sākotnējo sinhronizāciju, lai migrētu visus nepieciešamos datus no programmas Finance and Operations uz klientu piesaistes programmu. Papildinformāciju skatiet sadaļā [Sākotnējās sinhronizācijas apsvērumi](initial-sync-guidance.md).

## <a name="order-table"></a>Pasūtījumu tabula

1. Kolonnā **Uzņēmums** ievadiet uzņēmuma nosaukumu, piemēram, **USMF**.
2. Kopējiet kolonnas **Pasūtījuma ID** vērtību CSV failā uz kolonnu **Pārdošanas pasūtījuma numura**.
3. Kopējiet kolonnas **Pasūtījuma ID** vērtību CSV failā uz kolonnu **Rēķina debitora numurs**.
4. Kopējiet CSV faila kolonnas **Nosūtīt uz valsti/reģionu** vērtību uz kolonnu **Nosūtīt uz valsti/reģionu**. Šādas vērtības piemēri ietver **ASV** un **Savienotie Štati**.
5. Iestatiet **Pieprasīto saņemšanas datuma** kolonnu. Ja neizmantojat saņemšanas datumu, CSV failā izmantojiet **Pieprasītā piegādes datuma**, **Izpildes datuma** un **Datuma iesniegšanas** kolonnas. Šīs vērtības piemērs ir **2020-03-27T00:00:00Z**.
6. Iestatiet kolonnu **Valoda**. Šīs vērtības piemērs ir **en-us**.
7. Iestatiet kolonnu **Pasūtījuma tips**, izmantojot kolonnu **Balstīts uz krājumu**.

## <a name="order-products-table"></a>Pasūtījuma preču tabula

- Kolonnā **Uzņēmums** ievadiet uzņēmuma nosaukumu, piemēram, **USMF**.

## <a name="products-table"></a>Preču tabula

Tā kā dati no **Produkti** tabula ir izstrādāta tā, lai tā varētu plūst vienā virzienā no programmas Finance and Operations uz klientu piesaistes lietotni, inicializācija nav nepieciešama. Palaidiet sākotnējo sinhronizāciju, lai migrētu visus nepieciešamos datus no programmas Finance and Operations uz klientu piesaistes programmu. Papildinformāciju skatiet sadaļā [Sākotnējās sinhronizācijas apsvērumi](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Piedāvājuma un piedāvājuma preču tabulas

Lai iegūtu informāciju par **Piedāvājumu** tabulu, izpildiet iepriekš šīs tēmas sadaļā [Pasūtījumu tabula](#order-table) norādītās instrukcijas. Lai iegūtu informāciju par **Piedāvājuma preču** tabulu, izpildiet iepriekš šīs tēmas sadaļā [Pasūtījuma preču tabula](#order-products-table) norādītās instrukcijas.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

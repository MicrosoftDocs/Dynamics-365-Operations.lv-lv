---
title: Migrēt potenciālo klientu uz kases datiem no datu integrētāja uz duālo rakstīšanas metodi
description: Šajā rakstā ir aprakstīts, kā migrēt potenciālā klienta datus uz skaidras naudas datiem no datu integrētāja uz dubulto rakstiet.
author: RamaKrishnamoorthy
ms.date: 02/01/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-26
ms.openlocfilehash: bbf5a7c2f409003816e2becf1a58ee7d7d5aafb2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289086"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Migrēt potenciālo klientu uz kases datiem no datu integrētāja uz duālo rakstīšanas metodi

[!include [banner](../../includes/banner.md)]

DataIntegrator pieejamais skaidras naudas risinājuma potenciālais klients nav saderīgs ar dubulto rakstiet. Iemesls tam ir konta msdynce_AccountNumber indekss konta tabulā, kas bija daļa no potenciālā klienta naudas risinājumiem. Ja šis indekss pastāv, divas dažādas juridiskas personas nevar izveidot vienu un to pašu debitora konta numuru. Varat izvēlēties sākt jaunu ar dubulto rakstiet, migrējot potenciālo klientu uz skaidras naudas datiem no datu integrētāja uz dubulto rakstiet, vai varat instalēt potenciālā klienta pēdējo "dorman" versiju skaidras naudas risinājumam. Šajā rakstā ir apskatītas abas šīs pieejas.

## <a name="install-the-last-dorman-version-of-the-data-integrator-prospect-to-cash-solution"></a>Instalējiet datu integrētāāja potenciālā klienta pēdējo "dorman" versiju skaidras naudas risinājumam

**P2C versijas 15.0.0.2** tiek uzskatīts par datu integrētāja potenciālā klienta naudas risinājuma pēdējo "dorman" versiju. Varat lejupielādēt to no [FastTrack for Dynamics 365](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/Dual-write/P2C).

Jums tas ir jāinstalē manuāli. Pēc instalēšanas viss paliek precīzi tāds pats, izņemot to, msdynce_AccountNumber tiek noņemts indekss.

## <a name="steps-to-migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Soļi, lai migrētu potenciālā klienta datus no datu integrētāja uz dubulto rakstiet

Veiciet šīs darbības, lai migrētu potenciālo klientu uz skaidras naudas datiem no datu integrētāja uz duālo rakstīšanas metodi.

1. Palaidiet potenciālo klientu skaidras naudas datu integrētājam darbiem, lai izpildītu vienu pilnu sinhronizāciju. Šādā veidā jūs nodrošināt, ka abām sistēmām (finanšu un operāciju programmām un debitoru piesaistes programmām) ir visi dati.
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
5. Izveidojiet dubultās rakstīšanas savienojumu starp finanšu un operāciju programmu un debitoru saistību programmu vienai vai vairākām juridiskām personām.
6. Iespējojiet dubultās rakstīšanas tabulas kartes un veiciet sākotnējo sinhronizāciju nepieciešamajiem atsauces datiem. (Plašāku informāciju skatiet [Sākotnējās sinhronizācijas apsvērumi](initial-sync-guidance.md).) Pieprasīto datu piemēri ietver debitoru grupas, maksājumu termiņus un maksājumu grafikus. Neiespējojiet dubultās rakstīšanas kartes tabulām, kurām nepieciešama inicializēšana, piemēram, kontam, piedāvājumam, piedāvājuma rindai, pasūtījuma un pasūtījuma rindu tabulām.
7. Debitoru aktivācijas programmā atveriet sadaļu **Papildu iestatījumi \> Sistēmas iestatījumi \> Datu pārvaldība \> Dublikātu noteikšanas kārtulas** un deaktivizējiet visas kārtulas.
8. Inicializējiet tabulas, kas uzskaitītas 2. darbībā. Norādījumus skatiet pārējās šī raksta sadaļās.
9. Atveriet finanšu un operāciju programmu un iespējojiet tabulu kartes, piemēram, konta, piedāvājuma, piedāvājuma rindas, pasūtījuma un pasūtījuma rindu tabulas kartes. Palaidiet sākotnējo sinhronizāciju. (Plašāku informāciju skatiet [Sākotnējās sinhronizācijas apsvērumi](initial-sync-guidance.md).) Šis process sinhronizēs papildu informāciju no finanšu un operāciju programmas, piemēram, apstrādes statusu, nosūtīšanas un norēķinu adreses, vietas un noliktavas.

## <a name="account-table"></a>Kontu tabula

1. Kolonnā **Uzņēmums** ievadiet uzņēmuma nosaukumu, piemēram, **USMF**.
2. Slejā **Attiecību tips** ievadiet **Debitoru** kā statisku vērtību. Iespējams, ka nevēlaties klasificēt katru konta ierakstu kā debitoru biznesa loģikā.
3. Kolonnā Debitoru **grupas ID** ievadiet debitoru grupas numuru no finanšu un operāciju programmas. Noklusējuma vērtība no potenciālā klienta uz skaidras naudas risinājumu ir **10**.
4. Ja izmantojat risinājumu Potenciālais klients, lai veiktu risinājumu skaidrā naudā, nepielāgojot **Konta numuru**, ievadiet **Konta numura vērtību** kolonnā **Puses numurs**. Ja ir pielāgojumi un nav zināms puses numurs, velciet šo informāciju no finanšu un operāciju programmas.

## <a name="contact-table"></a>Kontaktpersonu tabula

1. Kolonnā **Uzņēmums** ievadiet uzņēmuma nosaukumu, piemēram, **USMF**.
2. Iestatiet tālāk norādītās kolonnas, pamatojoties uz **IsActiveCustomer** vērtību CSV failā:

    - Ja **IsActiveCustomer** CSV failā ir iestatīts uz **Jā**, iestatiet kolonnu **Pārdodams** uz **Jā**. Kolonnā Debitoru **grupas ID** ievadiet debitoru grupas numuru no finanšu un operāciju programmas. Noklusējuma vērtība no potenciālā klienta uz skaidras naudas risinājumu ir **10**.
    - Ja **IsActiveCustomer** CSV failā ir iestatīts uz **Nē**, iestatiet kolonnu **Pārdodams** uz **Nē** un iestatiet kolonnu **Kontaktpersona** **Debitors**.

3. Ja izmantojat potenciālo klientu skaidras naudas risinājumu, nepielāgojot **Kontaktpersonas numuru**, iestatiet šādas kolonnas:

    - Migrēt kontaktpersonas numuru no CSV faila (**msdynce\_contactnumber**) kontaktpersonas numuram tabulā **Kontaktpersonas** (**msdndi\_contactnumber**).
    - Lietojiet **Kontaktpersonas numura** tabulas vērtības kolonnā **Puses numurs**.
    - Lietojiet **Kontaktpersonas numura** tabulas vērtības kolonnā **Konta numurs/Kontaktpersonas ID**.

## <a name="invoice-table"></a>Rēķinu tabula

Tā kā dati no rēķinu **tabulas** ir paredzēti vienvirziena plūsmai no finanšu un operāciju programmas uz debitoru iesaistīšanas programmu, nav nepieciešama inicializācija. Palaidiet sākotnējo sinhronizāciju, lai migrētu visus nepieciešamos datus no finanšu un operāciju programmas uz debitoru lietojumprogrammu. Papildinformāciju skatiet sadaļā [Sākotnējās sinhronizācijas apsvērumi](initial-sync-guidance.md).

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

Tā kā dati no tabulas **Preces** ir paredzēti vienvirziena plūsmai no finanšu un operāciju programmas uz debitoru iesaistīšanas programmu, nav nepieciešama inicializācija. Palaidiet sākotnējo sinhronizāciju, lai migrētu visus nepieciešamos datus no finanšu un operāciju programmas uz debitoru lietojumprogrammu. Papildinformāciju skatiet sadaļā [Sākotnējās sinhronizācijas apsvērumi](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Piedāvājuma un piedāvājuma preču tabulas

Tabulai **Piedāvājums** izpildiet iepriekš šī raksta [sadaļā Pasūtījumu](#order-table) tabula norādītās instrukcijas. Lai iegūtu informāciju par **Piedāvājuma preču** tabulu, izpildiet iepriekš šīs tēmas sadaļā [Pasūtījuma preču tabula](#order-products-table) norādītās instrukcijas.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]


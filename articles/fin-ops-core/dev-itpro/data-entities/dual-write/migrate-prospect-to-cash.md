---
title: Migrēt potenciālo klientu uz kases datiem no datu integrētāja uz duālo rakstīšanas metodi
description: Šajā tēmā aprakstīts, kā migrēt potenciālo klientu uz skaidras naudas datiem no datu integrētāja uz duālo rakstīšanas metodi.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/04/2021
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
ms.search.validFrom: 2021-01-04
ms.openlocfilehash: f1478f0246e7f1ff8bd72232cbaf4c2034cf4edb
ms.sourcegitcommit: 6af7b37b1c8950ad706e684cc13a79e662985b34
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/14/2021
ms.locfileid: "4959850"
---
# <a name="migrate-prospect-to-cash-data-from-data-integrator-to-dual-write"></a>Migrēt potenciālo klientu uz kases datiem no datu integrētāja uz duālo rakstīšanas metodi

[!include [banner](../../includes/banner.md)]

Veiciet šīs darbības, lai migrētu potenciālo klientu uz skaidras naudas datiem no datu integrētāja uz duālo rakstīšanas metodi.

1. Palaidiet potenciālo klientu skaidras naudas datu integrētājam darbiem, lai izpildītu vienu pilnu sinhronizāciju. Šādā veidā jūs nodrošināt, ka abām sistēmām (Finance and Operations programmām un customer engagement programmām) ir visi dati.
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
5. Izveidojiet dubultās rakstīšanas savienojumu starp Finance and Operations programmu un customer engagement programmu vienai vai vairākām juridiskām personām.
6. Iespējojiet dubultās rakstīšanas tabulas kartes un veiciet sākotnējo sinhronizāciju nepieciešamajiem atsauces datiem. (Plašāku informāciju skatiet [Sākotnējās sinhronizācijas apsvērumi](initial-sync-guidance.md).) Pieprasīto datu piemēri ietver debitoru grupas, maksājumu termiņus un maksājumu grafikus. Neiespējojiet dubultās rakstīšanas kartes tabulām, kurām nepieciešama inicializēšana, piemēram, kontam, piedāvājumam, piedāvājuma rindai, pasūtījuma un pasūtījuma rindu tabulām.
7. Debitoru aktivācijas programmā atveriet sadaļu **Papildu iestatījumi \> Sistēmas iestatījumi \> Datu pārvaldība \> Dublikātu noteikšanas kārtulas** un deaktivizējiet visas kārtulas.
8. Inicializējiet tabulas, kas uzskaitītas 2. darbībā. Lai iegūtu norādījumus, skatiet pārējās šīs tēmas sadaļas.
9. Atveriet Finance and Operations programmu un iespējojiet tabulu kartes, piemēram, konta, piedāvājuma, piedāvājuma rindas, pasūtījuma un pasūtījuma rindu tabulas kartes. Palaidiet sākotnējo sinhronizāciju. (Plašāku informāciju skatiet [Sākotnējās sinhronizācijas apsvērumi](initial-sync-guidance.md).) Šis process sinhronizēs papildinformāciju no Finance and Operations programmas, piemēram, apstrādes statusu, nosūtīšanas un norēķinu adreses, vietas un noliktavas.

## <a name="account-table"></a>Kontu tabula

1. Kolonnā **Uzņēmums** ievadiet uzņēmuma nosaukumu, piemēram, **USMF**.
2. Slejā **Attiecību tips** ievadiet **Debitoru** kā statisku vērtību. Iespējams, ka nevēlaties klasificēt katru konta ierakstu kā debitoru biznesa loģikā.
3. Kolonnā **Debitoru grupas ID** ievadiet debitoru grupas numuru no Finance and Operations programmas. Noklusējuma vērtība no potenciālā klienta uz skaidras naudas risinājumu ir **10**.
4. Ja izmantojat risinājumu Potenciālais klients, lai veiktu risinājumu skaidrā naudā, nepielāgojot **Konta numuru**, ievadiet **Konta numura vērtību** kolonnā **Puses numurs**. Ja ir pielāgojumi un nav zināms puses numurs, velciet šo informāciju no Finance and Operations programmas.

## <a name="contact-table"></a>Kontaktpersonu tabula

1. Kolonnā **Uzņēmums** ievadiet uzņēmuma nosaukumu, piemēram, **USMF**.
2. Iestatiet tālāk norādītās kolonnas, pamatojoties uz **IsActiveCustomer** vērtību CSV failā:

    - Ja **IsActiveCustomer** CSV failā ir iestatīts uz **Jā**, iestatiet kolonnu **Pārdodams** uz **Jā**. Kolonnā **Debitoru grupas ID** ievadiet debitoru grupas numuru no Finance and Operations programmas. Noklusējuma vērtība no potenciālā klienta uz skaidras naudas risinājumu ir **10**.
    - Ja **IsActiveCustomer** CSV failā ir iestatīts uz **Nē**, iestatiet kolonnu **Pārdodams** uz **Nē** un iestatiet kolonnu **Kontaktpersona** **Debitors**.

3. Ja izmantojat potenciālo klientu skaidras naudas risinājumu, nepielāgojot **Kontaktpersonas numuru**, iestatiet šādas kolonnas:

    - Migrēt kontaktpersonas numuru no CSV faila (**msdynce\_contactnumber**) kontaktpersonas numuram tabulā **Kontaktpersonas** (**msdndi\_contactnumber**).
    - Lietojiet **Kontaktpersonas numura** tabulas vērtības kolonnā **Puses numurs**.
    - Lietojiet **Kontaktpersonas numura** tabulas vērtības kolonnā **Konta numurs/Kontaktpersonas ID**.

## <a name="invoice-table"></a>Rēķinu tabula

Tā kā dati no tabulas **Rēķini** ir paredzēti vienvirziena plūsmai no programmas Finance and Operations uz customer engagement programmu, inicializēšana nav nepieciešama. Veiciet sākotnējo sinhronizāciju, lai migrētu visus nepieciešamos datus Finance and Operations no programmas uz customer engagement programmu. Papildinformāciju skatiet sadaļā [Sākotnējās sinhronizācijas apsvērumi](initial-sync-guidance.md).

## <a name="order-table"></a>Pasūtījumu tabula

1. Kolonnā **Uzņēmums** ievadiet uzņēmuma nosaukumu, piemēram, **USMF**.
2. Kopējiet kolonnas **Pasūtījuma ID** vērtību CSV failā uz kolonnu **Pārdošanas pasūtījuma numura**.
3. Kopējiet kolonnas **Pasūtījuma ID** vērtību CSV failā uz kolonnu **Rēķina debitora numurs**.
4. Kopējiet CSV faila kolonnas **Nosūtīt uz valsti/reģionu** vērtību uz kolonnu **Nosūtīt uz valsti/reģionu**. Šādas vērtības piemēri ietver **ASV** un **Savienotie Štati**.
5. Iestatiet **Pieprasīto saņemšanas datuma** kolonnu. Ja neizmantojat saņemšanas datumu, CSV failā izmantojiet **Pieprasītā piegādes datuma**, **Izpildes datuma** un  **Datuma iesniegšanas** kolonnas. Šīs vērtības piemērs ir **2020-03-27T00:00:00Z**.
6. Iestatiet kolonnu **Valoda**. Šīs vērtības piemērs ir **en-us**.
7. Iestatiet kolonnu **Pasūtījuma tips**, izmantojot kolonnu **Balstīts uz krājumu**.

## <a name="order-products-table"></a>Pasūtījuma preču tabula

- Kolonnā **Uzņēmums** ievadiet uzņēmuma nosaukumu, piemēram, **USMF**.

## <a name="products-table"></a>Preču tabula

Tā kā dati no tabulas **Preces** ir paredzēti vienvirziena plūsmai no programmas Finance and Operations uz customer engagement programmu, inicializēšana nav nepieciešama. Veiciet sākotnējo sinhronizāciju, lai migrētu visus nepieciešamos datus Finance and Operations no programmas uz customer engagement programmu. Papildinformāciju skatiet sadaļā [Sākotnējās sinhronizācijas apsvērumi](initial-sync-guidance.md).

## <a name="quote-and-quote-product-tables"></a>Piedāvājuma un piedāvājuma preču tabulas

Lai iegūtu informāciju par **Piedāvājumu** tabulu, izpildiet iepriekš šīs tēmas sadaļā [Pasūtījumu tabula](#order-table) norādītās instrukcijas. Lai iegūtu informāciju par **Piedāvājuma preču** tabulu, izpildiet iepriekš šīs tēmas sadaļā [Pasūtījuma preču tabula](#order-products-table) norādītās instrukcijas.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
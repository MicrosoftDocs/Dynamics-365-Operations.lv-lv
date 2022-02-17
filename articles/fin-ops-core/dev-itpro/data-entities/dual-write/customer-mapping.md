---
title: Integrētie debitoru pamatdati
description: Šajā tēmā ir aprakstīta debitoru datu integrācija starp Finance and Operations un Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 41e4b6c192b6125a144e4d5ef952ba0975821d44
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8063293"
---
# <a name="integrated-customer-master"></a>Integrētie debitoru pamatdati

[!include [banner](../../includes/banner.md)]



Klienta datus var apgūt vairāk nekā vienā Dynamics 365 lietojumprogrammā. Piemēram, klienta rinda var rasties, izmantojot pārdošanas darbību programmā Dynamics 365 Sales (Customer Engagement programmā), vai rinda var rasties, izmantojot mazumtirdzniecības darbību pakalpojumā Dynamics 365 Commerce (Finance and Operations programmā). Neatkarīgi no tā, no kurienes radušies klienta dati, tie tiek integrēti aizkulisēs. Integrētie klientu pamatdati sniedz jums elastību, lai varētu apgūt klienta datus jebkurā Dynamics 365 lietojumprogrammā, un sniedz visaptverošu skatījumu par klientu visā Dynamics 365 lietojumprogrammu komplektā.

## <a name="customer-data-flow"></a>Debitora datu plūsma

*Debitors* ir pareizi definēta koncepcija programmās. Tādēļ debitoru datu integrēšana ietver tikai debitora koncepta saskaņošanu starp abām programmām. Nākamajā attēlā ir parādīta debitoru datu plūsma.

![Debitora datu plūsma.](media/dual-write-customer-data-flow.png)

Debitorus kopumā var iedalīt divos tipos: komerciālie/organizāciju debitori un debitori/galalietotāji. Šie divi debitoru tipi tiek dažādi uzglabāti un apstrādāti programmās Finance and Operations un Dataverse.

Sadaļā Finance and Operations gan komerciālie/organizatoriskie klienti, gan patērētāji/galalietotāji tiek apgūti vienā tabulā ar nosaukumu **CustTable** (CustCustomerV3Entity), un tie tiek klasificēti, **pamatojoties uz atribūtu Tips**. (Ja **Tips** ir iestatīts uz **Organizācija**, tad debitors ir komerciāls/organizācijas debitors, un ja **Tips** ir iestatīts uz **Persona**, tad debitors ir debitors/galalietotājs.) Primārā kontaktpersonas informācija tiek apstrādāta, izmantojot SMMContactPersonEntity elementu.

Programmā Dataverse komerciālie/organizāciju debitoru pamatdati tiek apkopoti Konta elementā, un tiek identificēti kā debitori, kas atribūts **RelationshipType** ir iestatīts uz **Debitors**. Gan debitorus/galalietotājus, gan kontaktpersonu ataino tabula Kontaktpersonas. Lai nodrošinātu skaidru dalījumu starp debitoru/galalietotāju un kontaktpersonu, elementam **Kontaktpersona** ir Būla karodziņš ar nosaukumu **Pārdodams**. Ja **Pārdodams** ir **Patiess**, kontaktpersona ir debitors/galalietotājs, un šai kontaktpersonai var izveidot piedāvājumus un pasūtījumus. Ja **Pārdodams** ir **Nepatiess**, kontaktpersona ir tikai debitora primārā kontaktpersona.

Kad nepārdodama kontaktpersona piedalās piedāvājumu vai pasūtījumu procesā **Pārdodams** ir iestatīts kā **Patiess**, lai atzīmētu kontaktpersonu kā pārdodamu kontaktpersonu. Kontaktpersona, kas ir kļuvusi par pārdodamu kontaktpersonu, joprojām paliek pārdodama kontaktpersona.

## <a name="templates"></a>Veidnes

Debitora dati ietver visu informāciju par debitoru, piemēram, debitora grupu, adreses, kontaktinformāciju, maksājuma profilu, rēķina profilu un lojalitātes programmas statusu. Tabulas karšu vākšana darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.

Finance and Operations programmas | Customer engagement programmas         | Apraksts
----------------------------|---------------------------------|------------
[CDS kontaktpersonas V2](mapping-reference.md#115) | kontaktpersonas | Šī veidne sinhronizē visu primāro, sekundāro un terciāro kontaktpersonas informāciju par debitoriem un kreditoriem.
[Debitoru grupas](mapping-reference.md#126) | msdyn_customergroups | Šī veidne sinhronizē debitoru grupas informāciju.
[Debitora maksāšanas metode](mapping-reference.md#127) | msdyn_customerpaymentmethods | Šī veidne sinhronizē debitoru maksājuma metodes informāciju.
[Debitori V3](mapping-reference.md#101) | konti | Šī veidne sinhronizē debitora pamatinformāciju komerciāliem un organizācijas debitoriem.
[Debitori V3](mapping-reference.md#116) | kontaktpersonas | Šī veidne sinhronizē klienta pamatdatus par debitoriem un gala lietotājiem.
[Nosaukuma afiksi](mapping-reference.md#155) | msdyn_nameaffixes | Šī veidne sinhronizē nosaukumu afiksu atsauces datus par debitoriem un kreditoriem.
[Maksāšanas dienu rindas CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Šī veidne sinhronizē maksāšanas dienu rindas atsauces datus par debitoriem un kreditoriem.
[Maksāšanas dienas CDS](mapping-reference.md#158) | msdyn_paymentdays | Šī veidne sinhronizē maksāšanas dienu atsauces datus par debitoriem un kreditoriem.
[Maksājumu grafika rindas](mapping-reference.md#159) | msdyn_paymentschedulelines | Sinhronizē maksāšanas grafika rindu atsauces datus par debitoriem un kreditoriem.
[Maksājumu grafiks](mapping-reference.md#160) | msdyn_paymentschedules | Šī veidne sinhronizē maksāšanas grafika atsauces datus par debitoriem un kreditoriem.
[Apmaksas nosacījumi](mapping-reference.md#161) | msdyn_paymentterms | Šī veidne sinhronizē maksāšanas nosacījumu (apmaksas nosacījumu) atsauces datus par debitoriem un kreditoriem.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

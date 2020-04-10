---
title: Integrētie debitoru pamatdati
description: Šajā tēmā aprakstīta debitoru datu integrācija starp programmām Finance and Operations un Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 977b74b10b4549d09a8816264f9ff603fa86e91c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172835"
---
# <a name="integrated-customer-master"></a>Integrētie debitoru pamatdati

[!include [banner](../../includes/banner.md)]


Klienta datus var apgūt vairāk nekā vienā Dynamics 365 lietojumprogrammā. Piemēram, klienta ieraksts var rasties, izmantojot pārdošanas darbību programmā Dynamics 365 Sales (modeļa vadītā programmā pakalpojumā Dynamics 365), vai ieraksts var rasties, izmantojot mazumtirdzniecības darbību pakalpojumā Dynamics 365 Commerce (Finance and Operations programmā). Neatkarīgi no tā, no kurienes radušies klienta dati, tie tiek integrēti aizkulisēs. Integrētie klientu pamatdati sniedz jums elastību, lai varētu apgūt klienta datus jebkurā Dynamics 365 lietojumprogrammā, un sniedz visaptverošu skatījumu par klientu visā Dynamics 365 lietojumprogrammu komplektā.

## <a name="customer-data-flow"></a>Debitora datu plūsma

*Debitors* ir pareizi definēta koncepcija programmās. Tādēļ debitoru datu integrēšana ietver tikai debitora koncepta saskaņošanu starp abām programmām. Nākamajā attēlā ir parādīta debitoru datu plūsma.

![Debitora datu plūsma](media/dual-write-customer-data-flow.png)

Debitorus kopumā var iedalīt divos tipos: komerciālie/organizāciju debitori un debitori/galalietotāji. Šie divi debitoru tipi tiek dažādi uzglabāti un apstrādāti programmās Finance and Operations un Common Data Service.

Progeammā Finance and Operations gan komerciālo/organizāciju debitoru, gan debitoru/galalietotāju pamatdati tiek apkopoti vienā tabulā, kas saucas **CustTable** (CustomerCustomerV3Entity), un tie tiek klasificēti, pamatojoties uz atribūtu **Tips**. (Ja **Tips** ir iestatīts uz **Organizācija**, tad debitors ir komerciāls/organizācijas debitors, un ja **Tips** ir iestatīts uz **Persona**, tad debitors ir debitors/galalietotājs.) Primārā kontaktpersonas informācija tiek apstrādāta, izmantojot SMMContactPersonEntity elementu.

Programmā Common Data Service komerciālie/organizāciju debitoru pamatdati tiek apkopoti Konta elementā, un tiek identificēti kā debitori, kas atribūts **RelationshipType** ir iestatīts uz **Debitorsr**. Gan debitorus/galalietotājus, gan kontaktpersonu pārstāv Kontaktpersonas elements. Lai nodrošinātu skaidru dalījumu starp debitoru/galalietotāju un kontaktpersonu, elementam **Kontaktpersona** ir Būla karodziņš ar nosaukumu **Pārdodams**. Ja **Pārdodams** ir **Patiess**, kontaktpersona ir debitors/galalietotājs, un šai kontaktpersonai var izveidot piedāvājumus un pasūtījumus. Ja **Pārdodams** ir **Nepatiess**, kontaktpersona ir tikai debitora primārā kontaktpersona.

Kad nepārdodama kontaktpersona piedalās piedāvājumu vai pasūtījumu procesā **Pārdodams** ir iestatīts kā **Patiess**, lai atzīmētu kontaktpersonu kā pārdodamu kontaktpersonu. Kontaktpersona, kas ir kļuvusi par pārdodamu kontaktpersonu, joprojām paliek pārdodama kontaktpersona.

## <a name="templates"></a>Veidnes

Debitora dati ietver visu informāciju par debitoru, piemēram, debitora grupu, adreses, kontaktinformāciju, maksājuma profilu, rēķina profilu un lojalitātes programmas statusu. Elementa karšu vākšana darbojas kopā debitora datu mijiedarbības laikā, kā redzams nākamajā tabulā.

Finance and Operations programmas | Citas Dynamics 365 programmas         | Apraksts
----------------------------|---------------------------------|------------
CDS kontaktpersonas V2             | kontaktpersonas                        | Šī veidne sinhronizē visu primāro, sekundāro un terciāro kontaktpersonas informāciju par debitoriem un kreditoriem.
Debitoru grupas             | msdyn_customergroups            | Šī veidne sinhronizē debitoru grupas informāciju.
Debitora maksāšanas metode     | msdyn_customerpaymentmethods    | Šī veidne sinhronizē debitoru maksājuma metodes informāciju.
Debitori V3                | konti                        | Šī veidne sinhronizē debitora pamatinformāciju komerciāliem un organizācijas debitoriem.
Debitori V3                | kontaktpersonas                        | Šī veidne sinhronizē klienta pamatdatus par debitoriem un gala lietotājiem.
Nosaukuma afiksi                | msdyn_nameaffixes               | Šī veidne sinhronizē nosaukumu afiksu atsauces datus par debitoriem un kreditoriem.
Maksāšanas dienu rindas CDS V2    | msdyn_paymentdaylines           | Šī veidne sinhronizē maksāšanas dienu rindas atsauces datus par debitoriem un kreditoriem.
Maksāšanas dienas CDS            | msdyn_paymentdays               | Šī veidne sinhronizē maksāšanas dienu atsauces datus par debitoriem un kreditoriem.
Maksājumu grafika rindas      | msdyn_paymentschedulelines      | Sinhronizē maksāšanas grafika rindu atsauces datus par debitoriem un kreditoriem.
Maksājumu grafiks            | msdyn_paymentschedules          | Šī veidne sinhronizē maksāšanas grafika atsauces datus par debitoriem un kreditoriem.
Apmaksas nosacījumi            | msdyn_paymentterms              | Šī veidne sinhronizē maksāšanas nosacījumu (apmaksas nosacījumu) atsauces datus par debitoriem un kreditoriem.

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping contacts contacts](includes/CDSContactsV2-contacts.md)]

[!include [mapping customer group](includes/CustCustomerGroup-msdyn-customergroups.md)]

[!include [mapping customer payment method](includes/CustomerPaymentMethod-msdyn-customerpaymentmethods.md)]

[!include [mapping customer accounts](includes/CustomersV3-accounts.md)]

[!include [mapping customer contacts](includes/CustomersV3-contacts.md)]

[!include [mapping name affixes](includes/NameAffixes-msdyn-nameaffixes.md)]

[!include [mapping payment day lines](includes/PaymentDayLinesCdsV2-msdyn-paymentdaylines.md)]

[!include [mapping payment days](includes/PaymentDaysCds-msdyn-paymentdays.md)]

[!include [mapping payment schedule lines](includes/PaymentScheduleLines-msdyn-paymentschedulelines.md)]

[!include [mapping payment schedules](includes/PaymentSchedules-msdyn-paymentschedules.md)]

[!include [mapping terms of payment](includes/TermsofPayment-msdyn-paymentterms.md)]

---
title: Integrētie kreditora pamatdati
description: Šajā tēmā ir aprakstīta kreditora datu integrācija starp Finance and Operations programmām un Common Data Service.
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
ms.openlocfilehash: da451c63c23444da564307505d38699faf9df19a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770993"
---
# <a name="integrated-vendor-master"></a>Integrētie kreditora pamatdati

[!include [banner](../includes/banner.md)]

Termins *Kreditors* attiecas uz piegādātāja organizāciju vai vienīgo īpašnieku, kas ir piegādes ķēdes procesa daļa un kas piegādā preces uzņēmumam. Kaut arī *kreditors* ir reģistrēts koncepts Finance and Operations programmās, kreditora koncepts nepastāv citās Dynamics 365 programmās. Tā vietā daži uzņēmumi pārslogo Konta elementu, lai uzglabātu gan debitora informāciju, gan kreditora informāciju. Citi uzņēmumi izmanto pielāgotu kreditoru konceptu. Common Data Service integrācija atbalsta abus šos modeļus. Tāpēc atkarībā no jūsu biznesa varat iespējot jebkuru no modeļiem.

Kreditoru datu integrēšana starp Finance and Operations programmām un citām Dynamics 365 programmām ļauj veikt vairāku pamatdatu apkopošanu. Neatkarīgi no tā, no kurienes ir ieviests kreditora ieraksts, tas ir integrēts aiz ainām programmu robežās un infrastruktūras atšķirībās. 

### <a name="vendor-data-flow"></a>Kreditora datu plūsma

Ja vēlaties izmantot citas Dynamics 365 programmas kreditora pamatdatu apgūšanai un vēlaties nošķirt kreditora informāciju no debitora informācijas, varat izmantot jauno kreditora modeli.

![Kreditora datu plūsma](media/dual-write-vendor-data-flow.png)

Ja vēlaties izmantot citas Dynamics 365 programmas kreditora pamatdatu apgūšanai un vēlaties arī turpmāk izmantot Konta elementu kreditora informācijas glabāšanai, varat izmantot jauno paplašināto kreditora modeli. Šajā modelī paplašinātā kreditora informācija, piemēram, kreditoru grupa un kreditora grāmatošanas metode tiek glabāta kreditora detalizētajā informācijā.

![Kreditora paplašinātā datu plūsma](media/dual-write-vendor-detail.jpg)

Kreditora kontaktpersonas informācija ir līdzīga debitora kontaktpersonas informācijai. Nemanāmi kontaktpersonas informācija tiek glabāta un izgūta no tiem pašiem elementiem.

## <a name="templates"></a>Veidnes

Kreditora dati ietver visu informāciju par kreditoru, piemēram, kreditora grupu, adreses, kontaktinformāciju, maksājuma metodi un rēķina metodi. Elementa karšu vākšana darbojas kopā kreditora datu mijiedarbības laikā, kā redzams nākamajā tabulā.

Finance and Operations programmas | Citas Dynamics 365 programmas         | Apraksts
----------------------------|---------------------------------|------------
V2 kreditors               | Konts | Uzņēmumi, kas izmanto Konta elementu, lai glabātu kreditora informāciju, var turpināt to lietot tādā pašā veidā. Tie var arī izmantot skaidras kreditora funkcionalitātes priekšrocības, ko rada Finance and Operations programmu integrācija.
V2 kreditors               | Msdyn\_vendors | Uzņēmumiem, kas izmanto pielāgotu risinājumu kreditoriem, var izmantot standarta komplektācijas kreditora konceptu, kas ir ieviests pakalpojumā Common Data Service saistībā ar Finance and Operations programmu integrāciju. 
Kreditoru grupas | msdyn_vendorgroups | Šī veidne sinhronizē kreditoru grupas informāciju.
Piegādātāja maksāšanas metode | msdyn_vendorpaymentmethods | Šī veidne sinhronizē kreditora maksājuma metodes informāciju.
CDS kontaktpersonas V2             | kontaktpersonas                        | [Kontaktpersonas](dual-write-customer.md#cds-contacts-v2-to-contacts) veidne sinhronizē visu primāro, sekundāro un terciāro kontaktpersonas informāciju par debitoriem un kreditoriem.
Maksājumu grafika rindas      | msdyn_paymentschedulelines      | [Maksājumu grafika rindas](dual-write-customer.md#payment-schedule-lines-to-msdyn_paymentschedulelines) veidne sinhronizē maksāšanas grafika atsauces datus par debitoriem un kreditoriem.
Maksājumu grafiks            | msdyn_paymentschedules          | [Maksājumu grafiki](dual-write-customer.md#payment-schedule-to-msdyn_paymentschedules) veidne sinhronizē maksāšanas grafika atsauces datus par debitoriem un kreditoriem.
Maksāšanas dienu rindas CDS V2    | msdyn_paymentdaylines           | [Maksājuma dienas rindas](dual-write-customer.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) veidne sinhronizē maksājuma dienas rindu atsauces datus par debitoriem un kreditoriem.
Maksāšanas dienas CDS            | msdyn_paymentdays               | [Maksājumu dienas](dual-write-customer.md#payment-days-cds-to-msdyn_paymentdays) veidne sinhronizē maksāšanas dienu atsauces datus par debitoriem un kreditoriem.
Apmaksas nosacījumi            | msdyn_paymentterms              | [Apmaksas nosacījumi](dual-write-customer.md#terms-of-payment-to-msdyn_paymentterms) veidne sinhronizē apmaksas nosacījumu atsauces datus par debitoriem un kreditoriem.
Nosaukuma afiksi                | msdyn_nameaffixes               | [Nosaukumu afiksi](dual-write-customer.md#name-affixes-to-msdyn_nameaffixes) veidne sinhronizē nosaukumu afiksu atsauces datus par debitoriem un kreditoriem.

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [Vendors](dual-write/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](dual-write/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](dual-write/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]

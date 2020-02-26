---
title: Integrētie kreditoru pamatdati
description: Šajā tēmā aprakstīta kreditoru datu integrācija starp programmām Finance and Operations un Common Data Service.
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
ms.openlocfilehash: 2442a6869daac22a435c1a7504b93ea4b5c14747
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019894"
---
# <a name="integrated-vendor-master"></a>Integrētie kreditoru pamatdati

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

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
CDS kontaktpersonas V2             | kontaktpersonas                        | [Kontaktpersonas](customer-mapping.md#cds-contacts-v2-to-contacts) veidne sinhronizē visu primāro, sekundāro un terciāro kontaktpersonas informāciju par debitoriem un kreditoriem.
Maksājumu grafika rindas      | msdyn_paymentschedulelines      | [Maksājumu grafika rindas](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) veidne sinhronizē maksāšanas grafika atsauces datus par debitoriem un kreditoriem.
Maksājumu grafiks            | msdyn_paymentschedules          | [Maksājumu grafiki](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) veidne sinhronizē maksāšanas grafika atsauces datus par debitoriem un kreditoriem.
Maksāšanas dienu rindas CDS V2    | msdyn_paymentdaylines           | [Maksājuma dienas rindas](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) veidne sinhronizē maksājuma dienas rindu atsauces datus par debitoriem un kreditoriem.
Maksāšanas dienas CDS            | msdyn_paymentdays               | [Maksājumu dienas](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) veidne sinhronizē maksāšanas dienu atsauces datus par debitoriem un kreditoriem.
Apmaksas nosacījumi            | msdyn_paymentterms              | [Apmaksas nosacījumi](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) veidne sinhronizē apmaksas nosacījumu atsauces datus par debitoriem un kreditoriem.
Nosaukuma afiksi                | msdyn_nameaffixes               | [Nosaukumu afiksi](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) veidne sinhronizē nosaukumu afiksu atsauces datus par debitoriem un kreditoriem.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]

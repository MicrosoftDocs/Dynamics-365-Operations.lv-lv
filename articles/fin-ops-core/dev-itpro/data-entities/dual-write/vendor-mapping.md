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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 5c4cc92fd7809f4016d8421c98f41a85fcfedc7b
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997652"
---
# <a name="integrated-vendor-master"></a>Integrētie kreditoru pamatdati

[!include [banner](../../includes/banner.md)]



Termins *kreditors* attiecas uz piegādātāju organizāciju vai vienīgo īpašnieku, kas piegādā preces vai sniedz pakalpojumus uzņēmumam. Kaut arī *kreditors* ir reģistrēts koncepts Microsoft Dynamics 365 Supply Chain Management programmās, neviens cits kreditora koncepts nepastāv citās modeļa vadītajās Dynamics 365 programmās. Tomēr jūs varat pārslogot **Konta/Kontaktpersonas** elementu, lai glabātu informāciju par kreditoru. Integrētais kreditora šablons iepazīstina ar skaidri izteiktu kreditoru koncepciju modeļa vadītajās Dynamics 365 programmās. Varat vai nu izmantot jauno kreditora noformējumu, vai glabāt kreditora datus elementā **Konts/Kontaktpersona**. Duālais ieraksts atbalsta abas pieejas.

Abās pieejās tiek integrēti kreditoru dati starp portāliem Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service un Power Apps. Pakalpojumā Supply Chain Management dati ir pieejami darbplūsmām, piemēram, pirkšanas pieprasījumi un pirkšanas pasūtījumi.

## <a name="vendor-data-flow"></a>Kreditora datu plūsma

Ja nevēlaties glabāt kreditora datus elementā **Konts/Kontaktpersona** pakalpojumā Common Data Service, varat izmantot jauno kreditora noformējumu.

![Kreditora datu plūsma](media/dual-write-vendor-data-flow.png)

Ja nevēlaties turpināt glabāt kreditora datus elementā **Konts/Kontaktpersona** pakalpojumā , varat izmantot paplašināto kreditora noformējumu. Lai izmantotu paplašināto kreditoru noformējumu, ir jākonfigurē kreditoru darbplūsmas duālā ieraksta risinājuma pakotnē. Papildinformāciju skatiet šeit rakstā [Pārslēgšanās starp kreditoru noformējumiem ](vendor-switch.md).

![Kreditora paplašinātā datu plūsma](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Ja izmantojat Power Apps portālus pašapkalpošanās kreditoriem, kreditora informācija var plūst tieši uz Finance and Operations programmām.

## <a name="templates"></a>Veidnes

Kreditora dati ietver visu informāciju par kreditoru, piemēram, kreditora grupu, adreses, kontaktinformāciju, maksājuma metodi un rēķina metodi. Elementa karšu vākšana darbojas kopā kreditora datu mijiedarbības laikā, kā redzams nākamajā tabulā.

Finance and Operations programmas | Citas Dynamics 365 programmas     | Apraksts
----------------------------|-----------------------------|------------
V2 kreditors                   | Konts                     | Uzņēmumi, kas izmanto Konta elementu, lai glabātu kreditora informāciju, var turpināt to lietot tādā pašā veidā. Tie var arī izmantot skaidras kreditora funkcionalitātes priekšrocības, ko rada Finance and Operations programmu integrācija.
V2 kreditors                   | Msdyn\_vendors              | Uzņēmumiem, kas izmanto pielāgotu risinājumu kreditoriem, var izmantot standarta komplektācijas kreditora konceptu, kas ir ieviests pakalpojumā Common Data Service saistībā ar Finance and Operations programmu integrāciju. 
Kreditoru grupas               | msdyn\_vendorgroups         | Šī veidne sinhronizē kreditoru grupas informāciju.
Piegādātāja maksāšanas metode       | msdyn\_vendorpaymentmethods | Šī veidne sinhronizē kreditora maksājuma metodes informāciju.
CDS kontaktpersonas V2             | kontaktpersonas                    | [Kontaktpersonas](customer-mapping.md#cds-contacts-v2-to-contacts) veidne sinhronizē visu primāro, sekundāro un terciāro kontaktpersonas informāciju par debitoriem un kreditoriem.
Maksājumu grafika rindas      | msdyn\_paymentschedulelines | [Maksājumu grafika rindas](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines) veidne sinhronizē maksāšanas grafika atsauces datus par debitoriem un kreditoriem.
Maksājumu grafiks            | msdyn\_paymentschedules     | [Maksājumu grafiki](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules) veidne sinhronizē maksāšanas grafika atsauces datus par debitoriem un kreditoriem.
Maksāšanas dienu rindas CDS V2    | msdyn\_paymentdaylines      | [Maksājuma dienas rindas](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines) veidne sinhronizē maksājuma dienas rindu atsauces datus par debitoriem un kreditoriem.
Maksāšanas dienas CDS            | msdyn\_paymentdays          | [Maksājumu dienas](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays) veidne sinhronizē maksāšanas dienu atsauces datus par debitoriem un kreditoriem.
Apmaksas nosacījumi            | msdyn\_paymentterms         | [Apmaksas nosacījumi](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms) veidne sinhronizē apmaksas nosacījumu atsauces datus par debitoriem un kreditoriem.
Nosaukuma afiksi                | msdyn\_nameaffixes          | [Nosaukumu afiksi](customer-mapping.md#name-affixes-to-msdyn_nameaffixes) veidne sinhronizē nosaukumu afiksu atsauces datus par debitoriem un kreditoriem.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]

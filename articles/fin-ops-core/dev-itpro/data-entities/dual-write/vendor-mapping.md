---
title: Integrētie kreditoru pamatdati
description: Šajā rakstā aprakstīta kreditora datu integrācija starp finanšu un operāciju programmām un Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a2c32ef546a5bc74e090591c0ac9d51529299041
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112208"
---
# <a name="integrated-vendor-master"></a>Integrētie kreditoru pamatdati

[!include [banner](../../includes/banner.md)]



Termins *kreditors* attiecas uz piegādātāju organizāciju vai vienīgo īpašnieku, kas piegādā preces vai sniedz pakalpojumus uzņēmumam. Kaut arī *kreditors* ir reģistrēts koncepts Microsoft Dynamics 365 Supply Chain Management programmās, neviens cits kreditora koncepts nepastāv Customer Engagement programmās. Tomēr jūs varat pārslogot **Konta/Kontaktpersonas** tabulu, lai glabātu informāciju par kreditoru. Integrētais kreditora šablons iepazīstina ar skaidri izteiktu kreditoru koncepciju Customer Engagement programmās. Varat vai nu izmantot jauno kreditora noformējumu, vai glabāt kreditora datus tabulā **Konts/Kontaktpersona**. Duālais ieraksts atbalsta abas pieejas.

Abās pieejās tiek integrēti kreditoru dati starp portāliem Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service un Power Apps. Pakalpojumā Supply Chain Management dati ir pieejami darbplūsmām, piemēram, pirkšanas pieprasījumi un pirkšanas pasūtījumi.

## <a name="vendor-data-flow"></a>Kreditora datu plūsma

Ja nevēlaties glabāt kreditora datus tabulā **Konts/Kontaktpersona** pakalpojumā Dataverse, varat izmantot jauno kreditora noformējumu.

![Kreditora datu plūsma.](media/dual-write-vendor-data-flow.png)

Ja nevēlaties turpināt glabāt kreditora datus tabulā **Konts/Kontaktpersona** pakalpojumā , varat izmantot paplašināto kreditora noformējumu. Lai izmantotu paplašināto kreditoru noformējumu, ir jākonfigurē kreditoru darbplūsmas duālā ieraksta risinājuma pakotnē. Papildinformāciju skatiet šeit rakstā [Pārslēgšanās starp kreditoru noformējumiem](vendor-switch.md).

![Kreditora paplašinātā datu plūsma.](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Ja izmantojat portālus Power Apps pašapkalpošanās kreditoriem, kreditora informācija var plūst tieši uz finanšu un operāciju programmām.

## <a name="templates"></a>Veidnes

Kreditora dati ietver visu informāciju par kreditoru, piemēram, kreditora grupu, adreses, kontaktinformāciju, maksājuma metodi un rēķina metodi. Tabulas karšu vākšana darbojas kopā kreditora datu mijiedarbības laikā, kā redzams nākamajā tabulā.

Finance and Operations programmas | Customer engagement programmas     | Apraksts
----------------------------|-----------------------------|------------
[CDS kontaktpersonas V2](mapping-reference.md#115) | kontaktpersonas | Šī veidne sinhronizē visu primāro, sekundāro un terciāro kontaktpersonas informāciju par debitoriem un kreditoriem.
[Nosaukuma afiksi](mapping-reference.md#155) | msdyn_nameaffixes | Šī veidne sinhronizē nosaukumu afiksu atsauces datus par debitoriem un kreditoriem.
[Maksāšanas dienu rindas CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Šī veidne sinhronizē maksāšanas dienu rindas atsauces datus par debitoriem un kreditoriem.
[Maksāšanas dienas CDS](mapping-reference.md#158) | msdyn_paymentdays | Šī veidne sinhronizē maksāšanas dienu atsauces datus par debitoriem un kreditoriem.
[Maksājumu grafika rindas](mapping-reference.md#159) | msdyn_paymentschedulelines | Sinhronizē maksāšanas grafika rindu atsauces datus par debitoriem un kreditoriem.
[Maksājumu grafiks](mapping-reference.md#160) | msdyn_paymentschedules | Šī veidne sinhronizē maksāšanas grafika atsauces datus par debitoriem un kreditoriem.
[Apmaksas nosacījumi](mapping-reference.md#161) | msdyn_paymentterms | Šī veidne sinhronizē maksāšanas nosacījumu (apmaksas nosacījumu) atsauces datus par debitoriem un kreditoriem.
[Kreditori V2](mapping-reference.md#202) | msdyn_vendors | Uzņēmumi, kas kreditoriem izmanto pielāgotu risinājumu, var gūt labumu no nov atrašanās vietas kreditora koncepcijas Dataverse, kas tiek ieviesta finanšu un operāciju programmu integrācijas dēļ.
[Kreditoru grupas](mapping-reference.md#200) | msdyn_vendorgroups | Šī veidne sinhronizē kreditoru grupas informāciju.
[Piegādātāja maksāšanas metode](mapping-reference.md#201) | msdyn_vendorpaymentmethods | Šī veidne sinhronizē kreditora maksājuma metodes informāciju.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]


---
title: Common Data Service integrācijas konfigurēšana
description: Varat ieslēgt vai izslēgt integrāciju starp Common Data Service un Microsoft Dynamics 365 Human Resources instanci. Varat arī skatīt detalizētu informāciju par sinhronizāciju, dzēst izsekošanas datus un vēlreiz sinhronizēt elementu, lai palīdzētu novērst ar datiem saistītās problēmas starp abām vidēm.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 042daf3fdf7a906086af726472da050467d217e3
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009780"
---
# <a name="configure-common-data-service-integration"></a>Common Data Service integrācijas konfigurēšana

Varat ieslēgt vai izslēgt integrāciju starp Common Data Service un Microsoft Dynamics 365 Human Resources instanci. Varat arī skatīt detalizētu informāciju par sinhronizāciju, dzēst izsekošanas datus un vēlreiz sinhronizēt elementu, lai palīdzētu novērst ar datiem saistītās problēmas starp abām vidēm.

Izslēdzot integrāciju, lietotāji var veikt izmaiņas Human Resources vai Common Data Service, bet šīs izmaiņas netiek sinhronizētas starp abām vidēm.

Pēc noklusējuma integrācija starp Human Resources un Common Data Service ir vai nu izslēgta, vai ieslēgta atkarībā no demonstrāciju datu klātbūtnes vidēs.

- **Izslēgta** jaunām vidēm, kurās nav iekļauti demonstrāciju dati
- **Ieslēgta** jaunām vidēm, kurās iekļauti demonstrāciju dati

Jaunas vides, kurās iekļauti demonstrāciju dati, sāks sinhronizēt datus, kad tie tiek nodrošināti.

Iespējamas, velēsieties izslēgt integrāciju tālāk minētajās situācijās.

- Ja aizpildāt datus, izmantojot datu pārvaldības struktūru, un dati ir jāimportē vairākas reizes, lai tie būtu pareizā stāvoklī.

- Pastāv problēmas ar datiem vai nu Human Resources, vai Common Data Service. Izslēdzot integrāciju, varat dzēst ierakstu vienā vidē, nedzēšot to otrā. Atkal ieslēdzot integrāciju, ieraksts vidē, kurā tas netika dzēsts, tiks sinhronizēts ar vidi, kurā tas tika dzēsts. Sinhronizācija sākas nākamajā reizē, kad tiek izpildīts pakešuzdevums **Common Data Service integrācijas neatbildētā pieprasījuma sinhronizācija**.

> [!WARNING]
> Izslēdzot datu integrāciju, pārliecinieties, vai nerediģējat vienu un to pašu ierakstu abās vidēs. Atkal ieslēdzot integrāciju, tiks sinhronizēts pēdējais rediģētais ieraksts. Tāpēc, ja abās vidēs neveicat vienādas izmaiņas ierakstā, dati var tikt zaudēti.

## <a name="access-the-common-data-service-integration-page"></a>Piekļūšana Common Data Service integrācijas lapai

1. Human Resources instancē, kur vēlaties skatīt vai konfigurēt iestatījumus integrācijai ar Common Data Service, atlasiet elementu **Sistēmas administrēšana**.

    [![Sistēmas administrēšanas elements](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Atlasiet cilni **Saites**.

    [![Saišu cilne](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Sadaļā **Integrācijas** atlasiet **Common Data Service konfigurācija**.

    [![Common Data Service konfigurācijas saite](./media/hr-select-common-data-service-configuration.png)](./media/hr-select-common-data-service-configuration.png)

## <a name="turn-data-integration-between-human-resources-and-common-data-service-on-or-off"></a>Datu integrācijas starp Human Resources un Common Data Service ieslēgšana vai izslēgšana

- Lai ieslēgtu integrāciju, iestatiet opciju **Iespējot integrāciju uz Common Data Service** uz **Jā**.

    > [!NOTE]
    > Ieslēdzot integrāciju, dati tiks sinhronizēti nākamajā reizē, kad tiek izpildīts sinhronizēšanas pakešuzdevums **Common Data Service integrācijas neatbildētā pieprasījuma sinhronizācija**. Pēc pakešuzdevuma pabeigšanas visiem datiem jābūt pieejamiem.

- Lai izslēgtu integrāciju, iestatiet opciju uz **Nē**.

[![Common Data Service integrācijas ieslēgšana vai izslēgšana](./media/hr-enable-or-disable-common-data-service-integration.png)](./media/hr-enable-or-disable-common-data-service-integration.png)

## <a name="view-data-integration-details"></a>Datu integrācijas detalizētas informācijas skatīšana

Kopsavilkuma cilnē **Administrēšana**, kas atrodas lapā **Common Data Service integrācija**, var redzēt, kā ieraksti ir saistīti kopā starp Human Resources un Common Data Service.

- Lai skatītu elementa ierakstus, atlasiet elementu laukā **CDS elementa nosaukums**. Režģis parāda visus ierakstus, kas ir saistīti ar atlasīto elementu.

[![Elementa ierakstu skatīšana](./media/hr-common-data-service-configuration-view-entity.png)](./media/hr-common-data-service-configuration-view-entity.png)

> [!NOTE]
> Ne visi Common Data Service elementi pašlaik ir uzskaitīti. Režģī parādās tikai tie elementi, kas atbalsta pielāgoto lauku izmantošanu. Jauni elementi kļūst pieejami, izmantojot pastāvīgus Human Resources laidienus.

Režģī ir iekļauti tālāk minētie lauki.

- **CDS elementa nosaukums** — elementa nosaukums Common Data Service.
- **CDS elementa atsauce** — identifikators, ko Common Data Service izmanto ieraksta identificēšanai. Šī vērtība ir ekvivalenta Human Resources vērtībai **RecId**. Identifikatoru varat atrast, atverot Common Data Service elementu Microsoft Excel.
- **Human Resources elementa nosaukums** — elements, kas pēdējoreiz sinhronizēja datus uz Common Data Service. Elementam var būt Common Data Service prefikss vai cits prefikss.
- **Human Resources atsauce** — vērtība **RecId**, kas saistīta ar Human Resources ierakstu.
- **Tika dzēsts no CDS** — vērtība, kas norāda, vai ieraksts tika dzēsts no Common Data Service.

## <a name="remove-the-association-of-a-record-in-human-resources-from-common-data-service"></a>Human Resources ieraksta saistības noņemšana no Common Data Service

Ja izjūtat problēmas datu sinhronizācijas laikā starp Human Resources un Common Data Service, iespējams, varēsiet tās atrisināt, dzēšot izsekošanu un ļaujot vēlreiz sinhronizēt izsekošanas tabulu. Noņemot saistību, un pēc tam mainot vai dzēšot ierakstu Common Data Service, izmaiņas netiks sinhronizētas ar Human Resources. Veicot izmaiņas Human Resources, tiek izveidots jauns izsekošanas ieraksts, un ieraksts tiek atjaunināts Common Data Service.

- Lai noņemtu ieraksta saistību starp Human Resources un Common Data Service, atlasiet elementu laukā **CDS elementa nosaukums** un tad atlasiet **Dzēst izsekošanas informāciju**.

[![Izsekošanas informācija dzēšana](./media/hr-common-data-service-configuration-clear-tracking.png)](./media/hr-common-data-service-configuration-clear-tracking.png)

Lai elementā izpildītu pilnu sinhronizāciju pēc izsekošanas dzēšanas, skatiet nākamo procedūru.

## <a name="sync-an-entity-between-human-resources-and-common-data-service"></a>Elementa sinhronizācija starp Human Resources un Common Data Service

Izmantojiet šo procedūru, ja izmaiņas Common Data Service aizņem pārāk ilgu laiku, lai tās parādītos Human Resources, vai ja pēc izsekošanas dzēšanas ir jāatsvaidzina izsekošanas tabula.

- Lai izpildītu pilnu elementa sinhronizāciju starp Human Resources un Common Data Service, atlasiet elementu laukā **CDS elementa nosaukums** un pēc tam atlasiet **Sinhronizēt tūlīt**.

[![Pilnīgas sinhronizācijas izpilde](./media/hr-common-data-service-configuration-sync-now.png)](./media/hr-common-data-service-configuration-sync-now.png)



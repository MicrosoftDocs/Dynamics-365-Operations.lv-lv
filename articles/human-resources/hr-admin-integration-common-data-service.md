---
title: Dataverse integrācijas konfigurēšana
description: Šajā tēmā aprakstīta integrācija starp programmām Microsoft Dataverse un Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CDSIntegrationAdministration
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a3fc3536880ac4334154638e44f2feca8cd5860d
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8688804"
---
# <a name="configure-dataverse-integration"></a>Dataverse integrācijas konfigurēšana


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Varat ieslēgt vai izslēgt integrāciju starp Microsoft Dataverse un Microsoft Dynamics 365 Human Resources. Varat arī skatīt detalizētu informāciju par sinhronizāciju, dzēst izsekošanas datus un vēlreiz sinhronizēt tabulu, lai palīdzētu novērst ar datiem saistītās problēmas starp abām vidēm.

> [!NOTE]
> Papildinformāciju par Dataverse (iepriekš Common Data Service) un terminoloģijas atjauninājumiem skatiet sadaļā [Kas ir Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Izslēdzot integrāciju, lietotāji var veikt izmaiņas Human Resources vai Dataverse, bet šīs izmaiņas netiek sinhronizētas starp abām vidēm.

Pēc noklusējuma datu integrācijas starp Personāla vadību un Dataverse ir izslēgta.

Iespējamas, velēsieties izslēgt integrāciju tālāk minētajās situācijās.

- Ja aizpildāt datus, izmantojot datu pārvaldības struktūru, un dati ir jāimportē vairākas reizes, lai tie būtu pareizā stāvoklī.

- Pastāv problēmas ar datiem vai nu Human Resources, vai Dataverse. Izslēdzot integrāciju, varat dzēst ierakstu vienā vidē, nedzēšot to otrā. Atkal ieslēdzot integrāciju, ieraksts vidē, kurā tas netika dzēsts, tiek sinhronizēts ar vidi, kurā tas tika dzēsts. Sinhronizācija sākas nākamajā reizē, kad tiek izpildīts pakešuzdevums **Dataverse integrācijas neatbildētā pieprasījuma sinhronizācija**.

> [!WARNING]
> Izslēdzot datu integrāciju, pārliecinieties, vai nerediģējat vienu un to pašu ierakstu abās vidēs. Atkal ieslēdzot integrāciju, tiks sinhronizēts pēdējais rediģētais ieraksts. Tāpēc, ja abās vidēs neveicat vienādas izmaiņas ierakstā, dati var tikt zaudēti.

## <a name="access-the-dataverse-integration-page"></a>Piekļūšana Dataverse integrācijas lapai

1. Human Resources instancē, kur vēlaties skatīt vai konfigurēt iestatījumus integrācijai ar Dataverse, atlasiet elementu **Sistēmas administrēšana**.

    [![Sistēmas administrēšanas elements.](./media/hr-select-system-administration.png)](./media/hr-select-system-administration.png)

2. Atlasiet cilni **Saites**.

    [![Saišu cilne.](./media/hr-system-administration-links.png)](./media/hr-system-administration-links.png)

3. Sadaļā **Integrācijas** atlasiet **Dataverse konfigurācija**.

    [![Dataverse konfigurācijas saite.](./media/hr-admin-integration-dataverse-select.png)](./media/hr-admin-integration-dataverse-select.png)

## <a name="turn-data-integration-between-human-resources-and-dataverse-on-or-off"></a>Datu integrācijas starp Human Resources un Dataverse ieslēgšana vai izslēgšana

- Lai ieslēgtu integrāciju, iestatiet opciju **Iespējot Dataverse integrāciju** uz **Jā** lapā **Microsoft Dataverse integrācija**.

    > [!NOTE]
    > Ieslēdzot integrāciju, dati tiks sinhronizēti nākamajā reizē, kad tiek izpildīts sinhronizēšanas pakešuzdevums **Dataverse integrācijas neatbildētā pieprasījuma sinhronizācija**. Pēc pakešuzdevuma pabeigšanas visiem datiem jābūt pieejamiem.

- Lai izslēgtu integrāciju, iestatiet opciju uz **Nē**.

[![Pakalpojuma Dataverse integrācijas ieslēgšana vai izslēgšana.](./media/hr-admin-integration-dataverse-enable-disable.png)](./media/hr-admin-integration-dataverse-enable-disable.png)

> [!WARNING]
> Lai veiktu datu migrācijas uzdevumus, ieteicams izslēgt Dataverse integrāciju. Lielas datu augšupielādes var būtiski ietekmēt veiktspēju. Piemēram, 2000 darbinieku augšupielādēšana var aizņemt vairākas stundas, ja integrācija ir iespējota, un mazāk par vienu stundu, kad tā ir atspējota. Šajā piemērā sniegtie numuri ir tikai demonstrācijas nolūkiem. Precīzs laika apjoms, kas nepieciešams, lai importētu ierakstus, var būtiski atšķirties atkarībā no daudziem faktoriem.

## <a name="view-data-integration-details"></a>Datu integrācijas detalizētas informācijas skatīšana

Kopsavilkuma cilnē **Administrēšana**, kas atrodas lapā **Microsoft Dataverse integrācija**, var redzēt, kā rindas ir saistītas kopā starp Human Resources un Dataverse.

- Lai skatītu tabulas rindas, atlasiet tabulu laukā **Dataverse tabulas**. Režģis parāda visas rindas, kas ir saistītas ar atlasīto tabulu.

> [!NOTE]
> Ne visas Dataverse tabulas pašlaik ir uzskaitītas. Režģī parādās tikai tās tabulas, kas atbalsta pielāgoto lauku izmantošanu. Jaunas tabulas kļūst pieejamas, izmantojot pastāvīgus Human Resources laidienus.

Režģī ir iekļauti tālāk minētie lauki.

- **Dataverse tabula** – tabulas nosaukums Dataverse.
- **Dataverse tabulas atsauce** – identifikators, ko Dataverse izmanto ieraksta identificēšanai. Šī vērtība ir ekvivalenta Human Resources vērtībai **RecId**. Identifikatoru varat atrast, atverot Dataverse tabulu Microsoft Excel.
- **Human Resources elementa nosaukums** — Human Resources elements, kas pēdējoreiz sinhronizēja datus uz Dataverse. Elementam var būt Dataverse prefikss vai cits prefikss.
- **Human Resources atsauce** — vērtība **RecId**, kas saistīta ar Human Resources ierakstu.
- **Tika dzēsts no Dataverse** – vērtība, kas norāda, vai rinda tika dzēsta no Dataverse.

> [!NOTE]
> Ieraksti Human Resources atbilst rindām, kas atrodas Dataverse.

## <a name="remove-the-association-of-a-human-resources-record-from-a-dataverse-row"></a>Human Resources ieraksta saistības noņemšana no Dataverse rindas

Ja izjūtat problēmas datu sinhronizācijas laikā starp Human Resources un Dataverse, iespējams, varēsiet tās atrisināt, dzēšot izsekošanu un ļaujot vēlreiz sinhronizēt izsekošanas tabulu. Noņemot saistību, un pēc tam mainot vai dzēšot rindu Dataverse, izmaiņas netiks sinhronizētas ar Human Resources. Veicot izmaiņas Human Resources, tiek izveidots jauns izsekošanas ieraksts, un rinda tiek atjaunināta Dataverse.

- Lai noņemtu ieraksta saistību starp Resources ierakstu un Dataverse rindu, atlasiet tabulu laukā **Dataverse tabula** un pēc tam atlasiet **Dzēst izsekošanas informāciju**.

[![Izsekošanas informācija dzēšana.](./media/hr-admin-integration-dataverse-clear-tracking.png)](./media/hr-admin-integration-dataverse-clear-tracking.png)

Lai tabulā izpildītu pilnu sinhronizāciju pēc izsekošanas dzēšanas, skatiet nākamo procedūru.

## <a name="sync-a-table-between-human-resources-and-dataverse"></a>Tabulas sinhronizācija starp Human Resources un Dataverse

Izmantojiet šo procedūru, ja:

- Izmaiņas no Dataverse aizņem pārāk daudz laika, lai parādītos Personāla vadībā.

- Pēc izsekošanas notīrīšanas ir jāatsvaidzina izsekošanas tabula.

Lai veiktu pilnu sinhronizāciju tabulā starp Human Resources un Dataverse:

1. Atlasiet tavulu laukā **Dataverse tabula**.

2. Atlasiet **Sinhronizēt tagad**.

[![Pilnīgas sinhronizācijas izpilde.](./media/hr-admin-integration-dataverse-sync-now.png)](./media/hr-admin-integration-dataverse-sync-now.png)

## <a name="see-also"></a>Skatiet arī

[Dataverse tabulas](hr-developer-entities.md)<br>
[Pakalpojuma Dataverse virtuālo tabulu konfigurēšana](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Bieži uzdotie jautājumi par Human Resources tabulām](hr-admin-virtual-entity-faq.md)<br>
[Kas ir Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Terminoloģijas atjauninājumi](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Daļēja novietojuma cikla inventarizācija
description: Cikla inventarizācijas plāni vada faktiskās inventarizācijas operācijas. Varat pieprasīt, ka tiek uzskaitītas tikai noteiktas preces un preču varianti, nevis lai visi rīcībā esošie krājumi kādā novietojumā.
author: perlynne
manager: tfehr
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable, WHSRFMenuItemCycleCount, WHSCycleCountPlanListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f228f10c5aeaca3f4fc9b97bf7b6cc4af1592b8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973614"
---
# <a name="partial-location-cycle-counting"></a>Daļēja novietojuma cikla inventarizācija

[!include [banner](../includes/banner.md)]

Cikla inventarizācijas plāni vada faktiskās inventarizācijas operācijas. Varat pieprasīt, ka tiek uzskaitītas tikai noteiktas preces un preču varianti, nevis lai visi rīcībā esošie krājumi kādā novietojumā.

Izmantojot cikla inventarizācijas plānus, lai izveidotu inventarizācijas darbu, varat vadīt faktiskās inventarizācijas operācijas. Varat pieprasīt, ka tiek uzskaitītas tikai noteiktas preces un preču varianti, nevis lai visi rīcībā esošie krājumi kādā novietojumā. Filtrējot pēc atsevišķām precēm, noliktavas pārvaldnieks var samazināt pārskatīšanas pieskaitāmo daudzumu, izvairīties no konsolidācijas kļūdām un ietaupīt laiku.

## <a name="how-to-configure-partial-location-cycle-counting"></a>Kā konfigurēt daļēju novietojuma cikla inventarizāciju

Kad noliktavas darba procesu izmantojat inventarizācijas operācijām, katram novietojumam tiek izveidots darba virsraksts. Kad definējat cikla inventarizācijas plānu, varat izmantot vaicājumu **Atlasīt novietojumus**, lai ierobežotu izveidoto cikla inventarizācijas darbu. Kad atlasāt preces šim cikla inventarizācijas plānam, varat atlasīt gan preču, gan preču variantu vaicājumus, lai precizētu, kas tiek uzskaitīts.

Varat ar cikla inventarizācijas plānu saistīt kādu **darba veidni**, lai definētu veidu, kā ir jāveido cikla inventarizācijas darbs. Uz darba veidni inventarizācijas operācijām ir tieša atsauce no cikla inventarizācijas plāna.

Kad definējat darba veidnes informāciju, varat izmantot opciju **Darba rindas pārtraukumi**, lai norādītu, vai inventarizācijas darba rindas ir jāgrupē pēc krājuma numura vai pēc preces varianta numura. Šī iestatīšana ir nepieciešama, ja vēlaties uzskaitīt rīcībā esošos krājumus tikai konkrētām precēm kādā novietojumā. Izveidotajās cikla inventarizācijas darbu rindās būs jūsu šeit definētais informācijas līmenis, un vadītā inventarizācijas operācija tiks apstrādāta, pamatojoties uz šo līmeni.

Ja cikla inventarizācijas plānus saistāt ar darba veidnēm, izmantojot opciju **Darba rindu pārtraukumi**, tad izveidotajam cikla inventarizācijas darbam ir atlasīts lauks **Daļēja cikla inventarizācija**, un tiek izveidotas vairākas cikla inventarizācijas darba rindas, pamatojoties uz darba veidnes definīciju.

Lai varētu apstrādāt daļēja cikla inventarizācijas darbu, kā daļa no cikla inventarizācijas iestatīšanas jums mobilās ierīces izvēlnes vienumam ir jāatlasa vismaz vienums **Parādīt krājuma numuru**. Noliktavas operatoram tiks lūgts ierakstīt tikai uzskaites informāciju, kas ir saistīta ar inventarizācijas rindām (krājumu kodus un preču dimensijas). Visi citi rīcībā esošie krājumi šim inventarizācijas procesam tiks ignorēti.

Daļējā cikla inventarizācija procesam datums/laiks **Pēdējā cikla inventarizācija** novietojumam netiks atjaunināts, kaut arī visi krājumi, kas atrodas norādītajā novietojumā, tiek saskaitīti. Daļējā cikla inventarizācija neņem vērā parametru **Dienas starp cikla inventarizāciju** lapā **Cikla inventarizācijas plāni** . Daļēja cikla inventarizācija neatbalsta vienlaicīgu vairāku krājumu inventarizāciju vienā un tajā pašā novietojumā. Daļējas cikla inventarizācijas funkcionalitātes rezultātā viens un tāds pats novietojums krājumam var tikt skaitīts vairākas reizes, kad tiek palaists **Procesa cikla inventarizācijas plāns** . Lai izvairītos no šāda scenārija, norādiet filtrus laukā **Atlasīt novietojumus** .

> [!NOTE]
> Noliktavas programma nenodrošina pogu **Pievienot LP vai preci**, kad izmantojat daļēju cikla skaitīšanas procesu.

## <a name="example"></a>Paraugs

Šajā piemērā noliktavā 61 ir jāuzskaita tikai krājums numur A0001.

1. Tiek izveidota jauna darba veidne cikla inventarizācijai. Lai inventarizācijas darbu rindas grupētu pēc krājuma koda, tiek izmantota opcija **Darba rindas pārtraukumi**. Tādēļ izveidotajā cikla inventarizācijas darbā būs rindas katram krājuma kodam. Rindas varat grupēt arī pēc preces varianta numura.
1. Tiek izveidots jauns cikla inventarizācijas plāns, kura ir atsauce uz jaunizveidoto darba veidni. Šis cikla inventarizācijas plāns ietver visus novietojumus noliktavā 61 (**Atlasīt novietojumus** vaicājums), kuros atrodas krājums numuram A0001. Konkrētu preču atlase tiek definēta sadaļā **Cikla inventarizācijas preču atlases**.
1. Varat atlasīt preces cikla inventarizācijas plāniem, iestatot lauka **Iztukšot atrašanās vietas** vērtību **Izslēgt tukšos**. Apstrādājot cikla inventarizācijas plānu, tiek izveidots daļēja cikla inventarizācijas darbs krājumam Nr. A0001. Faktisko uzskaites procesu var veikt, izmantojot mobilās ierīces izvēlnes vienumu vadītajai cikla inventarizācijai.

## <a name="additional-resources"></a>Papildu resursi

[Cikla inventarizācija](cycle-counting.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: "Daļēja novietojuma cikla inventarizācija"
description: "Cikla inventarizācijas plāni vada faktiskās inventarizācijas operācijas. Varat pieprasīt, ka tiek uzskaitītas tikai noteiktas preces un preču varianti, nevis lai visi rīcībā esošie krājumi kādā novietojumā."
author: perlynne
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSCycleCountPlan, WHSWorkLineCycleCount, WHSWorkTemplateLineGroup, WHSWorkTemplateTable
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 626b2f9f35b94124168adb7bb09c75a086d38a97
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="partial-location-cycle-counting"></a>Daļēja novietojuma cikla inventarizācija

[!include[banner](../includes/banner.md)]


Cikla inventarizācijas plāni vada faktiskās inventarizācijas operācijas. Varat pieprasīt, ka tiek uzskaitītas tikai noteiktas preces un preču varianti, nevis lai visi rīcībā esošie krājumi kādā novietojumā.

Izmantojot cikla inventarizācijas plānus, lai izveidotu inventarizācijas darbu, varat vadīt faktiskās inventarizācijas operācijas. Varat pieprasīt, ka tiek uzskaitītas tikai noteiktas preces un preču varianti, nevis lai visi rīcībā esošie krājumi kādā novietojumā. Filtrējot pēc atsevišķām precēm, noliktavas pārvaldnieks var samazināt pārskatīšanas pieskaitāmo daudzumu, izvairīties no konsolidācijas kļūdām un ietaupīt laiku.

## <a name="how-to-configure-partial-location-cycle-counting"></a>Kā konfigurēt daļēju novietojuma cikla inventarizāciju
Kad noliktavas darba procesu izmantojat inventarizācijas operācijām, katram novietojumam tiek izveidots darba virsraksts. Kad definējat cikla inventarizācijas plānu, varat izmantot vaicājumu **Atlasīt novietojumus**, lai ierobežotu izveidoto cikla inventarizācijas darbu. Kad atlasāt preces šim cikla inventarizācijas plānam, varat atlasīt gan preču, gan preču variantu vaicājumus, lai precizētu, kas tiek uzskaitīts. 

Varat ar cikla inventarizācijas plānu saistīt kādu **darba veidni**, lai definētu veidu, kā ir jāveido cikla inventarizācijas darbs. Uz darba veidni inventarizācijas operācijām ir tieša atsauce no cikla inventarizācijas plāna. 

Kad definējat darba veidnes informāciju, varat izmantot opciju **Darba rindas pārtraukumi**, lai norādītu, vai inventarizācijas darba rindas ir jāgrupē pēc krājuma numura vai pēc preces varianta numura. Šī iestatīšana ir nepieciešama, ja vēlaties uzskaitīt rīcībā esošos krājumus tikai konkrētām precēm kādā novietojumā. Izveidotajās cikla inventarizācijas darbu rindās būs jūsu šeit definētais informācijas līmenis, un vadītā inventarizācijas operācija tiks apstrādāta, pamatojoties uz šo līmeni. 

Ja cikla inventarizācijas plānus saistāt ar darba veidnēm, izmantojot opciju **Darba rindu pārtraukumi**, tad izveidotajam cikla inventarizācijas darbam ir atlasīts lauks **Daļēja cikla inventarizācija**, un tiek izveidotas vairākas cikla inventarizācijas darba rindas, pamatojoties uz darba veidnes definīciju. 

Lai varētu apstrādāt daļēja cikla inventarizācijas darbu, kā daļa no cikla inventarizācijas iestatīšanas jums mobilās ierīces izvēlnes vienumam ir jāatlasa vismaz vienums **Parādīt krājuma numuru**. Noliktavas operatoram tiks lūgts ierakstīt tikai uzskaites informāciju, kas ir saistīta ar inventarizācijas rindām (krājumu kodus un preču dimensijas). Visi citi rīcībā esošie krājumi šim inventarizācijas procesam tiks ignorēti. 

Attiecībā uz daļēja cikla inventarizācijas procesu datums/laiks **Pēdējā cikla inventarizācija** novietojumam netiek atjaunināts.

## <a name="example"></a>Piemērs
Šajā piemērā noliktavā 61 ir jāuzskaita tikai krājums numur A0001.

1.  Tiek izveidota jauna darba veidne cikla inventarizācijai. Lai inventarizācijas darbu rindas grupētu pēc krājuma koda, tiek izmantota opcija **Darba rindas pārtraukumi**. Tādēļ izveidotajā cikla inventarizācijas darbā būs rindas katram krājuma kodam. Rindas varat grupēt arī pēc preces varianta numura.
2.  Tiek izveidots jauns cikla inventarizācijas plāns, kura ir atsauce uz jaunizveidoto darba veidni. Šis cikla inventarizācijas plāns ietver visus novietojumus noliktavā 61 (vaicājums **Atlasīt novietojumus**), kuros atrodas krājums numuram A0001. Konkrētu preču atlase tiek definēta sadaļā **Cikla inventarizācijas preču atlases**.
3.  Preces cikla inventarizācijas plāniem varat atlasīt, laukam **Tukšie novietojumi** iestatot vērtību **Izslēgt tukšos**. Kad šis cikla inventarizācijas plāns tiek apstrādāts, tiek izveidots daļēja cikla inventarizācijas darbs krājumam numur A0001. Faktisko uzskaites procesu var veikt, izmantojot mobilās ierīces izvēlnes vienumu vadītajai cikla inventarizācijai.



<a name="see-also"></a>Skatiet arī
--------

[Cikla inventarizācija](cycle-counting.md)


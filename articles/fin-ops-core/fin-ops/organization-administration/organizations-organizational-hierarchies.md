---
title: Organizāciju un organizāciju hierarhiju pārskats
description: Organizācijas hierarhijas pārstāv attiecības starp organizācijām, kas veido jūsu uzņēmumu.
author: sericks007
ms.date: 01/03/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMOperatingUnit,
audience: Application User
ms.reviewer: sericks
ms.custom:
- "17291"
- intro-internal
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c8e8f2c2004582f42c3f464fedf9f3d049b5278f
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2022
ms.locfileid: "7991738"
---
# <a name="organizations-and-organizational-hierarchies-overview"></a>Organizāciju un organizāciju hierarhiju pārskats

[!include [banner](../includes/banner.md)]

Organizācija ir cilvēku grupa, kas strādā kopā, lai nodrošinātu biznesa procesu vai sasniegtu mērķi. Organizācijas hierarhijas pārstāv attiecības starp organizācijām, kas veido jūsu uzņēmumu.

## <a name="organizations"></a>Organizācijas

Varat definēt šādus iekšējo organizāciju veidus: juridiskas personas, pārvaldības struktūrvienības un darba grupas.

Visas iekšējās organizācijas ir **Puses** elementa veidi. Tāpēc šīs organizācijas izmanto adrešu grāmatu adreses un kontaktinformācijas saglabāšanai. Puse, kas var būt persona vai organizācija, var piederēt vienai vai vairākām adrešu grāmatām.

### <a name="legal-entities"></a>Juridiskās personas

Juridiskā persona ir organizācija, kurai ir reģistrēta vai likumā noteikta juridiskā struktūra. Juridiskas personas var noslēgt juridiskos līgumus, un tām ir nepieciešams sagatavot pārskatus, lai ziņotu par savu veiktspēju.

Uzņēmums ir juridiskas personas veids. Pašlaik uzņēmums ir vienīgais juridiskas personas veids, ko varat izveidot, un katra juridiska persona ir saistīta ar uzņēmuma ID. Šī saistība pastāv, jo daži programmas funkcionālie apgabali izmanto uzņēmuma ID vai DataAreaId savos datu modeļos. Šajos funkcionālos apgabalos uzņēmumi tiek izmantoti kā datu drošības robeža. Lietotāji var piekļūt tikai tā uzņēmuma datiem, kurš ir pašlaik pieteicies sistēmā.

### <a name="operating-units"></a>Pārvaldības struktūrvienības

Pārvaldības struktūrvienība ir organizācija, kas tiek lietota, lai sadalītu ekonomisko resursu un operatīvo procesu kontroli biznesā. Cilvēkiem pārvaldības struktūrvienībā ir pienākums maksimāli izmantot ierobežotos resursus, uzlabot procesus un atskaitīties par savu sniegumu.

Ir pieejami šādi pārvaldības struktūrvienību veidi: izmaksu centri, biznesa vienības, vērtību plūsmas, nodaļas un komercijas kanāli. Tabulā ir sniegta papildinformācija par katru pārvaldības struktūrvienības veidu.

| Pārvaldības struktūrvienības tips | Apraksts | Mērķis |
|---------------------|-------------|---------|
| Izmaksu centrs         | Pārvaldības struktūrvienība, kuras vadītāji atskaitās par budžetā ieplānotajiem un faktiskajiem izdevumiem. | Tiek izmantots vairāku juridisko personu biznesa procesu pārvaldībai un darbības kontrolei. |
| Biznesa vienība       | Pusautonoma pārvaldības struktūrvienība, kura tiek izveidot, lai izpildītu stratēģiskus biznesa mērķus. | Tiek izmantots finanšu pārskatiem, pamatojoties uz nozari vai preču rindu, kurus organizācija sastāda neatkarīgi no juridiskām personām. |
| Vērtību plūsma        | Pārvaldības struktūrvienība, kas kontrolē vienu vai vairākas ražošanas plūsmas. | Parasti tiek izmantots lean manufacturing, lai kontrolētu aktivitātes un plūsmas, kuras ir nepieciešamas, lai piegādātu preces vai pakalpojumus patērētājiem. |
| Nodaļa          | Pārvaldības struktūrvienība, kas pārstāv organizācijas kategoriju vai funkcionālo daļu, kas veic noteiktu uzdevumu, piemēram, pārdošanu vai uzskaiti. | Tiek izmantots, lai ziņotu par funkcionālajām jomām. Nodaļa var būt atbildīga par peļņu un zaudējumiem un var sastāvēt no izmaksu centru grupas. |
| Mazumtirdzniecības kanāls      | Pārvaldības struktūrvienība, kas pārstāv biznesa un biznesa veikalu, tiešsaistes veikalu vai zvanu centru. | Tiek izmantot viena vai vairāku veikalu pārvaldībai un darbības kontrolei vienā vai vairākās juridiskās personās. |

### <a name="teams"></a>Grupas

Komanda ir organizācija, kuras dalībniekiem piemīt kopīgā atbildība, interese un mērķis. Komandas nevar izmantot organizācijas hierarhijās.

## <a name="organizational-hierarchies"></a>Organizācijas hierarhijas

Iestatiet organizācijas hierarhijas, lai apskatītu savu uzņēmumu no dažādām perspektīvām un veidotu pārskatus. Piemēram, var iestatīt vienu juridisku personu hierarhiju nodokļu, juridisko vai ar likumu noteikto pārskatu veidošanai. Iestatiet hierarhiju, kas balstās uz pārvaldības struktūrvienību, lai veidotu pārskatus par finanšu informāciju, kura saskaņā ar likumu nav obligāta, bet tiek izmantota iekšējās kontroles nolūkiem. Piemēram, var izveidot pirkšanas hierarhiju, lai kontrolētu pirkšanas politiku, noteikumus un biznesa procesus.

> [!NOTE]
> Pēc pārvaldības struktūrvienības pievienošanas hierarhijai pārvaldības struktūrvienību nevar dzēst. 

Katrai hierarhijai tiek piešķirts mērķis. Hierarhijas mērķis nosaka organizāciju veidus, ko var iekļaut hierarhijā. Mērķis nosaka arī pielietojuma scenārijus, kuros hierarhiju var izmantot.

Organizācijas hierarhijā var koplietot parametrus, politiku un transakcijas. Organizācija var mantot vai ignorēt savas pamatorganizācijas parametrus. Tomēr koplietojamie pamatdati, piemēram, preces un adrešu grāmatas, attiecas uz visu organizāciju un tos nevar ignorēt atsevišķām organizācijām. Organizāciju un hierarhiju izveidi ir rūpīgi jāplāno. Papildinformāciju skatiet rakstā [Jūsu organizācijas hierarhijas plānošana](plan-organizational-hierarchy.md).

## <a name="additional-resources"></a>Papildu resursi
- [Organizācijas hierarhijas plānošana](plan-organizational-hierarchy.md)
- [Organizācijas hierarhijas izveide](tasks/create-organization-hierarchy.md)
- [Izveidot juridisko personu](tasks/create-legal-entity.md)
- [Pārvaldības struktūrvienības izveide](tasks/create-operating-unit.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

---
title: Mazumtirdzniecības transakciju konsekvences pārbaudītājs
description: Šajā tēmā ir aprakstīta mazumtirdzniecības transakciju konsekvences pārbaudītāja funkcionalitāte programmā Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 972c4d6b244eebc85cc801353ce8fb25ecbc0655
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517117"
---
# <a name="retail-transaction-consistency-checker"></a>Mazumtirdzniecības transakciju konsekvences pārbaudītājs


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Šajā tēmā ir aprakstīta mazumtirdzniecības transakciju konsekvences pārbaudītāja funkcionalitāte, kas ir ieviesta Microsoft Dynamics 365 for Finance and Operations versijā 8.1.3. Konsekvences pārbaudītājs identificē un izolē nekonsekventas transakcijas, pirms tās ir uzņemtas pārskatu grāmatošanas procesā.

Kad pārskats tiek grāmatots programmā Retail, grāmatošana var būt nesekmīga, jo mazumtirdzniecības transakciju tabulās pastāv nekonsekventi dati. Šādu datu problēmu var būt izraisījušas neparedzētas problēmas pārdošanas punkta (point of sale — POS) programmā, kā arī tādas var rasties, ja transakcijas tika nepareizi importētas no trešās puses POS sistēmām. Tālāk ir uzskaitīti daži no šādas nekonsekvences potenciālās rašanās piemēriem. 

  - Transakcijas kopsumma virsraksta tabulā neatbilst transakcijas kopsummai rindās.
  - Rindu skaits virsraksta tabulā neatbilst rindu skaitam transakcijas tabulā.
  - Nodokļi virsraksta tabulā neatbilst nodokļu summai rindās. 
  
Kad pārskatu grāmatošanas process uzņem nekonsekventas transakcijas, tiek izveidoti nekonsekventi pārdošanas rēķini un maksājumu žurnāli, līdz ar to viss pārskata grāmatošanas process ir nesekmīgs. Lai atkoptu pārskatus no šāda stāvokļa, ir jāizmanto sarežģīti datu labojumi vairākās transakciju tabulās. Mazumtirdzniecības transakciju konsekvences pārbaudītājs neļauj šādu problēmu rašanos.

Nākamajā diagrammā ir parādīts grāmatošanas process ar transakciju konsekvences pārbaudītāju.

![Pārskatu grāmatošanas process ar mazumtirdzniecības darījumu konsistences pārbaudītāju](./media/validchecker.png "Pārskatu grāmatošanas process ar mazumtirdzniecības darījumu konsistences pārbaudītāju")

Pakešuzdevums **Pārbaudīt veikala transakcijas** pārbauda mazumtirdzniecības darījumu tabulu konsekvenci tālāk norādītajos scenārijos.

- Debitora konts — pārliecinās, vai HQ debitoru pamatdatu mazumtirdzniecības transakciju tabulās pastāv attiecīgais debitora konts.
- Rindu skaits — pārliecinās, vai transakciju virsrakstu tabulā norādītais rindu skaits atbilst rindu skaitam pārdošanas transakciju tabulās.

## <a name="set-up-the-consistency-checker"></a>Konsekvences pārbaudītāja iestatīšana
Konfigurējiet pakešuzdevumu “Validēt veikala transakcijas” regulārai izpildīšanai sadaļā **Mazumtirdzniecība \> Mazumtirdzniecības IT \> POS grāmatošana**. Pakešuzdevumu var plānot atkarībā no veikala organizācijas hierarhijas, līdzīgi kā tiek iestatīti procesi “Aprēķināt pārskatu partijā” un “Grāmatot pārskatu partijā”. Iesakām šo pakešuzdevumu konfigurēt tā, lai dienas laikā tas tiktu izpildīts vairākas reizes, un to ieplānot tā, lai tas tiktu izpildīts katras P darba izpildes beigās.

## <a name="results-of-validation-process"></a>Validēšanas procesa rezultāti
Šī pakešuzdevuma validēšanas pārbaudes rezultāti tiek atzīmēti atbilstošajā mazumtirdzniecības transakcijā. Lauks **Validācijas statuss** mazumtirdzniecības transakcijas ierakstā ir iestatīts uz **Sekmīgs** vai **Kļūda**, un pēdējās validēšanas izpildes datums ir redzams laukā **Pēdējās validēšanas laiks**.

Lai redzētu aprakstošāku kļūdas tekstu saistībā ar validēšanas kļūmi, atlasiet attiecīgo mazumtirdzniecības veikala transakcijas ierakstu un noklikšķiniet uz pogas **Validācijas kļūdas**.

Uz pārskatiem netiek nogādātas transakcijas, kam validācijas pārbaude ir nesekmīga, un transakcijas, kas vēl nav validētas. Procesa “Aprēķināt pārskatu” laikā lietotājiem tiek ziņots, vai pastāv transakcijas, kas varēja tikt ietvertas pārskatā, bet netika tajā ietvertas.

Ja tiek atrasta kāda validācijas kļūda, vienīgais veids, kā šo kļūdu novērst, ir sazināties ar Microsoft atbalsta dienestu. Turpmākajos laidienos tiks pievienota iespēja lietotājiem izlabot nesekmīgos ierakstus, izmantojot lietotāja interfeisu. Kļūs pieejamas arī reģistrēšanas un auditēšanas iespējas, lai izsekotu modifikāciju vēsturi.

> [!NOTE]
> Kādā no turpmākajiem laidieniem tiks pievienotas papildu validēšanas kārtulas, lai atbalstītu vairāk scenāriju.

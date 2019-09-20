---
title: Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 14. marts)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-03-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ee8e076174acba8e706991f3086d6299a10945ec
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742497"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-march-14-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 14. marts)

[!include [banner](includes/banner.md)]

Šajā tēmā ir aprakstīti jaunie vai izmainītie programmas Talent līdzekļi.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract
Šajā laidienā ir ietverti nelieli kļūdu labojumi.

## <a name="changes-in-onboarding"></a>Izmaiņas pievienošanas procesā
Šajā laidienā ir ietverti nelieli kļūdu labojumi.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR
**8.1.2186 būvējums**

### <a name="performance-management-not-working-in-all-scenarios-when-using-duplicate-security-roles"></a>Veiktspējas pārvaldība nedarbojas visos scenārijos, kad tiek lietotas dublētas drošības lomas
Šajā laidienā veiktās izmaiņas ļauj izmantot veiktspējas pārvaldības scenārijus, kad tiek lietotas standarta vai dublētas lomas.

### <a name="mass-assign-checklists-to-workers"></a>Kontrolsarakstu piešķiršana nodarbinātajiem masveidā
Līdz ar šīs izmaiņas ieiešanu tagad varat atlasīt vairākus darbiniekus un lielapjomā piešķirt šiem darbiniekiem vienu vai vairākus kontrolsarakstus. 

### <a name="platform-update-24"></a>Platform update 24
Papildinformāciju par atjauninājumu Platform update 24 skatiet [Jaunumi un izmaiņas Finance and Operations atjauninājumā Platform update 24 (2019. gada marts)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24). Būtiskas izmaiņas atjauninājumā platform 24 ietver tālāk uzskaitītās. 

- Programmā Talent ir iespējoti brīdinājumi.
- Atjauninātā navigācijas josla tagad atrodas atbilstoši Office galvenei.

### <a name="office-location-update-switches-the-context-to-the-top-of-the-worker-list"></a>Biroja atrašanās vietas atjaunināšana pārslēdz kontekstu uz nodarbināto saraksta sākumu
Līdz ar pašreizējā laidiena ieviešanu biroja atrašanās vietas mainīšana vairs nepārslēdz kontekstu nodarbinātajam, kuru jūs skatāt, kamēr piešķirat biroja atrašanās vietu.

### <a name="position-assignment-end-date-doesnt-display-correctly-on-worker-hire-and-transfer-actions"></a>Nodarbinātā darbā pieņemšanas un pārsūtīšanas darbībās amata norīkojuma beigu datums netiek rādīts pareizi
Izmantojot darbības, amata norīkojuma beigu datumi tagad tiek rādīti pareizi, pamatojoties uz lietotāja vēlamo laika joslu.

### <a name="common-data-service-job-entity-doesnt-allow-job-type-and-job-function-fields-to-update"></a>Common Data Service darba elements neļauj atjaunināt laukus Darba tips un Darba funkcija
Common Data Service elementi tagad tiek sinhronizēti pareizi, kad notiek atjaunināšana, izmantojot Common Data Service.

## <a name="coming-soon"></a>Drīzumā

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Papildu atlīdzības drošība (fiksētā un mainīgā)
Daudzās organizācijās atlīdzību un atvieglojumu pārvaldnieki var piekļūt tikai noteiktiem atlīdzības ierakstiem. Piemēram, tie varētu būt par vadītājiem vai reģionālajiem darbiniekiem. Šīs izmaiņas dod iespēju personāla vadībai pārvaldīt un uzturēt atlīdzības plānus dažādām darbinieku grupām organizācijā. Fiksētajiem un mainīgajiem plāniem var piešķirt drošības lomas, kuras nosaka piekļuvi plāniem un ar šiem plāniem saistītajiem darbinieku datiem, piemēram, algu vai prēmiju ierakstiem. Atlīdzību šiem darbiniekiem var apstrādāt tikai lietotāji, kuriem ir lomas ar piešķirtu piekļuvi.

###  <a name="email-support-for-alerts"></a>E-pasta atbalsts brīdinājumiem
Līdz ar atjauninājuma Platform update 24 ieviešanu lietotāji var izveidot brīdinājumu kārtulas, kas automātiski izsūta e-pasta paziņojumus kontaktpersonām, ja kāds notikums tās aktivizē.

### <a name="duplicate-employee-check-interface-changes"></a>Dublētu darbinieku pārbaude: interfeisa izmaiņas
Līdz ar šīs izmaiņas ieviešanu dublikāti tiek noteikti, kad aizpildāt vārda/uzvārda/nosaukuma laukus, un statuss parāda, cik dublikātu tika atrasts. Varat atlasīt norādīto saiti, lai atvērtu jaunu lapu, kur novērtēt, vai atrastā atbilstība ir jāizmanto. Dublikātu forma netiek atvērta automātiski, lai izvairītos no datu ievades pārtraukšanas.

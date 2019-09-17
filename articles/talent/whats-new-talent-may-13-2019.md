---
title: Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 13. maijs)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
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
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: ffeeb3e2f5279a84c4c060b04fe46836b778f6c5
ms.sourcegitcommit: 1bf6a8b2f872394a4f242f9ff13c67e8e1ae8f65
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/03/2019
ms.locfileid: "1856452"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-13-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 13. maijs)

[!include [banner](includes/banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 for Talent.

## <a name="coming-soon-in-attract"></a>Drīzumā risinājumā Attract

### <a name="job-approvals-on-home-page"></a>Darba apstiprinājumi sākumlapā

Apstiprinājumi tiek rādīti informācijas paneļa sadaļā **Apstiprinājumi**. Apstiprinātāji var pārskatīt savus apstiprinājumus sadaļā **Piešķirts jums**, kurā norādīts darba ID, amats, citi apstiprinātāji un piešķirtais datums. Lietotāji, kuri iesniedz darbu apstiprināšanai, var pārskatīt savus darbus sadaļā **Jūsu pieprasījumi**, kurā norādīti apstiprinātāji, kuriem joprojām jāapstiprina iesniegtais darbs.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli programmas Dynamics 365 Talent: Onboard kļūdu labojumi.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2297. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).

### <a name="indicate-instance-type-when-provisioning-talent"></a>Instances tipa norādīšana, veicot nodrošināšanu programmā Talent

Nodrošinot programmā Talent jaunu instanci, varat norādīt, vai instances tips ir **Ražošana** vai **Smilškaste**, kas ļauj veikt jaunu līdzekļu agrīnu testēšanu. Visas esošās programmas Talent instances tiks atjauninātas uz instances tipu **Ražošana**. Ja vēlaties, lai kāda no jūsu esošajām instancēm tiktu atjaunināta uz instances tipu **Smilškaste**, lūdzu, sazinieties ar [atbalsta dienestu](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support), lai sāktu izmaiņu pieprasījumu.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service elementu atbalsts pielāgotajiem laukiem

Šīs nedēļas laidienā tālāk minētie Common Data Service elementi tagad atbalsta pielāgojamus laukus: Nodarbinātība, Atvieglojumu aprēķina biežums, Atvieglojumu aprēķina likme, Darba kalendāra brīvdienas un Identifikācijas tips.

### <a name="common-data-service-integration-page"></a>Common Data Service integrācijas lapa

Šajā laidienā ir paredzēta jauna opcija sadaļā **Sistēmas administrēšana > Saites > Integrācijas > Common Data Service konfigurācija**. Opcija **Common Data Service konfigurācija** sniedz administratoram vai datu pārvaldības administratoram zināmu elastību un ieskatus attiecībā uz Common Data Service. Izmantojot šo opciju, varat iespējot vai atspējot Common Data Service integrāciju ar Talent instanci un skatīt informāciju par sinhronizāciju starp Talent instanci un Common Data Service.

### <a name="import-performance-data-with-final-employee-rating-316710"></a>Importēt veiktspējas datus ar darbinieku galīgo novērtējumu (316710)

Šajā laidienā varat importēt vēsturiskos darbinieku novērtējuma datus. Laukam **FinalEmployeeRatingId** tagad ir rakstīšanas atļauja.

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a>Nevar izveidot nodarbinātā adresi pakalpojumā Common Data Service un sinhronizēt to ar programmu Talent (317555)

Šīs izmaiņas ļauj sinhronizēt ar programmu Talent tādus adreses datus, kas izveidoti Common Data Service.

## <a name="in-preview"></a>Priekšskatījumā

### <a name="new-page-to-validate-position-hierarchy-data"></a>Jauna lapa amatu hierarhijas datu pārbaudei

Personāla vadības speciālisti (HR) un administratori var pārbaudīt visu to ciklisko atsauču pārvaldības hierarhiju, kas varētu būt netīši importētas. Šai jaunajai lapai var piekļūt sadaļā **Organizācijas administrēšana > Saites > Amati > Amatu hierarhijas pārbaude**.

### <a name="specify-reason-codes-on-leave-types"></a>Atvaļinājumu tipu iemeslu kodu norādīšana

Organizācijām, iespējams, ir nepieciešama papildinformācija par brīvā laika pieprasījumiem. Tagad atvaļinājumu tipiem varat norādīt iemeslu kodus un ļaut darbiniekiem savos brīvā laika pieprasījumos atlasīt iemesla kodu.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Iemeslu kodu pieprasīšana noteiktiem atvaļinājumu tipiem brīvā laika pieprasījumos

Organizācijām var būt nepieciešami iemeslu kodi noteiktiem atvaļinājumu tipiem, kad darbinieki iesniedz brīvā laika pieprasījumu. Šī prasība var pastāvēt uzņēmuma politikas vai reglamentējošo prasību dēļ. Varat norādīt, kuriem atvaļinājumu tipiem ir nepieciešams iemesla kods, un varat pieprasīt, lai darbinieki savos brīvā laika pieprasījumos atvaļinājuma tipam norādītu iemesla kodu.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Atvaļinājumu un kavējumu transakciju sarakstu nodrošināšana personāla vadībai

Iespēja izsekot darbinieku brīvajam laikam un saprast, kā tiek aprēķināts brīvais laiks, ne tikai palīdz personāla vadībai (Human Resources — HR) atbildēt uz darbinieku jautājumiem, bet arī palīdz nodrošināt darbiniekiem precīzas brīvā laika piemaksas. Personāla vadībai tagad ir jauns skats uz transakcijām (dotācijām, uzkrājumiem, korekcijām un pieprasījumiem), lai personāla vadības darbinieki redzētu brīvā laika bilanču aprēķinu ietekmējošos faktorus.

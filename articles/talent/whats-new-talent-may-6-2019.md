---
title: Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 6. maijs)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 4830c5d626e5e10972c81c3445eb54e4b6b00e6c
ms.sourcegitcommit: 0400bfd66e98af50e64444a1c102575099a9312f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/09/2019
ms.locfileid: "1539409"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-6-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 6. maijs)

[!include [banner](includes/banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

### <a name="select-optional-documents-upon-offer-creation"></a>Izvēles dokumentu atlasīšana piedāvājuma izveides laikā

Kad atlasāt piedāvājuma pakotnes veidni, programma Attract tagad parāda uzvedni, lai jūs atlasītu piemērojamos izvēles dokumentus no šīs pakotnes veidnes. Varat pievienot citus neobligātus dokumentus, gatavojot piedāvājumu.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli programmas Dynamics 365 Talent: Onboard kļūdu labojumi.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2282. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-26"></a>Platformas update 26

Papildinformāciju par atjauninājumu Platform update 26 skatiet rakstā [Priekšskatījuma līdzekļi versijā Dynamics 365 for Finance and Operations Platform update 26 (2019. gada maijs)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26). 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service elementu atbalsts pielāgotajiem laukiem

Šīs nedēļas laidienā tālāk minētie elementi tagad atbalsta pielāgojamus laukus: Atvieglojumu aprēķina biežums, Atvieglojumu aprēķina likme, Atvieglojumu tips, Darba kalendārs, Darba kalendāra brīvdienas, Apmaksas cikls un Nodarbināta identifikācijas tipi.

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a>Atvaļinājuma masveida reģistrācijā mainot pakāpes bāzi uz “Darba stāža datums”, netiek atsvaidzināts sākotnējā uzkrājumu likme (318526)

Kad masveidā reģistrējat darbiniekus un maināt pakāpes bāzi, sākotnējais uzkrājums tagad ataino atlasīto pakāpes bāzi.

### <a name="workflow-showing-duplicate-place-holders-313636"></a>Darbplūsmā tiek rādīti vietturu dublikāti (313636)

Šajā laidienā veiktās izmaiņas novērš vietturu dublikātu veidošanos, kad tiek sūtīti darbplūsmas paziņojumi.

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a>Dimensiju lauki netiek atjaunināti, lietojot opciju "Atvērt programmā Excel" (176261)

Līdz ar šo laidienu varat atjaunināt finanšu dimensiju, izmantojot opciju **Atvērt programmā Excel** no lapas **Nodarbinātais**. 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a>Pakalpojumā Common Data Service izveidotā nodarbināta adrese nav sinhronizēta ar programmu Talent (317555)

Līdz ar šīm izmaiņām pakalpojumā Common Data Service izveidotās adreses tiek atjauninātas programmā Talent Core HR.


## <a name="in-preview"></a>Priekšskatījumā

### <a name="new-page-to-validate-position-hierarchy-data"></a>Jauna lapa amatu hierarhijas datu pārbaudei

Personāla vadības speciālisti (HR) un administratori tagad var pārbaudīt visu to ciklisko atsauču pārvaldības hierarhiju, kas varētu būt netīši importētas. Šai jaunajai lapai var piekļūt sadaļā **Organizācijas administrēšana > Saites > Amati > Amatu hierarhijas pārbaude**.

### <a name="specify-reason-codes-on-leave-types"></a>Atvaļinājumu tipu iemeslu kodu norādīšana

Organizācijām, iespējams, ir nepieciešama papildinformācija par brīvā laika pieprasījumiem. Tagad atvaļinājumu tipiem varat norādīt iemeslu kodus un ļaut darbiniekiem savos brīvā laika pieprasījumos atlasīt iemesla kodu.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Iemeslu kodu pieprasīšana noteiktiem atvaļinājumu tipiem brīvā laika pieprasījumos

Organizācijām var būt nepieciešami iemeslu kodi noteiktiem atvaļinājumu tipiem, kad darbinieki iesniedz brīvā laika pieprasījumu. Šī prasība var pastāvēt uzņēmuma politikas vai reglamentējošo prasību dēļ. Tagad varat norādīt, kuriem atvaļinājumu tipiem ir nepieciešams iemesla kods, un varat pieprasīt, lai darbinieki savos brīvā laika pieprasījumos atvaļinājuma tipam norādītu iemesla kodu.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Atvaļinājumu un kavējumu transakciju sarakstu nodrošināšana personāla vadībai

Iespēja izsekot darbinieku brīvajam laikam un saprast, kā tiek aprēķināts brīvais laiks, ne tikai palīdz personāla vadībai (Human Resources — HR) atbildēt uz darbinieku jautājumiem, bet arī palīdz nodrošināt darbiniekiem precīzas brīvā laika piemaksas. Personāla vadībai tagad ir jauns skats uz transakcijām (dotācijām, uzkrājumiem, korekcijām un pieprasījumiem), lai personāla vadības darbinieki redzētu bilanču aprēķinu ietekmējošos faktorus.

## <a name="coming-soon"></a>Drīzumā

### <a name="indicate-instance-type-when-provisioning-talent"></a>Instances tipa norādīšana, veicot nodrošināšanu programmā Talent

Nodrošinot programmā Talent jaunu instanci, varēsit norādīt, vai instances tips ir **Ražošana** vai **Smilškaste**, kas ļauj veikt jaunu līdzekļu agrīnu testēšanu. Visas esošās programmas Talent instances tiks atjauninātas uz instances tipu Ražošana. Ja vēlaties, lai kāda no jūsu esošajām instancēm tiktu atjaunināta uz instances tipu Smilškaste, lūdzu, sazinieties ar atbalsta dienestu, lai sāktu izmaiņu pieprasījumu.

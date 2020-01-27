---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 28. maijs)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2019
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
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1be555c35ef45029f2a26716e57a4e05c9be6112
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896846"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-28-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 28. maijs)

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract
Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Drīzumā risinājumā Attract

### <a name="job-approvals-on-home-page"></a>Darba apstiprinājumi sākumlapā

Apstiprinājumi tiek rādīti informācijas paneļa sadaļā **Apstiprinājumi**. Apstiprinātāji var pārskatīt savus apstiprinājumus sadaļā **Piešķirts jums**, kurā norādīts darba ID, amats, citi apstiprinātāji un piešķirtais datums. Lietotāji, kuri iesniedz darbu apstiprināšanai, var pārskatīt savus darbus sadaļā **Jūsu pieprasījumi**, kurā norādīti apstiprinātāji, kuriem joprojām jāapstiprina iesniegtais darbs.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard
Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR
Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2319.

### <a name="common-data-service-entity-support-for-custom-fields"></a>Common Data Service elementu atbalsts pielāgotajiem laukiem

Šajā laidienā tālāk minētie Common Data Service elementi tagad atbalsta pielāgojamus laukus: Atvieglojumu aprēķina likmes informācija, Darba kalendāra brīvdienu rinda un Nodarbinātība.

### <a name="copy-position-now-includes-payroll-details"></a>Vienums Kopēt amatu tagad ietver algas detalizēto informāciju
Izmantojot vienumu **Kopēt amatu** un atlasot visas opcijas, algas detalizētā informācija tagad ir ietverta kopijas informācijā. 

## <a name="in-preview-in-core-hr"></a>Priekšskatījumā programmā Core HR

### <a name="restrict-the-leave-types-in-time-off-requests"></a>Ierobežot atvaļinājumu tipus brīvā laika pieprasījumos

Organizācijas var piedāvāt darbiniekiem daudz dažādus atvaļinājumu tipus. Daži no šiem atvaļinājumu tipiem var nebūt piemēroti, lai darbinieki par tiem iesniegtu brīvā laika pieprasījumus, un tos pārvalda personāla vadības speciālisti (HR). Ar šo laidienu varat konfigurēt, kuriem atvaļinājumu tipiem darbinieki var iesniegt brīvā laika pieprasījumus. 

### <a name="new-page-to-validate-position-hierarchy-data"></a>Jauna lapa amatu hierarhijas datu pārbaudei

Personāla vadības speciālisti un administratori var pārbaudīt visu to ciklisko atsauču pārvaldības hierarhiju, kas varētu būt netīši importētas. Šai jaunajai lapai var piekļūt sadaļā **Organizācijas administrēšana > Saites > Amati > Amatu hierarhijas pārbaude**.

### <a name="specify-reason-codes-on-leave-types"></a>Atvaļinājumu tipu iemeslu kodu norādīšana

Organizācijām, iespējams, ir nepieciešama papildinformācija par brīvā laika pieprasījumiem. Tagad atvaļinājumu tipiem varat norādīt iemeslu kodus un ļaut darbiniekiem savos brīvā laika pieprasījumos atlasīt iemesla kodu.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Iemeslu kodu pieprasīšana noteiktiem atvaļinājumu tipiem brīvā laika pieprasījumos

Organizācijām var būt nepieciešami iemeslu kodi noteiktiem atvaļinājumu tipiem, kad darbinieki iesniedz brīvā laika pieprasījumu. Šī prasība var pastāvēt uzņēmuma politikas vai reglamentējošo prasību dēļ. Varat norādīt, kuriem atvaļinājumu tipiem ir nepieciešams iemesla kods, un varat pieprasīt, lai darbinieki savos brīvā laika pieprasījumos atvaļinājuma tipam norādītu iemesla kodu.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Atvaļinājumu un kavējumu transakciju sarakstu nodrošināšana personāla vadībai

Iespēja izsekot darbinieku brīvajam laikam un saprast, kā tiek aprēķināts brīvais laiks, ne tikai palīdz personāla vadībai (Human Resources — HR) atbildēt uz darbinieku jautājumiem, bet arī palīdz nodrošināt darbiniekiem precīzas brīvā laika piemaksas. Personāla vadībai tagad ir jauns skats uz transakcijām (dotācijām, uzkrājumiem, korekcijām un pieprasījumiem), lai personāla vadības darbinieki redzētu brīvā laika bilanču aprēķinu ietekmējošos faktorus.

---
title: Jaunumi vai izmaiņas risinājumā Dynamics 365 Talent (2019. gada 16. aprīlis)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/16/2019
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
ms.search.validFrom: 2019-04-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a37436eb15ee4c561d5d0c15c90e37815cb80860
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897929"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-16-2019"></a>Jaunumi vai izmaiņas risinājumā Dynamics 365 Talent (2019. gada 16. aprīlis)

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

### <a name="process-auditing"></a>Procesa audits

Tagad varat izsekot izmaiņām, kas veiktas attiecībā uz kandidātiem, vakancēm un darba pieteikumiem. Papildinformāciju skatiet sadaļā [Personāla atlases datu izmaiņu izsekošana](process-auditing.md).

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2239. Numuri iekavās attiecas uz atbalsta numuriem portālā Lifecycle Services (LCS).

### <a name="compensation-region-compensation-level-benefit-option-and-skill-type-entities-in-common-data-service-updated-to-include-customer-field-support"></a>Elementi Atlīdzības reģions, Atlīdzības līmenis, Atvieglojumu opcijas un Prasmju tips pakalpojumā Common Data Service ir atjaunināti, lai iekļautu debitoru lauku atbalstu.

Šajā laidienā šie pakalpojuma Common Data Service elementi ir atjaunināti, lai iekļautu iespēju iekļaut pielāgotu lauku, kas pievienots, izmantojot pakalpojumu Talent: Core HR.

### <a name="new-common-data-service-entity-support-for-compensation-vesting-rules-compensation-variable-plan-variable-compensation"></a>Jauns pakalpojuma Common Data Service elementu atbalsts šādiem elementiem: Atlīdzības izmaksas noteikumi, Mainīgās atlīdzības plāns, Mainīgā atlīdzība

Ar šo laidienu pakalpojumam Common Data Service ir pievienoti elementi Atlīdzības izmaksas noteikumi, Mainīgās atlīdzības plāns un Mainīgā atlīdzība. Šie elementi atbalsta arī pielāgotus laukus, kas pievienoti, izmantojot pakalpojumu Talent: Core HR.

### <a name="powerbi-refresh-issues-314342"></a>PowerBI atsvaidzināšanas problēmas (314342)

Šīs izmaiņas labo problēmu, kas saistīta ar PowerBI pārskatu pareizu atsvaidzināšanu.

### <a name="unable-to-click-directly-through-on-transition-tasks-in-employee-self-service-303309"></a>Nevar tieši noklikšķināt uz pārejas uzdevumiem darbinieku pašapkalpošanās sadaļā (303309)

Šīs izmaiņas nodrošina lietotājiem ar darbinieka lomu iespēju atlasīt un atjaunināt pārejas uzdevumus pakalpojuma Talent uzdevumu sarakstā.

### <a name="performance-feedback-email-message-updated-309615"></a>Atjaunināts veiktspējas atsauksmes e-pasta ziņojums (309615)

Līdz ar šīm izmaiņām tiek parādīts apstiprinājuma ziņojums, kad atsauksmes ir veiksmīgi iesniegtas.

### <a name="missing-tables-in-word-template-308048"></a>Iztrūkstošas tabulas Word veidnē (308048)

Līdz ar šīm izmaiņām, izveidojot Word veidni ar darbinieku un prasmju informāciju, Word dokumentā tiek parādītas tikai atlasītā darbinieka prasmes.

### <a name="when-applying-an-offboarding-checklist-an-error-is-displayed-299877"></a>Lietojot darba beigšanas kontrolsarakstu, tiek parādīta kļūda. (299877)

Līdz ar šīm izmaiņām tiek labota problēma, kas rodas, lietojot darba beigšanas kontrolsarakstu tieši no nodarbinātā veidlapas.

## <a name="in-preview"></a>Priekšskatījumā

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Atļaušana norādīt iemeslu kodus atvaļinājumu tipiem

Organizācijām, iespējams, ir nepieciešama papildinformācija par brīvā laika pieprasījumiem. Tagad atvaļinājumu tipiem varat norādīt iemeslu kodus un ļaut darbiniekiem savos brīvā laika pieprasījumos atlasīt iemesla kodu.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Iemeslu kodu pieprasīšana noteiktiem atvaļinājumu tipiem brīvā laika pieprasījumos

Organizācijām var būt nepieciešami iemeslu kodi noteiktiem atvaļinājumu tipiem, kad darbinieki iesniedz brīvā laika pieprasījumu. Tas varētu būt saistīts ar uzņēmuma politiku vai normatīvajām prasībām. Tagad varat norādīt, kuriem atvaļinājumu tipiem ir nepieciešams iemesla kods, un varat pieprasīt, lai darbinieki savos brīvā laika pieprasījumos atvaļinājuma tipam norādītu iemesla kodu.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Atvaļinājumu un kavējumu transakciju sarakstu nodrošināšana personāla vadībai

Darbinieku brīvā laika izsekošana un saprašana, kā tiek aprēķināts brīvais laiks, ne tikai palīdz personāla vadībai atbildēt uz darbinieku jautājumiem, bet arī nodrošina darbiniekiem precīzas brīvā laika piemaksas. Personāla vadībai tagad ir jauns skats uz transakcijām (dotācijām, uzkrājumiem, korekcijām un pieprasījumiem), lai redzētu bilanču aprēķinu ietekmējošos faktorus.

## <a name="coming-soon"></a>Drīzumā

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Lietotāja interfeisa uzlabojumi dublētu darbinieku pārbaudei

Līdz ar šīs izmaiņas ieviešanu dublikāti tiek noteikti, kad aizpildāt vārda/uzvārda/nosaukuma laukus, un statuss parāda atrasto dublikātu skaitu. Varat atlasīt norādīto saiti, lai atvērtu jaunu lapu, kur novērtēt, vai atrastā atbilstība ir jāizmanto. Lai izvairītos no datu ievades pārtraukšanas, dublikātu forma netiek atvērta automātiski.

### <a name="email-support-for-alerts"></a>E-pasta atbalsts brīdinājumiem

Līdz ar Finance and Operations atjauninājuma Platform update 25 ieviešanu lietotāji var izveidot brīdinājumu kārtulas, kas automātiski sūta e-pasta paziņojumus kontaktpersonām, ja kāds notikums tās aktivizē.



---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 3. decembris)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
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
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: bf1ad4ca2e0ab18aaa35a7410d80a54e7a2160ce
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528697"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 Talent (2019. gada 3. decembris)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Izmaiņas programmā Attract

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Izmaiņas programmā Onboard

Šajā laidienā ir ietverti nelieli kļūdu labojumi programmā Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Izmaiņas programmā Core HR

Šajā sadaļā aprakstītās izmaiņas attiecas uz būvējumu Nr. 8.1.2646. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta numuriem portālā Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Līdzekļu pārvaldības darbvieta

**Funkciju pārvaldības** darbvieta sniedz katrā laidienā piegādāto līdzekļu sarakstu. Pēc noklusējuma jaunie līdzekļi ir izslēgti. Varat izmantot darbvietu, lai tos ieslēgtu un skatītu ar tiem saistīto dokumentāciju. Papildinformāciju par Līdzekļu pārvaldību skatiet [Pārskats par līdzekļu pārvaldību](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Visi jaunie līdzekļi paliek priekšskatījumā vismaz 30 dienas, un parasti 30-60 dienas. Galvenās funkcijas parasti ir pieejamas katra gada oktobrī un aprīlī pēc priekšskatījuma perioda. Tiklīdz jūs redzat jaunas iespējas **Līdzekļu pārvaldības** darbvietā, varat tās ieslēgt. Daži līdzekļi var būt ieslēgti pēc noklusējuma.
 
Reizēm šis līdzeklis būs ieslēgts pēc noklusējuma, un to nevar izslēgt (piemēram, **Līdzekļu pārvaldības** darbvieta).
 
Kolīdz līdzeklis ir vispārīgi pieejams, to var ieslēgt vai izslēgt ražošanas vidēs. **Līdzekļu pārvaldības** darbvieta norāda, kad priekšskatījuma līdzeklis kļūs obligāts. Šis datums parasti ir 1. oktobris vai 1. aprīlis, lai to saskaņotu ar pusgada laidiena plāniem. Jūs nevarat izslēgt obligātos līdzekļus. Kamēr tas kļūst obligāts, varat ieslēgt vai izslēgt līdzekli visās vidēs.

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>Pievienota pakešuzdevumu vēstures tīrīšanas automātiska plānošana (332528)

Ar šīm izmaiņām **Pakešuzdevuma vēsture** tiek palaista katru vakaru, un tā noņem pakešuzdevuma vēstures vienumus, kas ir vecāki par 30 dienām.

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>Talants nereaģē uz nodarbinātā darbībām, ja identifikācijas numura garums neatbilst identifikācijas veidam (390971)

Šis laidiens novērš problēmu, kas atklājas, kad identifikācijas numura garums neatbilst identifikācijas veida definīcijai. 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>Fiksēta atlīdzība neatjaunina līmeni ar izmaiņām pozīciju detalizētā informācijā (348085)

Šīs nedēļas laidienā **Atlīdzības sākuma datums** nosaka darbu, kas saistīts ar amatu tajā brīdī, kad darbiniekam izveidots jauns fiksētās atlīdzības ieraksts.

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>Nodarbināto, darbinieku un līgumdarbinieku saraksts parāda nodarbinātā veidu kā "Abi", lai gan tam jābūt tikai "Nodarbinātais" vai "Līgumdarbinieks" (384473)

Šīs izmaiņas precīzi atspoguļo ievadīto nodarbinātā veidu (līgumdarbinieks vai darbinieka).

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>E-pasta paziņojumus par jaunu darbā pieņemšanas darbību drošības politikas dēļ nesatur informāciju par vārdu (383402)

Šīs izmaiņas izlabo informāciju, kas darbplūsmas vietturu ietvaros tiek rādīta vārda vai uzvārda laukos, kad ir iespējota papildu drošība.

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>Sistēma atļauj divus pilnas dienas atvaļinājuma pieprasījumus vienā un tajā pašā dienā (379284)

Ar šīm izmaiņām nevar izdot divus atvaļinājuma pieprasījumus vienai un tai pašai dienai. 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>Adrešu izmaiņu sarakstu vajadzētu kārtot pēc spēkā stāšanās datuma (352798)

Ar šīm izmaiņām adrešu izmaiņu saraksts tiek kārtots pēc **Spēkā stāšanās datums**.

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>Atvaļinājumu pieprasījumiem jāatļauj dzēšana no Common Data Service uz Talent (376999)

Ar šīm izmaiņām atvaļinājumu projektus un atceltus atvaļinājumu pieprasījumus var dzēst no Common Data Service un pēc tam noņem no Talent.

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>Tiek atļauta ienākumu veida koda dzēšana, ja tas pats ienākumu veida kods ir piešķirts darbiniekam (371792)

Šajā laidienā vispirms darbiniekam jānoņem ienākumu veida kods un tikai tad ienākumu veida kodu var dzēst no sistēmas.

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>Nevar pabeigt atvaļinājumu un kavējumu darbplūsmu ar diviem apstiprināšanas posmiem (391116)

Ar šīm izmaiņām atvaļinājumu un kavējumu darbplūsma turpinās visos posmos, ja pieprasījumam ir konfigurēts vairāk nekā viens apstiprināšanas posms.

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>Izdošanas datums nesinhronizējas ar Common Data Service, ja tas tiek atjaunināts vai ievadīts no Talent (397361)

Šīs izmaiņas novērš problēmu, kad ieraksta **Personas identifikācija** izdošanas datums no Talent nesinhronizējās ar Common Data Service.

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>Piešķirot vadītāju amatam, tiek parādīta hierarhijas riņķveida atsauces kļūda (386659)

Šīs izmaiņas labo unikālo scenāriju, kur riņķveida atsauces kļūda tiek parādīta, amatam piešķirot jaunu vadītāju.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Common Data Service entītijas, kas atbalsta pielāgotos laukus

Tālāk minētās Common Data Service entītijas tagad atbalsta pielāgotus laukus.

| Vārds/nosaukums | Elements |
| --- | --- |
| Bankas konta izdevumi | cdm_bankaccountdisbursement |
| Atvieglojumu aprēķina biežums | cdm_benefitcalculationfrequency |
| Atvieglojumu aprēķina biežuma izmaksas periods | cdm_benefitcalculationfrequencypayperiod |
| Atvieglojumu aprēķina likme | cdm_benefitcalculationrate |
| Atvieglojumu aprēķina likmes detalizēta informācija | cdm_benefitcalculationratedetail |
| Atvieglojumu opcija | cdm_benefitoption |
| Atvieglojumu plāns | cdm_benefitplan (nav iespējots pielāgoto lauku atbalsts) |
| Atvieglojumu veids | cdm_benefittype |
| Biznesa procesu kalendārs | cdm_businessprocesscalendar |
| Biznesa procesu grupu piešķire | cdm_businessprocessgroupassignment |
| Biznesa procesu bibliotēkas uzdevumu grupa | cdm_businessprocesslibrarytaskgroup |
| Biznesa procesu stadija | cdm_businessprocessstage |
| Kontrolsaraksta veidnes galvene | cdm_businessprocesstemplateheader |
| Kontrolsaraksta veidnes uzdevums | cdm_businessprocesstemplatetask |
| Uzņēmums | cdm_company |
| Atlīdzības fiksētais plāns | cdm_compensationfixedplan |
| Atlīdzības režģis | cdm_compensationgrid |
| Atlīdzības līmenis | cdm_compensationlevel |
| Atlīdzības izmaksas biežums | cdm_compensationpayfrequency |
| Atlīdzības raksturojuma punktu iestatīšana | cdm_compensationreferencepointsetup |
| Atlīdzības raksturojuma punktu iestatīšanas līnija | cdm_compensationreferencepointsetupline |
| Atlīdzības reģions | cdm_compensationregion |
| Atlīdzības struktūra | cdm_compensationstructure |
| Atlīdzības mainīgais plāns | cdm_compensationvariableplan |
| Atlīdzības mainīgā plāna līmenis | cdm_compensationvariableplantype |
| Atlīdzības mainīgā plāna tips | cdm_compensationvariableplantype |
| Nodaļa | cdm_department |
| Nodarbinātība | cdm_employment |
| Etniskā izcelsme | cdm_ethnicorigin |
| Fiksētas atlīdzības notikums | cdm_fixedcompensationevent |
| Darbs | cdm_job |
| Darba funkcija | cdm_jobfunction |
| Amats | cdm_jobposition |
| Darba tips | cdm_jobtype |
| Valoda | cdm_language |
| Transakcija Atstāt tukšu | cdm_leavebanktransaction |
| Atvaļinājuma reģistrācija | cdm_leaveenrollment |
| Atvaļinājumu plāns | cdm_leaveplan |
| Atvaļinājuma pieprasījums | cdm_leaverequest |
| Atvaļinājuma pieprasījuma informācija | cdm_leaverequestdetail |
| Atvaļinājuma tips | cdm_leavetype |
| Atvaļinājuma veida iemesla kods | cdm_leavetypereasoncode |
| Izmaksu cikls | cdm_paycycle |
| Apmaksas periods | cdm_payperiod |
| Algas nopelnīšanas kods | cdm_payrollearningcode |
| Personas identifikācijas dokumenta izdevējiestāde | cdm_personidentificationissuingagency |
| Amata veids | cdm_positiontype |
| Amatā nodarbinātā piešķire | cdm_positionworkerassignmentmap |
| Iemesla kods | cdm_reasoncode |
| Prasmju veids | cdm_skilltype |
| Nodokļu reģions | cdm_taxregion |
| Izmaksu noteikums | cdm_vestingrule |
| Veterāna statuss | cdm_veteranstatus |
| Darba kalendārs | cdm_workcalendar |
| Darba kalendāra diena | cdm_workcalendarday |
| Brīvdienas darba kalendārā |cdm_workcalendarholiday |
| Brīvdienu rinda darba kalendārā | cdm_workcalendarholidayline |
| Darba kalendāra laika intervāls | cdm_workcalendartimeinterval (nav iespējots pielāgoto lauku atbalsts) |
| Nodarbinātais | cdm_worker |
| Nodarbinātā adrese | cdm_workeraddress |
| Nodarbinātā bankas konts | cdm_workerbankaccount |
| Nodarbinātā fiksētā atlīdzība | cdm_workerfixedcompensation |
| Nodarbinātā personas dati | cdm_workerpersonaldetail |
| Nodarbinātās personas identifikācijas numurs | cdm_workerpersonidentificationnumber |
| Nodarbinātās personas identifikācijas veids | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>Priekšskatījumā

Priekšskatījuma līdzekļi ir pieejami tikai **Smilškastes** vidēs.

### <a name="print-performance-reviews"></a>Veiktspējas pārskatu drukāšana

Aplūkojiet [Drukāšanas veiktspējas pārskati](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) Dynamics 365: 2019. gada izlaiduma 2. laidiena plāns.

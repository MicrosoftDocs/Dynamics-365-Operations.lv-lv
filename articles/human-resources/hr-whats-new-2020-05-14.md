---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 14. maijs)
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 14. maiju.
author: andreabichsel
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f1ef15bec1d2eb7b7aaca3a413e13089b36315fd
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465298"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 14. maijs)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.3244. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta atsauces numuriem portālā Lifecycle Services (LCS).

## <a name="platform-changes"></a>Platformas izmaiņas

Platformas izmaiņas iekļautas šīs nedēļas laidienā. Papildinformāciju skatiet [Platformas atjauninājumi Finance and Operations programmu versijai 10.0.10 (2020. gada maijs)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34). Šajā laidienā ir ietverti kļūdu labojumi un izmaiņas saglabātajos skatos.
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a>Nodrošināts, lai Dataverse salasīšanas saraksti atbilst Atvaļinājumu uzskaitījumiem (436343)

Dataverse salasīšanas saraksti tagad atbilst Atvaļinājumu uzskaitījumiem.

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a>Lietotājiem atļauts konfigurēt atvaļinājuma pieprasījuma darbplūsmu, pamatojoties uz pieprasījuma daudzumu (300044)

Lietotāji var konfigurēt atvaļinājuma pieprasījumu darbplūsmas, pamatojoties uz pieprasījumu daudzumu.
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a>Jauna nodarbinātā veidlapa atklāj datus, izmantojot izvēlni Skats, kad ir iespējota papildu drošība (403185)

Šis laidiens labo kā tiek skatīti juridisko personu nodarbinātie, kad ir iespējota papildu piekļuve un ir pieejami citu uzņēmumu nodarbinātie.

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a>Ļauts izpildīt atvaļinājuma uzkrājumus vienam plānam vai vienam uzņēmumam (318844)

Ar šīm izmaiņām varat izpildīt uzņēmuma vai plāna uzkrājumus.
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a>Amata pilnas slodzes ekvivalenta (FTE) rādīšana veidlapā Reģistrētie nodarbinātie (414658)

Nodarbinātā amata FTE vērtība nosaka nodarbinātā uzkrājuma likmi, ja atvaļinājuma veidā ir iespējota opcija FTE. Šis lauks tagad ir iekļauts veidlapā **Reģistrētie nodarbinātie** un dialogā **Masveida reģistrācija**.

## <a name="add-leave-balance-expiration-batch-job-431266"></a>Atvaļinājuma bilances pakešuzdevuma beigu datuma pievienošana (431266)

Tagad ir pieejams jauns pakešuzdevums, kas darbojas katru dienu. Tas samazina atlikušo atvaļinājuma bilanci, kad beigu datumi kļūst aktuāli.

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a>Eksportējot personiskās kontaktpersonas nodarbinātajam, izmantojot Nodarbinātā personiskās kontaktpersonas personu, netiek eksportētas personiskās kontaktpersonas ar attiecību veidu Vecāks (345893)

**Nodarbinātā personiskās kontaktpersonas personas** datu elements (**HcmPersonalContactPersonEntity** elementā DMF un **PersonalContactPerson** elementā OData) nevarēja eksportēt personiskās kontaktpersonas ar attiecību veidu **Vecāks**. Šī problēma ir novērsta personiskajām kontaktpersonām, kas izveidotas pēc šīm izmaiņām. Esošās personiskās kontaktpersonas ar veidu **Vecāks** tiks labotas turpmākajos laidienos.

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a>Pamatojuma kodi tiek rādīti dažādos scenārijos, kad tie tiek atzīmēti kā Atvaļinājums un kavējums un ir iespējota racionalizēta darbinieka veidlapa (434163)

Šīs izmaiņas ierobežo pamatojuma kodus tikai Atvaļinājumu un kavējumu kodiem, kad iespējojat racionalizētu darbinieka ierakstu.

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a>Priekšskatījuma funkcija Piešķirt atvaļinājuma plānu darbiniekiem nākotnē rāda kļūdas ziņojumu (433555)

Šīs izmaiņas labo kļūdas ziņojumu, kad atvaļinājuma plānam ir piešķirti divi atvaļinājumu veidi, un jūs mēģināt piešķirt darbinieku.

## <a name="getting-started-banner-appears-for-all-users-441731"></a>Darba sākšanas reklāmkarogs tiek rādīts visiem lietotājiem (441731)

Ar šīm izmaiņām Darba sākšanas reklāmkarogs ir slēpts lietotājiem, kas nav Sistēmas administratori vai Datu pārvaldības administratori. 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a>Dataverse Darbinieka adreses elements darbojas atšķirīgi, attiecībā uz datuma laika spēkā stāšanās datumiem Personāla vadības programmā (425071)

Šīs izmaiņas nodrošina adreses informācijas saskaņošanu noteiktos scenārijos, pamatojoties uz adreses datumiem.

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a>Nav iespējams pievienot pielikumu apstiprinātam atvaļinājuma pieprasījumam (425407)

Ar šīs nedēļas laidienu varat pievienot pielikumus apstiprinātajiem atvaļinājuma pieprasījumiem, nemainot atvaļinājuma pieprasījumu.

## <a name="in-preview"></a>Priekšskatījumā

## <a name="leave-suspension"></a>Atvaļinājuma atlikšana

Jūs varat atlikt atvaļinājumu un prombūtni darbiniekam Personāla vadības programmā. Aizturot atvaļinājumu, tiek apturēti atvaļinājumu uzkrājumi atsevišķiem atvaļinājumu veidiem. Ja atlikšana notiek pēc uzkrājumu procesa, aizturētā atvaļinājuma rezultātā izveido proporcionālu pārrēķinu darbinieka atvaļinājuma bilancei. Papildinformāciju skatiet [Aizturēt atvaļinājumu](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Atjaunināt lietotāja pieredzi, lai norādītu, ka uzkrāšana ir apturēta (429550)

Lietotāja pieredze tagad norāda, ka uzkrājums ir atlikts plānam.

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a>Aizturēt atvaļinājumu uzkrājumu norādīto atvaļinājumu veidiem (272447)

Šajā laidienā PV var izveidot kārtulu, kas aptur atvaļinājumu uzkrājumus darbiniekiem ar atvaļinājumu pieprasījumiem, kas ievadīti neapmaksātam atvaļinājumam. Neapmaksāts atvaļinājums var būt veids, bet tam nav obligāti jābūt. Jūs varat aizturēt jebkuru atvaļinājumu, pamatojoties uz citu atvaļinājumu veidu.

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a>DMF elements ir pieejams uzkrājumu atlikšanai (429549)

DMF elements tagad ir pieejams uzkrājumu atlikšanai.

## <a name="add-reason-code-to-accrual-suspensions-429547"></a>Pievienot uzkrājumu atlikšanas iemesla kodu (429547)

Pamatojuma kodi ir pievienoti uzkrāšanas apturēšanai.

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a>Sākt pāreju no Personāla vadības parametriem uz atvaļinājumu un kavējuma parametriem

Šis laidiens sāk apvienot Personāla vadības parametrus ar atvaļinājumu un kavējumu parametriem.

## <a name="carry-forward-rules"></a>Pārnešanas kārtulas

Jūs varat norādīt pārnešanas atvaļinājuma veidu pārnešanas bilancēm, ja pārnestās korekcijas tiek pārsūtītas. Piemēram, ja darbinieks pārnes 10 dienas, jūs varat izvēlēties citu atvaļinājuma veidu šīm 10 dienām. Papildinformāciju skatiet [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
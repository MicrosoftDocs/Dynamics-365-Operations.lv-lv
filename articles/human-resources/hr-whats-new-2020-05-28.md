---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 28. maijs)
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 28. maiju.
author: andreabichsel
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 624201841b512b01daf94d13e3d9fe7c381f5c11b328d57e22fbd73e1066bf88
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741385"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 28. maijs)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.3287. Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a>LeaveRequest elements nedarbojas, ja iespējojat vairākus veidus atvaļinājumu plānam (447498)

Ar šo izmaiņu **LeaveEnrollmentV2Entity** tagad ir pieejams, lai labotu kļūdu, kas rodas, iespējojot vairākus atvaļinājumu veidus.

## <a name="batch-contention-reduction-feature-preview-446619"></a>Partijas konfliktsituācijas samazināšanas līdzeklis (priekšskatījums) (446619)

Iespējojot šo līdzekli, var sagaidīt, ka, atlasot uzdevumus un apstrādājot darbus, pakešveida struktūras tabulu aizturēšana tiks samazināta.

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a>UpdateConflict, saglabājot darbinieku, neļauj rediģēt ierakstu programmā Personas (427915)

Šīs izmaiņas labo kļūdu, pievienojot jaunu darbinieku, atjauninot adreses informāciju un mainot valodas preferenci. Šajā unikālajā scenārijā tiek parādīta kļūda, kas norāda, ka ierakstu nevarēja atjaunināt. 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a>Nav iespējams pievienot pielikumu apstiprinātam atvaļinājuma pieprasījumam, lai to iesniegtu atkārtoti (425407)

Šī izmaiņa tagad ļauj pievienot pielikumus apstiprinātiem atvaļinājumu pieprasījumiem.

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a>Lietotājs var ievadīt kompensāciju darbiniekam citas juridiskās personas veidlapā (409529)

Šī izmaiņa atspējo kompensāciju opcijas, lai novērstu nejaušu kompensācijas ierakstu ievadīšanu nepareizai juridiskajai personai.

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a>Kļūda, pārsūtot darbinieku un darbinieka amata piešķires datumu, rodas pirms amata ilguma (429402)

Pārsūtot darbinieku šajā scenārijā, ir atjaunināti kļūdu ziņojumi, lai labāk aprakstītu problēmas novēršanai nepieciešamās izmaiņas.

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a>Pielikumu iespējas Darbinieku pašapkalpošanās atvieglojumu reģistrācijā
 
Tagad varat pievienot pielikumus atvieglojumu reģistrācijas procesa laikā katram plānam, kurā darbinieks ir reģistrējies. Pēc tam varat skatīt pielikumus veidlapā **Darbinieka reģistrētais atvieglojums**.

## <a name="in-preview"></a>Priekšskatījumā

## <a name="human-resources-application-in-teams"></a>Programma Human Resources programmā Teams

Darbinieki var skatīt un pieprasīt prombūtnes laiku sistēmā Microsoft Teams. Tās var mijiedarboties ar robotu, lai izveidotu atvaļinājumu pieprasījumus. Papildinformāciju skatiet sadaļā [Personāla vadība programms sistēmā Teams](./hr-admin-teams-leave-app.md). 

## <a name="leave-suspension"></a>Atvaļinājuma atlikšana

Jūs varat atlikt atvaļinājumu un prombūtni darbiniekam Personāla vadības programmā. Aizturot atvaļinājumu, tiek apturēti atvaļinājumu uzkrājumi atsevišķiem atvaļinājumu veidiem. Ja atlikšana notiek pēc uzkrājumu procesa, aizturētā atvaļinājuma rezultātā izveido proporcionālu pārrēķinu darbinieka atvaļinājuma bilancei. Papildinformāciju skatiet [Aizturēt atvaļinājumu](hr-leave-and-absence-suspend-leave.md).

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a>Atjaunināt lietotāja pieredzi, lai norādītu, ka uzkrāšana ir apturēta (429550)

Lietotāja pieredze tagad norāda, ka uzkrājums ir atlikts plānam.

## <a name="coming-soon"></a>Drīzumā

## <a name="database-logging-in-preview-in-june"></a>Datu bāzes reģistrēšana (priekšskatījumā jūnijā)

Datu bāzes reģistrācijas līdzeklis ļauj noteikt, kura tabula un lauki ir jāpārrauga. Tas arī ļauj noteikt notikumus, kam jāizraisa izmaiņu izsekošana. Ir pieejamas ieprasījuma iespējas, lai laika gaitā skatītu šīs izmaiņas.

## <a name="buy-and-sell-leave-in-preview-june-1"></a>Atvaļinājuma pirkšana un pārdošana (priekšskatījumā 1. jūnijā)

Dažas organizācijas sniedz atvieglojumus, kas ļauj darbiniekiem pirkt vai pārdot atvaļinājumu. Šo procesu bieži pārvalda manuāli. Šis līdzeklis nodrošina automatizētu veidu, kā pārvaldīt Cilvēkresursu departamenta politikas un pieprasījumus, un palīdz likvidēt kļūdas, racionalizējot atvaļinājumu pārvaldības procesu. Plašāku informāciju skatiet:

- [Atvaļinājuma iegādes un pārdošanas politiku pārvaldība](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Atvaļinājuma iegāde un pārdošana](hr-employee-self-service-buy-sell-leave.md)

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Datu pārvaldības struktūras (DMF) elementi atvieglojumu pārvaldībai
 
Tiek izlaisti atvieglojumu pārvaldības elementi. DMF elementi ļauj importēt un eksportēt datus, lai viegli konfigurētu atvieglojumu pārvaldību. Lai pārvietotu datus, būs pieejama arī atvieglojumu pārvaldības veidne. Veidne eksportē un importē datus secīgā veidā, lai ievērotu datu atkarības.

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a>Pievienot uzkrājumu atlikšanas iemesla kodu (1. jūnijs)

Pamatojuma kodi ir pievienoti uzkrāšanas apturēšanai.

## <a name="carry-forward-rules-june-1"></a>Pārnešanas kārtulas (1. jūnijs)

Jūs varat norādīt pārnešanas atvaļinājuma veidu pārnešanas bilancēm, ja pārnestās korekcijas tiek pārsūtītas. Piemēram, ja darbinieks pārnes 10 dienas, jūs varat izvēlēties citu atvaļinājuma veidu šīm 10 dienām. Papildinformāciju skatiet [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a>Aizturēt atvaļinājumu uzkrājumu norādīto atvaļinājumu veidiem (1. jūnijs)

Šajā laidienā PV var izveidot kārtulu, kas aptur atvaļinājumu uzkrājumus darbiniekiem ar atvaļinājumu pieprasījumiem, kas ievadīti neapmaksātam atvaļinājumam. Neapmaksāts atvaļinājums var būt veids, bet tam nav obligāti jābūt. Jūs varat aizturēt jebkuru atvaļinājumu, pamatojoties uz citu atvaļinājumu veidu.

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a>DMF elements ir pieejams uzkrājumu atlikšanai (1. jūnijs)

DMF elements tagad ir pieejams uzkrājumu atlikšanai.

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
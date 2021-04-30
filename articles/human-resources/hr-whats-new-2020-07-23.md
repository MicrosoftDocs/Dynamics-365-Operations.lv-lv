---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 23. jūlijs)
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 23. jūliju.
author: andreabichsel
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb4ef2bf335e19d0d890465c851c46f66ef8bd8e
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891869"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 23. jūlijs)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.3416. Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a>Finanšu dimensiju dzēšana Pozīcijā nedarbojas, kā paredzēts (445476)

Noņemot dimensijas no pozīcijas, tās pašas pozīcijas tiek noņemtas no Dataverse.

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a>Pozīcijas, kas nav hierarhijā, rāda neaktīvās pozīcijas (397257)

Pozīcijas, kas ir neaktīvas (ir beidzies derīguma termiņš), vairs netiek rādītas pozīciju hierarhijā kā **Pozīcijas, kas nav hierarhijā**. 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a>Pārbaude, kas rodas starp LeaveEnrollmentEntity un HcmWorkerEntity Datu pārvaldības struktūras (DMF) importēšanā, izraisa lēnu datu noslodzi (442324)

Šī izlaiduma izmaiņas palielina **LeaveEnrollmentEntity** veiktspēju.

## <a name="unable-to-personalize-in-organization-administration-447490"></a>Nevar personalizēt Organizācijas administrācijā (447490)

Ar šīm izmaiņām jūs varat personalizēt saites **Organizācijas administrācijā**.

## <a name="in-preview"></a>Priekšskatījumā

## <a name="mandatory-fields"></a>Obligātie lauki 

Tagad ir iespējams padarīt laukus obligātus, izmantojot Personāla vadības personalizēšanas iespējas. Šim līdzeklim nepieciešami **Saglabātie skati**.

## <a name="human-resources-application-in-teams"></a>Programma Human Resources programmā Teams

Darbinieki var skatīt un pieprasīt prombūtnes laiku sistēmā Microsoft Teams. Tās var mijiedarboties ar robotu, lai izveidotu atvaļinājumu pieprasījumus. Papildinformāciju skatiet sadaļā [Personāla vadība programms sistēmā Teams](./hr-admin-teams-leave-app.md). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Datu pārvaldības struktūras (DMF) elementi atvieglojumu pārvaldībai
 
Tiek izlaisti atvieglojumu pārvaldības elementi. DMF elementi ļauj jums importēt un eksportēt datus, lai viegli konfigurētu atvieglojumu pārvaldību. Lai pārvietotu datus, būs pieejama atvieglojumu pārvaldības veidne. Veidne eksportē un importē datus secīgi, lai ievērotu datu atkarības.

## <a name="buy-and-sell-leave"></a>Atvaļinājuma iegāde un pārdošana 

Dažas organizācijas sniedz atvieglojumus, kas ļauj darbiniekiem pirkt vai pārdot atvaļinājumu. Šo procesu bieži pārvalda manuāli. Šis līdzeklis automatizē personāla vadības departamenta politikas un pieprasījumu pārvaldību. Tas vienkāršo atvaļinājumu pārvaldības procesu un palīdz likvidēt kļūdas. Plašāku informāciju skatiet:

- [Atvaļinājuma iegādes un pārdošanas politiku pārvaldība](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Atvaļinājuma iegāde un pārdošana](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Atstāt uzkrājumu vienam uzņēmumam vai atsevišķam plānam

Debitori var apstrādāt uzkrājumus vienam uzņēmumam vai atsevišķam atvaļinājumu un prombūtnes plānam. Šī iespēja nodrošina skaidrību uzkrāšanas procesā debitoriem ar dažādiem atvaļinājumu gadiem vai atvaļinājumu uzkrāšanas politikām. Lai iegūtu papildu informāciju, skatiet [Uzkrāt atvaļinājumu pēc uzņēmuma vai atvaļinājuma plāna](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Pielikumu pievienošana brīvā laika pieprasījumiem

Iespēja pievienot pielikumus apstiprinātajiem atvaļinājumu pieprasījumiem ir kritiski nepieciešama pašreizējā COVID-19 vidē. Tagad darbinieki var pievienot šos pielikumus. Tām ir arī vairāk izpratnes par to, kā tiek atjaunināti atvaļinājumu pieprasījumi. Lai iegūtu papildu informāciju, skatiet [Pielikumu pievienošana esošam pieprasījumam](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Pievienot uzkrājumu atlikšanas iemesla kodu 

Pamatojuma kodi ir pievienoti uzkrāšanas apturēšanai.

## <a name="carry-forward-rules"></a>Pārnešanas kārtulas 

Jūs varat norādīt pārnešanas atvaļinājuma veidu pārnešanas bilancēm, ja pārnestās korekcijas tiek pārsūtītas. Piemēram, ja darbinieks pārnes 10 dienas, jūs varat izvēlēties citu atvaļinājuma veidu šīm 10 dienām. Papildinformāciju skatiet [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Aizturēt atvaļinājumu uzkrājumu norādīto atvaļinājumu veidiem

Jūs varat izveidot kārtulu, kas aptur atvaļinājumu uzkrājumus darbiniekiem ar atvaļinājumu pieprasījumiem, kas ievadīti neapmaksātam atvaļinājumam. Neapmaksāts atvaļinājums var būt veids, bet tam nav obligāti jābūt. Jūs varat aizturēt jebkuru atvaļinājumu, pamatojoties uz citu atvaļinājumu veidu.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF elements ir pieejams uzkrājumu atlikšanai 

DMF elements tagad ir pieejams uzkrājumu atlikšanai.

## <a name="coming-soon"></a>Drīzumā

## <a name="checklist-entities-included-in-dataverse"></a>Kontrolsaraksta entītijas iekļautas Dataverse

Kontrolsaraksta elementi Pievienošana, Noņemšana, Pārsūtīšana un Biznesa procesi drīz būs pieejami Dataverse.

## <a name="platform-changes"></a>Platformas izmaiņas

Platformas atjauninājums 10.0.12 (36)

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
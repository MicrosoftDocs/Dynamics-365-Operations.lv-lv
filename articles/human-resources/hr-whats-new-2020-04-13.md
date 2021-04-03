---
title: Jaunumi vai izmaiņas risinājumā Dynamics 365 Human Resources (2020. gada 13. aprīlis)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 13. aprīli.
author: andreabichsel
manager: tfehr
ms.date: 04/13/2020
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
ms.search.validFrom: 2020-04-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8fdf23b735700009c97c02c0b53b370773d0acce
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465346"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-13-2020"></a>Jaunumi vai izmaiņas risinājumā Dynamics 365 Human Resources (2020. gada 13. aprīlis)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.3136. Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.

## <a name="new-production-release-cadence"></a>Jauns ražošanas laidiena ritms

Ar šīs nedēļas laidienu Personāla vadības laidienu ritms mainās no iknedēļas atjauninājumiem uz atjauninājumiem reizi divās nedēļās. Lai nodrošinātu saskaņotību ar drošām izvietošanas praksēm, kā arī uzturētu augstus stabilitātes un uzticamības standartus pakalpojumā, pakalpojumu atjauninājumu izvietošanas process visiem reģioniem tagad ir divu nedēļu izvēršana. Ir paredzēta papildu pārbaudes un uzraudzība, lai nodrošinātu veiksmīgu izvietošanu katrā procesa posmā. Lai iegūtu papildu informāciju par laidiena ritmu skatiet rakstu [Atjaunināšanas process](hr-admin-setup-update-process.md).

## <a name="rounding-precision-field-isnt-editable-after-specifying-a-rounding-type-435616"></a>Noapaļošanas precizitātes lauks nav rediģējams pēc Noapaļošanas veida norādīšanas (435616)

Ar šī izmaiņām lauks **Noapaļošanas precizitāte** tagad ir pieejams pēc lauka **Noapaļošanas veids** atjaunināšanas.

## <a name="cant-edit-leave-enrollment-end-date-when-the-leave-plan-doesnt-have-accrual-periods-413628"></a>Nevar rediģēt atvaļinājuma reģistrācijas beigu datumu, kad atvaļinājumu plānam nav uzkrāšanas periodu (413628)

Tagad varat rediģēt reģistrācijas beigu datumu, neuzrādot kļūdu "Jānorāda lauka uzkrāšanas datums."

## <a name="employment-entity-doesnt-sync-to-dataverse-430834"></a>Nodarbinātības elements nav sinhronizēts ar Dataverse (430834)

Šīs izmaiņas labo problēmu, kad nodarbinātības dati netika sinhronizēti ar Dataverse pēc finanšu dimensiju pievienošanas. 

## <a name="remove-multi-parenting-for-work-calendar-time-interval-entity-431775"></a>Noņemt vairāku vecāku izmantošanu Darba kalendāra laika intervāla elementam (431775)

Šīs izmaiņas noņem vairāku vecāku izmantošanu **Darba kalendāra laika intervāla** elementam.

## <a name="filter-with-cast-function-doesnt-work-on-odata-call-position-worker-assignment-entity-431699"></a>Filtrs ar CAST funkciju nedarbojas uz OData zvana Pozīcijas darbinieka piešķires elementā (431699)

Šis atjauninājums ietver izmaiņas, lai atļautu filtru ar CAST funkciju, kas ir OData **Pozīcijas darbinieka piešķires** elementam.

## <a name="in-preview"></a>Priekšskatījumā

## <a name="leave-suspension"></a>Atvaļinājuma atlikšana

Jūs varat atlikt atvaļinājumu un prombūtni darbiniekam Personāla vadības programmā. Aizturot atvaļinājumu, tiek apturēti atvaļinājumu uzkrājumi atsevišķiem atvaļinājumu veidiem. Ja atlikšana notiek pēc uzkrājumu procesa, aizturētā atvaļinājuma rezultātā izveido proporcionālu pārrēķinu darbinieka atvaļinājuma bilancei. Papildinformāciju skatiet [Aizturēt atvaļinājumu](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Pārnešanas kārtulas

Jūs varat norādīt pārnešanas atvaļinājuma veidu pārnešanas bilancēm, ja pārnestās korekcijas tiek pārsūtītas. Piemēram, ja darbinieks pārnes 10 dienas, jūs varat izvēlēties citu atvaļinājuma veidu šīm 10 dienām. Papildinformāciju skatiet [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md).

## <a name="known-issues"></a>Zināmās problēmas

## <a name="employment-details-entity"></a>Nodarbinātības informācijas elements

**Nodarbinātības informācijas** elements ir atjaunināts ar šādiem laukiem:

- **PayFrequency**
- **Nodarbinātības kategorijas ID**
- **Nodarbinātības veids**
- **EmploymentType ID**
- **Pabalstu nodarbinātības statuss**

Šo lauku iestatīšanas dati paļaujas uz atvieglojumu pārvaldību, kas ir iespējota **Līdzekļu pārvaldības** darbvietā. Neaizpildiet vai neatjauniniet šos laukus **Nodarbinātības informācijas** elementā, jo importēšanas laikā radīsies kļūdas.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint priekšskatījums dažās vidēs nedarbojas

Ja dokumenta priekšskatījums dokumentiem, kas saglabāti SharePoint programmā, nedarbojas, veiciet šādas darbības:

1. Pārbaudiet, vai administratora lietotāja kontam ir e-pasts, kas saistīts ar lietotāja ierakstu. Šo informāciju varat aplūkot lapā **Lietotājs**. Ja e-pasta ziņojums nav iestatīts, e-pasta ziņojums un nodrošinātājs ir jāpievieno, izmantojot OData Excel pievienojumprogrammu. Pēc noklusējuma e-pasta adrese nav atrodama Excel noformējumā. Jums vajadzēs rediģēt Excel noformējumu, pievienot visus laukus, piemērot un atsvaidzināt. Kad šīs darbības ir izpildītas, varat atjaunināt administratora kontu.

2. Pēc tam, kad administratora kontam ir saistītais e-pasta konts, piesakieties pakalpojumā Human Resources ar administratora akreditācijas datiem.

3. Lai sāktu dokumenta priekšskatījumu, piekļūstiet SharePoint pielikumam.

4. Piesakieties ar citu lietotāja kontu, kam ir piekļuve pielikumiem, un apstipriniet, ka priekšskatījums darbojas kā paredzēts.

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
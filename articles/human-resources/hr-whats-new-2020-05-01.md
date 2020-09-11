---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 1. maijs)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 1. maiju.
author: Darinkramer
manager: AnnBe
ms.date: 05/01/2020
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
ms.author: dkrame
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 074c678d9d8294aabf4e78b2a6ee0fa53efbaf23
ms.sourcegitcommit: 2bcacef1e010c312f019dbf9740ce87d627848a7
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/20/2020
ms.locfileid: "3712284"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-1-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2020. gada 1. maijs)

Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.3196. Dažos virsrakstos redzamie numuri iekavās attiecas uz LCS atbalsta numuriem atsaucei.

## <a name="new-performance-management-entities-available-in-data-management-framework-dmf"></a>Datu pārvaldības struktūrā (DMF) ir pieejami jauni veiktspējas pārvaldības elementi

Šobrīd ir pieejami šādi elementi. Ja neredzat šos elementus, kas uzskaitīti elementu sarakstā, izmantojiet **Atsvaidzināšanas elementu** opciju sadaļā **Struktūras parametri > Elementa iestatījumi > Atsvaidzināt elementu sarakstu**.

- **Diskusiju kompetence**
- **Diskusiju mērķi**
- **Diskusiju mērījums**
- **Diskusiju tēma**
- **Veiktspējas žurnāls**
- **Mērījums**
- **Mērķa mērījums**

Turklāt **Diskusiju** elementam tika pievienots **Kopējais rezultāts** un **Vidējais rezultāts**.

## <a name="increase-length-of-leave-request-comments-275641"></a>Palielināt atvaļinājuma pieprasījumu komentāru (275641) garumu

Komentāri par atvaļinājumu pieprasījumiem tagad ļauj izmantot vairāk par 100 rakstzīmēm.

## <a name="final-comments-on-reviews-dont-appear-when-the-manager-or-employee-is-signed-into-a-different-company-431688"></a>Beigu komentāri par pārskatiem neparādās, kad vadītājs vai darbinieks ir pieteicies citā uzņēmumā (431688)

Visi komentāri tagad būs redzami, apskatot pārskatus.

## <a name="user-defined-links-arent-supported-on-new-worker-form-390374"></a>Lietotāja definētās saites netiek atbalstītas jaunā darbinieka formā (390374)

Lietotāja definētās saites tagad ir aktivizētas pilnveidotajā **Darbinieka** formā.

## <a name="hcmratinglevelentity-causes-odata-api-crash-439476"></a>HcmRatingLevelEntity izraisa OData API avāriju (439476)

Šīs izmaiņas labo API avāriju. Dublikāta nosaukums parādīja šo kļūdu.

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

## <a name="known-issues"></a>Zināmās problēmas

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
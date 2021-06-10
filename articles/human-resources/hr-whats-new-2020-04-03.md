---
title: Jaunumi vai izmaiņas risinājumā Dynamics 365 Human Resources (2020. gada 3. aprīlis)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 3. aprīli.
author: andreabichsel
ms.date: 04/03/2020
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
ms.search.validFrom: 2020-04-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 899ec0ee6a92763259f2f63d9de94e09c3f713d4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6051069"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-3-2020"></a>Jaunumi vai izmaiņas risinājumā Dynamics 365 Human Resources (2020. gada 3. aprīlis)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 Human Resources. Izmaiņas attiecas uz būvējuma numuru 8.1.3111. Dažos virsrakstos redzamie numuri iekavās attiecas uz atbalsta atsauces numuriem portālā Lifecycle Services (LCS).

## <a name="features-that-are-generally-available-the-week-of-april-6"></a>Funkcijas, kas parasti ir pieejamas no 6. aprīļa nedēļas

- **Atvaļinājumu un prombūtnes līdzekļi** - Papildinforāciju skatiet [Atvaļinājumu un prombūtnes pārskats](hr-leave-and-absence-overview.md).

- **Atvieglojumu pārvaldības līdzekļi** - papildinformāciju skatiet [Atvieglojumu pārvaldības pārskats](hr-benefits-management-overview.md).

## <a name="human-resources-environment-limits-are-now-based-on-updated-licensing-394595"></a>Human Resources vides ierobežojumi tagad ir balstīti atjauninātajā licencēšanā (394595)

Ir mainījies vižu skaita ierobežojums vienam projektam LCS. Iepriekšējais ierobežojums bija divas vides. Ražošanas un smilškastes vides skaita ierobežojums, ko var izveidot programmai Human Resources pakalpojumā LCS, tagad ir balstīts atjauninātajā licencēšanā. Tagad ir iespējams izveidot tik daudz vides, cik nepieciešams, katram LCS projektam atkarībā no iegādāto licenču skaita. Jaunā licencēšana, kas atjaunināta 2020. gada 1. februārī, ļauj klientiem iegādāties papildu vides. Plašāku informāciju par licencēšanas prasībām papildu vidēm skatiet [Dynamics 365 licencēšanas rokasgrāmatā](https://dynamics.microsoft.com/pricing/#HumanResources).
 
## <a name="error-when-trying-to-delete-a-questionnaire-428603"></a>Kļūda, mēģinot dzēst anketu (428603)

Šīs nedēļas atjauninājums novērš problēmu, kad, mēģinot dzēst anketu, parādās šāda kļūda:

Atrasts nesabalansēts X + + TTSBEGIN/TTSCOMMIT pāris.

## <a name="performance-journal-and-professional-certificates-security-issue-428499"></a>Veiktspējas žurnāla un profesionālo sertifikātu drošības problēma (428499)

Šī izmaiņa ierobežo gan veiktspējas žurnālu, gan profesionālo sertifikātu redzamību, pamatojoties uz uzņēmumiem, kuriem tie ir pieejami. 

## <a name="the-abbreviation-for-quebec-and-manitoba-387510"></a>Kvebekas un Manitobas saīsinājums (387510)

Sākuma dati ir atjaunināti, lai atspoguļotu pareizo saīsinājumu Manitobai un Kvebekai.

## <a name="new-entities-available-in-data-management-framework"></a>Jauni elementi pieejami Datu pārvaldības struktūrā

Šobrīd ir pieejami šādi elementi. Ja neredzat šos elementus, kas uzskaitīti elementu sarakstā, izmantojiet **Atsvaidzināšanas elementu** opciju sadaļā **Struktūras parametri > Elementa iestatījumi > Atsvaidzināt elementu sarakstu**.

 - Atvaļinājuma un kavējuma bankas transakcija V2
 - Atvaļinājuma un kavējuma reģistrācija V2
 - Atvaļinājuma un kavējuma plāna pakāpe V2
 - Atvaļinājuma un kavējuma plāns V2

## <a name="dataverse-solution-is-now-available-with-the-following-changes"></a>Dataverse risinājums tagad ir pieejams ar šādām izmaiņām:

| apraksts | Labot |
| --- | --- |
| **Darba/amata** elementa izmaiņas | <ul><li>**Kompensācijas reģions** pievienots</li>|
| **Darba amata dimensijas** pievienotais elements | <ul><li>**Finanšu dimensijas** pievienotas</li>
| **Darbinieka** elementa izmaiņas | <ul><li>**Vārdu secība** pievienota</li><li>**Darbi no mājām** pievienoti</li><li>**Valoda** pievienota</li><li>**Darba stāža datums** pievienots</li><li>**Gadadienas datums** pievienots</li><li>**Sākotnējais darbā pieņemšanas datums** pievienots</li></ul> |
| **Nodarbinātības** elementa izmaiņas | <ul><li>**Finanšu dimensijas** pievienotas</li><li>**Darba attiecību pārtraukšanas pamatojums** pievienots</li><li>**Beigu datums** pārdēvēts no **Pārejas datuma**</li><li>**Probācijas datums** pievienots</li></ul> |
| **Darbinieka adreses** elementa izmaiņas | <ul><li>**Adrese** pievienota</li><li>**1. adreses rinda**, **2. adreses rinda** un **3. adreses rinda** atzīmēta norakstīšanai</li></ul> |
| Jaunas mainīgās atlīdzības iestatījuma entitījas | <ul><li>**Atlīdzības mainīgā plāna tips**</li><li>**Atlīdzības mainīgā sistēma**</li><li>**Izmaksas noteikumi**</li><li>**Atlīdzības mainīgā plāna līmenis**</li></ul> |
| Jauna **Darbinieka kalendāra nodarbinātības** entitīja | <ul><li>**Darba kalendāra elements** pievienots</li></ul> |
| Jauna **Algas pozīcijas detalizētas informācijas** entitīja | <ul><li>**Algas pozīcijas detalizēta informācija** pievienota</li></ul> |
| Jauna **Nosaukuma** entitīja | <ul><li>**Nosaukums** pievienots</li></ul>Jaunā **Nosaukuma** entītija ir iekļauta Dataverse, bet šajā laikā nav atsauces no **Darba amata** vai **Darba** vienībām. |

> [!NOTE]
> Finanšu dimensijas abām pozīcijām un nodarbinātībai nodrošina viena virziena integrēšanu personāla vadības resursu atjauninājumiem Dataverse. Finanšu dimensiju atjauninājumi pašlaik nesinhronizējas no Dataverse uz personāla vadības resursiem.

Nākamo dažu nedēļu laikā šīs elementa izmaiņas būs pieejamas visās vidēs. Lai manuāli instalētu jaunāko Dataverse risinājumu Personāla vadībai:

1.  Dodieties uz [Power Platform Administrēšanas centru](https://admin.powerplatform.microsoft.com).

2.  Atlasiet **Vides**.

3.  Sameklējiet vidi, ko vēlaties atjaunināt. Apkārtējai videi ir jāatbilst **Vides nosaukumam** **Dataverse informācijas** sadaļā, kas atrodas sadaļā **Par** personāla vadības veidlapā.

4.  Atlasiet vidi, lai skatītu vides informāciju.

5.  Darbību joslas augšdaļā atlasiet pogu **Pārvaldīt risinājumus**. Tiks atvērts jauns pārlūkprogrammas logs un navigēs uz **Dynamics 365 administrēšanas centru** vides kontekstā.

6.  **Risinājumu** sarakstā atlasiet **Dynamics 365 Human Resources enkurs**.

7.  Atlasiet **Atjaunināt**, lai izmantotu jaunāko risinājumu.

## <a name="in-preview"></a>Priekšskatījumā

## <a name="leave-suspension"></a>Atvaļinājuma atlikšana

Jūs varat atlikt atvaļinājumu un prombūtni darbiniekam Personāla vadības programmā. Aizturot atvaļinājumu, tiek apturēti atvaļinājumu uzkrājumi atsevišķiem atvaļinājumu veidiem. Ja atlikšana notiek pēc uzkrājumu procesa, aizturētā atvaļinājuma rezultātā tiks izveidots proporcionāls pārrēķins darbinieka atvaļinājuma bilancei. Papildinformāciju skatiet [Aizturēt atvaļinājumu](hr-leave-and-absence-suspend-leave.md).

## <a name="carry-forward-rules"></a>Pārnešanas kārtulas

Jūs varat norādīt pārnešanas atvaļinājuma veidu pārnešanas bilancēm, ja pārnestās korekcijas tiek pārsūtītas. Piemēram, ja darbinieks pārnes 10 dienas, jūs varat izvēlēties citu atvaļinājuma veidu šīm 10 dienām. Papildinformāciju skatiet [Atvaļinājumu un prombūtnes veidu konfigurēšana](hr-leave-and-absence-types.md).

## <a name="coming-soon"></a>Drīzumā

## <a name="new-production-release-cadence"></a>Jauns ražošanas laidiena ritms

No aprīļa Personāla vadības laidienu ritms mainīsies no iknedēļas atjauninājumiem uz atjauninājumiem reizi divās nedēļās. Lai nodrošinātu saskaņotību ar drošām izvietošanas praksēm, kā arī uzturētu augstus stabilitātes un uzticamības standartus pakalpojumā, pakalpojumu atjauninājumu izvietošanas process visiem reģioniem būs divu nedēļu izvēršana. Būs paredzēta papildu pārbaudes un uzraudzība, lai nodrošinātu veiksmīgu izvietošanu katrā procesa posmā. Lai iegūtu papildu informāciju par laidiena ritmu skatiet rakstu [Atjaunināšanas process](hr-admin-setup-update-process.md).

## <a name="known-issues"></a>Zināmās problēmas

## <a name="employment-detail-entity"></a>Nodarbinātības informācijas elements

**Nodarbinātības informācijas** entītija ir atjaunināta ar šādiem laukiem: **PayFrequency**, **Nodarbinātības kategorijas ID**, **Nodarbinātības veids**, **EmploymentType ID** un **Atvieglojumu nodarbinātības statuss**. Šo lauku iestatīšanas dati paļaujas uz atvieglojumu pārvaldību, kas ir iespējota Līdzekļu pārvaldībā. Šos laukus nedrīkst aizpildīt vai atjaunināt **Nodarbinātības informācijas** entītijā, jo importēšanas laikā radīsies kļūdas.

## <a name="sharepoint-preview-doesnt-work-in-some-environments"></a>SharePoint priekšskatījums dažās vidēs nedarbojas

Ja dokumenta priekšskatījums dokumentiem, kas saglabāti SharePoint programmā, nedarbojas, veiciet šādas darbības:

1. Pārbaudiet, vai administratora lietotāja kontam ir e-pasts, kas saistīts ar lietotāja ierakstu. Šo informāciju varat aplūkot lapā **Lietotājs**. Ja e-pasta ziņojums nav iestatīts, e-pasta ziņojums un nodrošinātājs ir jāpievieno, izmantojot OData Excel pievienojumprogrammu. Pēc noklusējuma e-pasta adrese nav atrodama Excel noformējumā. Jums vajadzēs rediģēt Excel noformējumu, pievienot visus laukus, piemērot un atsvaidzināt. Kad šīs darbības ir izpildītas, varat atjaunināt administratora kontu.

2. Pēc tam, kad administratora kontam ir saistītais e-pasta konts, piesakieties pakalpojumā Human Resources ar administratora akreditācijas datiem.

3. Lai sāktu dokumenta priekšskatījumu, piekļūstiet SharePoint pielikumam.

4. Piesakieties ar citu lietotāja kontu, kam ir piekļuve pielikumiem, un apstipriniet, ka priekšskatījums darbojas kā paredzēts.

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2019. gada laidiena 2. kopumu](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
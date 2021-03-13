---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2020. gada 22. oktobrī
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 22. oktobri.
author: jcart1106
manager: tfehr
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 41b4e92720c6a9f830d940900c3c6e5b0a173de0
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130835"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2020. gada 22. oktobrī

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Dynamics 365 Human Resources. Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Dynamics 365 Human Resources 2020 laidiena 2. kopuma pārskats](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.3680.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Platformas atjauninājums 10.0.14(38) | -- | [Platformas atjauninājumi programmu Finance and Operations versijai 10.0.14 (2020. gada novembris)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14) |
| Organizācijas un personāla vadības darbplūsmas pieredzes uzlabojumi | [Organizācijas un personāla vadības darbplūsmas pieredzes uzlabojumi](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurācijas opcija, lai novietotu sarakstu Man piešķirtie darba elementi](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varam atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs| Izsniegt  | Apraksts|
| --- | --- | --- |
| 437922 | Importējot FMLA stundas, izmantojot DMF elementu, rodas tikai lasāma kļūda. | FMLA stundu elementa lietošana, lai importētu ar FMLA gadījumu saistītās stundas, neizdevās. Mēs pievienojām loģikas, lai nodrošinātu, ka importētās stundas nepārsniedz gadījumam atlikušās stundas. |
| 512019 | Nepareiza **Pēdējās pārnešanas** summa. | Lapā **Brīvais laiks** mainot **Sākuma datumu** uz nākamā finanšu perioda pirmo dienu, tika parādīta nepareiza **Pēdējās pārnešanas** summa veidam **Ikgadējais atvaļinājums**. Tagad tiek parādīta pareizā summa. |
| 458639 | Elements **Darbinieka kontaktpersonas** neatbalsta izmaiņu izsekošanas režīmu. | Mēs atjauninājām elementu **Darbinieka kontaktpersonas**, lai to varētu izmantot, ieviešot paši savus datu bāzes (BYOD) scenārijus.|
| 505347 | Apmācības vadītāji varēja iesniegt atvaļinājuma pieprasījumu darbiniekam, kad tika iespējots līdzeklis Racionalizētais darbinieks. | Lomām, kas nav cilvēkresursu palīgs un cilvēkresursu vadītājs, nav atļauts iesniegt brīvā laika pieprasījumus darbiniekiem. |
| 513490 | Atvieglojumu pārvaldības reģistrēšana: pievienojiet reģistrāciju plāniem bez seguma opcijām. | Mēs iespējojām reģistrācijas rezultātus **Plānam bez seguma opcijām**. Tagad tie tiek rādīti tabulā **Procesa rezultāti**, un tie ir pareizi sakārtoti, lai tiktu rādīti augšgalā. |
| 517021 | Nevar atlasīt vairākus plānus ar to pašu kodu **Plāna veids**, ja **Plāna veidam** ir viena reģistrācija katram veidam. | Mēs izmainījām ierobežojumus, atlasot plānus, kuros ir atļauta tikai viena reģistrācija. Ierobežojumi tagad ir līmenī **Plāna veida kods**, nevis **Plāna veids**. Šī izmaiņa ļauj tādiem plāniem kā HSA un FSA, kas ir vienāda veida, piešķirt atsevišķu **Plāna veida kodu**. Tādējādi varat atlasīt abus plānus vienam reģistrācijas periodam. |
| 444791 | Nevar skatīt atlīdzību Darbinieku pašapkalpošanās sistēmā, kad Atlīdzības plānā ir ieslēgta opcija **Ierobežot piekļuvi**. | Darbinieka pašapkalpošanās **Atlīdzības** kartē pašreizējā atlīdzības summa un procentuālās vērtības pieaugums rādīja "0", ja darbinieks bija reģistrēts plānā, kuram bija ieslēgta opcija **Ierobežota piekļuve** un kurš bija piešķirts noteiktām lomām. Mēs atrisinājām šo problēmu, tāpēc darbinieks un vadītājs vienmēr var redzēt atlīdzības informāciju paši par sevi un saviem tiešajiem padotajiem. |
| 457542 | Kursa informācijas atjaunināšana pēc kursa slēgšanas neatjaunina šo pašu informāciju darbiniekam, kas izgāja kursu. | Darbinieka informācija tagad tiek pareizi atjaunināta, kad maināt kursu informāciju pēc tā slēgšanas un atkārtotas atvēršanas. |
| 515342 | Nevar ievietot datus, izmantojot **XCDSLeaveRequestDetailEntity**. Uzņēmums nav atrodams vai nepastāv. | Tagad varat izmantot **XCDSLeaveRequestDetailEntity** datu ievietošanai. |
| 514743 | Izmantojot Microsoft Exchange, radās kļūda veidlapā **E-pasta parametri**. | Ziņojums "Nevarēja ielādēt failus vai montāžu..." tika parādīts lapā **E-pasta parametri**, kad e-pasta nodrošinātājs tika iestatīts uz **Exchange**. Šis labojums atļauj arī ielādēt lapu **E-pasta parametri** un to saglabāt, kā paredzēts. |


## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Programma Human Resources programmā Microsoft Teams | [Darbinieka atvaļinājuma un prombūtnes pieredze programmā Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Programma Human Resources programmā Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Atvaļinājumu pieprasījumu pārvaldība programmā Teams](hr-teams-leave-app.md) |
| Uzlaboti darbplūsmas pieprasījumi un apstiprinājumi | [Organizācijas un personāla vadības darbplūsmas pieredzes uzlabojumi](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurācijas opcija, lai novietotu sarakstu Man piešķirtie darba elementi](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Virtuālie elementi Dataverse programmai Human Resources | [Dynamics 365 Human Resources pamatdatu izvēršana programmā Dataverse](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Dataverse virtuālo elementu konfigurēšana](hr-admin-integration-common-data-service-virtual-entities.md) |
| Integrācija ar LinkedIn Talent Hub | [Integrācija ar LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integrācija ar LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
| Vadītāja pašapkalpošanās pielāgotās saites | [Vadītāja pašapkalpošanās pielāgotās saites](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Vadītāja pašapkalpošanās pielāgotās saites](https://aka.ms/MSSCustomLinks) |

## <a name="coming-soon"></a>Drīzumā

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Dynamics 365 Human Resources 2020 laidiena 2. kopuma pārskats](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2020. gada laidiena 2. kopumu](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

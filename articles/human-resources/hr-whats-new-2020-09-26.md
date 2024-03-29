---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2020. gada 26. septembrī
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni vai mainīti programmā Microsoft Dynamics 365 Human Resources 2020. gada 26. septembrī.
author: jcart1106
ms.date: 09/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2f78201585101e2848eded69e03d5eb4c22d7e9a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066768"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-26-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2020. gada 26. septembrī

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā Dynamics 365 Human Resources. Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2020 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.3589-hf.3.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētais līdzeklis parasti ir pieejams ar šo laidienu:

- **Platformas atjauninājums 10.0.13 tagad ir pieejams:** plašāku informāciju par šo atjauninājumu skatiet platformas atjauninājumos finanšu un operāciju programmu versijā 10.0.13 [(2020. gada oktobris)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13.md).

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Iespējams, šim rakstam ir pieejami atjauninājumi, lai iekļautu kļūdu labojumus, kas to izlaboja būvējuma laikā pēc šī raksta sākotnējā publicēšanas.

| Problēmas numurs | Problēma | Apraksts |
| --- | --- | --- |
| 469495 | Noklusējuma finanšu dimensiju režģa un dialoglodziņa atjauninājums | Finanšu dimensiju režģis un dialoglodziņš ir atjaunināts visā programmā Human Resources. |
| 474887 | Atvaļinājuma pieprasījuma darba vienība atver nepareizu saiti manuālā lēmumā | Kad darbplūsmas konfigurācija ietver manuālu lēmumu, pārvietojoties uz atvaļinājuma pieprasījumu no **Man piešķirtās darba vienības**, tiek atvērta nepareiza saite, parādot tukšu formu vai atvaļinājuma pieprasījumu, ko izveidojis pašreizējais lietotājs, nevis to, kas piešķirta manuālajam lēmumam. |
| 474962 | Atvaļinājumu un kavējumu parametru elementam ir lauki ar neskaidriem etiķetēm | Atvaļinājuma un prombūtnes parametru elementa etiķetes tiek atjauninātas, lai tās būtu skaidrākas. |
| 481401 | Uzkrāšanas apstrāde uzkaras, kad uzkrāšanas datums ir pēc uzkrāšanas sākuma datuma un mēneša beigās | Uzkrāšanas apstrāde tiek atjaunināta, lai nebūtu aizkaves, kad uzkrāšanas datuma bāze ir pēc uzkrāšanas sākuma datuma un mēneša beigās. |
| 447167 | Ierakstu, kam beidzas derīgums, sarakstos ir neaktīvi darbinieki | Cilnē **Ieraksti, kam beidzas derīgums** sadaļā **Personāla vadība** bija iekļauti neaktīvi darbinieki. Tagad tā ietver tikai aktīvos darbiniekus. |
| 486840 | No **Man piešķirtās darba vienības** tiek atvērts nepareizs prombūtnes atvaļinājuma pieprasījums | Atlasot prombūtnes atvaļinājuma pieprasījumu no **Man piešķirtās darba vienības**, vairs netiek atvērts visjaunākais pašreizējam lietotājam piešķirtais prombūtnes atvaļinājuma pieprasījums. |
| 506868 | Dataverse Lauks **Nosaukums** nav iestatīts elementam **Amats** | Lauks **Nosaukums** elementos **Darbs** un **Amats** tiek rādīts kā nenorādīts. Tagad tiek parādīts lauks **Nosaukums**. |
| 430359 | Nevar piekļūt darba beigšanas kontrolsaraksta uzdevumiem ar piešķirtām vadītāja un darbinieka lomām | Darbinieki ar turpmāku darba pārtraukšanas datumu nevarēja piekļūt kontrolsaraksta uzdevumiem, ja tiem bija tikai darbinieka vai vadītāja loma. Tagad lietotāji, kuriem ir tikai darbinieka vai vadītāja loma, var piekļūt darba beigšanas uzdevumiem ar turpmāku darba pārtraukšanas datumu. |
| 458102 | Izveidojot jaunu darbinieku, tas netiek parādīts elementā **Darbinieka algas informācija** | Jauni darbinieki tiek iekļauti darbinieka algas informācijas elementā, neatverot darbinieka algas informāciju pirms elementa eksportēšanas. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Programma Human Resources programmā Microsoft Teams | [Darbinieka atvaļinājuma un prombūtnes pieredze programmā Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Programma Human Resources programmā Teams](./hr-admin-teams-leave-app.md)<br>[Atvaļinājumu pieprasījumu pārvaldība programmā Teams](hr-teams-leave-app.md) |
| Uzlaboti darbplūsmas pieprasījumi un apstiprinājumi | [Organizācijas un personāla vadības darbplūsmas pieredzes uzlabojumi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurācijas opcija, lai novietotu sarakstu Man piešķirtie darba elementi](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |

## <a name="coming-soon"></a>Drīzumā

Nākamajam laidienam ir plānots šāda jauns līdzeklis:

- [Vadītāja pašapkalpošanās pielāgotās saites](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2019 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Papildu resursi

[Jaunumi vai izmaiņas Human Resources](hr-admin-whats-new.md)
[Pakalpojuma Dynamics 365 Human Resources 2020. gada laidiena 2. kopuma pārskats](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)
[Atjaunināšanas process](hr-admin-setup-update-process.md)
[Pārvaldības līdzekļi](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

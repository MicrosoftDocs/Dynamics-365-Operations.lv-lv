---
title: Jaunumi vai izmaiņas risinājumā Dynamics 365 Human Resources 2021. gada 5. aprīlis
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 5. aprīli.
author: marcelbf
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 19ac856de0fed9253bf79cb4c06d4347e5a19c77
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693477"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-5-2021"></a>Jaunumi vai izmaiņas risinājumā Dynamics 365 Human Resources 2021. gada 5. aprīlis

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4074.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Ierobežot darbiniekus rediģēt uzņēmuma kontaktinformāciju | [Ierobežot darbiniekus rediģēt uzņēmuma kontaktinformāciju](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Ierobežot personas informācijas rediģēšanu](./hr-employee-self-service-restrict-editing.md)|

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varam atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Izsniegt |  Apraksts |
| --- | --- | --- |
| 550852 | Poga **Apstiprinājums** netiek validēta ar obligātiem laukiem, kas iestatīti veidlapā **Pārskats**. | Kad veidlapā **Pārskats** lauks tiek iestatīts kā obligāts un izmaiņas vadītāja lomai tiek publicētas, veidlapa netiek validēta, kā paredzēts. |
| 559564 | Vēsturiskas darbinieka darbības fiksētas atlīdzības izmaiņai rada kļūdu lietotājiem, ar kuriem pārtrauktas darba attiecības. | Izejošā darbinieka atlīdzības nodarbinātā darbība rada kļūdu. Kad darba attiecības ar darbinieku ir pārtrauktas, nodarbinātā veicināšanas darbība pirms darba attiecību pārtraukšanas rada kļūdu. |
| 560074 | Nodarbinātības kategoriju nolaižamais saraksts nefiltrē **Nodarbinātā veidu** un rāda kategorijas darbiniekiem un līgumdarbiniekiem. | Veidlapā **Darbinieks** nolaižamajā sarakstā **Nodarbinātības kategorija** ir jārāda vai nu darbinieka, vai līgumdarbinieka kategorijas, pamatojoties uz nodarbinātā veidu. |
| 567388 | Daļa tikko izveidoto darbinieku informācijas netiek sinhronizēta ar tabulu **cdm_worker** pakalpojumā Dataverse. | Izveidojot jaunu darbinieka ierakstu, jaunais ieraksts tiks sinhronizēts ar tabulu **cdm_worker** pakalpojumā Dataverse, taču ne visi rekvizīti tiks iekļauti Dataverse ierakstā. |
| 563837 | Līdzekļi, kas nav pieejami Human Resources displejā. | Vairākas funkcijas, kas neattiecas uz Human Resources displeju Līdzekļu pārvaldībā. Tagad šie līdzekļi tiek noņemti no to līdzekļu saraksta, kurus var iespējot, izmantojot Human Resources. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Atvieglojumu pārvaldības darbvieta | [Atvieglojumu pārvaldības darbvieta (Priekšskatījums)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Atvieglojumu pārvaldības darbvieta](hr-benefits-management-workspace.md) |

## <a name="coming-soon"></a>Drīzumā

| Funkcija | Detalizētā informācija |
| --- | --- |
| Vadītāja ievadītās prasmes saviem darbiniekiem var automātiski apstiprināt ar darbplūsmu | Drīzumā. |
| Platformas atjauninājums 10.0.17 (41) | Ir ieplānots, ka platformas atjaunināšana 10.0.17 sāks izriti ar nākamo laidienu 2021. gada 19. aprīlī. Papildinformāciju skatiet Platformas [atjauninājumos Finanšu un operāciju programmu versijā 10.0.17 (2021. gada aprīlis)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md). |

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 1. kopumu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
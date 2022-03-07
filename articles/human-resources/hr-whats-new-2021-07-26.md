---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 26. jūlijs
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 26. jūliju.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-26
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 810511c42cd690579d8c8b6ebcc17b0cf7fcb9eb2b999822dc2226fabd127cc6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771519"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-26-2021"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 26. jūlijs

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4384.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Platformas update 10.0.20 | -- | [Platformas atjauninājumi programmu Finance and Operations versijai 10.0.20 (2021. gada augusts)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20) |

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varam atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Problēma |  Apraksts |
| --- | --- | --- |
| 600422 | Algas adreses apstiprināšana neizdevās, ja tika veikta gatavība apmaksai. | Pārbaude ir atjaunināta, lai pieprasītu tikai vienu adresi ar tipu 'Algas uzņēmuma vieta' un tikai vienu adresi, kuru tips ir 'Algu darba vieta'. |
| 601226 | Datu integrācijas problēma: algu integrācijas eksporta projektam nav opcijas pilnai pašpiegādes | Algas integrācija Uz Ceridian DayForce tika veikts inkrementāla izvilkšana, nevis pilna izvilkšana. Ceridian darbībai vienmēr jābūt pilnīgai atsvaidzināšanai. Šī problēma tagad ir labota, datu eksporta projekta elementi vairs netiks apvērsti inkrementālai izvilkšanai. |
| 602272 | Tagad trūkst darbinieku pašapkalpošanās darbvietai pievienotās preces un šim darbiniekam vairs nevar pievienot elementus | Esam labojuši personalizēšanas problēmu darbinieku pašapkalpošanās pakalpojumiem. Skatā var pievienot jaunu failu, un lietotājiem tiks redzama jebkāda esošā personalizēšana |
| 600711 | Pusgada definīcijas atlases lauks iespējots pilnas dienas atvaļinājumu pieprasījumiem | Šī problēma tagad ir labota un pusdienas definīcijas lauks tiks iespējots tikai tad, ja darbinieki atlasīs atvaļinājuma tipu ar iespējotu pusgada definīciju un pusgadu kā atlasīto summas vērtību |
| 602208 | Uzkrāšanas likmes vienības, kas parāda stundas, nevis dienas | Šī problēma tagad ir labota. Veidlapa **Izslēgtais laiks** rādīs pareizu **Uzkrājuma likmes** kolonnas atvaļinājuma vienību (stundas vai dienas). |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Atvieglojumu pārvaldības darbvieta | [Atvieglojumu pārvaldības darbvieta (Priekšskatījums)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Atvieglojumu pārvaldības darbvieta](hr-benefits-management-workspace.md) |
| Aktivizēt vienkāršoto algu integrāciju (Algu integrācijas API) | [Iespējot vienkāršotu integrāciju ar personāla algu sniedzējiem](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algu aprēķina integrācijas API](hr-admin-integration-payroll-api-introduction.md)|
|  Atļaut kavējumu pārvaldniekam pārvaldīt atvaļinājumu | [Atļaut kavējumu pārvaldniekam pārvaldīt atvaļinājumu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Ar šo laidienu mēs atjauninām kavējumu pārvaldnieka darbvietas skatu. Papildinformāciju skatiet sadaļā [Kavējumu pārvaldības lomas konfigurēšana](https://go.microsoft.com/fwlink/?linkid=2168107).|
|  Konfigurēt pielikuma prasības pa atvaļinājuma veidiem | [Konfigurēt pielikuma prasības pa atvaļinājuma veidiem](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Konfigurēt atvaļinājumu un kavējumu veidus](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Konfigurējiet atvaļinājuma vienības katram atvaļinājuma veidam | [Konfigurējiet atvaļinājuma vienības katram atvaļinājuma veidam](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Konfigurēt atvaļinājumu un kavējumu veidus](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Dot iespēju darbiniekus atzīmēt kā gatavus apmaksai | [Dot iespēju darbiniekus atzīmēt kā gatavus apmaksai](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Gatavs apmaksai](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Drīzumā

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 2. kopumu](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

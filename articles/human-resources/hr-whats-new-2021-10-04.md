---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 5. oktobrī
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 5. oktobri.
author: marcelbf
ms.date: 10/05/2021
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
ms.search.validFrom: 2021-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 206c7f590b495278b7899271db0e83b3a4da3edc
ms.sourcegitcommit: 42bd701179e664947b6eafcd1804c83a5e64abcb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2021
ms.locfileid: "7641434"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-5-2021"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 5. oktobrī

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Microsoft Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4485.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
|---|---|---|
| Platformas atjauninājums 10.0.21 (45) | -- | [Platformas atjauninājumi programmu Finance and Operations versijai 10.0.21 (2021. gada oktobris)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |


### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varētu atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Problēma | Apraksts |
|---|---|---|
| 598896 | Darbinieka summa netiek parādīta, kamēr darbinieks nav pabeidzis reģistrāciju | Lapā **Darbinieku patstāvīgi izmantojamais pakalpojums**, darbinieka summa atvieglojumam netika parādīta. Darbinieka summa tagad tiek parādīta lapā **Atvieglojumu pašapkalpošanās sistēma**.  |
| 613440 | Nevar eksportēt datus no **Datu pārvaldības** | Eksportējot datus projektam **Datu pārvaldībā**, eksportētēšana neizdodas. |
| 618327 | Slēgtie un nākamie periodi ir parādīti atvieglojumu pārskata lapā **Pārskatu parametri** | Pārvietojoties uz **Atvieglojumu pārskatu** **Darbinieku pašapkalpošanās** sadaļā, lapa **Pārskata parametri** parāda **Ierakstus, kas jāiekļauj** un kopsavilkuma cilnes **Palaist fonā**. Šīs sadaļas tika noņemtas.|
| 618326 | Nepareiza **Pārskatu parametru** lapa tiek parādīta atvieglojumu pārskata sadaļā **Darbinieku patstāvīgi izmantojamais pakalpojums**| Pārvietojoties uz **Atvieglojumu pārskata** galamērķa lapu, lietotājs varēja atlasīt atvieglojumu plānu periodus, kas ir slēgti vai ir datēti ar nākotnes datumu, iegūstot tukšu lapu. Sarakstā ir jāparāda tikai pašreizējais atvieglojumu plāna periods. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Lai iegūtu papildinformāciju par to, kā ieslēgt priekšskatījuma līdzekļus, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
|---|---|---|
| Atvieglojumu pārvaldības darbvieta | [Atvieglojumu pārvaldības darbvieta (Priekšskatījums)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Atvieglojumu pārvaldības darbvieta](hr-benefits-management-workspace.md) |
| Pielāgotie lauki Piemērotības opcijā |[Pielāgoto lauku atbalsts atbilstības apstrādei](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Pielāgoto lauku izmantošana atbilstības apstrādei](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| Atvieglojumu pārskats |[Atvieglojumu pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [Atvieglojumu pārskats](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>Zināmās atvieglojumu pārskatu problēmas

| Problēma | Apraksts |
|---|---|
|Kļūda, pārskatu nosūtot pa e-pastu, izmantojot **GER pārskata galamērķi** | Atvieglojumu pārskatu var iestatīt, lai izmantotu e-pasta parametrus **GER pārskata galamērķu** lapā. Aizpildot pārskata iestatīšanu un drukāšanu, lietotājs saņems formatēšanas kļūdu, un atvieglojumu paziņojums netiks nosūtīts.|

## <a name="feature-management-changes"></a>Līdzekļu pārvaldības izmaiņas

| Funkcija | Apraksts |
|---|---|
|Veiktspējas žurnālu paplašināto pārskatu skats | Šis līdzeklis šajā laidienā tiks iespējots pēc noklusējuma. |

## <a name="coming-soon"></a>Drīzumā

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funkcija | Informācija |
|---|---|
| Platformas atjauninājums 10.0.22 (46) | Ir ieplānots, ka platformas atjauninājuma 10.0.22 izlaišana tiks sākta ar pakalpojuma laidienu 2021. gada 1. novembrī. Papildinformāciju skatiet sadaļā [Platformas atjauninājumi Finance and Operations programmu versijai 10.0.22 (2021. gada novembris)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22). |



## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 2. kopumu](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

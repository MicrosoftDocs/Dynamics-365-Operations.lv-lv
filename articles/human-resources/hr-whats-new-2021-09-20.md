---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 20. septembrī
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 20. septembri.
author: marcelbf
ms.date: 09/20/2021
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
ms.search.validFrom: 2021-09-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3f4fc4768f8c96678b216709f78af6d3ddfd4132
ms.sourcegitcommit: ba8ca42e43e1a5251cbbd6ddb292566164d735dd
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/25/2021
ms.locfileid: "7556937"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-20-2021"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 20. septembrī

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Microsoft Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4464.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
|---|---|---|
| Aktivizēt vienkāršoto algu integrāciju (Algu integrācijas API) | [Iespējot vienkāršotu integrāciju ar personāla algu sniedzējiem](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algu aprēķina integrācijas API](hr-admin-integration-payroll-api-introduction.md) |
| Dot iespēju darbiniekus atzīmēt kā gatavus apmaksai | [Dot iespēju darbiniekus atzīmēt kā gatavus apmaksai](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Gatavs apmaksai](/dynamics365/human-resources/hr-compensation-payroll) |

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varētu atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Problēma | Apraksts |
|---|---|---|
| 619774 | Adreses apraksta rediģēšana reāllaikā nav sinhronizēta ar Dataverse. | Rediģējot darbinieka adreses aprakstu, atjauninātais apraksts reāllaikā netiek sinhronizēts ar Dataverse. Abonements tabulā **Loģistikas novietojums** tika atjaunināts atjauninājuma nosūtīšanai. |
| 614603| Ja nav atlasīts **Darbinieka personāla darbību** parametrs, lapā **Darbinieks** rodas kļūda. | Pieņemot darbā jaunu darbinieku vai pārvietojoties uz lapu **Darbinieks**, tiek parādīta tālāk šāda kļūda: "Lauks **Personāla darbības tips** ir jāaizpilda", pat ja **Personāla darbības** ir izslēgtas. |
| 615367 | Cilne **Apstiprināts brīvais laiks** parāda brīdinājumu un tiek parādīts nepareizi. | Ja atvaļinājuma vienība ir iestatīta uz **Dienas** pirms funkcionalitātes **Konfigurēt atvaļinājumu vienības atvaļinājuma tipam** iespējošanas, cilne **Apstiprināts brīvais laiks** parāda nederīgu brīdinājumu un nepareizas kolonnas. |


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
| **Pārskatu parametru** lapa sadaļā **Darbinieku pašapkalpošanās** atvieglojumu pārskatam nav pareiza. | Pārvietojoties uz **Atvieglojumu pārskatu** **Darbinieku pašapkalpošanās** sadaļā, lapa **Pārskata parametri** parāda **Ierakstus, kas jāiekļauj** un kopsavilkuma cilnes **Palaist fonā**.  Tie ir jānoņem. |
| Slēgtie un nākamie periodi ir parādīti atvieglojumu pārskata **Pārskatu parametru** lapā. | Pārvietojoties uz **Atvieglojumu pārskata** galamērķa lapu, lietotājs var atlasīt atvieglojumu plānu periodus, kas ir slēgti vai ir datēti ar nākotnes datumu, kas būs tukša lapa. Sarakstā ir jāparāda tikai pašreizējais atvieglojumu plāna periods. |
|Kļūda, kad pārskatu nosūtāma pa e-pastu, izmantojot GER pārskata galamērķi. | Atvieglojumu pārskatu var iestatīt, lai izmantotu e-pasta parametrus **GER pārskata galamērķu** lapā. Aizpildot pārskata iestatīšanu un drukāšanu, lietotājs saņems formatēšanas kļūdu, un atvieglojumu paziņojums netiks nosūtīts.|


## <a name="coming-soon"></a>Drīzumā

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funkcija | Detalizētā informācija |
|---|---|
| Platformas atjauninājums 10.0.21 (45) | Ir ieplānots, ka platformas atjaunināšana 10.0.21 sāks izriti ar pakalpojuma laidienu 2021. gada 4. oktobrī. Papildinformāciju skatiet [Platformas atjauninājumi Finance and Operations programmu versijai 10.0.21 (2021. gada oktobris)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
|Veiktspējas žurnālu paplašināto pārskatu skats | Nākamās izrites laikā šī funkcija tiks aktivizēta pēc noklusējuma. |


## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 2. kopumu](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

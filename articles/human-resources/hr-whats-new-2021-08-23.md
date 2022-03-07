---
title: Jaunumi un izmaiņas risinājumā Dynamics 365 Human Resources 2021. gada 23. augustā
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 23. augustu.
author: marcelbf
ms.date: 08/23/2021
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
ms.search.validFrom: 2021-08-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 21c9ee0206bd77a8a2ec42501d64e83077baef09
ms.sourcegitcommit: 696796ca5635863850ae9ef16fc1fb0fc46ce8f0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/28/2021
ms.locfileid: "7441679"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-23-2021"></a>Jaunumi un izmaiņas risinājumā Dynamics 365 Human Resources 2021. gada 23. augustā

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Microsoft Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4419.

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varētu atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Problēma | Apraksts |
| --- | --- | --- |
| 594066 | Nevar dzēst kontaktpersonas informāciju | Atlasot kontaktpersonas informācijas ieraksta dzēšanu darbiniekam, tiek dzēst ieraksts, kas nav atlasītais ieraksts. |
| 611339 | Pievienojot personalizāciju, bankas konts neņem vērā filtru un ienes pirmo ierakstu | Personalizācijas pievienošanas dēļ bankas kontu saraksts palaiž personalizācijas vaicājumu, pirms ir palaists datu avota vaicājums, kā rezultātā vaicājums ienes augšējo ierakstu neatkarīgi no darbinieka, kura informācija tiek skatīta. |
| 591806 | Ienākošie termiņu datumi netiek aprēķināti pareizi | Termiņu datumi netiek pareizi aprēķināti, ja spēkā ir šādi nosacījumi: Kontrolsaraksti, kuri tiek izveidoti, izmanto kalendāru, kas izmanto papildināto laika diapazonu (piemēram, no 2005. līdz 2050. gadam) un lietotāja preferences izmanto laika zonu, kas nav Centrālais Standarta laiks. |   
| 592749 | Atvaļinājuma bilance nav pareiza sadaļā **Darbinieku pašapkalpošanās** | Ja darbinieks ir nodarbināts vairāk nekā vienā juridiskajā vienībā un ir iespējots starpuzņēmumu atvaļinājuma skats, atvaļinājuma bilance var būt nepareiza. |
| 603133 | Negaidīts brīdinājums, pieprasot brīvo laiku | Pieprasot brīvo laiku, lauka **Puse dienas** aizpildīšana pirms lauka **Daudzums** aizpildīšanas rada negaidītu brīdinājumu. |
| 606546 | Atlasītais lauks nav redzams apstiprinātajā brīvajā laikā | Aizzīmes lodziņš vairāku apstiprināto atvaļinājuma pieprasījumu atlasei nav redzams. |
| 597059 | Darbinieks nav redzams sadaļā **Atvaļinājumu un prombūtnes uzņēmuma kalendārs** | Darbinieks nav redzams **Atvaļinājumu un prombūtnes uzņēmuma kalendārā**, ja piemērotais datu diapazons ietver jebkuru dienu, kurai tika liegts atvaļinājuma pieprasījums. |


## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Lai iegūtu papildinformāciju par to, kā ieslēgt priekšskatījuma līdzekļus, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Atvieglojumu pārvaldības darbvieta | [Atvieglojumu pārvaldības darbvieta (Priekšskatījums)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Atvieglojumu pārvaldības darbvieta](hr-benefits-management-workspace.md) |
| Aktivizēt vienkāršoto algu integrāciju (Algu integrācijas API) | [Iespējot vienkāršotu integrāciju ar personāla algu sniedzējiem](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algu aprēķina integrācijas API](hr-admin-integration-payroll-api-introduction.md)|
| Atļaut kavējumu pārvaldniekam pārvaldīt atvaļinājumu | [Atļaut kavējumu pārvaldniekam pārvaldīt atvaļinājumu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Ar šo laidienu mēs atjauninām kavējumu pārvaldnieka darbvietas skatu. Papildinformāciju skatiet sadaļā [Kavējumu pārvaldības lomas konfigurēšana](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Konfigurēt pielikuma prasības pa atvaļinājuma veidiem | [Konfigurēt pielikuma prasības pa atvaļinājuma veidiem](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Konfigurēt atvaļinājumu un kavējumu veidus](https://go.microsoft.com/fwlink/?linkid=2168108)|
| Konfigurējiet atvaļinājuma vienības katram atvaļinājuma veidam | [Konfigurējiet atvaļinājuma vienības katram atvaļinājuma veidam](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Konfigurēt atvaļinājumu un kavējumu veidus](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Dot iespēju darbiniekus atzīmēt kā gatavus apmaksai | [Dot iespēju darbiniekus atzīmēt kā gatavus apmaksai](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Gatavs apmaksai](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Drīzumā

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funkcija | Detalizētā informācija |
| --- | --- |
| Platformas atjauninājums 10.0.21 (45) | Ir ieplānots, ka platformas atjaunināšana 10.0.21 sāks izriti ar pakalpojuma laidienu 2021. gada 4. oktobrī. Papildinformāciju skatiet [Platformas atjauninājumi Finance and Operations programmu versijai 10.0.21 (2021. gada oktobris)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 2. kopumu](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

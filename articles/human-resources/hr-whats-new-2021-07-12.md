---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 12. jūlijs
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 12. jūliju.
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
ms.search.validFrom: 2021-07-12
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4ebe5a6ae19d00b94247381c700ff21d31910fcac1968ab4f8a673f89ddd2f0f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782639"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-12-2021"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 12. jūlijs

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4353.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
|  Pakalpojumu rādīšanas gadu pārslēgšanās | |Šī iespēja sniedz iespēju izmantot dažādus datumus, lai aprēķinātu pakalpojuma gadus, kas attēloti lapā **Racionalizēta darbinieka ieraksts** un lapā **Cilvēki**.  Tas būs pieejams [Human Resources parametros](/dynamics365/human-resources/hr-setup-parameters). |


### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varam atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Problēma |  Apraksts |
| --- | --- | --- |
| 595871 | Par personāla vadības rūti ir nepareiza Dataverse terminoloģija | Ar Common Data Service zīmola maiņu uz Dataverse ir atjaunināta terminoloģija Microsoft Dynamics 365 Human Resources informācijas rūtī (**Palīdzība un Atbalsts > Par**). |
| 598676 | Racionalizēta darbinieka ieraksta veidlapa ignorē uzdevumu, var izveidot kļūdu, izmantojot to ar saglabāto skatu| Ja saglabātajā skatā ir ieslēgts līdzeklis 'Racionalizēts darbinieka ieraksts', lapā **Darbinieks** programma var neizdoties, ja iestatījums **Vienmēr ir atvērts rediģēšanai**. |
| 592344 |Darbinieku sastāva sadaļa pozīcijā jālasa tikai tad, ja ir iespējota atvieglojumu pārvaldība | Darbinieku sastāva informācija tiek izveidota, izmantojot mantojuma atvieglojumu funkcionalitāti.  Ja atvieglojumu pārvaldība ir iespējota, lauki būs tikai lasāmi. Ja atvieglojumu pārvaldība ir ieslēgta un **Slēpt mantojuma atvieglojumu veidlapas** ir iestatītas uz **Jā** koplietotos HR parametros, cilne **Darbinieku kompensācija** tiks paslēpta. |
| 598617 | **HcmDiscussion** veidlapas aktivizēšanas cilne rada bezgalīgu cilpu, kad tiek lietotas personalizēšanas | Ja gan režģa, gan detaļu skatam ir ieslēgts skats **Vienmēr atvērts rediģēšanai**, kods, kas aktivizē cilni ignorētajā uzdevuma metodē, konfliktē ar personalizēšanu par to, kādai kontrolei ir jāfokusē un jārediģē bezgalīga cilpa. |
| 593553 | Žurnāla datuma lauks Veiktspējas žurnālā tiek rādīts UTC formātā | Lauks **Žurnāla datums** veiktspējas žurnāliem tiek rādīts UTC laika joslā, nevis sistēmas datumu iestatījumā definētajā laika joslā, kas izraisa datuma nepareizu rādīšanu dažām laika joslām. |
| 586930 | Aktivitātes atvēršana veiktspējas mērķiem atver pilnīgi atšķirīgu ierakstu | Ja līdzekļu pārvaldībā ir iespējots līdzeklis 'Veiktspējas žurnālu paplašināto pārskatu skats', paplašināto pārskatu veiktspējas mērķu atlasīšana cilnē **Mana grupa** **Darbinieku pašapkalpošana** atver darbinieka mērķus, nevis atlasīto darbinieku. |
| 569959 |  Elements HcmPositionWorkerAssignmentV2 nepiešķir amatam darbinieku | Lietotāji saņēma kļūdu, pievienojot atrašanās vietas piešķires ierakstu, izmantojot entītiju, un publicēšana neizdevās. |
| 582259 | VETS 4212 pārskats izmanto veidlapu 2017, nevis veidlapu 2020 | Atjaunināts līdz 2020 formātam.  Lai ielādētu jauno formātu, dodieties uz **Pārskata konfigurācijas** un izdzēsiet VETS-4212 pārskatu kreisajā kolonnā. Dodieties uz **Elektroniskie pārskati — Repozitoriji — HR resursi** un atlasiet **Atvērt**.  Atlasiet **VETS-4212 PDF izdruku** un pēc tam atlasiet **Importēt**.|


## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Atvieglojumu pārvaldības darbvieta | [Atvieglojumu pārvaldības darbvieta (Priekšskatījums)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Atvieglojumu pārvaldības darbvieta](hr-benefits-management-workspace.md) |
| Aktivizēt vienkāršoto algu integrāciju (Algu integrācijas API) | [Iespējot vienkāršotu integrāciju ar personāla algu sniedzējiem](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algu aprēķina integrācijas API](hr-admin-integration-payroll-api-introduction.md)|
|  Atļaut kavējumu pārvaldniekam pārvaldīt atvaļinājumu | [Atļaut kavējumu pārvaldniekam pārvaldīt atvaļinājumu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | [Konfigurēt lomu prombūtnes pārvaldnieks](https://go.microsoft.com/fwlink/?linkid=2168107)|
|  Konfigurēt pielikuma prasības pa atvaļinājuma veidiem | [Konfigurēt pielikuma prasības pa atvaļinājuma veidiem](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Konfigurēt atvaļinājumu un kavējumu veidus](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Konfigurējiet atvaļinājuma vienības katram atvaļinājuma veidam | [Konfigurējiet atvaļinājuma vienības katram atvaļinājuma veidam](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Konfigurēt atvaļinājumu un kavējumu veidus](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Dot iespēju darbiniekus atzīmēt kā gatavus apmaksai | [Dot iespēju darbiniekus atzīmēt kā gatavus apmaksai](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Gatavs apmaksai](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Drīzumā

| Funkcija | Detalizētā informācija |
| --- | --- |
| Platformas atjauninājums 10.0.20 (44) | Ir ieplānots, ka platformas atjaunināšana 10.0.20 sāks izriti ar pakalpojuma laidienu 2021. gada 26. jūlijā. Papildinformāciju skatiet [Platformas atjauninājumi Finance and Operations programmu versijai 10.0.20 (2021. gada augusts)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20). |

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 1. kopumu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Jaunumi un izmaiņas risinājumā Dynamics 365 Human Resources 2021. gada 9. augustā
description: Šajā rakstā aprakstīti līdzekļi, kas ir jauni vai mainīti programmā Microsoft Dynamics 365 Human Resources 2021. gada 9. augustā.
author: marcelbf
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ad1397084dd3eb210065fe6d8c20c5b8253cd206
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882871"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-9-2021"></a>Jaunumi un izmaiņas risinājumā Dynamics 365 Human Resources 2021. gada 9. augustā

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā ierodas programmā Microsoft Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4393.

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varētu atjaunināt šo rakstu, lai ietvertu kļūdu labojumus, kas to izlaboja būvējuma laikā pēc šī raksta sākotnējā publicēšanas.

| Problēmas numurs | Problēma | Apraksts |
| --- | --- | --- |
| 558385 | Noklusējuma adresāts nav atlasīts, ja noklusējuma dizainam ir ieslēgta **Automātiskās atlases** opcija. | Šī problēma tagad ir labota. Vairāki noklusējuma adresāti tiek automātiski atlasīti piemērotos plānos, ja ir ieslēgta **Automātiskās atlases** dizaina opcija lapā **Kopīgotie cilvēkresursu parametri**. |
| 589617 | Lapā **Pārtraukums** bilances **Pieejams pirkšanai** un **Pieejams pārdošanai** ir tukšas, ja piekļuve ir ierobežota noteiktam uzņēmumam. | Šī problēma tagad ir labota. Lapā **Pārtraukums** ir parādītas īstās bilances **Pieejams pirkšanai** un **Pieejams pārdošanai**, ja piekļuve ir ierobežota noteiktam uzņēmumam. |

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
| Platformas atjauninājums 10.0.21 (45) | Ir ieplānots, ka platformas atjaunināšana 10.0.21 sāks izriti ar pakalpojuma laidienu 2021. gada 4. oktobrī. Papildinformāciju skatiet Platformas [atjauninājumos Finanšu un operāciju programmu versijā 10.0.21 (2021. gada oktobris)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 2. kopumu](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

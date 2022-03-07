---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 6. septembrī
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 6. septembri.
author: marcelbf
ms.date: 09/06/2021
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
ms.search.validFrom: 2021-09-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2add53b4b014cb65caacff03bf175078d2b70d8f
ms.sourcegitcommit: a73df4ddc7f8ddc9e37269c0236dc1bb9b7c7966
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485911"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-6-2021"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 6. septembrī

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Microsoft Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4443.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
|---|---|---|
| Atļaut kavējumu pārvaldniekam pārvaldīt atvaļinājumu | [Atļaut kavējumu pārvaldniekam pārvaldīt atvaļinājumu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | Ar šo laidienu mēs atjauninām kavējumu pārvaldnieka darbvietas skatu. Papildinformāciju skatiet sadaļā [Kavējumu pārvaldības lomas konfigurēšana](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Konfigurēt pielikuma prasības pa atvaļinājuma veidiem | [Konfigurēt pielikuma prasības pa atvaļinājuma veidiem](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) | [Konfigurēt atvaļinājumu un kavējumu veidus](https://go.microsoft.com/fwlink/?linkid=2168108) |
| Konfigurējiet atvaļinājuma vienības katram atvaļinājuma veidam | [Konfigurējiet atvaļinājuma vienības katram atvaļinājuma veidam](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) | [Konfigurēt atvaļinājumu un kavējumu veidus](https://go.microsoft.com/fwlink/?linkid=2168215) |

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varētu atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Problēma | Apraksts |
|---|---|---|
| 610128 | Kļūda, publicējot datus, lietojot entitīju HcmDiscussionOverallCommentEntity | Kad dati ir publicēti no Excel darbgrāmatas uz entitīju HcmDiscussionOverallCommentEntity, tiek rādīta šāda kļūda: "Nevar noteikt datu avotu ieraksta ar veidu HcmTopicOverrall atrašanās vietu." |
| 589073 | EEO-1 pārskatā vērtība "Nav konkrēts" un tukšas lauka **Dzimums** vērtības kā vērtību "Sieviete". | Ja laukam **Dzimums** netiek konkretizēts lauks **Vīrietis** EEO-1 pārskats ģenerē noklusējuma vērtību **Sieviete**. |
| 589617 | Pārtraukuma kartītes bilance, un bilances Pieejams pirkšanai un Pieejams pārdošanai neparādās, kad lietotāju lomas tiek ierobežotas līdz konkrētai juridiskai personai. | Ja lietotājs (darbinieka loma) tiek ierobežota līdz konkrētai juridiskai personai, bilances neparādās pareizi kartītē **Pārtraukuma bilances** laukos **Pieejams pirkšanai** un **Pieejams pārdošanai**. |
| 604310 | Prombūtnes pārvaldnieka cilnei vajadzētu būt slēptai, ja lietotājam nav piešķirta prombūtnes hierarhija. | Konkrētajai juridiskajai personai cilni **Prombūtnes pārvaldnieks** vajadzētu slēpt pašapkalpošanas portālā, ja vien nav iespējots starpuzņēmumu parametrs un ar lietotāju nav saistīta vismaz vien prombūtnes hierarhija. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Lai iegūtu papildinformāciju par to, kā ieslēgt priekšskatījuma līdzekļus, skatiet sadaļu [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
|---|---|---|
| Aktivizēt vienkāršoto algu integrāciju (Algu integrācijas API) | [Iespējot vienkāršotu integrāciju ar personāla algu sniedzējiem](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algu aprēķina integrācijas API](hr-admin-integration-payroll-api-introduction.md) |
| Atvieglojumu pārvaldības darbvieta | [Atvieglojumu pārvaldības darbvieta (Priekšskatījums)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Atvieglojumu pārvaldības darbvieta](hr-benefits-management-workspace.md) |
| Dot iespēju darbiniekus atzīmēt kā gatavus apmaksai | [Dot iespēju darbiniekus atzīmēt kā gatavus apmaksai](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Gatavs apmaksai](/dynamics365/human-resources/hr-compensation-payroll) |
| Pielāgotie lauki Piemērotības opcijā |[Pielāgoto lauku atbalsts atbilstības apstrādei](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Pielāgoto lauku izmantošana atbilstības apstrādei](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |

## <a name="coming-soon"></a>Drīzumā

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funkcija | Detalizētā informācija |
|---|---|
| Platformas atjauninājums 10.0.21 (45) | Ir ieplānots, ka platformas atjaunināšana 10.0.21 sāks izriti ar pakalpojuma laidienu 2021. gada 4. oktobrī. Papildinformāciju skatiet [Platformas atjauninājumi Finance and Operations programmu versijai 10.0.21 (2021. gada oktobris)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
| Atvieglojumu pārskats | Atvieglojumu pārskats darbinieka pašreizējo atvieglojumu atlases skatīšanai. Papildu informāciju skatiet Laidiena viļņa dokumenta sadaļā [Atvieglojumu pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement). |

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 2. kopumu](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

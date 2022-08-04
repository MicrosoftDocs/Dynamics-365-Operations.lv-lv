---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2021. gada 20. maijs)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 20. maiju.
author: marcelbf
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 36d490832edcef025cb24a06288eb021eb794bd9
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068490"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2021. gada 20. maijs)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4189.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Platformas atjauninājums 10.0.18 (42) | -- | [Platformas atjauninājumi finanšu un operāciju programmu versijā 10.0.18 (2021. gada maijs)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| Personāla vadības pievienojumprogramma programmai Microsoft Teams tagad atbalsta pusdienas definīcijas un dalītas dienas iespējas | -- | [Atvaļinājumu pieprasījumu pārvaldība programmā Teams](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varam atjaunināt šo rakstu, lai ietvertu kļūdu labojumus, kas to izlaboja būvējuma laikā pēc šī raksta sākotnējā publicēšanas.

| Problēmas numurs | Problēma |  Apraksts |
| --- | --- | --- |
| 583776 | Darbinieku masveida reģistrācija atvaļinājuma plānos rada dublētu ieraksta kļūdu | Šī kļūda ir novērsta ar jaunāko laidienu un masveida atvaļinājuma reģistrācijai vajadzētu tikt sekmīgi apstrādātai. |
| 582263 | Nevar vienlaikus palaist visu darbinieku dzīves notikumu apstrādi | Ja lauks **Darbinieks** dzīves notikuma apstrādei ir atstāts tukšs, visi darbinieki tiks apstrādāti. |
| 558383 | Primārais saņēmējs nav atzīmēts 100%, ja nav atlasīts noklusējuma saņēmējs | Kļūda ir novērsta, tāpēc lietotājam ir jāizvēlas tikai galvenā saņēmēja maiņa.|
| 509404 | Nodaļas darbinieku skaita analīze, kas neietekmē darbinieku kustību starp nodaļām |Ir atjaunināta analīze, lai ietvertu darbinieku pārsūtīšanu starp nodaļām|
| 579420 | Režģu līdzekļa iesaldēšanas kolonnas vēl nav pieejamas | **Iesaldēšanas kolonnas režģu** funkcija, kas nav pieejama Personāla vadībā, tika uzskaitīta kā pieejama Līdzekļu pārvaldībā. Līdzeklis ir noņemts no iespējojamo līdzekļu saraksta. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Pielāgotā lauka atbalsts atvieglojumu pārvaldības atbilstības noteikumos | [Pielāgots lauka atbalsts atbilstības apstrādei](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Atbilstības noteikumu konfigurēšana](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Atvieglojumu pārvaldības darbvieta | [Atvieglojumu pārvaldības darbvieta (Priekšskatījums)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Atvieglojumu pārvaldības darbvieta](hr-benefits-management-workspace.md) |
| Atvaļinājuma un kavējumu darbplūsmas pieredzes uzlabojumi | [Atvaļinājuma un kavējumu darbplūsmas pieredzes uzlabojumi](https://go.microsoft.com/fwlink/?linkid=2147528) | [Pieprasīt brīvo laiku](hr-employee-self-service-request-time-off.md)|
| Aktivizēt vienkāršoto algu integrāciju (Algu integrācijas API) | [Iespējot vienkāršotu integrāciju ar personāla algu sniedzējiem](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algu aprēķina integrācijas API](hr-admin-integration-payroll-api-introduction.md)|
| Atvaļinājuma uzkrājumu darījumu auditēšana | - | [Atvaļinājuma uzkrājumu darījumu auditēšana](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Drīzumā

| Funkcija | Detalizētā informācija |
| --- | --- |
|  Atļaut kavējumu pārvaldniekam pārvaldīt atvaļinājumu | [Atļaut kavējumu pārvaldniekam pārvaldīt atvaļinājumu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 1. kopumu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]


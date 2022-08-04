---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2021. gada 3. maijs)
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 3. maiju.
author: marcelbf
ms.date: 05/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: df8bd0277e4f27c23ba25c886d12f589913e5d46
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066229"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-3-2021"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources (2021. gada 3. maijs)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4140.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Pievienojiet informācijas joslu, kad tiek izveidoti dzīves notikumi. | - | Izveidojot dzīves notikumu, informācijas joslā tiek rādīts ziņojums, kas norāda izveidotā dzīves notikuma tipu.

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varam atjaunināt šo rakstu, lai ietvertu kļūdu labojumus, kas to izlaboja būvējuma laikā pēc šī raksta sākotnējā publicēšanas.

| Problēmas numurs | Problēma |  Apraksts |
| --- | --- | --- |
| 559312 |  Līmenis netiek rādīts, veidojot fiksētas atlīdzības sistēmu darbiniekam. |  Ja starp lietotāja laika joslu un uzņēmuma laika joslu pastāv neatbilstība, atlīdzības līmeni darbam nevar nolasīt. Vaicājums ir atjaunināts, lai ielādētu, pamatojoties uz UTC laiku. |
| 573676  | **Atvieglojumu plāna** formā nevar pievienot jaunu periodu. | Forma ir atjaunināta tā, lai poga **Jauns** ir iespējota kopsavilkuma cilnē **Periods** sadaļā **Atvieglojumu plāni**. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Atvieglojumu pārvaldības darbvieta | [Atvieglojumu pārvaldības darbvieta (Priekšskatījums)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Atvieglojumu pārvaldības darbvieta](hr-benefits-management-workspace.md) |
| Atvaļinājuma un kavējumu darbplūsmas pieredzes uzlabojumi | [Atvaļinājuma un kavējumu darbplūsmas pieredzes uzlabojumi](https://go.microsoft.com/fwlink/?linkid=2147528) | [Pieprasīt brīvo laiku](hr-employee-self-service-request-time-off.md)|
| Aktivizēt vienkāršoto algu integrāciju (Algu integrācijas API) | [Iespējot vienkāršotu integrāciju ar personāla algu sniedzējiem](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Algu aprēķina integrācijas API](hr-admin-integration-payroll-api-introduction.md)|
| Atvaļinājuma uzkrājumu darījumu auditēšana | - | [Atvaļinājuma uzkrājumu darījumu auditēšana](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Drīzumā

| Funkcija | Detalizētā informācija |
| --- | --- |
| Platformas atjauninājums 10.0.18 (42) | Ir ieplānots, ka platformas atjaunināšana 10.0.18 sāks izriti ar pakalpojuma laidienu 2021. gada 17. maijā. Papildinformāciju skatiet platformas [atjauninājumos finanšu un operāciju programmu versijā 10.0.18 (2021. gada maijs)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Pielāgotā lauka atbalsts atvieglojumu pārvaldības atbilstības noteikumos  | [Pielāgots lauka atbalsts atbilstības apstrādei](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 1. kopumu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]


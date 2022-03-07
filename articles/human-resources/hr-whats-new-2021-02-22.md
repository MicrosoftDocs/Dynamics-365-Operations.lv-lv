---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 22. februārī
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 22. februāri.
author: marcelbf
ms.date: 02/22/2021
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
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 379a902489bdccdfa3490a830cc3b0bbf7639e7f0b62079a3ff3a999b0a7c412
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721563"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-22-2021"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 22. februārī

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.3988.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Dynamics 365 Human Resources lietotne programmai Microsoft Teams | [Darbinieka atvaļinājuma un prombūtnes pieredze programmā Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Programma Human Resources programmā Teams](./hr-admin-teams-leave-app.md)<br>[Atvaļinājumu pieprasījumu pārvaldība programmā Teams](hr-teams-leave-app.md) |

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varam atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Izsniegt |  Apraksts |
| --- | --- | --- |
| 529994 | **Darbinieka** formā, modificējot lauku **Zināms kā**, netiek izraisīts Dataverse atjauninājums | Fiksētā problēma, ko Dataverse neatjaunina, ja lauks **Zināms kā** ir atjaunināts **Darbinieka** formā. |
| 532651 | Kompensācijas analīzes PBI pārskatā netiek izmantota valūtas konvertēšana, aprēķinot rādītājus visiem uzņēmumiem | Fiksētā problēma, kur Atlīdzības analīzes PBI pārskats nepareizi konvertē valūtas. |
| 552226 | Dzīves notikumu apstrāde aizver un atkārtoti atver plānus vairākas reizes vienam dzīves notikumam  | Fiksētā problēma, kad darbinieks ir vairākās juridiskajās personām un notiek dzīves notikums, dzīves notikuma ieraksts ģenerē katrai juridiskajai personai, kurā darbinieks ir. Apstrādājot dzīves notikumus, jāatlasa juridiskā persona, kas to apstrādā. Tomēr apstrādes loģika ierobežo sevi šai juridiskajai personai. Tā vietā tas apstrādā visām juridiskajām personām un aizver un atkārtoti atver plānus atlasītajā juridiskajām personām. Šī darbība ir dzīves notikums, lai to vairākas reizes apstrādātu vienā juridiskajā personā, kā rezultātā notiek katra plāna vairākkārtēja atvēršana/aizvēršana, kuru ietekmē dzīves notikums. |
| 518064 | Tikai viena atkarīga no piemērotajiem plāniem, ja vairāki no tiem ir atzīmēti kā noklusējuma adresāti | Fiksētā problēma, kuras dēļ vairāki noklusējuma adresāti nav automātiski atlasīti piemērotos plānos. Tagad varat arī nozīmēt primāro saņēmēju personīgajai kontaktpersonai. Ja pastāv vairāki saņēmēji, primārais saņēmējs tiek uzskaitīts kā 100% piemērotos plānos. |
| 552365 | Uzdāiniet savas datu bāzes (BYOD) eksporta darbus, ja pēc jaunināšanas uz platformas atjauninājumu 40 | Fiksētā problēma, kad BYOD eksportē neizdosies pēc Platformas atjauninājuma 40 lietošanas videi. |
| 547123 | Ierobežot uzdevumu skaitu, uz kuru attiecas vaicājums sarakstā Uzdevumi informācijas panelī | Uzdevumu sarakstā parādīto uzdevumu skaits tagad ir ierobežots līdz 15, lai labotu veiktspējas problēmu, ko rada pārmērīga uzdevumu skaits, kas mēģina ielādēt. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Starpuzņēmumu skats par atvaļinājumu vadītājiem | [Starpuzņēmumu skats par darbinieka atvaļinājumu vadītājiem](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurēt atvaļinājumu un kavējumu parametrus](./hr-leave-and-absence-parameters.md) |
| Atvieglojumu pārvaldības darbvieta | [Atvieglojumu pārvaldības darbvieta (Priekšskatījums)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Atvieglojumu pārvaldības darbvieta](hr-benefits-management-workspace.md) |
| Ierobežot darbiniekus rediģēt uzņēmuma kontaktinformāciju | [Ierobežot darbiniekus rediģēt uzņēmuma kontaktinformāciju](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Ierobežot personiskās informācijas rediģēšanu](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Drīzumā

| Funkcija | Detaļas |
| --- | --- |
| Vadītāja ievadītās prasmes saviem darbiniekiem var automātiski apstiprināt ar darbplūsmu | Drīzumā. |

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminoloģijas atjauninājumi programmai Microsoft Dataverse

2020. gada novembrī Common Data Service ir pārdēvēts par [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Lai uzzinātu vairāk, skatiet [oficiālo paziņojumu](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) emuārā Power Apps. Saistībā ar šo nosaukuma maiņu ir atjaunināta noteikta terminoloģija Dataverse. Piemēram, *elements* tagad ir *tabula* un *lauks* tagad ir *kolonna*. Papildinformāciju skatiet sadaļā [Terminoloģijas atjauninājumi](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Šajā laidienā terminoloģija, kas saistīta ar Dynamics 365 Human Resources integrāciju ar Dataverse, ir atjaunināta visā programmā, lai atspoguļotu šīs izmaiņas. Piemēram, **Common Data Service integrācijas veidlapa** tagad ir **Microsoft Dataverse integrācija**.

Papildinformāciju par Dynamics 365 Human Resources integrāciju ar Microsoft Dataverse, skatiet sadaļā [Konfigurēt Microsoft Dataverse integrāciju](./hr-admin-integration-common-data-service.md) un [Konfigurēt Microsoft Dataverse virtuālās tabulas](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="updates-to-service-deployment"></a>Pakalpojumu izvietošanas atjauninājumi

Sākot ar 2021. gada 22. februāra laidienu, mēs koriģējam mūsu reģionālās pakalpojuma atjauninājumu izvietošanu. Pielāgojumi ietvers secības pagriešanu, kādā globālie reģioni saņem atjauninājumus cilvēkresursu pakalpojumam, un gaidīšanas laika modifikācijas starp atjaunināšanas stadijām. Šo izmaiņu dēļ mēs vēl vairāk lietojam Drošas izvietošanas prakses (SDP), lai uzlabotu pakalpojumu stabilitātes, kvalitātes un atbalsta sistēmu.

Turpināsim sekot divu nedēļu izvietošanas kadencei. Tomēr debitori var paziņojumu par to, ka atjauninājumi parasti tiek pielietoti savām personāla vadības vidēm divu nedēļu cikla dienā nekā iepriekšējos laidienos.

Papildinformāciju par pakalpojumu atjaunināšanas procesu skatiet sadaļā [Atjaunināšanas process](./hr-admin-setup-update-process.md).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 1. kopumu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 8. martā
description: Šajā rakstā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 8. martu.
author: marcelbf
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9280e85f9701573717c4115b4d752ed11be4862e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868073"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-08-2021"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 8. martā

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā rakstā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.4017.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Starpuzņēmumu skats par atvaļinājumu vadītājiem | [Starpuzņēmumu skats par darbinieka atvaļinājumu vadītājiem](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurēt atvaļinājumu un kavējumu parametrus](./hr-leave-and-absence-parameters.md) |

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varam atjaunināt šo rakstu, lai ietvertu kļūdu labojumus, kas to izlaboja būvējuma laikā pēc šī raksta sākotnējā publicēšanas.

| Problēmas numurs | Problēma |  Apraksts |
| --- | --- | --- |
| 486611 | Ja tiek iespējota funkcija **Iespējot atvaļinājumu visos kalendāros**, atvaļinājums tiks atainots atvaļinājumu kalendārā | Ja visos kalendāros ir iespējots **Atspējot atvaļinājumu visos kalendāros**, informācija par atvaļinājumu vairs netiek atainota, ja ir iespējota funkcija Atvaļinājumu un kavējumu kalendāra uzlabojumi.|
| 508972 | Atvaļinājuma un kavējumu bankas darbības entītijai trūkst reģistrācijas apstiprinājuma | Izmantojot entītiju Atvaļinājuma un Kavējuma bankas darbība, sistēmā reģistrētos darbiniekus vairs nevar importēt. |
| 554854 | Atjaunina nodarbinātības entītijas kļūdu kalendāru, ja noklusējuma juridiskā persona lietotāja opcijās atšķiras | Nodarbinātības personas lietošana, lai atjauninātu kalendāru darbiniekam, vairs nesniedz kļūdu, ja noklusējuma juridiskā persona Lietotāja opcijās atšķiras. |
| 558347 | "Nevar izveidot ierakstu formas konfigurācijās (FormRunConfiguration)", ielādējot sākuma lapu. | "Nevar izveidot ierakstu formas konfigurācijās (FormRunConfiguration)", ielādējot sākuma lapu. |
| 557327 | Atvieglojumu pārvaldības darbvieta: virs režģa tiek parādīta atstarpe. | Fiksēto lietotāju pieredzes problēma saistībā ar neparedzētu atšķirību, kas parādās darbvietas Atvieglojumi tabulas režģa robežās. |
| 557334 | Atvieglojumu pārvaldības darbvieta: atlases nolaižamajā lodziņā **Periods** ir jābūt redzamai tikai cilnē **Kopsavilkums** | Atvieglojumu **Perioda** atlases nolaižamais saraksts tagad tiek parādīts tikai tad, ja cilne **Kopsavilkums** ir aktīva Atvieglojumu darbvietā, nevis sadaļās **Procesa rezultāti** un **Saites**. |
| 557336 | Atvieglojumu pārvaldības darbvieta: **Atvērt reģistrāciju ar izņemtiem plāniem** teksts ir apcirsts elementa skatā | Elementa skatā mainīts teksts uz **Izņemtie plāni... atveriet reģistrāciju**, lai izvairītos no nepieciešamā konteksta apciršanas. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Atvieglojumu pārvaldības darbvieta | [Atvieglojumu pārvaldības darbvieta (Priekšskatījums)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Atvieglojumu pārvaldības darbvieta](hr-benefits-management-workspace.md) |
| Ierobežot darbiniekus rediģēt uzņēmuma kontaktinformāciju | [Ierobežot darbiniekus rediģēt uzņēmuma kontaktinformāciju](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Ierobežot personiskās informācijas rediģēšanu](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Drīzumā

| Funkcija | Detaļas |
| --- | --- |
| Vadītāja ievadītās prasmes saviem darbiniekiem var automātiski apstiprināt ar darbplūsmu | Drīzumā. |

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 1. kopumu](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
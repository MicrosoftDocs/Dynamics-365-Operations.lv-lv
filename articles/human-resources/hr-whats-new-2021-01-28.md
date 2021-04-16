---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 28. janvāris
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 28. janvāri.
author: marcelbf
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 36509cc5663073fd1e3b7f41a600c7816bfbdff6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791249"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 28. janvāris

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.3906.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Integrēt atvieglojumu iemeslu kodus **Personāla pārvaldības** darbvietā | -- | [Iestatiet cēloņa kodus](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varam atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.


| Problēmas numurs | Izsniegt |  Apraksts |
| --- | --- | --- |
| 539456 | Kalendārs rāda atvaļinājuma veidu peles kursora tekstā, ja ir iespējots parametrs **Rādīt tikai prombūtni bez detalizētas informācijas**. | Ja opcija **Rādīt tikai prombūtni bez detalizētas informācijas** ir iespējota, pieprasījuma datums tiek parādīts peles kursora tekstā. |
| 528907 | Piešķirot piekļuvi juridiskajai personai par darbinieku lomu, vadītāji nevar redzēt atvaļinājumu bilances aktivitāti darbiniekiem Darbinieku pašapkalpošanās sadaļas apgabalā **Mana grupa**. |Šīs opcijas iestatīšana tagad ļauj vadītājiem turpināt skatīt atvaļinājuma bilances aktivitāti. |
| 526280 | Atļauju kļūda hcmWorkerEntity, HcmEmployeeEntity un HcmContractorEntity. | Lietotāji, kuriem bija loma, kas nav sistēmas administratora loma, nevarēja eksportēt sarakstā uzskaitītos elementus, jo laukā NationalityCountryRegion radās atļauju kļūda. Lietotājiem būs nepieciešamas tālāk minētās privilēģijas, lai eksportētu šo informāciju: HcmWorkerEntityMaintain, HcmWorkerEntityView, HcmEmployeeEntityMaintain, HcmEmployeeEntityMaintain, HcmEmployeeEntityView, HcmContractorEntityMaintain un HCMContractorEntityView. |
| 542147 | Lauki **Bankas konta numurs** un **Maršrutēšanas numurs** ir obligāti, pievienojot bankas kontu Darbinieku pašapkalpošanās sadaļā. | Tika novērsta kļūda, kad darbiniekiem tika prasīts ievadīt laukus **Bankas konta numurs** un **Maršrutēšanas numurs**, pievienojot bankas konta informāciju. Šie lauki vairs nav obligāti, saglabājot jaunu bankas konta informāciju. |
| 543641 | Pasta indekss netiek aizpildīts elektroniskajos pārskatos. | Novērsta kļūda, kur pasta indekss netika ievadīts ACA pārskatā seguma kodiem L, izmantojot Q. |
| 545402 | Lai noņemtu 404 kļūdas, pievienojiet maršrutēšanas izmaiņas failam UserBranding.js. | Lietotājs konsolē vairs neredzēs 404 kļūdas. |

## <a name="in-preview"></a>Priekšskatījumā   

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Programma Human Resources programmā Microsoft Teams | [Darbinieka atvaļinājuma un prombūtnes pieredze programmā Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Programma Human Resources programmā Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Atvaļinājumu pieprasījumu pārvaldība programmā Teams](hr-teams-leave-app.md) |
| Starpuzņēmumu skats par atvaļinājumu vadītājiem | [Starpuzņēmumu skats par darbinieka atvaļinājumu vadītājiem](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurēt atvaļinājumu un kavējumu parametrus](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |

## <a name="coming-soon"></a>Drīzumā

| Funkcija | Detaļas |
| --- | --- |
| E-pasta apstiprināšana atvieglojumu reģistrācijai | Šis līdzeklis nodrošina opciju darbiniekiem nosūtīt apstiprinājuma e-pastu, kad viņi iepazīsies ar atvieglojumu reģistrācijas pieredzi Darbinieku pašapkalpošanās sadaļā. Šī funkcija būs pieejama 1. februārī. Papildinformāciju skatiet sadaļā [Atvieglojumu pārvaldības parametru konfigurēšana katram uzņēmumam](hr-benefits-setup-parameters-per-company.md). |
| Vadītāja ievadītās prasmes saviem darbiniekiem var automātiski apstiprināt ar darbplūsmu | Drīzumā. |

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2021 laidiena 1. kopuma pārskats](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminoloģijas atjauninājumi programmai Microsoft Dataverse

2020. gada novembrī Common Data Service ir pārdēvēts par [Microsoft Dataverse](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro). Lai uzzinātu vairāk, skatiet [oficiālo paziņojumu](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) emuārā Power Apps. Saistībā ar šo nosaukuma maiņu ir atjaunināta noteikta terminoloģija Dataverse. Piemēram, *elements* tagad ir *tabula* un *lauks* tagad ir *kolonna*. Papildinformāciju skatiet sadaļā [Terminoloģijas atjauninājumi](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Šajā laidienā terminoloģija, kas saistīta ar Dynamics 365 Human Resources integrāciju ar Dataverse, ir atjaunināta visā programmā, lai atspoguļotu šīs izmaiņas. Piemēram, **Common Data Service integrācijas veidlapa** tagad ir **Microsoft Dataverse integrācija**.

Papildinformāciju par Dynamics 365 Human Resources integrāciju ar Microsoft Dataverse, skatiet sadaļā [Konfigurēt Microsoft Dataverse integrāciju](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service) un [Konfigurēt Microsoft Dataverse virtuālās tabulas](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2021. gada laidiena 1. kopumu](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
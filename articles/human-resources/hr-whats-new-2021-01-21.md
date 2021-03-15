---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 21. janvāris
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2021. gada 21. janvāri.
author: marcelbf
manager: tfehr
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: af847ed36187c0d0629ce4063d9c17cb0fa8cfcf
ms.sourcegitcommit: 630a0b3f800f36ced49b79156dd52132904fef75
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/25/2021
ms.locfileid: "5060846"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2021. gada 21. janvāris

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Dynamics 365 Human Resources 2020 laidiena 2. kopuma pārskats](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.3866.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Platformas atjauninājums 10.0.16(40) | -- | [Platformas atjauninājumi programmu Finance and Operations versijai 10.0.16 (2021. gada februāris)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16) |
| Uzlaboti darbplūsmas pieprasījumi un apstiprinājumi | [Organizācijas un personāla vadības darbplūsmas pieredzes uzlabojumi](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurācijas opcija, lai novietotu sarakstu Man piešķirtie darba elementi](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Pieejamās aprūpes akta (ACA) saskaņotības atjauninājumi formai 1095-C, formai 1095-B un elektroniskie pārskati mantojuma atvieglojumos | -- | -- | 
| Atvieglojumu pārvaldība tagad atbalsta ACA saskaņotības pārskatus ASV juridiskajām personām | -- | [Ģenerēt ACA pārskatus Atvieglojumu pārvaldībā](hr-benefits-management-aca-reports.md) |
| Atvieglojumu pārvaldībā tagad tiek rādītas atvieglojumu likmes pakāpes un atvieglojumu likmes dubultu pakāpju elementi  | -- | -- |

### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varam atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Izsniegt |  Apraksts |
| --- | --- | --- |
| 533079 | Navigācijas kļūda "Forma tika izsaukta nepareizi", kad mēģinām skatīt ieturējumus. | Novērsta kļūda, meklējot atvieglojumu ieturējumus ar skatu **No datuma**. |
| 543641 | Pasta indekss netiek aizpildīts elektroniskajos pārskatos.  | Novērsta iekšēja kļūdu pasta indeksā, kas neparādās ACA elektroniskajā pārskatos Atvieglojumu pārvaldībai, ja seguma kods ir M līdz Q. |
| 542815 | Darbinieku pašapkalpošanās personu kontaktpersonu ekrāns ļauj darbiniekiem skatīt citu personu kontaktpersonas. | Novērsta kļūda, kur veidlapa **Rediģēt** Darbinieku patstāvīgi izmantojamajām personas kontaktpersonām pietiekami neierobežo tās vaicājumu, lai garantētu, ka tiek izgūta tikai viena kontaktpersona, ļaujot lietotājam izmantot īsinājumtaustiņus citu personu kontaktpersonu skatīšanai. |
| 536157 | Nevar atvērt lapu **Microsoft Dataverse integrācija** Sistēmas administrēšanā IsVirtualEntityPackageInstalled() izsaukuma dēļ. | Problēma neļauj **Microsoft Dataverse integrācijas** lapu ielādēt Human Resources. |
| 533079 | Navigācijas kļūda "Forma tika izsaukta nepareizi", kad mēģinām skatīt ieturējumus. | Novērsta kļūda, kas radās Atvieglojumu pārvaldības veidlapā **Ieturējumi**, ja tā tiek skatīta **No datuma**. |
| 537264 | Kandidāta ierakstā trūkst kopsavilkuma cilnes **Personas informācija**. | Tagad kandidāta personas informācija ir pieejama kandidāta ierakstā. |
| 537267 | **Profesionālā pieredze** nerāda iekšējos kandidātu ierakstos. | Tagad kopsavilkuma cilne **Profesionālā pieredze** rāda iekšējos kandidātu ierakstos. Iepriekš, ja kandidāts bija iekšējs, **Profesionālā pieredze** tika aizstāta ar **Nodarbinātības vēsturi**, kas ir kandidāta nodarbinātības vēsture organizācijā. Abas ir piemērojamas un jāparāda iekšējiem kandidātiem. |
| 537067 | Netiek parādīts **Atļauts sazināties ar darba devēju**. | Vadīkla **Atļauts sazināties ar darba devēju** tika pievienota kandidāta ieraksta rūtij **Rediģēt profesionālo pieredzi**. |
| 525957 | **Kandidāta statuss** neatjaunina iekšējos kandidātus, kad pārsūtīšana ir pabeigta. | Kad pārsūtīšana ir pabeigta (poga **Mainīt amatu** vai **Turpināt** ir atlasīta lapā **Pārcelt darbinieku uz jaunu amata piešķīrumu**), **Statusam** kandidāta ierakstā ir jāmainās uz **Pieņemts**. |
| 537051 | Indijas rūpijas un Turcijas liras valūtas simboli nav pareizi sinhronizēti Dataverse | Tagad Indijas rūpijas un Turcijas liras simboli ir pareizi sinhronizēti Dataverse. |
| 534846 | Darbinieku darbā pieņemšanas tabulām jābūt iespējotām Datu pārvaldībai. | Jaunās tabulas, kas izveidotas darbinieku pieņemšanas pieprasījumiem un kandidātiem, tagad ir iespējotas Datu pārvaldībai. Tas ļauj iespējot izmaiņu izsekošanu tabulām, iespējojot OData izmaiņu izsekošanu X Dataverse virtuālajās tabulās. |
| 533474 | Labo trūkstošo atsauci uz Microsoft.SqlServer.XEvent.dll. | Montāžas ielādes izņēmumi Microsoft.SqlServer.XEvent.dll bloķēja Dataverse virtuālo tabulu iestatīšanu dažās vidēs. |
| 481122 | **Personas** darbalauks, kurā tiek rādīti noņemtie amati. | Noņemtie amati tika rādīti kā atvērti amati darbvietā **Personas**. Noņemtie amati vairs netiek rādīti. | 
| 541978 | Pievienojiet primāro e-pasta adresi BaseWorker elementam. | Šīs izmaiņas dēļ darbinieka primārā e-pasta adrese tika pievienota hcmWorkerBaseEntity. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Programma Human Resources programmā Microsoft Teams | [Darbinieka atvaļinājuma un prombūtnes pieredze programmā Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Programma Human Resources programmā Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Atvaļinājumu pieprasījumu pārvaldība programmā Teams](hr-teams-leave-app.md) |
| Integrācija ar LinkedIn Talent Hub | [Integrācija ar LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integrācija ar LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
| Starpuzņēmumu skats par atvaļinājumu vadītājiem | [Starpuzņēmumu skats par darbinieka atvaļinājumu vadītājiem](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurēt atvaļinājumu un kavējumu parametrus](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
|Papildu ieskats atvaļinājumu atlikumos nodrošināšana| [Papildu ieskats atvaļinājumu atlikumos nodrošināšana](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Darbinieka atvaļinājuma pārvaldība](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-employee-leave) |
| Vadītāji, kas var iesniegt kandidātu atlases pieprasījumus amatiem | [Vadītāji, kas var iesniegt kandidātu atlases pieprasījumu atvērtajiem amatiem](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Pievienot personāla atlases pieprasījumu](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Uzlabotais kandidātu profils Personāla pārvaldībā | [Uzlabotais kandidātu profils personāla pārvaldībā](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Pievienot vai rediģēt kandidāta profilu](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Iespējot vienkāršotu integrāciju ar personāla atlases sniedzējiem | [Iespējot vienkāršotu integrāciju ar personāla atlases sniedzējiem](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Kandidātu pieņemšana darbā](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |

## <a name="coming-soon"></a>Drīzumā
| Funkcija | Detaļas |
| --- | --- |
| E-pasta apstiprināšana atvieglojumu reģistrācijai | Šis līdzeklis nodrošina opciju darbiniekiem nosūtīt apstiprinājuma e-pastu, kad viņi iepazīsies ar atvieglojumu reģistrācijas pieredzi Darbinieku pašapkalpošanās sadaļā. Papildinformāciju skatiet sadaļā [Atvieglojumu pārvaldības parametru konfigurēšana katram uzņēmumam](hr-benefits-setup-parameters-per-company.md). |
| Vadītāja ievadītās prasmes saviem darbiniekiem var automātiski apstiprināt ar darbplūsmu | Drīzumā. |

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Dynamics 365 Human Resources 2020 laidiena 2. kopuma pārskats](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Terminoloģijas atjauninājumi programmai Microsoft Dataverse

2020. gada novembrī  Common Data Service ir pārdēvēts par [Microsoft Dataverse](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro). Lai uzzinātu vairāk, skatiet [oficiālo paziņojumu](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/)  Power Apps emuārā. Saistībā ar šo nosaukuma maiņu ir atjaunināta noteikta terminoloģija Dataverse. Piemēram, *elements* tagad ir *tabula* un *lauks* tagad ir *kolonna*. Papildinformāciju skatiet sadaļā [Terminoloģijas atjauninājumi](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

Šajā laidienā terminoloģija, kas saistīta ar Dynamics 365 Human Resources integrāciju ar Dataverse, ir atjaunināta visā programmā, lai atspoguļotu šīs izmaiņas. Piemēram, **Common Data Service integrācijas veidlapa**  tagad ir **Microsoft Dataverse integrācija**.

Papildinformāciju par Dynamics 365 Human Resources integrāciju ar Microsoft Dataverse, skatiet sadaļā [Konfigurēt Microsoft Dataverse integrāciju](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service) un [Konfigurēt Microsoft Dataverse virtuālās tabulas](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2020. gada laidiena 2. kopumu](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
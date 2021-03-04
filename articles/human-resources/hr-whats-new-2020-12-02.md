---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2020. gada 2. decembris
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 2. decembri.
author: marcelbf
manager: tfehr
ms.date: 12/02/2020
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
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aba35563266d1149131124f489f89da61432bfb2
ms.sourcegitcommit: 0354ca7e566fbd2eb0aabdd40000d4ac5c44ea78
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/04/2020
ms.locfileid: "4669178"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2020. gada 2. decembris

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Dynamics 365 Human Resources 2020 laidiena 2. kopuma pārskats](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.3788.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Vadītāji, kas var iesniegt kandidātu atlases pieprasījumus amatiem | [Vadītāji, kas var iesniegt kandidātu atlases pieprasījumu atvērtajiem amatiem](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Pievienot personāla atlases pieprasījumu](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Uzlabotais kandidātu profils Personāla pārvaldībā | [Uzlabotais kandidātu profils personāla pārvaldībā](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Pievienot vai rediģēt kandidāta profilu](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Iespējot vienkāršotu integrāciju ar personāla atlases sniedzējiem | [Iespējot vienkāršotu integrāciju ar personāla atlases sniedzējiem](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Personāla atlases kandidāti](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |
| Vadītāja pašapkalpošanās pielāgotās saites | [Vadītāja pašapkalpošanās pielāgotās saites](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Vadītāja pašapkalpošanās pielāgotās saites](https://aka.ms/MSSCustomLinks) |


### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varam atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Izsniegt | Apraksts |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult jāiekļauj datu apstrādei izmantotais datums un laiks. | BenefitEligibity apstrādes rezultāts tagad ietver pēdējās apstrādes datetimestamp, kuras trūka agrāk. |
| 526903 | Atvieglojumu reģistrācija nenotiek plāniem, kuri ietver apgādājamos, kad opcija **Automātiski izraudzītie pārstāvji** ir ieslēgta **Personāla vadības kopīgotos parametros**. | Novērsta problēma, kad apgādājamajiem neizdevās reģistrēt pabalstus, kad noklusējuma saņēmējiem bija ieslēgta opcija **Automātiski izraudzītie pārstāvji**. |
| 521922 | Parametrs **Rādīt prombūtni bez detalizētas informācijas** rāda detalizētu informāciju par pārtraukuma pieprasījumiem grupas kavējuma kalendārā. | Atvaļinājuma tips, atvaļinājuma tipa krāsa un dienas detaļas tika rādītas grupas kavējuma kalendārā, kad opcija **Rādīt prombūtni bez detalizētas informācijas** tika iestatīta uz **Jā** sadaļā **Atvaļinājumu un prombūtnes parametros**. Tas ir ziņots, un tagad atvaļinājuma veids netiek rādīts un noklusējuma atvaļinājuma tipa krāsa (tumši zilā krāsā) tiek izmantota visiem atvaļinājumu tipiem grupas kavējumu kalendārā. |
| 527316 | Darba, amata un darbinieka paziņojumu nosaukumu izmaiņas netiek sinhronizētas. | Nosaukumu relācija iepriekš tika pievienota Darba, Amata un Darbinieku vienībām. Šīs relācijas sinhronizācija darbojas no Personāla vadības sinhronizācijas uz Common Data Service, bet nedarbojās ar paziņojumiem no Common Data Service. Tas ir noziņots. |
| 512275 | Noņemiet krāsu opcijas no **Atvaļinājuma un prombūtnes parametriem**. | Tagad, kad ir definētas atvaļinājumu tipa krāsas, vairs nav nepieciešamas krāsu opcijas **Atvaļinājumu un prombūtnes parametros**, tāpēc tās tika noņemtas. |
| 437112 | Maldinošs kļūdas ziņojuma teksts darbinieka amata piešķires laikā. | Atjaunināja kļūdas ziņojumu, pieņemot darbā darbinieku un mēģinot piešķirt darbinieku amatam, kas nav aktīvs. Atjaunināts ziņojums **Norādītā pozīcija nav aktīva nodarbinātības sākuma datumā. Lūdzu, pārbaudiet šīs pozīcijas ilgumu.** |
| 527816 | Veiktspējas problēmas ar **Pārtraukuma** lapu. | Ir uzlabojusies veiktspēja lapā **Pārtraukums**. |
| 523158 | BenefitPeriodMigrationUpgrade un BenefitPlanMigrationUpgrade netiek veikti. | Novērstas problēmas ar pabalstu migrācijas darbiem, kas saistīti ar nepareizi veiktu **Periodu** un **Plānu**. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Programma Human Resources programmā Microsoft Teams | [Darbinieka atvaļinājuma un prombūtnes pieredze programmā Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Programma Human Resources programmā Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Atvaļinājumu pieprasījumu pārvaldība programmā Teams](hr-teams-leave-app.md) |
| Uzlaboti darbplūsmas pieprasījumi un apstiprinājumi | [Organizācijas un personāla vadības darbplūsmas pieredzes uzlabojumi](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurācijas opcija, lai novietotu sarakstu Man piešķirtie darba elementi](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Integrācija ar LinkedIn Talent Hub | [Integrācija ar LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integrācija ar LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
|Starpuzņēmumu skats par atvaļinājumu vadītājiem | [Starpuzņēmumu skats par darbinieka atvaļinājumu vadītājiem](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurēt atvaļinājumu un kavējumu parametrus](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
|Papildu ieskats atvaļinājumu atlikumos nodrošināšana| [Papildu ieskats atvaļinājumu atlikumos nodrošināšana](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Darbinieka atvaļinājuma pārvaldība](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-employee-leave) |
| Vadītāji, kas var iesniegt kandidātu atlases pieprasījumus amatiem | [Vadītāji, kas var iesniegt kandidātu atlases pieprasījumu atvērtajiem amatiem](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Pievienot personāla atlases pieprasījumu](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Uzlabotais kandidātu profils Personāla pārvaldībā | [Uzlabotais kandidātu profils personāla pārvaldībā](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Pievienot vai rediģēt kandidāta profilu](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Iespējot vienkāršotu integrāciju ar personāla atlases sniedzējiem | [Iespējot vienkāršotu integrāciju ar personāla atlases sniedzējiem](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Personāla atlases kandidāti](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |

## <a name="coming-soon"></a>Drīzumā

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Dynamics 365 Human Resources 2020 laidiena 2. kopuma pārskats](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2020. gada laidiena 2. kopumu](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2020. gada 2. decembris
description: Šajā tēmā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Human Resources uz 2020. gada 2. decembri.
author: marcelbf
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6e02586ad3e6b4428f2ba826851db6ebc3172bdf1760b483032f5159e7864a81
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782663"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Jaunumi un izmaiņas programmā Dynamics 365 Human Resources 2020. gada 2. decembris

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir jauni, mainīti vai drīzumā gaidāmi programmā Dynamics 365 Human Resources.

Papildinformāciju par mūsu atjaunināšanas procesu un grafiku skatiet sadaļā [Atjaunināšanas process](hr-admin-setup-update-process.md).

Papildinformāciju par jaunajiem līdzekļiem un to paredzētajiem vispārējās pieejamības datumiem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2020 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>Šajā laidienā

Šajā laidienā ietilpst tālāk minētie jaunie līdzekļi un kļūdu labojumi. Izmaiņas attiecas uz būvējuma numuru 8.1.3788.

### <a name="new-features"></a>Jauni līdzekļi

Zemāk minētie līdzekļi parasti ir pieejami ar šo laidienu.

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Vadītāji, kas var iesniegt kandidātu atlases pieprasījumus amatiem | [Vadītāji, kas var iesniegt kandidātu atlases pieprasījumu atvērtajiem amatiem](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Pievienot personāla atlases pieprasījumu](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Uzlabotais kandidātu profils Personāla pārvaldībā | [Uzlabotais kandidātu profils personāla pārvaldībā](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Pievienot vai rediģēt kandidāta profilu](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Iespējot vienkāršotu integrāciju ar personāla atlases sniedzējiem | [Iespējot vienkāršotu integrāciju ar personāla atlases sniedzējiem](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Personāla atlases kandidāti](./hr-personnel-recruit.md) |
| Vadītāja pašapkalpošanās pielāgotās saites | [Vadītāja pašapkalpošanās pielāgotās saites](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Vadītāja pašapkalpošanās pielāgotās saites](./hr-employee-manager-self-service-custom-links.md) |


### <a name="bug-fixes"></a>Kļūdu labojumi

Šajā laidienā ir iekļauti tālāk minētie kļūdu labojumi.

> [!NOTE]
> Mūsu mērķis ir nodot jums šo informāciju pēc iespējas ātrāk. Mēs varam atjaunināt šo tēmu, lai iekļautu kļūdu labojumus, kas padarīja to par būvējumu pēc šīs tēmas sākotnējās publicēšanas.

| Problēmas numurs | Izsniegt | Apraksts |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult jāiekļauj datu apstrādei izmantotais datums un laiks. | BenefitEligibity apstrādes rezultāts tagad ietver pēdējās apstrādes datetimestamp, kuras trūka agrāk. |
| 526903 | Atvieglojumu reģistrācija nenotiek plāniem, kuri ietver apgādājamos, kad opcija **Automātiski izraudzītie pārstāvji** ir ieslēgta **Personāla vadības kopīgotos parametros**. | Novērsta problēma, kad apgādājamajiem neizdevās reģistrēt pabalstus, kad noklusējuma saņēmējiem bija ieslēgta opcija **Automātiski izraudzītie pārstāvji**. |
| 521922 | Parametrs **Rādīt prombūtni bez detalizētas informācijas** rāda detalizētu informāciju par pārtraukuma pieprasījumiem grupas kavējuma kalendārā. | Atvaļinājuma tips, atvaļinājuma tipa krāsa un dienas detaļas tika rādītas grupas kavējuma kalendārā, kad opcija **Rādīt prombūtni bez detalizētas informācijas** tika iestatīta uz **Jā** sadaļā **Atvaļinājumu un prombūtnes parametros**. Tas ir ziņots, un tagad atvaļinājuma veids netiek rādīts un noklusējuma atvaļinājuma tipa krāsa (tumši zilā krāsā) tiek izmantota visiem atvaļinājumu tipiem grupas kavējumu kalendārā. |
| 527316 | Darba, amata un darbinieka paziņojumu nosaukumu izmaiņas netiek sinhronizētas. | Nosaukumu relācija iepriekš tika pievienota Darba, Amata un Darbinieku vienībām. Šīs relācijas sinhronizācija darbojas no Personāla vadības sinhronizācijas uz Dataverse, bet nedarbojās ar paziņojumiem no Dataverse. Tas ir noziņots. |
| 512275 | Noņemiet krāsu opcijas no **Atvaļinājuma un prombūtnes parametriem**. | Tagad, kad ir definētas atvaļinājumu tipa krāsas, vairs nav nepieciešamas krāsu opcijas **Atvaļinājumu un prombūtnes parametros**, tāpēc tās tika noņemtas. |
| 437112 | Maldinošs kļūdas ziņojuma teksts darbinieka amata piešķires laikā. | Atjaunināja kļūdas ziņojumu, pieņemot darbā darbinieku un mēģinot piešķirt darbinieku amatam, kas nav aktīvs. Atjaunināts ziņojums **Norādītā pozīcija nav aktīva nodarbinātības sākuma datumā. Lūdzu, pārbaudiet šīs pozīcijas ilgumu.** |
| 527816 | Veiktspējas problēmas ar **Pārtraukuma** lapu. | Ir uzlabojusies veiktspēja lapā **Pārtraukums**. |
| 523158 | BenefitPeriodMigrationUpgrade un BenefitPlanMigrationUpgrade netiek veikti. | Novērstas problēmas ar pabalstu migrācijas darbiem, kas saistīti ar nepareizi veiktu **Periodu** un **Plānu**. |

## <a name="in-preview"></a>Priekšskatījumā

Tālāk norādītie jaunie līdzekļi ir priekšskatījumā. Papildinformāciju par līdzekļu ieslēgšanu vai izslēgšanu skatiet sadaļā [Līdzekļu pārvaldība](hr-admin-manage-features.md).

| Funkcija | Nodošanas izpildei plāns | Dokumentācija |
| --- | --- | --- |
| Programma Human Resources programmā Microsoft Teams | [Darbinieka atvaļinājuma un prombūtnes pieredze programmā Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Programma Human Resources programmā Teams](./hr-admin-teams-leave-app.md)<br>[Atvaļinājumu pieprasījumu pārvaldība programmā Teams](hr-teams-leave-app.md) |
| Uzlaboti darbplūsmas pieprasījumi un apstiprinājumi | [Organizācijas un personāla vadības darbplūsmas pieredzes uzlabojumi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurācijas opcija, lai novietotu sarakstu Man piešķirtie darba elementi](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Integrācija ar LinkedIn Talent Hub | [Integrācija ar LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integrācija ar LinkedIn Talent Hub](./hr-admin-integration-linkedin.md) |
|Starpuzņēmumu skats par atvaļinājumu vadītājiem | [Starpuzņēmumu skats par darbinieka atvaļinājumu vadītājiem](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurēt atvaļinājumu un kavējumu parametrus](./hr-leave-and-absence-parameters.md) |
|Papildu ieskats atvaļinājumu atlikumos nodrošināšana| [Papildu ieskats atvaļinājumu atlikumos nodrošināšana](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Darbinieka atvaļinājuma pārvaldība](./hr-leave-and-absence-manage-employee-leave.md) |
| Vadītāji, kas var iesniegt kandidātu atlases pieprasījumus amatiem | [Vadītāji, kas var iesniegt kandidātu atlases pieprasījumu atvērtajiem amatiem](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Pievienot personāla atlases pieprasījumu](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Uzlabotais kandidātu profils Personāla pārvaldībā | [Uzlabotais kandidātu profils personāla pārvaldībā](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Pievienot vai rediģēt kandidāta profilu](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Iespējot vienkāršotu integrāciju ar personāla atlases sniedzējiem | [Iespējot vienkāršotu integrāciju ar personāla atlases sniedzējiem](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Personāla atlases kandidāti](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Drīzumā

Pilnīgu sarakstu ar plānotajiem līdzekļiem un to ieplānotajiem laidieniem skatiet sadaļā [Pakalpojuma Dynamics 365 Human Resources 2020 laidiena 2. kopuma pārskats](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Skatiet arī

[Jaunumi un izmaiņas programmā Human Resources](hr-admin-whats-new.md)</br>
[Pārskats par Dynamics 365 Human Resources 2020. gada laidiena 2. kopumu](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Procesa atjaunināšana](hr-admin-setup-update-process.md)</br>
[Līdzekļu pārvaldība](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
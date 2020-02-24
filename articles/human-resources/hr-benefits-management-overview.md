---
title: Atvieglojumu pārvaldības pārskats
description: Pārskats par atvieglojumu pārvaldības priekšskatījuma līdzekli Dynamics 365 Human Resources. Piedāvājiet saviem darbiniekiem paplašinātas atvieglojumu opcijas ar ērti lietojamu tiešsaistes pieredzi.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029467"
---
# <a name="benefits-management-overview"></a>Atvieglojumu pārvaldības pārskats

[!include [banner](includes/preview-feature.md)]

Lai saglabātu konkurētspēju, jāpiedāvā bagātīgs atvieglojumu kopums, lai piesaistītu un saglabātu labākos darbiniekus. Papildus standarta atvieglojumiem, piemēram, ārstniecības un zobārstniecības apdrošināšanai, varat arī piedāvāt tādus paplašinātos pakalpojumus kā palīdzība ar adopciju, atpūtas programmas un pabalsts apģērbam. Microsoft Dynamics 365 Human Resources atvieglojumu pārvaldības priekšskatījuma līdzeklis nodrošina elastīgu risinājumu, kas atbalsta plaša spektra atvieglojumu opcijas. Human Resources ietver arī ērti lietojamu darbinieku pieredzi, kas demonstrē jūsu piedāvājumus.

- Uzlabotie atvieglojumu plāni ļauj izveidot un pārvaldīt unikālus atvieglojumu plānus, kā arī atbalstīt kompleksas atvieglojumu apjoma tabulas un ligzdotos līmeņus. Ērtākai darbinieku pieredzei varat viegli izveidot atvieglojumu programmas, komplektus un automātiskas reģistrācijas kārtulas.

- Brīvā režīma kredīta programmas ļauj jums proporcionāli atbalstīt pensionēšanos un citus dzīves notikumus.

- Plašie piemērotības kārtulas nodrošina vajadzīgā atvieglojuma pieejamību attiecīgajiem darbiniekiem.

- Tiešsaistes atvieglojumu reģistrācija sniedz darbiniekiem ērtu pieredzi.

- Kvalificēta dzīves notikumu apstrāde integrējas darbinieku patstāvīgi izmantojamā pakalpojumā un atbalsta arī turpmākos dzīves notikumus.

Ja vēlaties piekļūt demonstrācijas datiem, būs nepieciešams atkārtoti izvietot savu smilškastes vidi.

Varat sniegt tiešas atsauksmes vai pārskatu par problēmām, rakstot uz: D365BenefitsPreview@microsoft.com.

## <a name="benefits-management-known-issues"></a>Zināmās atvieglojumu pārvaldības problēmas

### <a name="eligibility-processing"></a>Apstrādes piemērotība

Apstrādājot piemērotību atvieglojumiem, kas izmanto 1-5X algu, % no algas un fiksētās summas seguma summu, sadaļā **Nodarbinātības vēsture** datums **Detalizēta informācija par atvieglojumu** jāiestata uz **Nodarbināšanas sākuma datums**. Tāpat jāiekļauj **Nostrādātās stundas**, **Maksājumu biežums** un **Gada atvieglojumu algas summa**. Ja nodarbinātajam noteikta fiksēta atlīdzība, ievadiet **Nostrādātās stundas** un **Maksājumu biežums**. Tiks aprēķināta gada algas summa. Ja darbinieks ir algots, nav nepieciešamas ievadīt **Nostrādātas stundas**. Mēs iesakām, veidojot jaunus nodarbinātos, vispirms ievadīt fiksēto atlīdzību. Lai atjauninātu atvieglojumu detalizētas informācijas ierakstu, pārejiet uz **Nodarbinātais > Nodarbinātā vēsture > Detalizēta informācija par nodarbinātību**. Pielāgojiet datumu nodarbinātā pieņemšanas datumam.

### <a name="employee-self-service"></a>Darbinieku patstāvīgi izmantojamais pakalpojums

Darbinieka summa netiek aprēķināta, kad tiek atjaunināta seguma summa dzīvības apdrošināšanai. Piemēram, ja darbiniekam tiek piedāvāts dzīvības apdrošināšanas plāns, tas var atlasīt līdz $ 50 000 lielu segumu, kas izmaksās $ 0,36 par katriem seguma $ 1000.  Kad darbinieks atjaunina seguma summu, darbinieka saistītās izmaksas paliek nulle.

Atvieglojumu plānam, kas atļauj tikai vienu šī plāna veida atlasi, lietotājs saņem kļūdas paziņojumu, ja mēģinās atmest plānu pēc tā atlasīšanas. Piemēram, lietotājs atlasa ārstniecības plānu un ievieto to grozā. Pēc tam lietotājs citam ārstniecības plānam izvēlas **Atmest**. Lietotājs saņems kļūdas paziņojumu.

## <a name="enable-benefits-management"></a>Atvieglojumu pārvaldības iespējošana

Atvieglojumu pārvaldība ir priekšskatījuma līdzeklis, un tas ir pieejams tikai vidēs **Smilškaste**. Šajos rakstos aprakstīts, kā Human Resources ieslēgt priekšskatījuma līdzekļus. Tajos arī norādīts, kādus pastāvošos Human Resources līdzekļus aizstāj šī atvieglojumu pārvaldība, vai kas tiek atspējoti, ieslēdzot atvieglojumu pārvaldību.

- [Līdzekļu pārvaldība](hr-admin-manage-features.md)
- [Priekšskatījuma līdzeklis: atvieglojumu pārvaldība](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a>Atvieglojumu pārvaldības konfigurēšana

Pirms varat izveidot atvieglojumu plānus saviem darbiniekiem, ir jākonfigurē plānu opcijas.

- [Atvieglojumu pārvaldības parametru iestatīšana](hr-benefits-setup-parameters.md)
- [Piemērotības kārtulu un opciju konfigurēšana](hr-benefits-setup-eligibility-rules.md)
- [Personisko kontaktpersonu piemērotības opciju konfigurēšana](hr-benefits-setup-contact-eligibility-options.md)
- [Seguma opciju izveide](hr-benefits-setup-coverage-options.md)
- [Maksājumu biežuma iestatīšana](hr-benefits-setup-payment-frequencies.md)
- [Dzīves notikumu veidu konfigurēšana](hr-benefits-setup-life-event-types.md)
- [Plānu veidu izveide](hr-benefits-setup-plan-types.md)
- [Iestatiet cēloņa kodus](hr-benefits-setup-reason-codes.md)
- [Līmeņu kodu iestatīšana](hr-benefits-setup-tier-codes.md)
- [Apjoma konfigurēšana](hr-benefits-setup-rates.md)
- [Ieturējumu konfigurēšana](hr-benefits-setup-deductions.md)
- [Gaidīšanas dienu konfigurēšana](hr-benefits-setup-waiting-days.md)
- [Gaidīšanas periodu konfigurēšana](hr-benefits-setup-waiting-periods.md)
- [Noapaļošanas kārtulu konfigurēšana](hr-benefits-setup-rounding-rules.md)
- [Nodarbinātības kategoriju izveide](hr-benefits-setup-employment-categories.md)
- [Nodarbinātības veidu iestatīšana](hr-benefits-setup-employment-types.md)
- [Darbinieku patstāvīgi izmantojamā pakalpojuma konfigurēšana](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Atvieglojumu plānu izveide

Šajos rakstos ir parādīts, kā izveidot atvieglojumu plānus, ieskaitot komplektus un brīvā režīma kredīta programmas.

- [Atvieglojumu plānu iestatīšana](hr-benefits-plans-setup.md)
- [Nodarbināto atvieglojumu plānu izveide](hr-benefits-plans-worker.md)
- [Brīvā režīma kredīta programmu iestatīšana](hr-benefits-plans-flex-credit-programs.md)
- [Turpmāko dzīves notikumu konfigurēšana](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a>Atvieglojumu plānu apstrāde

Dažas no veiktajām izmaiņām nepieciešams apstrādāt, lai tās aktivizētu.

- [Reģistrācijas piemērotības apstrāde](hr-benefits-process-enrollment-eligibility.md)
- [Dzīves notikumu apstrāde](hr-benefits-process-life-events.md)
- [Dzīves notikumu izmaiņu apstrāde](hr-benefits-process-life-event-changes.md)
- [Dzīves notikumu piemērotības apstrāde](hr-benefits-process-life-event-eligibility.md)
- [Apjoma izmaiņu apstrāde](hr-benefits-process-rate-changes.md)


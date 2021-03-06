---
title: Atvieglojumu pārvaldības pārskats
description: Pārskats par Atvieglojumu pārvaldības līdzekli Dynamics 365 Human Resources. Piedāvājiet saviem darbiniekiem paplašinātas atvieglojumu opcijas ar ērti lietojamu tiešsaistes pieredzi.
author: andreabichsel
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1b6ace2ce83c668e83ec1b433f8062148a6dfaf4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059068"
---
# <a name="benefits-management-overview"></a>Atvieglojumu pārvaldības pārskats

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Lai saglabātu konkurētspēju, jāpiedāvā bagātīgs atvieglojumu kopums, lai piesaistītu un saglabātu labākos darbiniekus. Papildus standarta atvieglojumiem, piemēram, ārstniecības un zobārstniecības apdrošināšanai, varat arī piedāvāt tādus paplašinātos pakalpojumus kā palīdzība ar adopciju, atpūtas programmas un pabalsts apģērbam. Microsoft Dynamics 365 Human Resources atvieglojumu pārvaldība nodrošina elastīgu risinājumu, kas atbalsta plaša spektra atvieglojumu opcijas. Human Resources ietver arī ērti lietojamu darbinieku pieredzi, kas demonstrē jūsu piedāvājumus.

- Uzlabotie atvieglojumu plāni ļauj izveidot un pārvaldīt unikālus atvieglojumu plānus, kā arī atbalstīt kompleksas atvieglojumu apjoma tabulas un ligzdotos līmeņus. Ērtākai darbinieku pieredzei varat viegli izveidot atvieglojumu programmas, komplektus un automātiskas reģistrācijas kārtulas.

- Brīvā režīma kredīta programmas ļauj jums proporcionāli atbalstīt pensionēšanos un citus dzīves notikumus.

- Plašie piemērotības kārtulas nodrošina vajadzīgā atvieglojuma pieejamību attiecīgajiem darbiniekiem.

- Tiešsaistes atvieglojumu reģistrācija sniedz darbiniekiem ērtu pieredzi.

- Kvalificēta dzīves notikumu apstrāde atbalsta turpmākos dzīves notikumus.

Ja vēlaties piekļūt demonstrācijas datiem, būs nepieciešams atkārtoti izvietot savu smilškastes vidi.

>[!NOTE]
>Tagad varat pielāgot atvieglojumu pārvaldības veidlapas. Tagad varat pievienot pielāgotos laukus, kas saistīti ar seguma likmēm, veidlapai **Seguma opcija** atvieglojumu plāniem. Lai iegūtu papildinformāciju par darbu ar pielāgotiem laukiem, skatiet rakstā [Pielāgotie lauki](hr-developer-custom-fields.md).
>![Atvieglojumu pārvaldības pielāgotie lauki](media/hr-benefits-management-custom-fields.png)

## <a name="enable-benefits-management"></a>Atvieglojumu pārvaldības iespējošana

Šī tēma apraksta, kā ieslēgt Human Resources priekšskatījuma līdzekļus. Tajā arī norādīts, kādus pastāvošos Human Resources līdzekļus aizstāj šī atvieglojumu pārvaldība, vai kas tiek atspējoti, ieslēdzot atvieglojumu pārvaldību.

> [!IMPORTANT]
> Pēc tam, kad iespējojat Atvieglojumu pārvaldību **Ražošanas** vidē, to nevar atspējot. Iesakām iespējot un testēt Atvieglojumu pārvaldību **Smilškastes** vidē pirms tās iespējošanas **Ražošanas** vidē. Pastāv būtiskas atšķirības starp mantoto Atvieglojumu funkcionalitāti un jauno Atvieglojumu pārvaldības funkcionalitāti, kam nepieciešami papildu iestatījumi, un tie ir jāpārbauda pirms ielaišanas ražošanā.

- [Līdzekļu pārvaldība](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a>Darbinieku informācijas konfigurēšana

Pirms varat reģistrēt darbiniekus atvieglojumos, jānorāda vajadzīgā informācija. Jums ir jāpiesaka darbinieks **Fiksētās atlīdzības plānā** tā sākuma datumā un jāatlasa **Atvieglojumu apmaksas biežums** **Nodarbinātības informācijā** veidlapā **Darbinieks**.

Ja jums ir darbinieks, kurš saņem papildu atlīdzību, piemēram, komisijas, varat pievienot **Atvieglojumi gada algai** summu no darbinieka ieraksta. Human Resources izmanto **Atvieglojumi gada algai** summu, nosakot vajadzību summas, nevis fiksētās atlīdzības gada summu. **Atvieglojumi gada algai** ir jābūt derīgam no darbinieka sākuma datuma vai atvieglojumu perioda sākuma, atkarībā no tā, kurš ir vēlāks. Ja darbiniekam ir reģistrēta gan fiksēta atlīdzība, gan atvieglojumi gada algas summai, tad atvieglojumus gada algai izmantos, nosakot vajadzību summas.

Kad izveidojat atvieglojumu plānu, kas izmanto likmes, kas balstītas uz dzimumu vai vecumu, jums jāievada darbinieka dzimšanas datums un dzimums, lai aprēķinātu atvieglojumu izmaksas.

## <a name="configure-benefits-management"></a>Priekšrocību pārvaldības konfigurēšana

Pirms varat izveidot atvieglojumu plānus saviem darbiniekiem, ir jākonfigurē plānu opcijas.

- [Atvieglojumu pārvaldības parametru iestatīšana](hr-benefits-setup-parameters.md)
- [Piemērotības kārtulu un opciju konfigurēšana](hr-benefits-setup-eligibility-rules.md)
- [Konfigurēt personīgās saziņas piemērotības opcijas](hr-benefits-setup-contact-eligibility-options.md)
- [Izveidot seguma opcijas](hr-benefits-setup-coverage-options.md)
- [Iestatīt maksājumu biežumu](hr-benefits-setup-payment-frequencies.md)
- [Konfigurēt dzīves notikumu tipus](hr-benefits-setup-life-event-types.md)
- [Izveidot plānu tipus](hr-benefits-setup-plan-types.md)
- [Iestatiet cēloņa kodus](hr-benefits-setup-reason-codes.md)
- [Iestatīt pakāpju kodus](hr-benefits-setup-tier-codes.md)
- [Konfigurēt likmes](hr-benefits-setup-rates.md)
- [Konfigurēt ieturējumus](hr-benefits-setup-deductions.md)
- [Konfigurēt gaidīšanas dienas](hr-benefits-setup-waiting-days.md)
- [Konfigurēt gaidīšanas periodus](hr-benefits-setup-waiting-periods.md)
- [Iestatīt noapaļošanas noteikumus](hr-benefits-setup-rounding-rules.md)
- [Izveidot nodarbinātības kategorijas](hr-benefits-setup-employment-categories.md)
- [Nodarbinātības veidu iestatīšana](hr-benefits-setup-employment-types.md)
- [Darbinieku patstāvīgi izmantojamā pakalpojuma konfigurēšana](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Atvieglojumu plānu izveide

Šajos rakstos ir parādīts, kā izveidot atvieglojumu plānus, ieskaitot komplektus un brīvā režīma kredīta programmas.

- [Iestatīt atvieglojumu plānus](hr-benefits-plans-setup.md)
- [Iestatīt brīvā režīma kredīta programmas](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a>Apstrādāt atvieglojumu plānus

Dažas no veiktajām izmaiņām nepieciešams apstrādāt, lai tās aktivizētu.

- [Reģistrācijas piemērotības apstrāde](hr-benefits-process-enrollment-eligibility.md)
- [Dzīves notikumu apstrāde](hr-benefits-process-life-events.md)
- [Dzīves notikumu izmaiņu apstrāde](hr-benefits-process-life-event-changes.md)
- [Dzīves notikumu piemērotības apstrāde](hr-benefits-process-life-event-eligibility.md)
- [Apjoma izmaiņu apstrāde](hr-benefits-process-rate-changes.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
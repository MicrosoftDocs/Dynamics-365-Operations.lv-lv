---
title: Dynamics 365 Talent Pensionēšanās - Piesaistīt un Borta lietotnes
description: Šajā tēmā ir aprakstīta - Piesaistīt un Borta lietotņu aiziešana pensijā Dynamics 365 Talent.
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: df33f35f66e356c3c2a99f0d81ebba1d0f34b5d9
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8069408"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Dynamics 365 Talent: Attract un borta lietotņu norakstīšana


2019. gada decembrī mēs paziņojām par 2022. gada 1. februāra pensionēšanos Dynamics 365 Talent - Attract un Onboard lietotnēm, dodot mūsu klientiem divus gadus plānot.

Papildinformāciju par šo lietotņu aiziešanu pensijā skatiet:
 - [Dynamics 365 Talent Pensionēšanās - piesaistīt un Dynamics 365 Talent: Onboard lietot](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [Veiksmīgāka darbaspēka veidošana ar Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

Mēs turpināsim atbalstīt Dynamics 365 Human Resources, kas palīdzēs mūsu klientiem iegūt darbaspēka ieskatus, kas nepieciešami, lai izveidotu uz datiem balstītu darbinieku pieredzi vairākās jomās, piemēram:

- Kompensācija
- Atvieglojumi
- Atvaļinājumi un kavējumi
- Atbilstība
- Payroll
- Atsauksme par izpildi
- Apmācība un sertifikācija
- Patstāvīgi izmantojamo pakalpojumu programmas

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Dynamics 365 Talent bieži uzdotie jautājumi par programmu pensionēšanos

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>Kāda ir lietotāja pieredze gan Dynamics 365 Talent - Attract un Onboard lietotnes, sākot ar 2022. gada 1. februāri?

Lietotāji nevarēs izmantot lietojumprogrammas un tiks novirzīti uz pensijas lapu.

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>Vai klienti var turpināt eksportēt datus gan Dynamics 365 Talent - Attract un Onboard lietotnes pēc 2022. gada 1. februāra?
  
Nē, pensionēšanās tika izsludināta 2019. gada decembrī, un nepieciešamās eksporta iespējas tika nodrošinātas līdz 2022. gada 1. februārim. 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>Vai klienta dati, kas saistīti gan Dynamics 365 Talent ar - Attract, gan Onboard lietotnēm Dataverse, tiks dzēsti pēc 2022. gada 1. februāra?

Nē, Dataverse uzņēmumi paliks klienta vidē arī pēc pensionēšanās, ja vien netiks dzēsts vai atinstalēts Microsoft Dataverse human capital management talent risinājums.

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>Es zinu Talantu vides nosaukumu. Kā es varu redzēt Attract un Onboard datus Dataverse?

1.  Pieteikties Power Apps: https://make.powerapps.com
2.  Atlasiet vidi, kurā vēlaties redzēt piesaisti un borta datus.
3.  Dodieties uz **Dataverse > tabulas**. 
4.  Meklēšanas **vietā** ierakstiet "msdyn_". Ja redzat tabulu sarakstu, kas sākas ar "msdyn_" + tabulu nosaukumiem (piemērs: msdyn_candidate), tad esat atradis vidi ar Piesaisti un Borta datiem.

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>Es nezinu Talantu vides nosaukumu. Kā atrast vidi, kurai ir dati par Dynamics 365 Talent: Attract Dynamics 365 Talent: Onboard lietojumprogrammām?

1)  Pieteikties Power Platform administrēšanas centrā: https://admin.powerplatform.microsoft.com/
2)  Atlasiet **Vides**.
3)  Atlasiet konkrētu novērtēsimo vidi.
4)  Atlasiet **Resursi > Dynamics 365 programmas**.
5)  Ja redzat **HCM Talent** risinājumu, šajā vidē ir jābūt tajā saglabātiem Piesaisti un Borta datiem. 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> **HCM Talent** risinājums tiek izmantots arī programmā Dynamics 365 Human Resources.

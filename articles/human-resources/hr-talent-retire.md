---
title: Aiziešana Dynamics 365 Talent pensijā - Kuru iestatīs un iestatīju programmas
description: Šajā rakstā ir aprakstīta - Sieto Dynamics 365 Talent un Onboard programmu aiziešana pensijā.
author: twheeloc
ms.date: 01/27/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, SysPolicyListPage, SysPolicySourceDocumentRuleType, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 16441
ms.assetid: 4ad0106f-5b07-4fd5-bc1a-5834fa9b198e
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 3039b0a837335a777cdd6ff22b8b6e7c014ef956
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845089"
---
# <a name="dynamics-365-talent-attract-and-onboard-apps-retirement"></a>Dynamics 365 Talent: Attract un tablo programmu norakstīšana


2019. gada decembrī mēs ar 2022 Dynamics 365 Talent . gada 1. februāri norakstījām aiziešanu no pensiju programmas < a0/>, ļaujot mūsu klientiem plānot divus gadus.

Papildinformāciju par šo programmu aiziešanu skatiet:
 - [Novilkšana Dynamics 365 Talent — kuru lietojumprogrammas un lietojumprogrammas Dynamics 365 Talent: Onboard](https://community.dynamics.com/365/humanresources/b/dynamics365forhumanresources/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)
 - [Darbaspēka veiksmīgas veidošanas ar Dynamics 365 Human Resources](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/12/06/building-a-more-successful-workforce-with-dynamics-365-human-resources)

Turpināsim atbalstu Dynamics 365 Human Resources, kas palīdzēs mūsu klientiem iegūt darbaspēka ieskatu, kas nepieciešama, lai veidotu uz datiem balstītu darbinieku pieredzi vairākās jomās, piemēram:

- Kompensācija
- Atvieglojumi
- Atvaļinājumi un kavējumi
- Atbilstība
- Payroll
- Atsauksme par izpildi
- Apmācība un sertifikācija
- Patstāvīgi izmantojamo pakalpojumu programmas

## <a name="dynamics-365-talent-apps-retirement-faq"></a>Dynamics 365 Talent programmu norakstīšanas BIEŽI UZDOTIE JAUTĀJUMI

### <a name="what-is-the-user-experience-for-both-dynamics-365-talent---attract-and-onboard-apps-starting-february-1-2022"></a>Kāda ir lietotāja pieredze gan Dynamics 365 Talent 2022. gada 1. februārī, gan jūsu rīcībā lietojumprogrammās?

Lietotāji nevarēs izmantot programmas un tiek pārvirzēti uz pensiju lapu.

### <a name="can-customers-continue-to-export-data-for-both-dynamics-365-talent---attract-and-onboard-apps-after-february-1-2022"></a>Vai debitori var turpināt eksportēt datus gan avota Dynamics 365 Talent, gan avota programmām pēc 2022. gada 1. februāra?
  
Nē, norakstīšana tika jāveic 2019. gada decembrī, un nepieciešamās eksporta iespējas tika nodrošinātas līdz 2022. gada 1. februārim. 

### <a name="will-the-customers-data-related-to-both-dynamics-365-talent---attract-and-onboard-apps-in-dataverse-be-deleted-after-february-1-2022"></a>Vai debitora dati, kas attiecas gan Dynamics 365 Talent uz programmu Kuru Dataverse, gan uz darbu, tiks dzēsti pēc 2022. gada 1. februāra?

Nē, entītijas Dataverse paliks debitora vidē Microsoft Dataverse pat pēc aiziešanas pensijā, ja vien Cilvēkkapitāla pārvaldības talantu risinājums netiek dzēsts vai atinstalēts.

### <a name="i-know-the-name-of-the-talent-environment-how-can-i-see-the-attract-and-onboard-data-in-dataverse"></a>Es zinu talantu vides nosaukumu. Kā es variet redzēt Apstrāde un Onboard datus Dataverse?

1.  Power Apps pieteikties:https://make.powerapps.com
2.  Atlasiet vidi, kurā vēlaties redzēt Toti un Onboard datus.
3.  Dodieties uz **Dataverse > tabulām**. 
4.  Meklēšanā ierakstiet "msdyn_ **"**. Ja ir redzams to tabulu saraksts, kuru nosaukumi sākas ar "msdyn_" + tabulu nosaukumi (piemēram, msdyn_candidate), ir atrasta vide ar Darbību un Uz tā vērstiem datiem.

[![Power Apps](./media/Powerapps.png)](./media/Powerapps.png)

### <a name="i-dont-know-the-name-of-the-talent-environment-how-can-i-find-the-environment-that-has-the-data-for-the-dynamics-365-talent-attract-and-dynamics-365-talent-onboard-applications"></a>Es nezinu talantu vides nosaukumu. Kā var atrast vidi, kurā ir šo un lietojumprogrammu Dynamics 365 Talent: Attract Dynamics 365 Talent: Onboard dati?

1)  Pieteikties administrēšanas Power Platform centrā: https://admin.powerplatform.microsoft.com/
2)  Atlasiet **Vides**.
3)  Atlasiet noteiktu vidi, ko novērtēt.
4)  Atlasiet **Resursus > Dynamics 365 programmām**.
5)  Ja ir instalēts **HCM Talantu** risinājums, šai videi ir jābūt tajā uzglabātiem Kātiem un Onboard datiem. 

[![Power Platform](./media/HCMTalent.png)](./media/HCMTalent.png)

> [!NOTE] 
> HCM **Talantu** risinājums tiek izmantots arī Dynamics 365 Human Resources.

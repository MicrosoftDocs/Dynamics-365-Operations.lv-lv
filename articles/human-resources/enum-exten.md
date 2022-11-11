---
title: Dzimuma pamata uzskaitījuma paplašināmība
description: Šajā rakstā sniegts pārskats par dzimuma pamata uzskaitījuma (uzskaitījuma) paplašināmību.
author: twheeloc
ms.date: 05/23/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, EssWorkspace
audience: Application User
ms.custom:
- "51941"
- intro-internal
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61a80c16d24d8fda264340d79ed393db3f635908
ms.sourcegitcommit: 1717ff6af1879c6f3a8360936c42ecf55f86acd0
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/07/2022
ms.locfileid: "9749302"
---
# <a name="gender-base-enum-extensibility"></a>Dzimuma pamata uzskaitījuma paplašināmība

Dzimuma **uzskaitījums** (uzskaitījums) tagad ir paplašināms. Šajā rakstā aprakstītas izmaiņas, kas jāveic koda bāzē, ja plānojat paplašināt dzimuma **uzskaitījumu**.

## <a name="gender-vs-hcmpersongender"></a>Dzimums pret HcmPersonGender

Pastāv divi dzimuma vērtību uzskaitījumi:

- **Dzimums** (programmu platforma)
- **HcmPersonGender** (PersonnelManagement)

Dzimuma **uzskaitījums** tiek izmantots visā Microsoft Dynamics 365 Finansēs, **bet HcmPersonGender ir īpaši** paredzēts cilvēkresursu kapitāla pārvaldībai (HCM) funkcionalitātei. Ja izmantojat HCM funkcionalitāti **un** veicat jebkādas izmaiņas uzskaitījumā Dzimums, **apsveriet iespēju veikt tās pašas izmaiņas hcmPersonGender**. Piemēram, ja jūs pievienojat **transgender** **dzimuma** uzskaitījumam, **pievienojiet Transgender** **arī HcmPersonGender** enum.

## <a name="hcmpersongendertranformutil-class"></a>HcmPersonGenderTranformUtil (klase)

Tika izveidota **jauna klase HcmPersonGenderTranformUtil**, lai atļautu transformēt starp diviem pamata uzskaitījumiem. Šajā klasē ir divas metodes: **convertGenderToHcmPersonGender** un **convertHcmPersonGenderToGender**. Ir jāizveido paplašinājums, izmantojot **·** **komandu ķēdes klasi vai notikumu apdarinātājus, un jāpaplašina abas metodes, lai kartētu jaunās vērtības, kas tiek pievienotas** pamata uzskaitījumam.

## <a name="payrollstatewagetaxprepdp-class"></a>PayrollStateWageTaxPrepDP (klase)

**PayrollStateWageTaxPrepDP** **ir datu sniedzēja klase algas stāvokļa algas nodokļa iepriekšējas** algas SQL servera pārskatu izveides pakalpojumiem (SSRS) pārskatam. Amerikas Savienotajām Valstīm ir pieejamas trīs vērtības: **Toms**, **Sieviete** **un Nenorādīts**. **Metodē populatePayrollStateWageTaxPrepTmp** ir pārslēgšanās priekšraksts, kas tiek izmantots, **lai kartētu HcmPersonGender** uzskaitījuma vērtību uz vienu no trim laukiem: **IsMale**, **IsFemale** vai **IsUnspecifiedGender**. Pārslēgšanās pārskata noklusējuma vērtība ir **IsUnspecifiedGender**. **Ja pievienojat jebkādas vērtības hcmPersonGender** uzskaitījumam, lai to kartētu atšķirīgi, ir jāizveido paplašinājums, izmantojot komandu ķēdes klasi virs metodes populatePayrollStateWageTaxPrepTmp **,** **lai** pēc vajadzības mainītu vērtību.

## <a name="smmoutlooksync_contact-class"></a>smmOutlookSync_Contact (klase)

Integrācijas **smmOutlookSync_Contact klases vērtības uz Outlook un kontaktpersonām** **un no** tās **.** **Outlook** atbalsta trīs vērtības: **Sieviete**, **Sieviete** **un Nenorādīts**. Klasei ir divas metodes, lai palīdzētu kartēt **dzimumus** uz **OutlookGenders**. Noklusējuma metode ir NonSpecific **/UnSpecified**. Ja izveidojat papildu vērtības **dzimuma** uzskaitījumam, jums ir jāizveido paplašinājums, **izmantojot komandu** ķēdes klasi abām metodēm un kartēt pēc nepieciešamības.

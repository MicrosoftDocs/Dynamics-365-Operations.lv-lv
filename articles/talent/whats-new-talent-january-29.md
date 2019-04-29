---
title: Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 31. janvāris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d4504cebb7702c7163c94badeeb06d9af0e5467e
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/19/2019
ms.locfileid: "857642"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a>Jaunumi un izmaiņas programmā Dynamics 365 for Talent (2019. gada 31. janvāris)

[!include [banner](includes/banner.md)]

Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Dynamics 365 for Talent.

**8.1.2128 būvējums**

## <a name="core-hr-changes"></a>Core HR izmaiņas

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a>Paņemtajā brīvajā laikā personas kartītē Atvaļinājums netiek ņemti vērā atvaļinājumu plāna datumi
Gadījumā, ja atvaļinājumu plāni netiek izpildīti kalendārā gada ietvaros, kartītē **Paņemts** tagad ir norādīts brīvais laiks, kas ir paņemts plānā noteiktajā atvaļinājuma gadā. Piemēram, ja organizācijas atvaļinājuma gads ir no 1. jūnija līdz 30. maijam un darbinieks ir izmantojis 3 atvaļinājuma dienas decembrī, kartītē **Paņemts** 15. janvārī tiks rādītas 3 dienas. 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a>Uzkrātais daudzums neatbilst pakāpju datuma bāzei
Atvaļinājumiem un kavējumiem ir pievienotas jaunas opcijas (parametri **Personāla vadība**), lai klienti varētu noteikt, kad ir spēkā darbinieku nodarbinātības mēnešu datums. Dažām organizācijām datums ir mēneša beigās, bet citām tas var būt nākamā mēneša sākumā. Piemēram, viena organizācija var piešķirt prombūtnes laiku 31. decembrī, savukārt cita var piešķirt prombūtnes laiku 1. janvārī. Šī opcija ļauj izvēlēties, kad jāveic piešķiršana. 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a>Nodarbināto darbā pieņemšanas darbības ir iestrēgušas statusā “Darbplūsma izpildīta“
Ir veiktas izmaiņas, lai labotu problēmu, kad neliels skaits darbplūsmu tika pabeigts ar statusu “Darbplūsma izpildīta”. Tagad jaunajām darbplūsmām statusam būtu jāmainās uz “Pabeigts”, kad darbplūsma tiek pabeigta. Visām darbplūsmām, kuru statuss ir “Darbplūsma izpildīta”, tas tiks mainīts uz kļūdas statusu, lai to atjauninātu vai noņemtu nepieciešamības gadījumā. 

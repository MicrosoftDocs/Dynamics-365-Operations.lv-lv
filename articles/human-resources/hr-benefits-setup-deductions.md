---
title: Konfigurēt ieturējumus
description: Izmantojiet ieturējumus Microsoft Dynamics 365 Human Resources, lai noteiktu, cik daudz, ja vispār, ieturētu no darbinieka algas par katru atvieglojumu.
author: andreabichsel
ms.date: 04/06/2020
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
ms.openlocfilehash: 4fac1624ce3a88b9fb4adcf303860e82f9d9165b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055560"
---
# <a name="configure-deductions"></a>Konfigurēt ieturējumus

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Izmantojiet ieturējumus Microsoft Dynamics 365 Human Resources, lai noteiktu, cik daudz, ja vispār, ieturētu no darbinieka algas par katru atvieglojumu. Ieturējumi stājas spēkā noteiktā datumā, tāpēc varat uzturēt vēsturisku ieturējumu informācijas reģistru. 

1. Darbvietā **Atvieglojumu pārvaldība**, sadaļā **Iestatījumi** atlasiet **Ieturējumi**.

2. Atlasiet **Jauns**.

3. Norādiet vērtības tālāk minētajos laukos.

   | Lauks | Apraksts |
   | --- | --- |
   | **Ieturējumi** | Unikālais ID, kas tiek izmantots atvieglojumu ieturējumu identificēšanai. |
   | **Apraksts** | Ieturējuma apraksts. |
   | **Ir spēkā** | Sākuma datums. Noklusējuma vērtība ir pašreizējais sistēmas datums. |
   | **Termiņa beigas** | Beigu datums. Noklusējuma vērtība ir 12/31/2154, kas nozīmē nekad. |
   | **Virsraksts** | Virsraksta kods no algu sistēmas, ko šie ieturējumi izmantos ieturējumu darbinieka daļai, apstrādājot atvieglojumus no algas. To izmanto, kad izmantojat trešās puses algu nodrošinātāju. |
   | **Darbinieka algas ieturējumu atsauce** | Ieturējumu kods no algu sistēmas, ko šie ieturējumi izmantos ieturējumu darbinieka daļai, apstrādājot atvieglojumus no algas. |
   | **Summas virsraksts** | Virsraksta kods no algu sistēmas, ko šī ieturējumu summa izmantos ieturējumu darbinieka daļai, apstrādājot atvieglojumus no algas. To parasti izmanto, kad izmantojat trešās puses algu nodrošinātāju. |
   | **Var izdzēst** | Norāda, vai eksportētā vērtība no Dynamics 365 for Finance and Operations var izraisīt vērtības dzēšanu algu sistēmā. |
   | **Pārī savienotās kolonnas** | Norāda, vai uz algu sistēmu eksportēt virsrakstu un ieturējumu summu pāra blakus esošās kolonnās. |
   | **Izmaiņu spēkā stāšanās datums** | Datums, kad atvieglojumu ieturējumu izmaiņas stāsies spēkā. Šajā datumā sistēma automātiski maina atvieglojumu ieturējumu un atjaunina visus atvieglojumu plānus, kas saistīti ar šo ieturējumu, kamēr vien izpildāt **Ieturējumu izmaiņu atjaunināšanas** apstrādi. |
   | **Ieturējumu maiņa ir pabeigta** | Tiklīdz ieturējumu atjaunināšanas apstrāde mainīs atvieglojumu ieturējumu likmi, izvēles rūtiņa **Ieturējumu izmaiņas pabeigtas** tiks atlasīta automātiski. |
   
4. Lai izsekotu un uzturētu izmaiņas atvieglojumu likmes iestatījumā, atlasiet **Darbības** un pēc tam atlasiet **Uzturēt versijas**.

5. Atlasiet **Saglabāt**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
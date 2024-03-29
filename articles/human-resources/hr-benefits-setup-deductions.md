---
title: Konfigurēt ieturējumus
description: Izmantojiet ieturējumus Microsoft Dynamics 365 Human Resources, lai noteiktu, cik daudz, ja vispār, ieturētu no darbinieka algas par katru atvieglojumu.
author: twheeloc
ms.date: 08/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 46a37aebf99751d16952d3d7c07c538713377a67
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324879"
---
# <a name="configure-deductions"></a>Konfigurēt ieturējumus


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
   | **Var izdzēst** | Norāda, vai eksportēta vērtība no Dynamics 365 Finanšu var radīt to, ka vērtība tiek dzēsta algu sistēmā. |
   | **Pārī savienotās kolonnas** | Norāda, vai uz algu sistēmu eksportēt virsrakstu un ieturējumu summu pāra blakus esošās kolonnās. |
   | **Izmaiņu spēkā stāšanās datums** | Datums, kad atvieglojumu ieturējumu izmaiņas stāsies spēkā. Šajā datumā sistēma automātiski maina atvieglojumu ieturējumu un atjaunina visus atvieglojumu plānus, kas saistīti ar šo ieturējumu, kamēr vien izpildāt **Ieturējumu izmaiņu atjaunināšanas** apstrādi. |
   | **Ieturējumu maiņa ir pabeigta** | Tiklīdz ieturējumu atjaunināšanas apstrāde mainīs atvieglojumu ieturējumu likmi, izvēles rūtiņa **Ieturējumu izmaiņas pabeigtas** tiks atlasīta automātiski. |
   
4. Lai izsekotu un uzturētu izmaiņas atvieglojumu likmes iestatījumā, atlasiet **Darbības** un pēc tam atlasiet **Uzturēt versijas**.

5. Atlasiet **Saglabāt**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]


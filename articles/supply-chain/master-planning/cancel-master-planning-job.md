---
title: Vispārējās plānošanas darba atcelšana
description: Šajā tēmā izskaidrots, kā atcelt aktīvu plānošanas darbu, kas izmanto iebūvētās plānošanas funkcionalitāti.
author: ChristianRytt
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3d5dad766f4c01e993dd77dd762595b29208c6cb
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264750"
---
# <a name="cancel-a-master-planning-job"></a>Vispārējās plānošanas darba atcelšana

[!include [banner](../includes/banner.md)]

Pakalpojumā Microsoft Dynamics 365 Supply Chain Management ir vairākas opcijas, kā atcelt vispārējās plānošanas darbu. Piemēram, iespējams, jūs vēlēsities atcelt vispārējās plānošanas darbu, ja tas tika sākts kļūdas dēļ vai darbojas ilgāk, nekā paredzēts, un jūs vēlaties to beigt. Labākais veids, kā atcelt plānošanas darbu, ir no lapas **Nepabeigtie plānošanas procesi**. Alternatīvās opcijas no lapām **Pakešuzdevumi** un **Uzlabotie pakešuzdevumi** var izmantot tikai tad, ja, atceļot vispārējās plānošanas darbu no lapas **Nepabeigtie plānošanas procesi**, tas dažu minūšu laikā netika izpildīts.

## <a name="preferred-cancel-option"></a>Vēlamā atcelšanas opcija
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a>Atcelt vispārējās plānošanas darbu no lapas **Nepabeigtie plānošanas procesi**
1. Dodieties uz **Vispārējā plānošana > Uzziņas un atskaites > Vispārējā plānošana > Nepabeigtie plānošanas procesi**.
2. Atlasiet līniju ar plānošanas procesu, kuru vēlaties atcelt.
3. Noklikšķiniet uz **Atcelt**.

## <a name="additional-cancel-options"></a>Papildu atcelšanas opcijas
Tās var izmantot tikai tad, ja, atceļot vispārējās plānošanas darbu no lapas **Nepabeigtie plānošanas procesi**, tas dažu minūšu laikā netika izpildīts.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Vispārējās plānošanas darba dzēšana no lapas **Pakešuzdevumi**
1. Dodieties uz **Sistēmas administrēšana > Pieprasījumi > Pakešuzdevumi**.
2. Atlasiet līniju ar plānošanas darbu, kuru vēlaties dzēst.
3. Noklikšķiniet uz **Dzēst**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Pārtraukt vispārējās plānošanas darbu no lapas **Uzlabotie pakešuzdevumi**
1. Dodieties uz **Sistēmas administrēšana > Pieprasījumi > Pakešuzdevumi**.
2. Ja darba ID sarakstā nav redzams, noklikšķiniet uz **Pārslēgties uz uzlaboto formu**, pretējā gadījumā pārejiet pie nākamās darbības.
3. Atvērt pakešuzdevumu. Noklikšķiniet uz **Darba ID** pakešuzdevumam ar uzdevumiem, kurus vēlaties beigt.
4. Sadaļā **Pakešuzdevumi** atlasiet uzdevumus, kurus nepieciešams beigt.
5. Noklikšķiniet uz **Mainīt statusu**, izvēlieties **Atcelt** un noklikšķiniet uz **Labi**.
6. Kopsavilkuma cilnē **Pakešuzdevumi** noklikšķiniet uz **Pārtraukt**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
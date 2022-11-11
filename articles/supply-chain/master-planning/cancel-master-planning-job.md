---
title: Atcelt darbu, kas tika izveidots, izmantojot novecojušu vispārējās plānošanas programmu
description: Šajā rakstā ir izskaidrots, kā atcelt aktīvo plānošanas darbu, kas izmanto novecojušu vispārējās plānošanas programmu.
author: t-benebo
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7b71a43f407050dccb7550db7c4b6a98a596d589
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740882"
---
# <a name="cancel-a-job-that-was-created-using-the-deprecated-master-planning-engine"></a>Atcelt darbu, kas tika izveidots, izmantojot novecojušu vispārējās plānošanas programmu

[!include [banner](../includes/banner.md)]

Ir vairākas iespējas atcelt darbu, kas tika izveidots, izmantojot novecojušu vispārējās plānošanas programmu. Piemēram, iespējams, jūs vēlēsities atcelt vispārējās plānošanas darbu, ja tas tika sākts kļūdas dēļ vai darbojas ilgāk, nekā paredzēts, un jūs vēlaties to beigt.

Labākais veids, kā atcelt plānošanas darbu, ir no lapas **Nepabeigtie plānošanas procesi**. Alternatīvās opcijas no lapām **Pakešuzdevumi** un **Uzlabotie pakešuzdevumi** var izmantot tikai tad, ja, atceļot vispārējās plānošanas darbu no lapas **Nepabeigtie plānošanas procesi**, tas dažu minūšu laikā netika izpildīts.

## <a name="preferred-cancel-option"></a>Vēlamā atcelšanas opcija

### <a name="cancel-master-planning-job-from-the-unfinished-planning-processes-page"></a>Atcelt vispārējās plānošanas darbu no nepabeigto plānošanas procesu lapas

1. Dodieties uz **Vispārējā plānošana > Uzziņas un atskaites > Vispārējā plānošana > Nepabeigtie plānošanas procesi**.
2. Atlasiet līniju ar plānošanas procesu, kuru vēlaties atcelt.
3. Atlasiet **Atcelt**.

## <a name="additional-cancel-options"></a>Papildu atcelšanas opcijas

Tās var izmantot tikai tad, ja, atceļot vispārējās plānošanas darbu no lapas **Nepabeigtie plānošanas procesi**, tas dažu minūšu laikā netika izpildīts.

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a>Vispārējās plānošanas darba dzēšana no lapas **Pakešuzdevumi**

1. Dodieties uz **Sistēmas administrēšana > Pieprasījumi > Pakešuzdevumi**.
2. Atlasiet līniju ar plānošanas darbu, kuru vēlaties dzēst.
3. Atlasiet **Dzēst**.

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a>Pārtraukt vispārējās plānošanas darbu no lapas **Uzlabotie pakešuzdevumi**

1. Dodieties uz **Sistēmas administrēšana > Pieprasījumi > Pakešuzdevumi**.
2. Ja darba ID sarakstā nav redzams, noklikšķiniet uz **Pārslēgties uz uzlaboto formu**, pretējā gadījumā pārejiet pie nākamās darbības.
3. Atvērt pakešuzdevumu. Atlasiet darba **ID pakešuzdevumam** ar uzdevumiem, ko vēlaties beigt.
4. Sadaļā **Pakešuzdevumi** atlasiet uzdevumus, kurus nepieciešams beigt.
5. Atlasiet **Mainīt statusu**, izvēlieties **Atcelšana un** noklikšķiniet uz **Labi**.
6. Kopsavilkuma cilnē **Pakešuzdevumi** noklikšķiniet uz **Pārtraukt**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
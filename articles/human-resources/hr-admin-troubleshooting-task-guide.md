---
title: Uzdevumu ceļvežu saglabāšana pakalpojumā LCS un to atkārtošana
description: Šajā rakstā paskaidrots, kā saglabāt uzdevumu ceļvežus pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) un pēc tam tos atkārtoti skatīt.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d6102bafc9b55f9eff05bfc4a63c177c6548694
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463266"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a>Uzdevumu ceļvežu saglabāšana pakalpojumā LCS un to atkārtošana

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

**Informācija par vidi** 

Programma Microsoft Dynamics 365 Human Resources, kas ir izvietota, izmantojot pakalpojumu Microsoft Dynamics Lifecycle Services (LCS)

**Problēma**

Debitors vēlas saglabāt jaunos uzdevumu ierakstus savā LCS projektā un tad atkārtot saglabātos uzd. ceļvežus.

**Risinājums**

Rīkojieties šādi, lai saglabātu uzd. ierakstu LCS.

1. Pierakstieties LCS un atl. projektu.
2. Atl. elementu **Biznesa procesu modelētājs**.
3. Skatiet lapu atjauninātajā BPM pieredzē.
4. Atlasiet bibl. un tad atlasiet **Kopēt**.
5. Ievadiet nosauk. biznesa procesu modelētāja (BPM) modelim.
6. Pierakstieties Human Resources no LCS.
7. Laukā **Meklēt** ievadiet **palīdzība**. Atveras Lifecycle Services palīdz.
8. Atl. pogu **Atsvaidzināt** Lifecycle Services palīdzības konfigurācijai.

    Ir jāparādās jaunajai BPM bibliotēkai, un tai jābūt aktīvai.

9. Aizvērt lapu.
10. Izveid. uzd. ierakstu.
11. Pēc beigām atl. **Sagl. pakalpojumā Lifecycle Services**.

    ![Saglabāt pakalpojumos Lifecycle Services](media/task-guides.png)

12. Atlasiet BPM bibliotēku un zaru, kurā saglabāt uzd. ierakstu.

Rīkojieties šādi, lai atkārtotu uzd. ceļv. no LCS.

1. Palaidiet Uzd. reģ.
2. Atl. **Atvērt no LCS**.
3. Atlasiet bibliotēku un BPM zaru, kurā ir saglabātais uzd. ceļvedis.
4. Atv. uzd. ceļvedi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
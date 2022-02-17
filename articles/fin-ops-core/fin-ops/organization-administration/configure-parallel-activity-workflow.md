---
title: Paralēlu aktivitāšu konfigurēšana darbplūsmā
description: Lai konfigurētu paralēlu aktivitāti, darbplūsmas redaktorā izpildiet tālāk aprakstītās procedūras.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 054d62e2ff094aee987f8c6e04e2f2e173da633d
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068767"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>Paralēlu aktivitāšu konfigurēšana darbplūsmā

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

Lai konfigurētu paralēlu aktivitāti, darbplūsmas redaktorā izpildiet tālāk aprakstītās procedūras.

Paralēlā aktivitāte sastāv no darbplūsmas zariem, kas darbojas vienlaicīgi.

## <a name="name-a-parallel-activity"></a>Paralēlās aktivitātes nosaukums

Lai ievadītu paralēlās aktivitātes nosaukumu, izpildiet tālāk aprakstītās darbības.

1. Ar peles labo pogu noklikšķiniet uz paralēlās aktivitātes un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu formu **Rekvizīti**.
2. Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
3. Laukā **Nosaukums** ievadiet unikālu paralēlās aktivitātes nosaukumu.
4. Noklikšķiniet uz **Aizvērt**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Konfigurēt paralēlās aktivitātes zarus

Lai pievienotu un konfigurētu šīs paralēlās aktivitātes zarus, izpildiet tālāk aprakstītās darbības.

1. Veiciet dubultklikšķi uz paralēlās aktivitātes, lai parādītu paralēlās aktivitātes zarus.
2. Lai pievienotu zaru, velciet elementu **Zars** no apgabala **Darbplūsmas elementi** uz ievietošanas punktu uz audekla. Nākamajā attēlā ir redzams ievietošanas punkts.

    ![Ievietošanas punkts.](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > Zaru secība nav svarīga, jo visi paralēlās aktivitātes zari darbojas vienlaicīgi.

3. Lai konfigurētu katru zaru, skatiet sadaļu [Konfigurēt paralēlus zarus darbplūsmā](configure-parallel-branch-workflow.md).


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
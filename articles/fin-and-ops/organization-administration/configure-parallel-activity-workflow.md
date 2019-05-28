---
title: Paralēlu aktivitāšu konfigurēšana darbplūsmā
description: Lai konfigurētu paralēlu aktivitāti, darbplūsmas redaktorā izpildiet tālāk aprakstītās procedūras.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 01c1fa876dd66ba6f0e1cdcecff56f424e117bd9
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563323"
---
# <a name="configure-parallel-activities-in-a-workflow"></a>Paralēlu aktivitāšu konfigurēšana darbplūsmā

[!include [banner](../includes/banner.md)]

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

    ![Ievietošanas punkts](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > Zaru secība nav svarīga, jo visi paralēlās aktivitātes zari darbojas vienlaicīgi.

3. Lai konfigurētu katru zaru, skatiet sadaļu [Konfigurēt paralēlu zaru](configure-parallel-branch-workflow.md).

---
title: "Konfigurēt paralēlu aktivitāti darbplūsmā"
description: "Lai konfigurētu paralēlu aktivitāti, darbplūsmas redaktorā izpildiet tālāk aprakstītās procedūras."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: ce3fca9d2dbca046232365b1375bfd920d5b10fd
ms.contentlocale: lv-lv
ms.lasthandoff: 04/25/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Konfigurēt paralēlu aktivitāti darbplūsmā

[!include[banner](../includes/banner.md)]


Lai konfigurētu paralēlu aktivitāti, darbplūsmas redaktorā izpildiet tālāk aprakstītās procedūras.

Paralēlā aktivitāte sastāv no darbplūsmas zariem, kas darbojas vienlaicīgi.

## <a name="name-a-parallel-activity"></a>Paralēlās aktivitātes nosaukums
Lai ievadītu paralēlās aktivitātes nosaukumu, izpildiet tālāk aprakstītās darbības.
1.  Ar peles labo pogu noklikšķiniet uz paralēlās aktivitātes un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu formu **Rekvizīti**.
2.  Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.
3.  Laukā **Nosaukums** ievadiet unikālu paralēlās aktivitātes nosaukumu.
4.  Noklikšķiniet uz **Aizvērt**.

## <a name="configure-the-branches-of-a-parallel-activity"></a>Konfigurēt paralēlās aktivitātes zarus
Lai pievienotu un konfigurētu šīs paralēlās aktivitātes zarus, izpildiet tālāk aprakstītās darbības.
1.  Veiciet dubultklikšķi uz paralēlās aktivitātes, lai parādītu paralēlās aktivitātes zarus.
2.  Lai pievienotu zaru, velciet elementu **Zars** no apgabala **Darbplūsmas elementi** uz ievietošanas punktu uz audekla. Šajā attēlā redzams ievietošanas punkts.![Ievietošanas punkts](./media/workflow_insertionpoint.gif)
    | **Piezīme**                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | Zaru secība nav svarīga, jo visi paralēlās aktivitātes zari darbojas vienlaicīgi. |

3.  Lai konfigurētu katru zaru, skatiet sadaļu [Konfigurēt paralēlu zaru](configure-parallel-branch-workflow.md).







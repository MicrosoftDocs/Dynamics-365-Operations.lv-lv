---
title: "Konfigurēt paralēlu aktivitāti darbplūsmā"
description: "Lai konfigurētu paralēlu aktivitāti, darbplūsmas redaktorā izpildiet tālāk aprakstītās procedūras."
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
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
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 818fb054742b935d002a7341e54a37eca0bb4761
ms.lasthandoff: 03/31/2017


---

# <a name="configure-a-parallel-activity-in-a-workflow"></a>Konfigurēt paralēlu aktivitāti darbplūsmā

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

3.  Lai konfigurētu katru zaru, skatiet sadaļu [Konfigurēt paralēlu zaru](http://axhelp.dynamics.com/en/wiki/configure-a-parallel-branch/).





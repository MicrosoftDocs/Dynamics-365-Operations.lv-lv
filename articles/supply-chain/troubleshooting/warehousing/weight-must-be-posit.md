---
title: Svara vērtībai jābūt pozitīvai.
description: Svara vērtībai jābūt pozitīvai.
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSContainerCloseDiag_canClose
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: dcbcde3143cb509b68b277cb7c709263e2659b5b
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924307"
---
# <a name="weight-must-be-positive"></a>Svara vērtībai jābūt pozitīvai.

Kļūdas kods: WeightMustBePositive

## <a name="symptoms"></a>Simptomi

Sistēma parāda šādu kļūdas ziņojumu:

> Svaram jābūt pozitīvam.

## <a name="cause"></a>Iemesls

Lauks **Bruto svars** ir iestatīts uz *0* (nulle) vai negatīvu vērtību.

## <a name="resolution"></a>Novēršana

Lai noteiktu svaru, izpildiet tālāk aprakstītās darbības.

- Laukā **Bruto svars** iestatiet vērtību. Tad atlasiet vienību nolaižamajā sarakstā.
- Atlasiet **Iegūt sistēmas svaru**, lai aprēķinātu vērtību **Bruto svars**.

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
ms.openlocfilehash: 27ec37e0c0644ff10ece4626d5c136bca3c52ef12f1c6de947afd03003a5368a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776780"
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

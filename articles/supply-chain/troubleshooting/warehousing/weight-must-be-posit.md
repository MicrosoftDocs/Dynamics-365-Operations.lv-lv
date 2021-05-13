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
# <a name="weight-must-be-positive"></a><span data-ttu-id="9d141-103">Svara vērtībai jābūt pozitīvai.</span><span class="sxs-lookup"><span data-stu-id="9d141-103">Weight must be positive</span></span>

<span data-ttu-id="9d141-104">Kļūdas kods: WeightMustBePositive</span><span class="sxs-lookup"><span data-stu-id="9d141-104">Error code: WeightMustBePositive</span></span>

## <a name="symptoms"></a><span data-ttu-id="9d141-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="9d141-105">Symptoms</span></span>

<span data-ttu-id="9d141-106">Sistēma parāda šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="9d141-106">The system shows the following error message:</span></span>

> <span data-ttu-id="9d141-107">Svaram jābūt pozitīvam.</span><span class="sxs-lookup"><span data-stu-id="9d141-107">Weight must be positive.</span></span>

## <a name="cause"></a><span data-ttu-id="9d141-108">Iemesls</span><span class="sxs-lookup"><span data-stu-id="9d141-108">Cause</span></span>

<span data-ttu-id="9d141-109">Lauks **Bruto svars** ir iestatīts uz *0* (nulle) vai negatīvu vērtību.</span><span class="sxs-lookup"><span data-stu-id="9d141-109">The **Gross Weight** field is set to *0* (zero) or a negative value.</span></span>

## <a name="resolution"></a><span data-ttu-id="9d141-110">Novēršana</span><span class="sxs-lookup"><span data-stu-id="9d141-110">Resolution</span></span>

<span data-ttu-id="9d141-111">Lai noteiktu svaru, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9d141-111">To specify a weight, follow one of these steps.</span></span>

- <span data-ttu-id="9d141-112">Laukā **Bruto svars** iestatiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="9d141-112">In the **Gross weight** field, set a value.</span></span> <span data-ttu-id="9d141-113">Tad atlasiet vienību nolaižamajā sarakstā.</span><span class="sxs-lookup"><span data-stu-id="9d141-113">Then select a unit in the drop-down list.</span></span>
- <span data-ttu-id="9d141-114">Atlasiet **Iegūt sistēmas svaru**, lai aprēķinātu vērtību **Bruto svars**.</span><span class="sxs-lookup"><span data-stu-id="9d141-114">Select **Get system weight** to calculate the **Gross weight** value.</span></span>

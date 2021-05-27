---
title: Vienā kvītī vairākiem darbu virsrakstiem tiek drukāta tikai viena etiķete
description: Vienā kvītī vairākiem darbu virsrakstiem tiek drukāta tikai viena etiķete.
author: perlynne
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8e11dc918eb3c9085018d15b43819522cc8bebe3
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026710"
---
# <a name="only-one-label-is-printed-for-multiple-work-headers-on-a-single-receipt"></a><span data-ttu-id="12a73-103">Vienā kvītī vairākiem darbu virsrakstiem tiek drukāta tikai viena etiķete</span><span class="sxs-lookup"><span data-stu-id="12a73-103">Only one label is printed for multiple work headers on a single receipt</span></span>

<span data-ttu-id="12a73-104">KB numurs: 4614667</span><span class="sxs-lookup"><span data-stu-id="12a73-104">KB number: 4614667</span></span>

## <a name="symptoms"></a><span data-ttu-id="12a73-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="12a73-105">Symptoms</span></span>

<span data-ttu-id="12a73-106">Vienai un tai pašai mērķa numura zīmei kā vienas noliktavas lietotnes saņemšanas notikumam tiek izveidotas vairāki darba virsraksti.</span><span class="sxs-lookup"><span data-stu-id="12a73-106">Multiple work headers are created for the same target license plate as part of a single warehouse app receiving event.</span></span> <span data-ttu-id="12a73-107">Tomēr pēc preces saņemšanas tiek drukāta tikai viena numura zīmes etiķete.</span><span class="sxs-lookup"><span data-stu-id="12a73-107">However, only one license plate label is printed when the product is received.</span></span>

## <a name="resolution"></a><span data-ttu-id="12a73-108">Novēršana</span><span class="sxs-lookup"><span data-stu-id="12a73-108">Resolution</span></span>

<span data-ttu-id="12a73-109">Sistēma darbojas kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="12a73-109">The system is behaving as designed.</span></span>

<span data-ttu-id="12a73-110">Pašreizējā dizainā vienmēr tiek izveidota viena numura zīmes etiķete neatkarīgi no darba virsraksta un darba rindu kombināciju skaita.</span><span class="sxs-lookup"><span data-stu-id="12a73-110">In the current design, a single license plate label is always generated, regardless of the number of work header and work line combinations that exist.</span></span> <span data-ttu-id="12a73-111">Ģenerētā etiķete ietver informāciju tikai vienai kombinācijai.</span><span class="sxs-lookup"><span data-stu-id="12a73-111">The generated label includes the information for only one combination.</span></span>

<span data-ttu-id="12a73-112">Lai novērstu šo problēmu, pārliecinieties, vai darba virsraksta izveide vienmēr ir kartēta tikai uz vienu mērķa numura zīmi.</span><span class="sxs-lookup"><span data-stu-id="12a73-112">To work around this issue, make sure that work header creation is always mapped to just one target license plate.</span></span>

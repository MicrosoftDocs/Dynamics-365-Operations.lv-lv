---
title: Pabeigtā pārskata atsaukšana izveido neparedzētu atvērtu darbību
description: Pabeigtā pārskata atsaukšana, kurai ir iezīmēšana, izveido atvērtu darbību, kurā anulētajam daudzumam ir tādas pašas krājumu dimensijas kā anulētajai darbībai.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ProdTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: ea9044a9008e766c7fc92f98e27cfb91076f5b44
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026723"
---
# <a name="reversal-of-reporting-as-finished-creates-an-unexpected-open-transaction"></a><span data-ttu-id="5b8c5-103">Pabeigtā pārskata atsaukšana izveido neparedzētu atvērtu darbību</span><span class="sxs-lookup"><span data-stu-id="5b8c5-103">Reversal of reporting as finished creates an unexpected open transaction</span></span>

<span data-ttu-id="5b8c5-104">KB numurs: 4612469</span><span class="sxs-lookup"><span data-stu-id="5b8c5-104">KB number: 4612469</span></span>

## <a name="symptoms"></a><span data-ttu-id="5b8c5-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="5b8c5-105">Symptoms</span></span>

<span data-ttu-id="5b8c5-106">Ja atsaucat pabeigto pārskatu, kuram ir iezīmēšana, sistēma izveido atvērtu darbību, kurā anulētajam daudzumam ir tādas pašas krājumu dimensijas kā anulētajai darbībai.</span><span class="sxs-lookup"><span data-stu-id="5b8c5-106">If you reverse reporting as finished that has marking, the system creates an open transaction where the reversed quantity has the same inventory dimensions as the transaction that was reversed.</span></span>

## <a name="resolution"></a><span data-ttu-id="5b8c5-107">Novēršana</span><span class="sxs-lookup"><span data-stu-id="5b8c5-107">Resolution</span></span>

<span data-ttu-id="5b8c5-108">Atsaucot pabeigto operāciju, krājumu dimensija tiek inicializēta no ražošanas žurnāla.</span><span class="sxs-lookup"><span data-stu-id="5b8c5-108">When you reverse a report-as-finished operation, the inventory dimension is initialized from the production journal.</span></span> <span data-ttu-id="5b8c5-109">Tāpēc tā iegūst partijas numuru.</span><span class="sxs-lookup"><span data-stu-id="5b8c5-109">Therefore, it gets the batch number.</span></span> <span data-ttu-id="5b8c5-110">Iezīmēšanas dēļ pārdošanas pasūtījuma darījumi pārmantos partijas numuru.</span><span class="sxs-lookup"><span data-stu-id="5b8c5-110">Because of marking, the sales order transactions will inherit the batch number.</span></span>

<span data-ttu-id="5b8c5-111">Dimensiju var atiestatīt, kad tiek grāmatota pabeigšana.</span><span class="sxs-lookup"><span data-stu-id="5b8c5-111">The dimension can be reset when the reporting as finished is posted.</span></span>

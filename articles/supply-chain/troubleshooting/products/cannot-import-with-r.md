---
title: Nevar importēt krājumu, izmantojot Izlaistās preces V2 elementu
description: Nevar importēt krājumu, izmantojot Izlaistās preces V2 elementu.
author: t-benebo
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: EcoResProductDetailsExtended, DataManagementWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 8182f2f83f6a3e4cf54fe6fa64b25a2f461ff541
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026703"
---
# <a name="you-cant-import-an-item-by-using-the-released-products-v2-entity"></a><span data-ttu-id="8bdb1-103">Nevar importēt krājumu, izmantojot Izlaistās preces V2 elementu</span><span class="sxs-lookup"><span data-stu-id="8bdb1-103">You can't import an item by using the Released products V2 entity</span></span>

<span data-ttu-id="8bdb1-104">KB numurs: 4611825</span><span class="sxs-lookup"><span data-stu-id="8bdb1-104">KB number: 4611825</span></span>

## <a name="symptoms"></a><span data-ttu-id="8bdb1-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="8bdb1-105">Symptoms</span></span>

<span data-ttu-id="8bdb1-106">Kad mēģināt importēt krājumu, izmantojot *Izlaistās preces V2* elementu, tiek saņemts kļūdas ziņojums, kas līdzīgs šim piemēram:</span><span class="sxs-lookup"><span data-stu-id="8bdb1-106">When you try to import an item by using the *Released products V2* entity, you receive an error message that resembles the following example:</span></span>

> <span data-ttu-id="8bdb1-107">Nevar izveidot ierakstu laukā Krājumi — izsekošanas dimensiju grupas (EcoResTrackingDimensionGroupItem).</span><span class="sxs-lookup"><span data-stu-id="8bdb1-107">Cannot create a record in Items - tracking dimension groups (EcoResTrackingDimensionGroupItem).</span></span> <span data-ttu-id="8bdb1-108">Krājuma numurs: 2040663, Partija.</span><span class="sxs-lookup"><span data-stu-id="8bdb1-108">Item number: 2040663, Batch.</span></span> <span data-ttu-id="8bdb1-109">Ieraksts jau pastāv.</span><span class="sxs-lookup"><span data-stu-id="8bdb1-109">The record already exists.</span></span>

## <a name="resolution"></a><span data-ttu-id="8bdb1-110">Novēršana</span><span class="sxs-lookup"><span data-stu-id="8bdb1-110">Resolution</span></span>

<span data-ttu-id="8bdb1-111">Lai importētu jaunas izlaistās preces, *Izlaistās preces V2* entītijas vietā jums jāizmanto *Izlaistās preces izveide V2*.</span><span class="sxs-lookup"><span data-stu-id="8bdb1-111">To import new released products, you must use the *Released product creation V2* entity instead of the *Released products V2* entity.</span></span>

---
title: Konsolidēti partijas pasūtījumi
description: Šajā rakstā ir aprakstīts konsolidēto partijas pasūtījumu jēdziens.
author: ShylaThompson
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: faeb90aa3366a58b746c0b397dd950bfb8c9024f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432946"
---
# <a name="consolidated-batch-orders"></a><span data-ttu-id="d319e-103">Konsolidēti partijas pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="d319e-103">Consolidated batch orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d319e-104">Šajā rakstā ir aprakstīts konsolidēto partijas pasūtījumu jēdziens.</span><span class="sxs-lookup"><span data-stu-id="d319e-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="d319e-105">Saražotais lielapjoma krājums ir pamatkrājums, bet iepakotais krājums ir apakškrājums.</span><span class="sxs-lookup"><span data-stu-id="d319e-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="d319e-106">Lielapjoma un iepakotā krājuma saistību tiek izteikta lielapjoma krājuma pārveidē.</span><span class="sxs-lookup"><span data-stu-id="d319e-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="d319e-107">Šī lielapjoma krājuma pārveide ir definēta pašā lielapjoma krājumā.</span><span class="sxs-lookup"><span data-stu-id="d319e-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="d319e-108">Iepakotos krājumus var iepakot viena vai vairāku izmēru konteineros, kas tiek uzskatīti par vienu vienību.</span><span class="sxs-lookup"><span data-stu-id="d319e-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="d319e-109">Konsolidējot pasūtījumus no lielapjoma krājuma, visus saistītos partijas pasūtījumus varat skatīt vienā skatījumā — tas noder, lai noteiktu visu atlikušo darbu, kas vēl jāpaveic.</span><span class="sxs-lookup"><span data-stu-id="d319e-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="d319e-110">Konsolidētā partijas pasūtījumā var ietilpt jebkāda tālāk uzskaitīto pasūtījumu kombinācija.</span><span class="sxs-lookup"><span data-stu-id="d319e-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="d319e-111">Viens lielapjoma pasūtījums un vairāki iepakotie pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="d319e-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="d319e-112">Vairāki lielapjoma pasūtījumi un vairāki iepakotie pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="d319e-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="d319e-113">Vairāki lielapjoma pasūtījumi un viens iepakotais pasūtījums</span><span class="sxs-lookup"><span data-stu-id="d319e-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="d319e-114">Tikai iepakotie pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="d319e-114">Only packed orders</span></span>





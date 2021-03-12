---
title: Problēmu novēršana saistībā ar daļēju izlaidi un daļēju nosūtīšanu
description: Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar daļēju izlaidi un daļēju nosūtīšanu programmā Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: e89a430f90374733b23fadaf53f5bab598d67d62
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645952"
---
# <a name="troubleshoot-partial-releases-and-partial-shipments"></a><span data-ttu-id="cc2af-103">Problēmu novēršana saistībā ar daļēju izlaidi un daļēju nosūtīšanu</span><span class="sxs-lookup"><span data-stu-id="cc2af-103">Troubleshoot partial releases and partial shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc2af-104">Šajā tēmā ir aprakstīts, kā labot biežākās problēmas, kas var rasties, strādājot ar daļēju izlaidi un daļēju nosūtīšanu programmā Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cc2af-104">This topic describes how to fix common issues that you might encounter while you work with partial releases and partial shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="the-release-status-of-a-sales-order-remains-partially-released-even-after-the-sales-order-is-invoiced"></a><span data-ttu-id="cc2af-105">Pārdošanas pasūtījuma izlaišanas statuss paliek Daļēji izlaists pat pēc tam, kad pārdošanas pasūtījums ir iekļauts rēķinā.</span><span class="sxs-lookup"><span data-stu-id="cc2af-105">The release status of a sales order remains Partially released even after the sales order is invoiced.</span></span>

### <a name="issue-description"></a><span data-ttu-id="cc2af-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="cc2af-106">Issue description</span></span>

<span data-ttu-id="cc2af-107">Pārdošanas pasūtījums ir piegādes pasūtījums, bet vienam vai vairākiem krājumiem tajā ir cits piegādes veids.</span><span class="sxs-lookup"><span data-stu-id="cc2af-107">A sales order is a delivery order, but one or more items on it have a different mode of delivery.</span></span> <span data-ttu-id="cc2af-108">Pēc tam, kad pasūtījums ir iekļauts rēķinā, tam joprojām ir laidiena statuss *Daļēji izlaists*.</span><span class="sxs-lookup"><span data-stu-id="cc2af-108">After the order is invoiced, it still has a release status of *Partially released*.</span></span>

<span data-ttu-id="cc2af-109">Piemēram, pārdošanas pasūtījumam ir divi krājumi: viens piegādāšanai un viens saņemšanai.</span><span class="sxs-lookup"><span data-stu-id="cc2af-109">For example, a sales order has two items: one for delivery and one for pickup.</span></span> <span data-ttu-id="cc2af-110">Ir veikta gan nogādāšana, gan saņemšana.</span><span class="sxs-lookup"><span data-stu-id="cc2af-110">Both the delivery and the pickup have been done.</span></span> <span data-ttu-id="cc2af-111">Tāpēc abām rindām ir izrakstīts rēķins.</span><span class="sxs-lookup"><span data-stu-id="cc2af-111">Therefore, both lines have been invoiced.</span></span> <span data-ttu-id="cc2af-112">Tomēr izdošanas statuss joprojām tiek norādīts kā *Daļēji izlaists*, un tas ir maldinošs.</span><span class="sxs-lookup"><span data-stu-id="cc2af-112">However, the release status is still shown as *Partially released*, which is misleading.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="cc2af-113">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="cc2af-113">Issue resolution</span></span>

<span data-ttu-id="cc2af-114">Izdošanas statuss attiecas tikai uz pasūtījuma rindām, kur krājumi ir iespējoti noliktavas pārvaldībai.</span><span class="sxs-lookup"><span data-stu-id="cc2af-114">The release status applies only to order lines where the items are enabled for warehouse management.</span></span> <span data-ttu-id="cc2af-115">Tāpēc nodošanas statuss šajā scenārijā paliek *Daļēji izlaists*.</span><span class="sxs-lookup"><span data-stu-id="cc2af-115">Therefore, the release status remains *Partially released* in this scenario.</span></span> <span data-ttu-id="cc2af-116">Korporācija Microsoft ir izvērtējusi šo problēmu un ir noteikusi, ka tas ir līdzekļa ierobežojums.</span><span class="sxs-lookup"><span data-stu-id="cc2af-116">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="cc2af-117">Paplašinājumu var pievienot kā daļu no pavadzīmes un rēķinu izrakstīšanas procesa, lai atjauninātu izlaides statusu.</span><span class="sxs-lookup"><span data-stu-id="cc2af-117">An extension could be added as part of the packing slip and invoicing process to update the release status.</span></span>
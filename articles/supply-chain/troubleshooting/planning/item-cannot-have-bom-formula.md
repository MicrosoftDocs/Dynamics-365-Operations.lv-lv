---
title: Krājumam nevar būt MK vai formula
description: Mēģinot apstiprināt pasūtījumu, krājuma validācijas laikā tiek parādīts kļūdas ziņojums. Tas norāda, ka krājumam nevar būt materiālu komplekts (MK) vai formula.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 6739b8b1e4d080055a2a0501427eac1c2e8a96c5
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294128"
---
# <a name="item-cant-have-a-bom-or-formula"></a><span data-ttu-id="6d2ff-104">Krājumam nevar būt MK vai formula</span><span class="sxs-lookup"><span data-stu-id="6d2ff-104">Item can't have a BOM or formula</span></span>

<span data-ttu-id="6d2ff-105">Kļūdas kods: PRO2614</span><span class="sxs-lookup"><span data-stu-id="6d2ff-105">Error code: PRO2614</span></span>

## <a name="symptoms"></a><span data-ttu-id="6d2ff-106">Simptomi</span><span class="sxs-lookup"><span data-stu-id="6d2ff-106">Symptoms</span></span>

<span data-ttu-id="6d2ff-107">Mēģinot apstiprināt pasūtījumu, krājuma validācijas laikā tiek parādīts šis kļūdas ziņojums:</span><span class="sxs-lookup"><span data-stu-id="6d2ff-107">When you try to firm an order, you receive the following error message during item validation:</span></span>

> <span data-ttu-id="6d2ff-108">Krājums nedrīkst saturēt MK formulu</span><span class="sxs-lookup"><span data-stu-id="6d2ff-108">Item cannot have a BOM or formula</span></span>

## <a name="resolution"></a><span data-ttu-id="6d2ff-109">Novēršana</span><span class="sxs-lookup"><span data-stu-id="6d2ff-109">Resolution</span></span>

<span data-ttu-id="6d2ff-110">Krājumiem, kuriem ir materiālu komplekts (MK) vai formula, jābūt tipam *Plānošanas krājums*, *MK* vai *formula*.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-110">Items that have a bill of materials (BOM) or formula must be of the *Planning item*, *BOM*, or *formula* type.</span></span> <span data-ttu-id="6d2ff-111">Lai mainītu krājuma tipu, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-111">To change the type of an item, follow these steps.</span></span>

1. <span data-ttu-id="6d2ff-112">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-112">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="6d2ff-113">Atveriet attiecīgo preci.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-113">Open the relevant product.</span></span>
1. <span data-ttu-id="6d2ff-114">Kopsavilkuma cilnē **Inženieris** iestatiet lauku **Ražošanas veids** uz *Plānošanas krājums*, *MK* vai *formula*.</span><span class="sxs-lookup"><span data-stu-id="6d2ff-114">On the **Engineer** FastTab, set the **Production type** field to *Planning item*, *BOM*, or *formula*.</span></span>

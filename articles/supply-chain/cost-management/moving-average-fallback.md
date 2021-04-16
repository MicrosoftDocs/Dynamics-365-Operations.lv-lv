---
title: Vidējās vērtības pārvietošanas regresa izmaksu secība
description: Šajā tēmā ir sniegta informācija par regresa izmaksu secību vidējā vērtības pārrēķiniem programmā Microsoft Dynamics 365 Supply Chain Management.
author: AndersGirke
ms.date: 03/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-03-25
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 09da3c3a79b5540670db25d5466023132d2848f4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832278"
---
# <a name="moving-average-fallback-cost-sequence"></a><span data-ttu-id="e361e-103">Vidējās vērtības pārvietošanas regresa izmaksu secība</span><span class="sxs-lookup"><span data-stu-id="e361e-103">Moving average fallback cost sequence</span></span>

<span data-ttu-id="e361e-104">Viens no veidiem, kā aprēķināt krājumu izmaksas, ir izmantot  _vidējo mainīgo_.</span><span class="sxs-lookup"><span data-stu-id="e361e-104">One way that you can calculate the cost of your inventory is by using a _moving average_.</span></span> <span data-ttu-id="e361e-105">Ar katru krājuma vienību var saistīt līdz trim izmaksu vērtībām:</span><span class="sxs-lookup"><span data-stu-id="e361e-105">Up to three cost values can be associated with each inventory item:</span></span>

- <span data-ttu-id="e361e-106">**Pēdējā izejas plūsma** - pēdējās izejas plūsmas izmaksas, kas tika piešķirtas pirms krājuma, bija negatīvas</span><span class="sxs-lookup"><span data-stu-id="e361e-106">**Last issue** – The last issue cost that was assigned before inventory went negative</span></span>
- <span data-ttu-id="e361e-107">**Aktīvās izmaksas** — jaunākās izmaksas, kas tika aktivizētas izmaksu aprēķināšanas versijā</span><span class="sxs-lookup"><span data-stu-id="e361e-107">**Active cost** – The latest cost that was activated in a costing version</span></span>
- <span data-ttu-id="e361e-108">**Preces cena** — izlaistajai precei norādītā cena</span><span class="sxs-lookup"><span data-stu-id="e361e-108">**Item price** – The cost that is specified for the released product</span></span>

<span data-ttu-id="e361e-109">Lai noteiktu, kuras no šīm izmaksu vērtībām ir jāizmanto vidējo aprēķinu pārvietošanā, sistēma izmanto _regresa izmaksu secību_, lai izveidotu preferenču secību vērtībām.</span><span class="sxs-lookup"><span data-stu-id="e361e-109">To determine which of these cost values should be used in moving average calculations, the system uses a _fallback cost sequence_ to establish the order of preference for the values.</span></span> <span data-ttu-id="e361e-110">Ja vēlamā izmaksu vērtība nav pieejama, sistēma izmanto nākamo vēlamo vērtību, un tā tālāk.</span><span class="sxs-lookup"><span data-stu-id="e361e-110">If the preferred cost value isn't available, the system uses the next-preferred value, and so on.</span></span>

<span data-ttu-id="e361e-111">Iepriekšējās Microsoft Dynamics 365 Supply Chain Management versijās sistēma izmantoja fiksētu regresa izmaksu secību (_Pēdējā izejas plūsma – Aktīvās izmaksas – Krājuma cena_).</span><span class="sxs-lookup"><span data-stu-id="e361e-111">In previous versions of Microsoft Dynamics 365 Supply Chain Management, the system used a fixed fallback cost sequence (_Last issue – Active cost – Item price_).</span></span> <span data-ttu-id="e361e-112">Versijā 10.0.11 šī secība joprojām ir noklusējuma secība.</span><span class="sxs-lookup"><span data-stu-id="e361e-112">In version 10.0.11, this sequence is still the default sequence.</span></span> <span data-ttu-id="e361e-113">Tomēr jūs varat arī ieslēgt līdzekli, kas ļauj atlasīt starp trim pieejamām alternatīvo izmaksu secībām.</span><span class="sxs-lookup"><span data-stu-id="e361e-113">However, you can also turn on a feature that lets you select among three available fallback cost sequences.</span></span> <span data-ttu-id="e361e-114">Šis līdzeklis var būt īpaši noderīgs uzņēmumiem, kas regulāri izmanto negatīvās krājumu vērtības.</span><span class="sxs-lookup"><span data-stu-id="e361e-114">This feature can be especially useful for organizations that regularly use negative inventory values.</span></span>

<span data-ttu-id="e361e-115">Lai būtu pieejams regresa izmaksu secības selektors, jums (vai administratoram) ir jāizmanto [Līdzekļu pārvaldība](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), lai ieslēgtu līdzekli ar nosaukumu _Vidējās vērtības pārvietošanas regresa izmaksu secība_.</span><span class="sxs-lookup"><span data-stu-id="e361e-115">To make the selector for the fallback cost sequence available, you (or an admin) must use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the feature that is named _Moving average fallback cost sequence_.</span></span>

<span data-ttu-id="e361e-116">Lai izvēlētos regresa izmaksu secību vidējās vērtības pārvietošanas aprēķinam, veiciet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="e361e-116">To select the fallback cost sequence for moving average calculations, follow these steps.</span></span>

1. <span data-ttu-id="e361e-117">Atveriet lapu **Parametri**.</span><span class="sxs-lookup"><span data-stu-id="e361e-117">Open the **Parameters** page.</span></span>
2. <span data-ttu-id="e361e-118">Cilnē **Krājumu uzskaite** sadaļā **Mainīgais vidējais** iestatiet **Regresa izmaksu secības** lauku uz vienu no šīm vērtībām:</span><span class="sxs-lookup"><span data-stu-id="e361e-118">On the **Inventory accounting** tab, in the **Moving average** section, set the **Fallback cost sequence** field to one of the following values:</span></span>

    - <span data-ttu-id="e361e-119">**Pēdējā izejas plūsma – Aktīvās izmaksas — Krājuma cena** — šī secība ir noklusētā secība.</span><span class="sxs-lookup"><span data-stu-id="e361e-119">**Last issue – Active cost – Item price** – This sequence is the default sequence.</span></span> <span data-ttu-id="e361e-120">Tā ir tā pati secība, kas tiek izmantota, ja _Mainīgās vidējās vērtības regresa izmaksu secība_ līdzeklis nav ieslēgts.</span><span class="sxs-lookup"><span data-stu-id="e361e-120">It's the same sequence that is used if the _Moving average fallback cost sequence_ feature isn't turned on.</span></span>
    - <span data-ttu-id="e361e-121">**Aktīvās izmaksas — Pēdējā izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="e361e-121">**Active cost – Last issue**</span></span>
    - <span data-ttu-id="e361e-122">**Aktīvās izmaksas — Krājuma cena** — organizācijām var rasties veiktspējas problēmas, ja tās izmanto biznesa procesus, kuros krājumi regulāri ir negatīvi, un tajā pašā laikā transakciju apjoms ir augsts.</span><span class="sxs-lookup"><span data-stu-id="e361e-122">**Active cost – Item price** – Organizations might experience performance issues if they use business processes where inventory regularly goes negative and, at the same time, the transaction volume is high.</span></span> <span data-ttu-id="e361e-123">Šis iestatījums var palīdzēt mazināt šīs veiktspējas problēmas.</span><span class="sxs-lookup"><span data-stu-id="e361e-123">This setting can help mitigate those performance issues.</span></span>

<span data-ttu-id="e361e-124">![Krājumu uzskaites parametri](media/inventory-accounting-parameters.png "Krājumu uzskaites parametri")</span><span class="sxs-lookup"><span data-stu-id="e361e-124">![Inventory accounting parameters](media/inventory-accounting-parameters.png "Inventory accounting parameters")</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
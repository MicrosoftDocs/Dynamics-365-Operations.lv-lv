---
title: "Vecākās partijas izdošana ar mobilo ierīci"
description: "Šajā tēmā ir aprakstīts, kā iestatīt un lietot opcijas, lai no mobilās ierīces izdotu vecāko partiju."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 929c55559f1eac9681e632572ffee71bf83158de
ms.contentlocale: lv-lv
ms.lasthandoff: 11/03/2017

---

# <a name="pick-oldest-batch-on-a-mobile-device"></a><span data-ttu-id="a90db-103">Vecākās partijas izdošana ar mobilo ierīci</span><span class="sxs-lookup"><span data-stu-id="a90db-103">Pick oldest batch on a mobile device</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a90db-104">Konfigurācijai **Izdot vecāko partiju** varat piekļūt no mobilās ierīces izvēlnes, un tā jums ļauj piespiest vai brīdināt noliktavas darbiniekus, ka viņu pašreizējā novietojumā ir jāizdod vecākā partija.</span><span class="sxs-lookup"><span data-stu-id="a90db-104">You can access the configuration **Pick oldest batch** via a mobile device menu and it allows you to force or warn warehouse workers to pick the oldest batch in their current location.</span></span>  

## <a name="where-it-applies"></a><span data-ttu-id="a90db-105">Darbības tvērums</span><span class="sxs-lookup"><span data-stu-id="a90db-105">Where it applies</span></span>
<span data-ttu-id="a90db-106">Vecākās partijas izdošana tiek konfigurēta mobilās ierīces izvēlnes vienumos, un tā ietekmē izdošanu partijā iekļautajiem krājumiem.</span><span class="sxs-lookup"><span data-stu-id="a90db-106">Pick oldest batch is configured on mobile device menu items and effects the pick for batch below items.</span></span>

## <a name="how-to-set-up-the-configuration-for-pick-oldest-batch"></a><span data-ttu-id="a90db-107">Kā iestatīt konfigurāciju Izdot vecāko partiju</span><span class="sxs-lookup"><span data-stu-id="a90db-107">How to set up the configuration for Pick oldest batch</span></span> 
<span data-ttu-id="a90db-108">Krājumiem, kas ir iestatīti lietot pastāvošu darbu **Izdot vecāko partiju**, no mobilās ierīces izvēlnes varat iestatīt opciju **Nav**, **Brīdināt** vai **Piespiest**.</span><span class="sxs-lookup"><span data-stu-id="a90db-108">For items that are set to use existing work, **Pick oldest batch** can be set to **None**, **Warn**, or **Force** from a mobile device menu.</span></span>

<span data-ttu-id="a90db-109">**Nav**: darbinieki nesaņem nekādus ziņojumus, un viņiem ir atļauts izdot jebkādu partiju savā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="a90db-109">**None**: Workers will not receive any messages and they will be allowed to pick any batch in their location.</span></span>

<span data-ttu-id="a90db-110">**Brīdināt** un **Piespiest**: kad darbinieks atlasa kādu partiju, virs šīs partijas vadīklas tiek parādīts saraksts ar partijām, kurām ir visvecākais beigu datums.</span><span class="sxs-lookup"><span data-stu-id="a90db-110">**Warn** and **Force**:  A list of the batch(es) with the oldest expiration date will be displayed above the batch control when the worker selects a batch.</span></span> <span data-ttu-id="a90db-111">Ja novietojums ir atkarīgs no noliktavas vienības, tad virs noliktavas vienības vadīklas tiek parādīts saraksts ar noliktavas vienībām, kurām ir visvecākā partija.</span><span class="sxs-lookup"><span data-stu-id="a90db-111">If the location is license plate controlled, a list of license plates that have the oldest batch will be displayed above the license plate control.</span></span> 
-   <span data-ttu-id="a90db-112">**Brīdināt**: ja darbinieks izvēlas noliktavas vienību vai partiju, kas netiek rādīta sarakstā, tad vadīkla kļūst tukša un tiek parādīts brīdinājums, ka var izvēlēties vecāku partiju.</span><span class="sxs-lookup"><span data-stu-id="a90db-112">**Warn**: If a worker chooses a license plate or batch that is not on the shown list, the control will be blanked and a warning will be shown that there is an older batch to select.</span></span> <span data-ttu-id="a90db-113">Ļaut varētu turpināt darbu, darbinieks var vēlreiz atlasīt to pašu noliktavas vienību vai partiju.</span><span class="sxs-lookup"><span data-stu-id="a90db-113">To be allowed to continue the work, the worker can select the same license plate or batch again.</span></span>  
-   <span data-ttu-id="a90db-114">**Piespiest**: darbinieki turpina saņemt ziņojumu, ka var izvēlēties vecāku partiju.</span><span class="sxs-lookup"><span data-stu-id="a90db-114">**Force**: Workers will continue to receive the message that there is an older batch to pick.</span></span>


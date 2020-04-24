---
title: Partijas un numura zīmes apstiprināšana
description: Šajā tēmā ir aprakstīts, kā iestatīt un lietot partijas un numura zīmes apstiprināšanas funkciju mobilajā ierīcē.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 020d33bfb7e23df7898414f5becf96d31307f2fa
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201322"
---
# <a name="batch-and-license-plate-confirmation"></a><span data-ttu-id="19efc-103">Partijas un numura zīmes apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="19efc-103">Batch and license plate confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19efc-104">Partijas apstiprināšanas funkcija sniedz iespēju mobilajā ierīcē apstiprināt to, ka tiek izdota pareizā partija.</span><span class="sxs-lookup"><span data-stu-id="19efc-104">Batch confirmation allows you to confirm that the correct batch is being picked from the mobile device.</span></span> <span data-ttu-id="19efc-105">Tikai veicot partijas augstākā līmeņa vienumu darba izdošanu (partijas austākais līmenis norāda, ka partija līmenis meklēšanas hierarhijā ir augstāks nekā atrašanās vietas līmenis), jums ir jāapstiprina, ka izdotā partija atbilst darba rindā norādītajai partijai.</span><span class="sxs-lookup"><span data-stu-id="19efc-105">On the initial pick of work for batch above-items only, where batch above indicates that batch ranges higher than location in the search hierarchy, you must verify that the batch that is picked matches the batch on the work line.</span></span> 

<span data-ttu-id="19efc-106">Numura zīmes apstiprināšanas funkcija sniedz iespēju mobilajā ierīcē apstiprināt to, ka tiek izdota pareizā numura zīme.</span><span class="sxs-lookup"><span data-stu-id="19efc-106">License plate confirmation allows you to confirm that the correct license plate is being picked from the mobile device.</span></span> <span data-ttu-id="19efc-107">Veicot izdošanu no sagatavošanas vietas, jums ir jāpārliecinās, ka izdotā numura zīme atbilst ar darbu saistītajai numura zīmei.</span><span class="sxs-lookup"><span data-stu-id="19efc-107">When picking work from a stage location, you must verify that the license plate that is picked matches the license plate that is associated with the work.</span></span> <span data-ttu-id="19efc-108">Ja darbs tiek sākts, skenējot numura zīmi, konfigurēšanas darbība tiek izlaista.</span><span class="sxs-lookup"><span data-stu-id="19efc-108">If the work is started by scanning a license plate, this confirmation step will be skipped.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="19efc-109">Darbības tvērums</span><span class="sxs-lookup"><span data-stu-id="19efc-109">Where it applies</span></span>
<span data-ttu-id="19efc-110">Apstiprināšana attiecas uz tālāk norādītajiem gadījumiem.</span><span class="sxs-lookup"><span data-stu-id="19efc-110">Confirmation applies in the following scenarios:</span></span>

- <span data-ttu-id="19efc-111">Partijas apstiprināšana attiecas uz partijas augstākā līmeņa vienumu darba sākotnējo izdošanu.</span><span class="sxs-lookup"><span data-stu-id="19efc-111">Batch confirmation applies to the initial picks of work for batch above-items.</span></span>
- <span data-ttu-id="19efc-112">Numura zīmes apstiprināšana attiecas uz izdošanu no sagatavošanas vietām.</span><span class="sxs-lookup"><span data-stu-id="19efc-112">License plate confirmation applies to picks from stage locations.</span></span>

## <a name="set-up-batch-and-license-plate-confirmation"></a><span data-ttu-id="19efc-113">Partijas un numura zīmes apstiprināšanas funkcijas iestatīšana</span><span class="sxs-lookup"><span data-stu-id="19efc-113">Set up batch and license plate confirmation</span></span>
<span data-ttu-id="19efc-114">Partijas un numura zīmes apstiprināšanas funkciju var iestatīt, izmantojot mobilās ierīces izvēlnes vienumus.</span><span class="sxs-lookup"><span data-stu-id="19efc-114">You can configure batch and license plate confirmation from the mobile device menu items.</span></span>  
1.  <span data-ttu-id="19efc-115">Izmantojot mobilās ierīces izvēlnes vienumus, pārejiet uz darba konfigurēšanas iestatījumu sadaļu.</span><span class="sxs-lookup"><span data-stu-id="19efc-115">From the mobile device menu items, enter the work confirmation setup.</span></span>  
2.  <span data-ttu-id="19efc-116">Atlasiet partijas vai numura zīmes apstiprināšanas opciju.</span><span class="sxs-lookup"><span data-stu-id="19efc-116">Select the option for either batch or license plate confirmation.</span></span> <span data-ttu-id="19efc-117">Abas opcijas ir pieejamas darba tipa izdošanām, kam nav iespējota automātiskā apstiprināšana.</span><span class="sxs-lookup"><span data-stu-id="19efc-117">Both options are available for work type picks that do not have automatic confirmation enabled.</span></span>  

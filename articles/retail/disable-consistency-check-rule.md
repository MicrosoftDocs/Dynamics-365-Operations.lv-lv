---
title: Kārtulu atspējošana mazumtirdzniecības transakciju konsekvences pārbaudītājā
description: Šajā tēmā ir aprakstīta mazumtirdzniecības transakciju konsekvences pārbaudītāja kārtulu atspējošanas funkcionalitāte risinājumā Microsoft Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4bf8df2fb9f8f5c33ceb13eb012fb6879f81ec66
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/14/2019
ms.locfileid: "2586301"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="944a0-103">Kārtulu atspējošana mazumtirdzniecības transakciju konsekvences pārbaudītājā</span><span class="sxs-lookup"><span data-stu-id="944a0-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="944a0-104">Mazumtirgotājiem var būt unikāli biznesa scenāriji un procesi.</span><span class="sxs-lookup"><span data-stu-id="944a0-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="944a0-105">Tāpēc ne visas kārtulas, kas iekļautas mazumtirdzniecības transakciju konsekvences pārbaudītājā pēc noklusējuma, ir piemērojamas visiem mazumtirgotājiem.</span><span class="sxs-lookup"><span data-stu-id="944a0-105">Therefore, not all the rules that are included by default in the retail transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="944a0-106">Lai pielāgotu atšķirības, Microsoft Dynamics 365 Retail nodrošina funkcionalitāti, ko var izmantot, lai atspējotu nepiemērojamas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="944a0-106">To accommodate differences, Microsoft Dynamics 365 Retail provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="944a0-107">Lai skatītu sarakstu ar mazumtirdzniecības transakciju konsekvences pārbaudītājā pieejamajām kārtulām jūsu vidē un katras kārtulas statusu, dodieties uz **Mazumtirdzniecība \> Headquarters iestatīšana \> Parametri \> Mazumtirdzniecības parametri** un atlasiet cilni **Transakciju validācija**.</span><span class="sxs-lookup"><span data-stu-id="944a0-107">To view the list of rules that are available in the retail transaction consistency checker in your environment, and to see the status of each rule, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="944a0-108">Pēc noklusējuma katras kārtulas statuss ir iestatīts uz **Iespējots**.</span><span class="sxs-lookup"><span data-stu-id="944a0-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="944a0-109">Tāpēc visas kārtulas tiek izmantotas, lai validētu mazumtirdzniecības transakcijas, pirms tās tiek importētas mazumtirdzniecības pārskatos.</span><span class="sxs-lookup"><span data-stu-id="944a0-109">Therefore, all the rules are used to validate retail transactions before they are pulled into the retail statements.</span></span> <span data-ttu-id="944a0-110">Lai atspējotu kārtulu, mainiet tās statusu uz **Atspējots**.</span><span class="sxs-lookup"><span data-stu-id="944a0-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="944a0-111">Atspējotās kārtulas netiek ņemtas vērā, kad mazumtirdzniecības transakcijas tiek validētas pārskata aprēķina procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="944a0-111">Disabled rules aren't considered when retail transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="944a0-112">Lai apietu visu validācijas procesu neatkarīgi no iespējotajām kārtulām, dodieties uz **Mazumtirdzniecība \> Headquarters iestatīšana \> Parametri \> Mazumtirdzniecības parametri** un pēc tam cilnē **Transakciju validācija** iestatiet opciju **Atspējot konsekvences pārbaudītāju mazumtirdzniecības transakcijām** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="944a0-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail \> Headquarters setup \> Parameters \> Retail parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Retail transactions** option to **Yes**.</span></span> <span data-ttu-id="944a0-113">Pēc tam, kad šī opcija ir iestatīta uz **Nē**, to nevar iestatīt atpakaļ uz **Jā** no lietotāja interfeisa (UI).</span><span class="sxs-lookup"><span data-stu-id="944a0-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>

---
title: Kārtulu atspējošana mazumtirdzniecības transakciju konsekvences pārbaudītājā
description: Šajā tēmā ir aprakstīta transakciju konsekvences pārbaudītāja kārtulu atspējošanas funkcionalitāte risinājumā Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 5eb2af7e3090daabccd338d5d0bc6a6ebc4ea663
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982694"
---
# <a name="disable-rules-in-the-retail-transaction-consistency-checker"></a><span data-ttu-id="2dd68-103">Kārtulu atspējošana mazumtirdzniecības transakciju konsekvences pārbaudītājā</span><span class="sxs-lookup"><span data-stu-id="2dd68-103">Disable rules in the retail transaction consistency checker</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2dd68-104">Mazumtirgotājiem var būt unikāli biznesa scenāriji un procesi.</span><span class="sxs-lookup"><span data-stu-id="2dd68-104">Retailers can have business scenarios and processes that are unique to them.</span></span> <span data-ttu-id="2dd68-105">Tāpēc ne visas kārtulas, kas iekļautas tirdzniecības transakciju konsekvences pārbaudītājā pēc noklusējuma, ir piemērojamas visiem mazumtirgotājiem.</span><span class="sxs-lookup"><span data-stu-id="2dd68-105">Therefore, not all the rules that are included by default in the commerce transaction consistency checker are applicable to all retailers.</span></span> <span data-ttu-id="2dd68-106">Lai pielāgotu atšķirības, Microsoft Dynamics 365 Commerce nodrošina funkcionalitāti, ko var izmantot, lai atspējotu nepiemērojamas kārtulas.</span><span class="sxs-lookup"><span data-stu-id="2dd68-106">To accommodate differences, Microsoft Dynamics 365 Commerce provides functionality that can be used to disable the rules that aren't applicable.</span></span>

<span data-ttu-id="2dd68-107">Lai skatītu sarakstu ar transakciju konsekvences pārbaudītājā pieejamajām kārtulām jūsu vidē un katras kārtulas statusu, dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Tirdzniecības parametri** un atlasiet cilni **Transakciju validācija**.</span><span class="sxs-lookup"><span data-stu-id="2dd68-107">To view the list of rules that are available in the transaction consistency checker in your environment, and to see the status of each rule, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and select the **Transaction validation** tab.</span></span>

<span data-ttu-id="2dd68-108">Pēc noklusējuma katras kārtulas statuss ir iestatīts uz **Iespējots**.</span><span class="sxs-lookup"><span data-stu-id="2dd68-108">By default, the status of every rule is set to **Enabled**.</span></span> <span data-ttu-id="2dd68-109">Tāpēc visas kārtulas tiek izmantotas, lai validētu transakcijas, pirms tās tiek importētas tirdzniecības pārskatos.</span><span class="sxs-lookup"><span data-stu-id="2dd68-109">Therefore, all the rules are used to validate transactions before they are pulled into the commerce statements.</span></span> <span data-ttu-id="2dd68-110">Lai atspējotu kārtulu, mainiet tās statusu uz **Atspējots**.</span><span class="sxs-lookup"><span data-stu-id="2dd68-110">To disable a rule, change its status to **Disabled**.</span></span> <span data-ttu-id="2dd68-111">Atspējotās kārtulas netiek ņemtas vērā, kad transakcijas tiek validētas pārskata aprēķina procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="2dd68-111">Disabled rules aren't considered when transactions are validated during the statement calculation process.</span></span>

<span data-ttu-id="2dd68-112">Lai apietu visu validācijas procesu neatkarīgi no iespējotajām kārtulām, dodieties uz **Mazumtirdzniecība un tirdzniecība \> Headquarters iestatīšana \> Parametri \> Tirdzniecības parametri** un pēc tam cilnē **Transakciju validācija** iestatiet opciju **Atspējot konsekvences pārbaudītāju tirdzniecības transakcijām** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="2dd68-112">To bypass the whole validation process, regardless of the rules that are enabled, go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**, and then, on the **Transaction validation** tab, set the **Disable consistency checker for Commerce transactions** option to **Yes**.</span></span> <span data-ttu-id="2dd68-113">Pēc tam, kad šī opcija ir iestatīta uz **Nē**, to nevar iestatīt atpakaļ uz **Jā** no lietotāja interfeisa (UI).</span><span class="sxs-lookup"><span data-stu-id="2dd68-113">After this option is set to **No**, it can't be set back to **Yes** from the user interface (UI).</span></span>

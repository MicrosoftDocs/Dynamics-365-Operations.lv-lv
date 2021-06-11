---
title: Izsaukt procesa automatizācijas plūsmas, lai izveidotu kvalitātes pasūtījumus
description: Šajā tēmā ir sniegti resursi Power Automate izmantošanai, lai to automatizētu biznesa procesus, izmantojot kvalitātes pārbaudes pasūtījumu piemēru.
author: cabeln
ms.date: 05/28/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-05-28
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: f35adab3075ba810964a41899ba95ae40c115e83
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115201"
---
# <a name="invoke-process-automation-flows-to-create-quality-orders"></a><span data-ttu-id="ba504-103">Izsaukt procesa automatizācijas plūsmas, lai izveidotu kvalitātes pasūtījumus</span><span class="sxs-lookup"><span data-stu-id="ba504-103">Invoke process automation flows to create quality orders</span></span>

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

<span data-ttu-id="ba504-104">Uzņēmumiem ir arvien lielāks pieprasījums automatizēt standarta biznesa procesus, nodrošināt ērtāku mijiedarbību ar darbiniekiem un izmantot dažādus datu signālus un sistēmas, lai automātiski vadītu biznesa procesus.</span><span class="sxs-lookup"><span data-stu-id="ba504-104">Organizations have an increasing demand to automate standard business processes, provide more convenient interactions to the staff, and utilize various data signals and systems to drive business processes automatically.</span></span> <span data-ttu-id="ba504-105">Ar robotizētu procesu automatizāciju (RPA) un Microsoft Power Automate, biznesi var izmantot bezkoda pieredzi, lai automatizētu atkārtotus procesus, tādējādi paaugstinot efektivitāti un precizitāti.</span><span class="sxs-lookup"><span data-stu-id="ba504-105">With robotic process automation (RPA) and Microsoft Power Automate, businesses can use a no-code experience to automate repetitive processes, thus gaining efficiency and accuracy.</span></span>

<span data-ttu-id="ba504-106">Lejupielādējama automatizācijas risinājuma veidne Supply Chain Management parāda, kā Power Automate var tikt izmantots, lai automatizētu biznesa procesus, kā piemēru izmantojot kvalitātes pasūtījumus.</span><span class="sxs-lookup"><span data-stu-id="ba504-106">The downloadable automation solution template for Supply Chain Management showcases how Power Automate can be used to automate business processes using quality orders as an example.</span></span>

<span data-ttu-id="ba504-107">Varat lejupielādēt automatizācijas risinājuma veidni [šeit](https://aka.ms/D365SCMQualityOrderRPASolution).</span><span class="sxs-lookup"><span data-stu-id="ba504-107">You can download the automation solution template [here](https://aka.ms/D365SCMQualityOrderRPASolution).</span></span>

<span data-ttu-id="ba504-108">Lai apskatītu šo funkciju un tās iespējas, skatiet sekojošo video: [Izmantot RPA, lai izveidotu kvalitātes pasūtījumus programmā Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span><span class="sxs-lookup"><span data-stu-id="ba504-108">For an overview of this feature and its capabilities, see the following video: [Utilize RPA to create quality orders in Dynamics 365 Supply Chain Management](https://www.youtube.com/watch?v=LFbzJ6-H89w)</span></span>

<span data-ttu-id="ba504-109">![Automatizācijas opcijas ar RPA](media/rpa-automation-options.png "Automatizācijas opcijas ar RPA")</span><span class="sxs-lookup"><span data-stu-id="ba504-109">![Automation options with RPA](media/rpa-automation-options.png "Automation options with RPA")</span></span>

<span data-ttu-id="ba504-110">Risinājuma Power Automate veidne ietver mākoņa automatizācijas plūsmu un darbvirsmas automatizācijas plūsmu, kas automatizē kvalitātes pasūtījumu izveidi programmā Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="ba504-110">The Power Automate solution template includes a cloud automation flow and a desktop automation flow that automate the creation of quality orders in Supply Chain Management.</span></span>

<span data-ttu-id="ba504-111">Automatizāciju var sākt, reaģējot uz daudziem notikumiem un signāliem, ieskaitot lietotāja ieejas vai datora signālus (ieskaitot lietisko internetu (IoT)).</span><span class="sxs-lookup"><span data-stu-id="ba504-111">The automation can be started in response to many events and signals, including user input or machine signals (including the Internet of Things (IoT)).</span></span> <span data-ttu-id="ba504-112">*Q-Order* Power Application piemērs ir iekļauts risinājuma veidnē.</span><span class="sxs-lookup"><span data-stu-id="ba504-112">The *Q-Order* Power Application example is included in the solution template.</span></span> <span data-ttu-id="ba504-113">Tas ļauj lietotājam skenēt preces QR kodu, ievadīt daudzumu un pievienot attēlus, izmantojot kameru.</span><span class="sxs-lookup"><span data-stu-id="ba504-113">It allows the user to scan an item QR code, enter quantity, and attach pictures using a camera.</span></span>

<span data-ttu-id="ba504-114">Risinājuma parametri tiek iekļauti, lai konfigurētu automatizāciju specifiskam lietošanas gadījumam ražošanas iestādē.</span><span class="sxs-lookup"><span data-stu-id="ba504-114">Solution parameters are included to configure the automation for a specific use case in a production facility.</span></span>

<span data-ttu-id="ba504-115">![Izveidot kvalitātes pārbaudes pasūtījumu](media/rpa-create-quality-roder.png "Izveidot kvalitātes pārbaudes pasūtījumu")</span><span class="sxs-lookup"><span data-stu-id="ba504-115">![Create quality order](media/rpa-create-quality-roder.png "Create quality order")</span></span>

<span data-ttu-id="ba504-116">Pilnu detalizēto rokasgrāmatu par to, kā lejupielādēt, instalēt un izmantot parauga risinājumu kvalitātes pasūtījuma izveides automatizēšanai, skatiet [Kvalitātes pasūtījuma izveides automatizēšana programmā Dynamics 365 Supply Chain Management ar Robotizēto procesu automatizāciju, izmantojot Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span><span class="sxs-lookup"><span data-stu-id="ba504-116">For a complete step-by-step guide about how to download, install, and use the sample solution for automating quality order creation, see [Automate quality order creation on Dynamics 365 Supply Chain Management with Robotic Process Automation using Power Automate Desktop](/power-automate/desktop-flows/dynamics365-scm-rpa).</span></span>


---
title: Čeku izveide ar statusu Tukšs
description: Šajā tēmā ir izskaidrots, kā izveidot tukšus čekus bankas kontam lapā Čeki.
author: abruer
manager: AnnBe
ms.date: 10/26/2017
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21941
ms.assetid: d7e22bd8-fd0d-47e1-843f-45ab0193ff8d
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2019-09-17
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 47d54524f87cf718b9b41462b5133df267d5dd9e
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570291"
---
# <a name="create-checks-that-have-blank-status"></a><span data-ttu-id="52d8a-103">Čeku izveide ar statusu Tukšs</span><span class="sxs-lookup"><span data-stu-id="52d8a-103">Create checks that have Blank status</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="52d8a-104">Šajā tēmā ir izskaidrots, kā izveidot tukšus čekus.</span><span class="sxs-lookup"><span data-stu-id="52d8a-104">This topic explains how to create blank checks.</span></span> <span data-ttu-id="52d8a-105">Piemēram, varat izveidot tukšu čeku, lai reģistrētu bojātu čeku, kuru nevar izmantot maksājumam.</span><span class="sxs-lookup"><span data-stu-id="52d8a-105">For example, you might create a blank check to record a check that has been damaged and can't be used for payment.</span></span>

<span data-ttu-id="52d8a-106">Lapā **Čeki** varat veikt čekiem paredzētus uzturēšanas uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="52d8a-106">On the **Checks** page, you perform maintenance tasks for checks.</span></span> <span data-ttu-id="52d8a-107">Piemēram, varat izveidot jaunus čeku numurus un dzēst čekus.</span><span class="sxs-lookup"><span data-stu-id="52d8a-107">For example, you can create new check numbers and delete checks.</span></span> <span data-ttu-id="52d8a-108">Varat arī izveidot čekus ar statusu **Tukšs**.</span><span class="sxs-lookup"><span data-stu-id="52d8a-108">You can also create checks that have a status of **Blank**.</span></span> <span data-ttu-id="52d8a-109">Pēc tam, kad ir izveidoti tukši čeki, tos nevar dzēst vai izmantot sistēmā atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="52d8a-109">After blank checks are created, they can't be deleted or reused in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="52d8a-110">Šis līdzeklis ir pieejams lapā **Čeki** tikai tad, ja ieslēgsit līdzekli **Čeku izveide ar statusu Tukšs lapā Čeki** lapā **Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="52d8a-110">This feature is available on the **Checks** page only if you turn on the **Create checks with a blank status on the Checks page** feature on the **Feature management** page.</span></span> <span data-ttu-id="52d8a-111">Ja šis līdzeklis nav ieslēgts, čekus ar statusu **Tukšs** var izveidot tikai no dialoglodziņa **Maksājums ar čeku** maksājuma ģenerēšanas procesa laikā sadaļā Kreditori.</span><span class="sxs-lookup"><span data-stu-id="52d8a-111">If the feature isn't turned on, checks that have **Blank** status can be created only from the **Payment by check** dialog box during the payment generation process in Accounts payable.</span></span>

<span data-ttu-id="52d8a-112">Lai atvērtu lapu **Čeki**, dodieties uz **Kases un bankas vadība \> Bankas konti \> Bankas konti** un pēc tam darbību rūtī cilnē **Pārvaldīt maksājumus** grupā **Saistītā informācijā** atlasiet **Čeki**.</span><span class="sxs-lookup"><span data-stu-id="52d8a-112">To open the **Checks** page, go to **Cash and bank management \> Bank accounts \> Bank accounts**, and then, on the Action Pane, on the **Manage payments** tab, in the **Related information** group, select **Checks**.</span></span> <span data-ttu-id="52d8a-113">Vai arī dodieties uz **Kases un bankas vadība \> Pieprasījumi un pārskati \> Čeki**.</span><span class="sxs-lookup"><span data-stu-id="52d8a-113">Alternatively, go to **Cash and bank management \> Inquiries and reports \> Checks**.</span></span>

<span data-ttu-id="52d8a-114">Pēc tam, lai izveidotu čekus ar statusu **Tukšs**, darbību rūtī atlasiet **Izveidot tukšus čekus**.</span><span class="sxs-lookup"><span data-stu-id="52d8a-114">Then, to create checks that have **Blank** status, on the Action Pane, select **Create blank checks**.</span></span> <span data-ttu-id="52d8a-115">Kamēr sistēma veido tukšus čekus, saistītais bankas konts tiek īslaicīgi deaktivizēts.</span><span class="sxs-lookup"><span data-stu-id="52d8a-115">While the system is creating blank checks, the associated bank account is temporarily inactivated.</span></span> <span data-ttu-id="52d8a-116">Tas samazina risku, ka maksājumi tiks ģenerēti tajā pašā laikā, kad tiek veidoti tukši čeki.</span><span class="sxs-lookup"><span data-stu-id="52d8a-116">This behavior reduces the risk that payments will be generated at the same time that blank checks are created.</span></span> <span data-ttu-id="52d8a-117">Kad apstrāde ir pabeigta, saistītais bankas konts tiek aktivizēts atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="52d8a-117">When the processing is completed, the associated bank account is reactivated.</span></span>

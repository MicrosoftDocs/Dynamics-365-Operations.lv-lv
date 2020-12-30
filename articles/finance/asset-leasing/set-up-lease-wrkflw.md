---
title: Nomas apstiprinājuma darbplūsmu iestatīšana
description: Tēmā ir izskaidrots, kā iestatīt apstiprināšanas darbplūsmu, kas tiks palaista, kad tiek izveidota jauna noma.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 58c0fd781710b7ab8efeaa7a6874f412279a5924
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445778"
---
# <a name="set-up-lease-approval-workflows"></a><span data-ttu-id="83e54-103">Nomas apstiprinājuma darbplūsmu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="83e54-103">Set up lease approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83e54-104">Tēmā ir izskaidrots, kā iestatīt apstiprināšanas darbplūsmu, kas tiks palaista, kad tiek izveidota jauna noma.</span><span class="sxs-lookup"><span data-stu-id="83e54-104">The topic explains how to set up an approval workflow that will run when a new lease is created.</span></span> <span data-ttu-id="83e54-105">Plašāku informāciju par to, kā izmantot darbplūsmu, skatiet tēmā [Nomu apstiprināšanas darbplūsmu izmantošana](use-create-lease-wrkflw.md).</span><span class="sxs-lookup"><span data-stu-id="83e54-105">For information about how to use the workflow, see [Use lease approval workflows](use-create-lease-wrkflw.md).</span></span> 

1. <span data-ttu-id="83e54-106">Dodieties uz **Līdzekļu noma \> Iestatījumi \> Nomas darbplūsma**.</span><span class="sxs-lookup"><span data-stu-id="83e54-106">Go to **Asset leasing \> Setup \> Lease workflow**.</span></span>
2. <span data-ttu-id="83e54-107">Lapā **Nomas darbplūsma** atlasiet **Jauna**.</span><span class="sxs-lookup"><span data-stu-id="83e54-107">On the **Lease workflow** page, select **New**.</span></span>
3. <span data-ttu-id="83e54-108">Parādītā dialoglodziņa sadaļā **Darbplūsmas veids** atlasiet saiti **Nomas darbplūsma**.</span><span class="sxs-lookup"><span data-stu-id="83e54-108">In the dialog box that appears, under **Workflow type**, select the **Lease workflow** link.</span></span>

    <span data-ttu-id="83e54-109">Programma ir atvērta.</span><span class="sxs-lookup"><span data-stu-id="83e54-109">The application is opened.</span></span> <span data-ttu-id="83e54-110">Kad tā ir palaista, pierakstieties Azure Active Directory (Azure AD), lai tiktu novirzīts uz darbplūsmas programmu.</span><span class="sxs-lookup"><span data-stu-id="83e54-110">After it runs, sign in to Azure Active Directory (Azure AD) to be redirected to the workflow application.</span></span>

4. <span data-ttu-id="83e54-111">Velciet elementu **Nomas darbplūsmas apstiprinājums** uz darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="83e54-111">Drag the **Lease workflow approval** element onto the workflow.</span></span>
5. <span data-ttu-id="83e54-112">Pievienojiet vienu mezglu no **sākuma** līdz **Nomas darbplūsmas apstiprinājumam**.</span><span class="sxs-lookup"><span data-stu-id="83e54-112">Connect one node from **Start** to **Lease workflow approval**.</span></span> <span data-ttu-id="83e54-113">Pēc tam pievienojiet **Nomas darbplūsmas apstiprinājums** elementam **Beigas**.</span><span class="sxs-lookup"><span data-stu-id="83e54-113">Then connect **Lease workflow approval** to **End**.</span></span>
6. <span data-ttu-id="83e54-114">Veiciet dubultklikšķi uz **Nomas darbplūsmas apstiprinājums**.</span><span class="sxs-lookup"><span data-stu-id="83e54-114">Double-click **Lease workflow approval**.</span></span>
7. <span data-ttu-id="83e54-115">Atlasiet **Rekvizīti** un pēc tam sadaļā **Pamata iestatījumi** ievadiet darbplūsmas nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="83e54-115">Select **Properties**, and then, under **Basic settings**, enter a name for the workflow.</span></span>

    <span data-ttu-id="83e54-116">Šajā lapā var arī iestatīt vairāk darbplūsmas parametru.</span><span class="sxs-lookup"><span data-stu-id="83e54-116">On this page, you can also set more parameters for the workflow.</span></span> <span data-ttu-id="83e54-117">Ja ieslēdzāt elementu **Automātiskās darbības**, sistēma automātiski veiks noteiktu darbību.</span><span class="sxs-lookup"><span data-stu-id="83e54-117">If you've turned on **Automatic actions**, the system will automatically take a specific action.</span></span> <span data-ttu-id="83e54-118">Paziņojumus var nosūtīt, ja tie ir norādīti cilnē **Paziņojumi**. Cilnē **Papildu iestatījumi** varat norādīt galīgo apstiprinātāju, iestatīt laika ierobežojumu un norādīt konkrētas darbības, kas ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="83e54-118">Notifications can be sent if they are specified on the **Notifications** tab. On the **Advanced settings** tab, you can specify a final approver, set a time limit, and designate specific actions that must be completed.</span></span>

8. <span data-ttu-id="83e54-119">Kad esat pabeidzis iestatīt darbplūsmas parametrus, atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="83e54-119">When you've finished setting the workflow parameters, select **Close**.</span></span>
9. <span data-ttu-id="83e54-120">Atlasiet **1. darbība** un pēc tam atlasiet **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="83e54-120">Select **Step 1**, and then select **Properties**.</span></span>
10. <span data-ttu-id="83e54-121">Sadaļā **Pamata iestatījumi** ievadiet darbības nosaukumu, izveidojiet apstiprinājuma tēmas rindu un norādiet apstiprinājuma norādījumus.</span><span class="sxs-lookup"><span data-stu-id="83e54-121">Under **Basic settings**, enter a name for the step, create a subject line for the approval, and specify instructions for the approval.</span></span>
11. <span data-ttu-id="83e54-122">Lapā **Piešķire** atlasiet piešķires tipu.</span><span class="sxs-lookup"><span data-stu-id="83e54-122">On the **Assignment** page, select the assignment type.</span></span>
12. <span data-ttu-id="83e54-123">Lai piešķirtu apstiprināšanai noteiktus lietotājus, atlasiet **Lietotājs**, atlasiet lietotājus, kas apstiprina nomas, un pēc tam atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="83e54-123">To assign specific users to the approval, select **User**, select the users who approve leases, and then select **Close**.</span></span>
13. <span data-ttu-id="83e54-124">Atlasiet **Saglabāt un aizvērt**, lai izveidotu darbplūsmu.</span><span class="sxs-lookup"><span data-stu-id="83e54-124">Select **Save and close** to create the workflow.</span></span> <span data-ttu-id="83e54-125">Pēc tam, kad tiek parādīta uzvedne, atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="83e54-125">Then, when you're prompted, select **OK**.</span></span>
14. <span data-ttu-id="83e54-126">Lapā **Darbplūsma izveide** atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="83e54-126">On the **Create workflow** page, select **Close**.</span></span>
14. <span data-ttu-id="83e54-127">Atlasiet jauno darbplūsmu un pēc tam atlasiet **Versijas**.</span><span class="sxs-lookup"><span data-stu-id="83e54-127">Select the new workflow, and then select **Versions**.</span></span> <span data-ttu-id="83e54-128">Pēc tam atlasiet **Padarīt aktīvu**, lai nodrošinātu, ka darbplūsma ir aktīva.</span><span class="sxs-lookup"><span data-stu-id="83e54-128">Then select **Make active** to ensure that the workflow is active.</span></span>
15. <span data-ttu-id="83e54-129">Atlasiet **Aizvērt**.</span><span class="sxs-lookup"><span data-stu-id="83e54-129">Select **Close**.</span></span> <span data-ttu-id="83e54-130">Tiek parādīta jauna aktīvā versija.</span><span class="sxs-lookup"><span data-stu-id="83e54-130">The new active version appears.</span></span>

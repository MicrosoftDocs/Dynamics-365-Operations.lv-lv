---
title: "Konfigurēt dokumenta rindas darbplūsmu"
description: "Šajā tēmā ir paskaidrots, kā konfigurēt dokumenta rindas darbplūsmas elementu."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1d36ec599250f62c523e8d538a37cada9b223007
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="configure-a-line-item-workflow"></a><span data-ttu-id="af06e-103">Konfigurēt dokumenta rindas darbplūsmu</span><span class="sxs-lookup"><span data-stu-id="af06e-103">Configure a line-item workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="af06e-104">Šajā tēmā ir paskaidrots, kā konfigurēt dokumenta rindas darbplūsmas elementu.</span><span class="sxs-lookup"><span data-stu-id="af06e-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="af06e-105">Lai konfigurētu dokumenta rindas darbplūsmas elementu, darbplūsmas redaktorā ar peles labo taustiņu noklikšķiniet uz elementa un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu lapu **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="af06e-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="af06e-106">Pēc tam izmantojiet tālāk aprakstītās procedūras, lai konfigurētu dokumenta rindas darbplūsmas elementa rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="af06e-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="af06e-107">Piešķiriet dokumenta rindas darbplūsmas elementa nosaukumu</span><span class="sxs-lookup"><span data-stu-id="af06e-107">Name the line-item workflow element</span></span>
<span data-ttu-id="af06e-108">Veiciet šādas darbības, lai ievadītu dokumenta rindas darbplūsmas elementa nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="af06e-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1.  <span data-ttu-id="af06e-109">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="af06e-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="af06e-110">Laukā **Nosaukums** ievadiet dokumenta rindas darbplūsmas elementa unikālo nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="af06e-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="af06e-111">Norādiet, vai visu rindu apstrādei tiek izmantota tā pati darbplūsma</span><span class="sxs-lookup"><span data-stu-id="af06e-111">Specify whether the same workflow is used to process all line items</span></span>
<span data-ttu-id="af06e-112">Veiciet šīs darbības, lai norādītu, vai visu dokumenta rindu apstrādei tiek izmantota tā pati darbplūsma.</span><span class="sxs-lookup"><span data-stu-id="af06e-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1.  <span data-ttu-id="af06e-113">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="af06e-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="af06e-114">Ja visu dokumenta rindu apstrādei jāizmanto tā pati darbplūsma, noklikšķiniet uz **Izsauciet vienu darbplūsmu visiem krājumiem rindā**.</span><span class="sxs-lookup"><span data-stu-id="af06e-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="af06e-115">Pēc tam atlasiet darbplūsmu, ko izmantot rindu vienumu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="af06e-115">Then select the workflow to use to process the line items.</span></span>
3.  <span data-ttu-id="af06e-116">Ja tādu rindu vienumu apstrādei, kas atbilst konkrētai nosacījumu kopai, jāizmanto noteikta darbplūsma, noklikšķiniet uz **Izsauciet darbplūsmu katram krājumam rindā**.</span><span class="sxs-lookup"><span data-stu-id="af06e-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="af06e-117">Pēc tam veiciet šīs darbības, lai definētu nosacījumu kopu:</span><span class="sxs-lookup"><span data-stu-id="af06e-117">Then follow these steps to define the set of conditions:</span></span>
    1.  <span data-ttu-id="af06e-118">Noklikšķiniet uz **Pievienot**.</span><span class="sxs-lookup"><span data-stu-id="af06e-118">Click **Add**.</span></span>
    2.  <span data-ttu-id="af06e-119">Atlasiet nosacījumu tabulā.</span><span class="sxs-lookup"><span data-stu-id="af06e-119">Select the condition in the table.</span></span>
    3.  <span data-ttu-id="af06e-120">Cilnē **Nosacījuma nosaukums** ievadiet nosaukumu nosacījumu kopai, kuru definējat.</span><span class="sxs-lookup"><span data-stu-id="af06e-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4.  <span data-ttu-id="af06e-121">Lai ievadītu nosacījumu, noklikšķiniet uz **Pievienot nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="af06e-121">Click **Add condition** to enter a condition.</span></span>
    5.  <span data-ttu-id="af06e-122">Ievadiet visus nepieciešamos papildu nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="af06e-122">Enter any additional conditions that are required.</span></span>
    6.  <span data-ttu-id="af06e-123">Lai pārbaudītu, vai ievadītā nosacījuma kopa ir pareizi konfigurēta, noklikšķiniet uz **Pārbaudīt**.</span><span class="sxs-lookup"><span data-stu-id="af06e-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="af06e-124">Lapas **Testēt darbplūsmas nosacījumu** apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu un pēc tam noklikšķiniet uz **Pārbaudīt**.</span><span class="sxs-lookup"><span data-stu-id="af06e-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="af06e-125">Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu definētajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="af06e-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="af06e-126">Noklikšķiniet uz **Labi** vai **Atcelt**, lai atgrieztos lapā **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="af06e-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="af06e-127">Cilnē **Darbplūsma** atlasiet darbplūsmu tādu rindu vienumu apstrādei, kuri atbilst definēto nosacījumu kopai.</span><span class="sxs-lookup"><span data-stu-id="af06e-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>






---
title: "Nosacījuma lēmumu konfigurēšana darbplūsmā"
description: "Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu nosacījuma lēmuma rekvizītus."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 64e8b2ed5c538cb982f9f03c1db24e38472be868
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---

# <a name="configure-conditional-decisions-in-a-workflow"></a><span data-ttu-id="558e1-103">Nosacījuma lēmumu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="558e1-103">Configure conditional decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="558e1-104">Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu nosacījuma lēmuma rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="558e1-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="558e1-105">Nosacījuma lēmums ir punkts, kurā darbplūsma sadalās divos atzaros.</span><span class="sxs-lookup"><span data-stu-id="558e1-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="558e1-106">Lai konfigurētu nosacījuma lēmumu darbplūsmas redaktorā, ar peles labo taustiņu noklikšķiniet uz nosacījuma lēmuma un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu formu **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="558e1-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="558e1-107">Piešķiriet lēmumam nosaukumu</span><span class="sxs-lookup"><span data-stu-id="558e1-107">Name a decision</span></span>
<span data-ttu-id="558e1-108">Lai ievadītu nosacījuma lēmuma nosaukumu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="558e1-108">Follow these steps to enter a name for a conditional decision.</span></span>
1.  <span data-ttu-id="558e1-109">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="558e1-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="558e1-110">Laukā **Nosaukums** ievadiet unikālu nosacījuma lēmuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="558e1-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="558e1-111">Iestatiet nosacījumus</span><span class="sxs-lookup"><span data-stu-id="558e1-111">Set conditions</span></span>
<span data-ttu-id="558e1-112">Sistēma nosaka, kurš zars tiek izmantots, novērtējot iesniegto dokumentu, lai noteiktu, vai tas atbilst konkrētajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="558e1-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>
1.  <span data-ttu-id="558e1-113">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="558e1-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="558e1-114">Noklikšķiniet uz **Pievienot nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="558e1-114">Click **Add condition**.</span></span>
3.  <span data-ttu-id="558e1-115">Ievadiet nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="558e1-115">Enter a condition.</span></span>
4.  <span data-ttu-id="558e1-116">Nepieciešamības gadījumā ievadiet papildu nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="558e1-116">Enter additional conditions, if they are required.</span></span>
5.  <span data-ttu-id="558e1-117">Lai pārbaudītu, vai ievadītie nosacījumi ir pareizi konfigurēti, veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="558e1-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="558e1-118">Noklikšķiniet uz **Pārbaudīt**, lai atvērtu formu **Testēt darbplūsmas nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="558e1-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="558e1-119">Formas apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="558e1-119">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="558e1-120">Noklikšķiniet uz **Tests**.</span><span class="sxs-lookup"><span data-stu-id="558e1-120">Click **Test**.</span></span> <span data-ttu-id="558e1-121">Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu definētajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="558e1-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="558e1-122">Noklikšķiniet uz **Labi** vai **Atcelt**, lai atgrieztos formā **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="558e1-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>







---
title: Nosacījuma lēmumu konfigurēšana darbplūsmā
description: Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu nosacījuma lēmuma rekvizītus.
author: ChrisGarty
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ed53eeb26e1b4b1df1647739ce1d115c7dd169f8
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747935"
---
# <a name="configure-conditional-decisions-in-a-workflow"></a><span data-ttu-id="ea038-103">Nosacījuma lēmumu konfigurēšana darbplūsmā</span><span class="sxs-lookup"><span data-stu-id="ea038-103">Configure conditional decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea038-104">Izmantojiet tālāk aprakstīto procedūru, lai konfigurētu nosacījuma lēmuma rekvizītus.</span><span class="sxs-lookup"><span data-stu-id="ea038-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="ea038-105">Nosacījuma lēmums ir punkts, kurā darbplūsma sadalās divos atzaros.</span><span class="sxs-lookup"><span data-stu-id="ea038-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="ea038-106">Lai konfigurētu nosacījuma lēmumu darbplūsmas redaktorā, ar peles labo taustiņu noklikšķiniet uz nosacījuma lēmuma un pēc tam noklikšķiniet uz **Rekvizīti**, lai atvērtu formu **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="ea038-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="ea038-107">Piešķiriet lēmumam nosaukumu</span><span class="sxs-lookup"><span data-stu-id="ea038-107">Name a decision</span></span>

<span data-ttu-id="ea038-108">Lai ievadītu nosacījuma lēmuma nosaukumu, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="ea038-108">Follow these steps to enter a name for a conditional decision.</span></span>

1. <span data-ttu-id="ea038-109">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="ea038-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ea038-110">Laukā **Nosaukums** ievadiet unikālu nosacījuma lēmuma nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="ea038-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="ea038-111">Iestatiet nosacījumus</span><span class="sxs-lookup"><span data-stu-id="ea038-111">Set conditions</span></span>

<span data-ttu-id="ea038-112">Sistēma nosaka, kurš zars tiek izmantots, novērtējot iesniegto dokumentu, lai noteiktu, vai tas atbilst konkrētajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="ea038-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>

1. <span data-ttu-id="ea038-113">Kreisajā rūtī noklikšķiniet uz **Pamata iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="ea038-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ea038-114">Noklikšķiniet uz **Pievienot nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="ea038-114">Click **Add condition**.</span></span>
3. <span data-ttu-id="ea038-115">Ievadiet nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="ea038-115">Enter a condition.</span></span>
4. <span data-ttu-id="ea038-116">Nepieciešamības gadījumā ievadiet papildu nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="ea038-116">Enter additional conditions, if they are required.</span></span>
5. <span data-ttu-id="ea038-117">Lai pārbaudītu, vai ievadītie nosacījumi ir pareizi konfigurēti, veiciet šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="ea038-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="ea038-118">Noklikšķiniet uz **Pārbaudīt**, lai atvērtu formu **Testēt darbplūsmas nosacījumu**.</span><span class="sxs-lookup"><span data-stu-id="ea038-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="ea038-119">Formas apgabalā **Pārbaudīt nosacījumu** atlasiet ierakstu.</span><span class="sxs-lookup"><span data-stu-id="ea038-119">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="ea038-120">Noklikšķiniet uz **Tests**.</span><span class="sxs-lookup"><span data-stu-id="ea038-120">Click **Test**.</span></span> <span data-ttu-id="ea038-121">Sistēma novērtē ierakstu, lai noteiktu, vai tas atbilst jūsu definētajiem nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="ea038-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="ea038-122">Noklikšķiniet uz **Labi** vai **Atcelt**, lai atgrieztos formā **Rekvizīti**.</span><span class="sxs-lookup"><span data-stu-id="ea038-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
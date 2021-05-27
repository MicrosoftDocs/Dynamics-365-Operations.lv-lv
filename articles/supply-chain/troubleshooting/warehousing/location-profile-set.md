---
title: Novietojuma profilā netiek atļauti negatīvi krājumi, bet atļauti negatīvi rīcībā esošie krājumi
description: Novietojuma profila opcijas Atļaut negatīvu krājumu vērtība ir iestatīta uz Nē, bet sistēma joprojām atļauj negatīvu rīcībā esošo krājumu daudzumu.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: WHSLocationProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 356d2dd7853bf93250e14eb9bd28a8a145794584
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026709"
---
# <a name="location-profile-disallows-negative-inventory-but-negative-on-hand-inventory-is-permitted"></a><span data-ttu-id="0d20a-103">Novietojuma profilā netiek atļauti negatīvi krājumi, bet atļauti negatīvi rīcībā esošie krājumi</span><span class="sxs-lookup"><span data-stu-id="0d20a-103">Location profile disallows negative inventory, but negative on-hand inventory is permitted</span></span>

<span data-ttu-id="0d20a-104">KB numurs: 4613622</span><span class="sxs-lookup"><span data-stu-id="0d20a-104">KB number: 4613622</span></span>

## <a name="symptoms"></a><span data-ttu-id="0d20a-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="0d20a-105">Symptoms</span></span>

<span data-ttu-id="0d20a-106">Novietojuma profila opcijas **Atļaut negatīvu krājumu** vērtība ir iestatīta uz *Nē*, bet sistēma joprojām atļauj negatīvu rīcībā esošo krājumu daudzumu.</span><span class="sxs-lookup"><span data-stu-id="0d20a-106">The **Allow negative inventory** option for the location profile is set to *No*, but the system still allows negative on-hand inventory.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="0d20a-107">Piemērs</span><span class="sxs-lookup"><span data-stu-id="0d20a-107">Example scenario</span></span>

<span data-ttu-id="0d20a-108">Valdības regulētiem darījumiem sistēmai jāspēj reģistrēt negatīvus krājumus, lai uzskaitītu zaudējumus.</span><span class="sxs-lookup"><span data-stu-id="0d20a-108">For government-regulated transactions, the system must be able to record negative inventory to book losses.</span></span> <span data-ttu-id="0d20a-109">Vēlaties, lai krājums varētu uzrādīt negatīvu krājumu, bet tikai noteiktās vietās, piemēram, tvertnēs.</span><span class="sxs-lookup"><span data-stu-id="0d20a-109">You want an item to be able to show negative inventory, but only in designated locations, such as tanks.</span></span> <span data-ttu-id="0d20a-110">Tomēr, ja krājumu modeļu grupa atļauj negatīvus krājumus, jūs sapratīsiet, ka nav svarīgi, vai vieta ir iestatīta, lai atļautu negatīvus krājumus.</span><span class="sxs-lookup"><span data-stu-id="0d20a-110">However, if the item model group allows negative inventory, you find that it doesn't matter whether the location is set to allow negative inventory.</span></span> <span data-ttu-id="0d20a-111">Ja krājums ir iestatīts tā, ka netiek atļauti negatīvi krājumi, nav svarīgi, kā tiek iestatīts novietojuma profils.</span><span class="sxs-lookup"><span data-stu-id="0d20a-111">If the item is set up so that negative inventory isn't allowed, it doesn't matter how the location profile is set up.</span></span>

## <a name="resolution"></a><span data-ttu-id="0d20a-112">Novēršana</span><span class="sxs-lookup"><span data-stu-id="0d20a-112">Resolution</span></span>

<span data-ttu-id="0d20a-113">Iestatījums **Atļaut negatīvu krājumu daudzumu** no novietojuma profila attiecas tikai uz noliktavas procesiem, piemēram, izdošanu.</span><span class="sxs-lookup"><span data-stu-id="0d20a-113">The **Allow negative inventory** setting from the location profile applies only to warehouse processes, such as picking.</span></span> <span data-ttu-id="0d20a-114">Tomēr krājumu modeļu grupas, kas ir iestatītas, lai atļautu negatīvu krājumu daudzumu, ietekmē visus procesus no Krājumu pārvaldības un noliktavas pārvaldības moduļiem, un novietojuma profils neignorēs šo iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="0d20a-114">However, item model groups that are set to allow negative inventory affect all processes from the Inventory management and Warehouse management modules, and the location profile won't override the setting.</span></span>

<span data-ttu-id="0d20a-115">Varat kontrolēt, vai noliktavai ir atļauts veikt negatīvu krājumu.</span><span class="sxs-lookup"><span data-stu-id="0d20a-115">You can control whether a warehouse is allowed to carry negative inventory.</span></span> <span data-ttu-id="0d20a-116">Iestatiet savu krājumu modeļu grupas, lai neatļautu negatīvus fiziskos krājumus, un iestatiet tikai atbilstošo noliktavu, lai ļautu negatīvus krājumus.</span><span class="sxs-lookup"><span data-stu-id="0d20a-116">Set your item model groups to disallow negative physical inventory, and set only the relevant warehouse to allow negative inventory.</span></span>

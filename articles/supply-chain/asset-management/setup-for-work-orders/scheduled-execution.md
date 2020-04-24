---
title: Plānotā izpilde
description: Šajā tēmā ir aprakstīta plānotā izpilde Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 976155b685498456952f7d715779d20191712103
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215520"
---
# <a name="scheduled-execution"></a><span data-ttu-id="a48b4-103">Plānotā izpilde</span><span class="sxs-lookup"><span data-stu-id="a48b4-103">Scheduled execution</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="a48b4-104">Lai iestatītu plānoto izpildi, varat izmantot darba pasūtījuma pakalpojumu līmeņus.</span><span class="sxs-lookup"><span data-stu-id="a48b4-104">You can use work order service levels to set up scheduled execution.</span></span> <span data-ttu-id="a48b4-105">(Plašāku informāciju par darba pasūtījumu pakalpojumu līmeņiem skatiet sadaļā [Pakalpojuma līmenis un apraksts](service-level-and-description.md).) Plānotā izpilde nodrošina elastību darba plānošanā uzturēšanas speciālistiem, jo varat iestatīt detalizētas vai mazāk detalizētas prasības intervālam, kurā darba pasūtījums ir jāpabeidz.</span><span class="sxs-lookup"><span data-stu-id="a48b4-105">(For more information about work order service levels, see [Service level and description](service-level-and-description.md).) Scheduled execution provides flexibility in work planning for maintenance workers, because you can set up more detailed or less detailed requirements for the interval that a work order should be completed during.</span></span> <span data-ttu-id="a48b4-106">Piemēram, uzturēšanas speciālists, kurš pabeidz uzdevumu ātrāk, nekā paredzēts ražošanā, iestāde var pāriet uz citu tuvumā esošu uzdevumu, kas tika ieplānots pašreizējai nedēļai, bet ne obligāti pašreizējai dienai.</span><span class="sxs-lookup"><span data-stu-id="a48b4-106">For example, a maintenance worker who completes a job faster than expected in a production facility might be able to move on to another nearby job that was planned for the current week but not necessarily for the current day.</span></span> <span data-ttu-id="a48b4-107">Šī pieeja ļauj optimizēt darbinieku plānošanu un darbu izpildi.</span><span class="sxs-lookup"><span data-stu-id="a48b4-107">This approach allows for optimization of worker planning and job completion.</span></span>

<span data-ttu-id="a48b4-108">Plānotās izpildes iestatījums, kas ir saistīts ar darba pasūtījumiem, var būt vispārīgs vai konkrēts.</span><span class="sxs-lookup"><span data-stu-id="a48b4-108">Scheduled execution setup, which is related to work orders, can be generic or specific.</span></span> <span data-ttu-id="a48b4-109">Varat iestatīt vispārīgās rindas, kuras nav ierobežotas konkrētiem darba pasūtījuma tipiem u. tml.</span><span class="sxs-lookup"><span data-stu-id="a48b4-109">You can set up generic lines that aren't limited to specific work order types, asset types, and so on.</span></span> <span data-ttu-id="a48b4-110">Vai arī varat izveidot plānotas izpildes rindas, kas attiecas uz konkrētu darba pasūtījuma tipu, līdzekļu tipu, uzturēšanas darba tipu u. tml.</span><span class="sxs-lookup"><span data-stu-id="a48b4-110">Alternatively, you can create scheduled execution lines that apply to a specific work order type, asset type, maintenance job type, and so on.</span></span>

1. <span data-ttu-id="a48b4-111">Atlasiet **Līdzekļu pārvaldība** \> **Iestatīšana** \> **Darba pasūtījumi** \> **Plānotā izpilde**.</span><span class="sxs-lookup"><span data-stu-id="a48b4-111">Select **Asset management** \> **Setup** \> **Work orders** \> **Scheduled execution**.</span></span>
2. <span data-ttu-id="a48b4-112">Atlasiet **Jauns**, lai izveidotu plānotās izpildes rindu.</span><span class="sxs-lookup"><span data-stu-id="a48b4-112">Select **New** to create a scheduled execution line.</span></span>
3. <span data-ttu-id="a48b4-113">Laukos **Funkcionālais novietojums**, **Darba pasūtījuma tips**, **Līdzekļu tips**, **Ražotājs**, **Modelis**, **Uzturēšanas darba tipa kategorija**, **Uzturēšanas darba tips**, **Uzturēšanas darba tipa variants** un **Tirdzniecība** atlasiet nepieciešamās vērtības.</span><span class="sxs-lookup"><span data-stu-id="a48b4-113">In the **Functional location**, **Work order type**, **Asset type**, **Manufacturer**, **Model**, **Maintenance job type category**, **Maintenance job type**, **Maintenance job type variant**, and **Trade** fields, select values as you require.</span></span>
4. <span data-ttu-id="a48b4-114">Laukā **Pakalpojuma līmenis** atlasiet darba pasūtījuma pakalpojuma līmeni.</span><span class="sxs-lookup"><span data-stu-id="a48b4-114">In the **Service level** field, select a work order service level.</span></span> <span data-ttu-id="a48b4-115">Ja atstāsiet šo lauku tukšu, būsiet izveidojis ieplānotās izpildes rindas vispārīgāko tipu.</span><span class="sxs-lookup"><span data-stu-id="a48b4-115">If you leave this field blank, you make the most generic type of scheduled execution line.</span></span> <span data-ttu-id="a48b4-116">Vispārīgās rindas piemēru skatiet pirmajā tālāk norādītās ilustrācijas ierakstā.</span><span class="sxs-lookup"><span data-stu-id="a48b4-116">For an example of a generic line, see the first record in the illustration that follows.</span></span> <span data-ttu-id="a48b4-117">Šī rinda iespējo visus darba pasūtījumus, kuriem nav darba pasūtījuma pakalpojuma līmeņa, kas jāieplāno konkrētā datumā un laikā.</span><span class="sxs-lookup"><span data-stu-id="a48b4-117">That line enables all work orders that have no work order service level to be scheduled for a specific date and time.</span></span>
5. <span data-ttu-id="a48b4-118">Laukā **Plānotā izpilde** atlasiet laika intervālu.</span><span class="sxs-lookup"><span data-stu-id="a48b4-118">In the **Scheduled execution** field, select the time interval.</span></span>
6. <span data-ttu-id="a48b4-119">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="a48b4-119">Select **Save**.</span></span>

![Plānotā izpilde](media/20-setup-for-work-orders.png)

---
title: Apjoma izmaiņu apstrāde
description: Apstrādājiet atvieglojumu likmju izmaiņas Microsoft Dynamics 365 Human Resources, kad jaunam vai esošam atvieglojumu plānam ir izmaiņas piemērotības kārtulas iestatījumos.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 850709480326f6a0871f19ea1bb287631cd58b42
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229948"
---
# <a name="process-rate-changes"></a><span data-ttu-id="15c62-103">Apjoma izmaiņu apstrāde</span><span class="sxs-lookup"><span data-stu-id="15c62-103">Process rate changes</span></span>

<span data-ttu-id="15c62-104">Apstrādājiet atvieglojumu likmju izmaiņas Microsoft Dynamics 365 Human Resources, kad jaunam vai esošam atvieglojumu plānam ir izmaiņas piemērotības kārtulas iestatījumos.</span><span class="sxs-lookup"><span data-stu-id="15c62-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="15c62-105">Ja plānam tiek izveidota un piešķirta jauna piemērotības kārtula, tas uzvedina sistēmu atkārtoti izpildīt nodarbinātā piemērotību, lai pārbaudītu, vai nodarbinātais tagad ir piemērots plānam, pamatojoties uz jaunajām piemērotības opcijām.</span><span class="sxs-lookup"><span data-stu-id="15c62-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="15c62-106">Darbvietā **Atvieglojumu pārvaldība** sadaļā **Apstrāde** atlasiet **Likmju izmaiņu atjauninājumu apstrāde**.</span><span class="sxs-lookup"><span data-stu-id="15c62-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="15c62-107">Dialoglodziņā **Izpildīt atvieglojumu likmju atjauninājumu apstrādi** norādiet vērtības tālāk minētajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="15c62-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="15c62-108">Lauks</span><span class="sxs-lookup"><span data-stu-id="15c62-108">Field</span></span> | <span data-ttu-id="15c62-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="15c62-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="15c62-110">**Reģistrācijas periods**</span><span class="sxs-lookup"><span data-stu-id="15c62-110">**Enrollment period**</span></span> | <span data-ttu-id="15c62-111">Reģistrācijas periods, kuram apstrādāt likmju izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="15c62-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="15c62-112">Ja vēlaties izpildīt apstrādi fonā, atlasiet **Izpildīt fonā** un veiciet tālāk minētos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="15c62-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="15c62-113">Ievadiet informāciju apstrādei.</span><span class="sxs-lookup"><span data-stu-id="15c62-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="15c62-114">Lai iestatītu periodisku darbu, atlasiet **Periodiskums**, ievadiet periodiskuma informāciju un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="15c62-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="15c62-115">Lai iestatītu darba brīdinājumu, atlasiet **Brīdinājumi**, atlasiet saņemamos brīdinājumus un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="15c62-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="15c62-116">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="15c62-116">Select **OK**.</span></span> <span data-ttu-id="15c62-117">Apstrāde tiks izpildīta ar iestatītajiem parametriem.</span><span class="sxs-lookup"><span data-stu-id="15c62-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="15c62-118">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="15c62-118">Select **OK**.</span></span>

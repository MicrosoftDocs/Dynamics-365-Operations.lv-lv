---
title: Apjoma izmaiņu apstrāde
description: Apstrādājiet atvieglojumu likmju izmaiņas Microsoft Dynamics 365 Human Resources, kad jaunam vai esošam atvieglojumu plānam ir izmaiņas piemērotības kārtulas iestatījumos.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 9ebe5cfc2bdf7790770d27ece2dc67f7677db593
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009765"
---
# <a name="process-rate-changes"></a><span data-ttu-id="567f5-103">Apjoma izmaiņu apstrāde</span><span class="sxs-lookup"><span data-stu-id="567f5-103">Process rate changes</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="567f5-104">Apstrādājiet atvieglojumu likmju izmaiņas Microsoft Dynamics 365 Human Resources, kad jaunam vai esošam atvieglojumu plānam ir izmaiņas piemērotības kārtulas iestatījumos.</span><span class="sxs-lookup"><span data-stu-id="567f5-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="567f5-105">Ja plānam tiek izveidota un piešķirta jauna piemērotības kārtula, tas uzvedina sistēmu atkārtoti izpildīt nodarbinātā piemērotību, lai pārbaudītu, vai nodarbinātais tagad ir piemērots plānam, pamatojoties uz jaunajām piemērotības opcijām.</span><span class="sxs-lookup"><span data-stu-id="567f5-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to re-run worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="567f5-106">Darbvietā **Atvieglojumu pārvaldība** sadaļā **Apstrāde** atlasiet **Likmju izmaiņu atjauninājumu apstrāde**.</span><span class="sxs-lookup"><span data-stu-id="567f5-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="567f5-107">Dialoglodziņā **Izpildīt atvieglojumu likmju atjauninājumu apstrādi** norādiet vērtības tālāk minētajiem laukiem.</span><span class="sxs-lookup"><span data-stu-id="567f5-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="567f5-108">Lauks</span><span class="sxs-lookup"><span data-stu-id="567f5-108">Field</span></span> | <span data-ttu-id="567f5-109">Apraksts</span><span class="sxs-lookup"><span data-stu-id="567f5-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="567f5-110">Reģistrācijas periods</span><span class="sxs-lookup"><span data-stu-id="567f5-110">Enrollment period</span></span> | <span data-ttu-id="567f5-111">Reģistrācijas periods, kuram apstrādāt likmju izmaiņas.</span><span class="sxs-lookup"><span data-stu-id="567f5-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="567f5-112">Ja vēlaties izpildīt apstrādi fonā, atlasiet **Izpildīt fonā** un veiciet tālāk minētos uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="567f5-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="567f5-113">Ievadiet informāciju apstrādei.</span><span class="sxs-lookup"><span data-stu-id="567f5-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="567f5-114">Lai iestatītu periodisku darbu, atlasiet **Periodiskums**, ievadiet periodiskuma informāciju un atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="567f5-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="567f5-115">Lai iestatītu darba brīdinājumu, atlasiet **Brīdinājumi**, atlasiet saņemamos brīdinājumus un pēc tam atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="567f5-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="567f5-116">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="567f5-116">Select **OK**.</span></span> <span data-ttu-id="567f5-117">Apstrāde tiks izpildīta ar iestatītajiem parametriem.</span><span class="sxs-lookup"><span data-stu-id="567f5-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="567f5-118">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="567f5-118">Select **OK**.</span></span>

---
title: Sinhronizēt datumu un laiku importa darbiem
description: Lai izvairītos no problēmām ar laika joslu pārveidošanām, importa darbiem izmantojiet UTC laika zonas.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae04b09a68e64d6d70c0329e689ab08c3903fca0
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798723"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="2f128-103">Sinhronizēt datumu un laiku importa darbiem</span><span class="sxs-lookup"><span data-stu-id="2f128-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f128-104">Ir svarīgi iestatīt jūsu importa darba laika joslu uz universālo koordinēto laiku (UTC).</span><span class="sxs-lookup"><span data-stu-id="2f128-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="2f128-105">Jūs variet redzēt negaidītus datumus un laikus jūsu importētos datos, ja izmantojat citu iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="2f128-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="2f128-106">Bez pareizā iestatījuma importēšanas process pārveido UTC datumu vietējā formātā un tad sistēmas iestatījumi to pārveido vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="2f128-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="2f128-107">Šī dubultā pārveidošana rada datumu maiņu starp programmām.</span><span class="sxs-lookup"><span data-stu-id="2f128-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="2f128-108">Piemēram, dubultā pārveidošana var radīt darbinieka sākuma datumu, kas var atšķirties no vietējo laika joslu atšķirībām Dynamics 365 Human Resources un Dynamics 365 Finance to dēļ.</span><span class="sxs-lookup"><span data-stu-id="2f128-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="2f128-109">Iestatot importa darbu UTC, šī problēma tiek atrisināta.</span><span class="sxs-lookup"><span data-stu-id="2f128-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="2f128-110">Pakalpojumā Dynamics 365 Finance and Operations atlasiet **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="2f128-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="2f128-111">Atlasiet **Importēt projektus** un pēc tam atlasiet projektu.</span><span class="sxs-lookup"><span data-stu-id="2f128-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="2f128-112">Sadaļā **Avota datuma formāts** atlasiet **CSV-unikodu**.</span><span class="sxs-lookup"><span data-stu-id="2f128-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="2f128-113">[![Mainīt avota datuma formātu uz UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="2f128-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="2f128-114">Mainiet **Laika joslu** uz **Universālo koordinēto laika joslu** un nomainiet **Valodu** uz **En-US**.</span><span class="sxs-lookup"><span data-stu-id="2f128-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>



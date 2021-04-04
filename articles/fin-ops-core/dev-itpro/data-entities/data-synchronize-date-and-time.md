---
title: Sinhronizēt datumu un laiku importa darbiem
description: Lai izvairītos no problēmām ar laika joslu pārveidošanām, importa darbiem izmantojiet UTC laika zonas.
author: Sunil-Garg
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ce3bf39e8342d3fe19a253f6d17684b2bd0aec0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570485"
---
# <a name="synchronize-date-and-time-in-import-jobs"></a><span data-ttu-id="fe54e-103">Sinhronizēt datumu un laiku importa darbiem</span><span class="sxs-lookup"><span data-stu-id="fe54e-103">Synchronize date and time in import jobs</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe54e-104">Ir svarīgi iestatīt jūsu importa darba laika joslu uz universālo koordinēto laiku (UTC).</span><span class="sxs-lookup"><span data-stu-id="fe54e-104">It's important to set the time zone for your import job to Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="fe54e-105">Jūs variet redzēt negaidītus datumus un laikus jūsu importētos datos, ja izmantojat citu iestatījumu.</span><span class="sxs-lookup"><span data-stu-id="fe54e-105">You might see unexpected dates and times in your imported data if you use a different setting.</span></span> <span data-ttu-id="fe54e-106">Bez pareizā iestatījuma importēšanas process pārveido UTC datumu vietējā formātā un tad sistēmas iestatījumi to pārveido vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="fe54e-106">Without the correct setting, the import process converts the UTC date to the local format, and then system settings converts it again.</span></span>

<span data-ttu-id="fe54e-107">Šī dubultā pārveidošana rada datumu maiņu starp programmām.</span><span class="sxs-lookup"><span data-stu-id="fe54e-107">This dual conversion causes dates to change between applications.</span></span> <span data-ttu-id="fe54e-108">Piemēram, dubultā pārveidošana var radīt darbinieka sākuma datumu, kas var atšķirties no vietējo laika joslu atšķirībām Dynamics 365 Human Resources un Dynamics 365 Finance to dēļ.</span><span class="sxs-lookup"><span data-stu-id="fe54e-108">For example, the dual conversion could cause an employee's start date to be different between Dynamics 365 Human Resources and Dynamics 365 Finance due to differences in local time zones.</span></span> <span data-ttu-id="fe54e-109">Iestatot importa darbu UTC, šī problēma tiek atrisināta.</span><span class="sxs-lookup"><span data-stu-id="fe54e-109">Setting the import job to UTC resolves this problem.</span></span>

1. <span data-ttu-id="fe54e-110">Pakalpojumā Dynamics 365 Finance and Operations atlasiet **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="fe54e-110">In Dynamics 365 Finance and Operations, select **Data management**.</span></span>

2. <span data-ttu-id="fe54e-111">Atlasiet **Importēt projektus** un pēc tam atlasiet projektu.</span><span class="sxs-lookup"><span data-stu-id="fe54e-111">Select **Import projects**, and then select the project.</span></span>

3. <span data-ttu-id="fe54e-112">Sadaļā **Avota datuma formāts** atlasiet **CSV-unikodu**.</span><span class="sxs-lookup"><span data-stu-id="fe54e-112">Under **Source date format**, select **CSV-Unicode**.</span></span>

   <span data-ttu-id="fe54e-113">[![Mainīt avota datuma formātu uz UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span><span class="sxs-lookup"><span data-stu-id="fe54e-113">[![Change source date format to UTC](./media/data-source-date-format.png)](./media/data-source-date-format.png)</span></span>

4. <span data-ttu-id="fe54e-114">Mainiet **Laika joslu** uz **Universālo koordinēto laika joslu** un nomainiet **Valodu** uz **En-US**.</span><span class="sxs-lookup"><span data-stu-id="fe54e-114">Change **Timezone** to **Coordinated Universal Timezone**, and change **Language** to **En-US**.</span></span>




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
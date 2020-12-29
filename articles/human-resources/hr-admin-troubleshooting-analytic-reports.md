---
title: Problēmu novēršanas analītiskie pārskati
description: Šajā rakstā paskaidrots, kā rīkoties, ja debitora datu izmaiņas neparādās nevienā no debitora darbvietām.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 99d9eb3a16e6470820a2eb0a19c1d50e89bd3d36
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4419577"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="2ca77-103">Problēmu novēršanas analītiskie pārskati</span><span class="sxs-lookup"><span data-stu-id="2ca77-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="2ca77-104">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="2ca77-104">**Issue**</span></span>

<span data-ttu-id="2ca77-105">Debitora datu izmaiņas neparādās nevienas debitora darbvietas cilnē **Analīze**.</span><span class="sxs-lookup"><span data-stu-id="2ca77-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="2ca77-106">**Iemesls**</span><span class="sxs-lookup"><span data-stu-id="2ca77-106">**Cause**</span></span>

<span data-ttu-id="2ca77-107">Pēc noklusējuma Microsoft Power BI pārskati tiek atsvaidzināti ik pēc četrām stundām saskaņā ar pakešuzdevuma Izvietot mērījumu grafiku.</span><span class="sxs-lookup"><span data-stu-id="2ca77-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="2ca77-108">**Izšķirtspēja**</span><span class="sxs-lookup"><span data-stu-id="2ca77-108">**Resolution**</span></span>

<span data-ttu-id="2ca77-109">Šo problēmu var izraisīt laika izvēle.</span><span class="sxs-lookup"><span data-stu-id="2ca77-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="2ca77-110">Rīkojieties šādi, lai palaistu pakešuzdevumu un atjauninātu anal. darbvietas.</span><span class="sxs-lookup"><span data-stu-id="2ca77-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="2ca77-111">Atv. lapu **Pakešuzdevumi** sadaļā **Sist. administr. \> Saites \> Pakešuzd. \> Pakešuzd**.</span><span class="sxs-lookup"><span data-stu-id="2ca77-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="2ca77-112">Vai lietojiet meklēš. un ievadiet **Pakešuzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="2ca77-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="2ca77-113">Atrodiet sarakstā darbu **Izvietot mērījumu**.</span><span class="sxs-lookup"><span data-stu-id="2ca77-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="2ca77-114">Atlasiet **Rediģēt** lapas augšpusē un iestatiet plānotajam sākuma datumam/laikam vērtību, kas atsvaidzinās analīzi tuvāk pašreizējam laikam.</span><span class="sxs-lookup"><span data-stu-id="2ca77-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Pakešuzdevumi](media/batch-jobs.png)

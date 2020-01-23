---
title: Anal. pārskati netiek atjaun.
description: Šajā tēmā paskaidrots, kā rīkoties, ja debitora datu izmaiņas neparādās nevienā no debitora darbvietām.
author: andreabichsel
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: fc2e6259a8f9d17dc0f7652f207acfa53da76a8d
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898577"
---
# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="b0634-103">Anal. pārskati netiek atjaun.</span><span class="sxs-lookup"><span data-stu-id="b0634-103">Analytic reports are not updated</span></span>

<span data-ttu-id="b0634-104">**Izsniegt**</span><span class="sxs-lookup"><span data-stu-id="b0634-104">**Issue**</span></span>

<span data-ttu-id="b0634-105">Debitora datu izmaiņas neparādās nevienas debitora darbvietas cilnē **Analīze**.</span><span class="sxs-lookup"><span data-stu-id="b0634-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="b0634-106">**Iemesls**</span><span class="sxs-lookup"><span data-stu-id="b0634-106">**Cause**</span></span>

<span data-ttu-id="b0634-107">Pēc noklusējuma Microsoft Power BI pārskati tiek atsvaidzināti ik pēc četrām stundām saskaņā ar pakešuzdevuma Izvietot mērījumu grafiku.</span><span class="sxs-lookup"><span data-stu-id="b0634-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="b0634-108">**Izšķirtspēja**</span><span class="sxs-lookup"><span data-stu-id="b0634-108">**Resolution**</span></span>

<span data-ttu-id="b0634-109">Šo problēmu var izraisīt laika izvēle.</span><span class="sxs-lookup"><span data-stu-id="b0634-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="b0634-110">Rīkojieties šādi, lai palaistu pakešuzdevumu un atjauninātu anal. darbvietas.</span><span class="sxs-lookup"><span data-stu-id="b0634-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="b0634-111">Atv. lapu **Pakešuzdevumi** sadaļā **Sist. administr. \> Saites \> Pakešuzd. \> Pakešuzd**.</span><span class="sxs-lookup"><span data-stu-id="b0634-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="b0634-112">Vai lietojiet meklēš. un ievadiet **Pakešuzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="b0634-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="b0634-113">Atrodiet sarakstā darbu **Izvietot mērījumu**.</span><span class="sxs-lookup"><span data-stu-id="b0634-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="b0634-114">Atlasiet **Rediģēt** lapas augšpusē un iestatiet plānotajam sākuma datumam/laikam vērtību, kas atsvaidzinās analīzi tuvāk pašreizējam laikam.</span><span class="sxs-lookup"><span data-stu-id="b0634-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Pakešuzdevumi](media/batch-jobs.png)

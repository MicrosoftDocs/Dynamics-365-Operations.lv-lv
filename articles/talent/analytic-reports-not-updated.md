---
title: "Anal. pārskati netiek atjaun."
description: "Šajā tēmā paskaidrots, kā rīkoties, ja debitora datu izmaiņas neparādās nevienā no debitora darbvietām."
author: Darinkramer
manager: AnnBe
ms.date: 11/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-11-02
ms.dyn365.ops.version: Talent
ms.translationtype: HT
ms.sourcegitcommit: d3f974f94b6c327fd70b8098d24f9e1f1e1e8eeb
ms.openlocfilehash: 46f426a4b0012e87b4d9d21032870ac7fc33c4ae
ms.contentlocale: lv-lv
ms.lasthandoff: 12/04/2018

---

# <a name="analytic-reports-are-not-updated"></a><span data-ttu-id="7c1a7-103">Anal. pārskati netiek atjaun.</span><span class="sxs-lookup"><span data-stu-id="7c1a7-103">Analytic reports are not updated</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7c1a7-104">**Izsniegt**</span><span class="sxs-lookup"><span data-stu-id="7c1a7-104">**Issue**</span></span>

<span data-ttu-id="7c1a7-105">Debitora datu izmaiņas neparādās nevienas debitora darbvietas cilnē **Analīze**.</span><span class="sxs-lookup"><span data-stu-id="7c1a7-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="7c1a7-106">**Iemesls**</span><span class="sxs-lookup"><span data-stu-id="7c1a7-106">**Cause**</span></span>

<span data-ttu-id="7c1a7-107">Pēc noklusējuma Microsoft Power BI pārsk. tiek atsvaidz. ik pēc četrām stundām saskaņā ar pakešuzdevuma “Izvietot mērījumu” grafiku.</span><span class="sxs-lookup"><span data-stu-id="7c1a7-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="7c1a7-108">**Izšķirtspēja**</span><span class="sxs-lookup"><span data-stu-id="7c1a7-108">**Resolution**</span></span>

<span data-ttu-id="7c1a7-109">Šo problēmu var izraisīt laika izvēle.</span><span class="sxs-lookup"><span data-stu-id="7c1a7-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="7c1a7-110">Rīkojieties šādi, lai palaistu pakešuzdevumu un atjauninātu anal. darbvietas.</span><span class="sxs-lookup"><span data-stu-id="7c1a7-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="7c1a7-111">Atv. lapu **Pakešuzdevumi** sadaļā **Sist. administr. \> Saites \> Pakešuzd. \> Pakešuzd**.</span><span class="sxs-lookup"><span data-stu-id="7c1a7-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="7c1a7-112">Vai lietojiet meklēš. un ievadiet **Pakešuzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="7c1a7-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="7c1a7-113">Atrodiet sarakstā darbu **Izvietot mērījumu**.</span><span class="sxs-lookup"><span data-stu-id="7c1a7-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="7c1a7-114">Atlasiet **Rediģēt** lapas augšpusē un iestatiet plānotajam sākuma datumam/laikam vērtību, kas atsvaidzinās analīzi tuvāk pašreizējam laikam.</span><span class="sxs-lookup"><span data-stu-id="7c1a7-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Pakešuzdevumi](media/batch-jobs.png)


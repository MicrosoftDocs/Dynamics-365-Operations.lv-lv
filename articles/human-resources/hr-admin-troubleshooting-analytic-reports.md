---
title: Problēmu novēršanas analītiskie pārskati
description: Šajā rakstā paskaidrots, kā rīkoties, ja debitora datu izmaiņas neparādās nevienā no debitora darbvietām.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: c5e1a1d7044567a07acedf71e65ed244275acfd9
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2021
ms.locfileid: "5113412"
---
# <a name="troubleshoot-analytic-reports"></a><span data-ttu-id="69ded-103">Problēmu novēršanas analītiskie pārskati</span><span class="sxs-lookup"><span data-stu-id="69ded-103">Troubleshoot analytic reports</span></span>

<span data-ttu-id="69ded-104">**Izejas plūsma**</span><span class="sxs-lookup"><span data-stu-id="69ded-104">**Issue**</span></span>

<span data-ttu-id="69ded-105">Debitora datu izmaiņas neparādās nevienas debitora darbvietas cilnē **Analīze**.</span><span class="sxs-lookup"><span data-stu-id="69ded-105">A customer's data changes don't appear on the **Analytics** tabs of any of the customer's workspaces.</span></span>

<span data-ttu-id="69ded-106">**Iemesls**</span><span class="sxs-lookup"><span data-stu-id="69ded-106">**Cause**</span></span>

<span data-ttu-id="69ded-107">Pēc noklusējuma Microsoft Power BI pārskati tiek atsvaidzināti ik pēc četrām stundām saskaņā ar pakešuzdevuma Izvietot mērījumu grafiku.</span><span class="sxs-lookup"><span data-stu-id="69ded-107">By default, Microsoft Power BI reports are refreshed every four hours, according to the schedule of the Deploy measurement batch job.</span></span>

<span data-ttu-id="69ded-108">**Izšķirtspēja**</span><span class="sxs-lookup"><span data-stu-id="69ded-108">**Resolution**</span></span>

<span data-ttu-id="69ded-109">Šo problēmu var izraisīt laika izvēle.</span><span class="sxs-lookup"><span data-stu-id="69ded-109">This issue might just be a matter of timing.</span></span> <span data-ttu-id="69ded-110">Rīkojieties šādi, lai palaistu pakešuzdevumu un atjauninātu anal. darbvietas.</span><span class="sxs-lookup"><span data-stu-id="69ded-110">Follow these steps to start the batch job and update the analytics workspaces.</span></span>

1. <span data-ttu-id="69ded-111">Atv. lapu **Pakešuzdevumi** sadaļā **Sist. administr. \> Saites \> Pakešuzd. \> Pakešuzd**.</span><span class="sxs-lookup"><span data-stu-id="69ded-111">Open the **Batch jobs** page at **System administration \> Links \> Batch jobs \> Batch jobs**.</span></span> <span data-ttu-id="69ded-112">Vai lietojiet meklēš. un ievadiet **Pakešuzdevumi**.</span><span class="sxs-lookup"><span data-stu-id="69ded-112">Alternatively, use Search, and enter **Batch Jobs**.</span></span>
1. <span data-ttu-id="69ded-113">Atrodiet sarakstā darbu **Izvietot mērījumu**.</span><span class="sxs-lookup"><span data-stu-id="69ded-113">Find the **Deploy measurement** job in the list.</span></span>
1. <span data-ttu-id="69ded-114">Atlasiet **Rediģēt** lapas augšpusē un iestatiet plānotajam sākuma datumam/laikam vērtību, kas atsvaidzinās analīzi tuvāk pašreizējam laikam.</span><span class="sxs-lookup"><span data-stu-id="69ded-114">Select **Edit** at the top of the page, and set the scheduled start date/time to a value that will refresh the analytics closer to the current time.</span></span>

![Pakešuzdevumi](media/batch-jobs.png)

---
title: Iestatīt PVN pārskatu kodus
description: PVN pārskatu kodi attiecas uz lauka numuru, kas norādīts PVN pārskatā.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: be24e18da63d1a613c3c6e72f7c767c7af9b6656
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222147"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="524e1-103">Iestatīt PVN pārskatu kodus</span><span class="sxs-lookup"><span data-stu-id="524e1-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="524e1-104">PVN pārskatu kodi attiecas uz lauka numuru, kas norādīts PVN pārskatā.</span><span class="sxs-lookup"><span data-stu-id="524e1-104">The Sales tax reporting codes refer to a field number that's listed on a sales tax report.</span></span> <span data-ttu-id="524e1-105">Tie tiek izmantoti konkrētu valstu pārskata izkārtojumos.</span><span class="sxs-lookup"><span data-stu-id="524e1-105">They are used on country-specific report layouts.</span></span> <span data-ttu-id="524e1-106">Tie tiek izmantoti arī PVN maksājumā pēc koda pārskata.</span><span class="sxs-lookup"><span data-stu-id="524e1-106">They're also used on the Sales tax payment by code report.</span></span> <span data-ttu-id="524e1-107">Šis pārskats rāda PVN summas segšanas periodam, kas apkopotas katram pārskata kodam.</span><span class="sxs-lookup"><span data-stu-id="524e1-107">That report shows sales tax amounts for a settlement period summarized for each reporting code.</span></span> <span data-ttu-id="524e1-108">Kad esat izveidojis PVN pārskata kodus, varat uz šiem kodiem atsaukties Pārskatu iestatīšanas kopsavilkuma cilnēs, kurām varat piekļūt lapā **PVN kods**.</span><span class="sxs-lookup"><span data-stu-id="524e1-108">After you create Sales tax reporting codes, you can refer to those codes on the Report setup FastTabs, which you can access from the **Sales tax code** page.</span></span> 

<span data-ttu-id="524e1-109">Šis paraugs izmanto DEMF demonstrācijas uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="524e1-109">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="524e1-110">Sadaļā **Navigācijas rūts**, pārejiet uz **Nodoklis > Iestatīšana > PVN > PVN pārskatu kodi**.</span><span class="sxs-lookup"><span data-stu-id="524e1-110">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="524e1-111">Klikšķiniet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="524e1-111">Click **New**.</span></span>
3. <span data-ttu-id="524e1-112">Atlasiet pārskata izkārtojumu, kuram atbilst pārskata kods.</span><span class="sxs-lookup"><span data-stu-id="524e1-112">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="524e1-113">Šis izkārtojums tiek izmantots, lai filtrētu pieejamos pārskata kodus PVN kodam.</span><span class="sxs-lookup"><span data-stu-id="524e1-113">This layout is used to filter the available reporting codes for a sales tax code.</span></span> <span data-ttu-id="524e1-114">Katrs PVN kods atbilst maksājumu periodam, kurš saistīts ar PVN iestādi, kas izmanto pārskata izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="524e1-114">Each sales tax code belongs to a settlement period, which belongs to a Sales tax authority, which uses a report layout.</span></span>  
4. <span data-ttu-id="524e1-115">Laukā **Pārskata kods** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="524e1-115">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="524e1-116">Laukā **Pārskata teksts** ievadiet aprakstu, kuru parādīt pārskatos.</span><span class="sxs-lookup"><span data-stu-id="524e1-116">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="524e1-117">Laukā **Īss apraksts** ievadiet aprakstu iekšējai lietošanai.</span><span class="sxs-lookup"><span data-stu-id="524e1-117">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="524e1-118">Noklikšķiniet uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="524e1-118">Click **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
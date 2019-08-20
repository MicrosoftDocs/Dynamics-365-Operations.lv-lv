---
title: Iestatīt PVN pārskatu kodus
description: PVN pārskatu kodi attiecas uz lauka numuru PVN pārskatā.
author: twheeloc
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 830a3465944b32cc17feee60e3cbc5ad0a4dc9d7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834779"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="9f353-103">Iestatīt PVN pārskatu kodus</span><span class="sxs-lookup"><span data-stu-id="9f353-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f353-104">PVN pārskatu kodi attiecas uz lauka numuru PVN pārskatā.</span><span class="sxs-lookup"><span data-stu-id="9f353-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="9f353-105">Tos izmanto valstij atbilstošu pārskatu izkārtojumos un PVN maksājumu pārskatā pēc kodiem, lai drukātu PVN summas apmaksas periodā, summējot pēc pārskata koda.</span><span class="sxs-lookup"><span data-stu-id="9f353-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="9f353-106">Kad esat izveidojis PVN pārskata kodus, varat uz tiem atsaukties Pārskatu iestatīšanas kopsavilkuma cilnē PVN koda lapā.</span><span class="sxs-lookup"><span data-stu-id="9f353-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="9f353-107">Šis paraugs izmanto DEMF demonstrācijas uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="9f353-107">This recording uses the DEMF demo company.</span></span>



1. <span data-ttu-id="9f353-108">Dodieties uz Nodokļi > Iestatīšana > PVN > PVN pārskata kodi.</span><span class="sxs-lookup"><span data-stu-id="9f353-108">Go to Tax > Setup > Sales tax > Sales tax reporting codes.</span></span>
2. <span data-ttu-id="9f353-109">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="9f353-109">Click New.</span></span>
3. <span data-ttu-id="9f353-110">Atlasiet pārskata izkārtojumu, kuram atbilst pārskata kods.</span><span class="sxs-lookup"><span data-stu-id="9f353-110">Select the report layout that the reporting code belongs to.</span></span>
    * <span data-ttu-id="9f353-111">Šis izkārtojums tiek izmantots, lai filtrētu pieejamos pārskata kodus PVN kodam.</span><span class="sxs-lookup"><span data-stu-id="9f353-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="9f353-112">Katrs PVN kods atbilst maksājumu periodam, kurš saistīts ar PVN iestādi, kas izmanto pārskata izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="9f353-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="9f353-113">Ievadiet numuru, kas ir saistīts ar lauku PVN pārskatā.</span><span class="sxs-lookup"><span data-stu-id="9f353-113">Enter a number that refers to a field on a sales tax report.</span></span>
5. <span data-ttu-id="9f353-114">Pārskata teksta laukā ievadiet aprakstu, kuru parādīt pārskatos.</span><span class="sxs-lookup"><span data-stu-id="9f353-114">In the Report text field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="9f353-115">Laukā Īss apraksts ievadiet aprakstu iekšējai lietošanai.</span><span class="sxs-lookup"><span data-stu-id="9f353-115">In the Brief description field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="9f353-116">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="9f353-116">Click Save.</span></span>


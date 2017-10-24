---
title: "Pārdošanas pārraudzība un uzcenojuma veiktspēja"
description: "Izmantojot programmatūru Microsoft Dynamics 365 for Retail, varat reāllaikā pārraudzīt pārdošanu un uzcenojuma veiktspēju."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations, Retail
ms.custom: 85123
ms.assetid: ddd15820-c3e6-4607-819e-8cef744ce9c9
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c2442f27221e429761abb8c1b17c50a737c10795
ms.contentlocale: lv-lv
ms.lasthandoff: 09/29/2017

---

# <a name="monitor-sales-and-margin-performance"></a><span data-ttu-id="34a91-103">Pārraudzīt pārdošanas un uzcenojuma veiktspēju</span><span class="sxs-lookup"><span data-stu-id="34a91-103">Monitor sales and margin performance</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="34a91-104">Izmantojot programmatūru Microsoft Dynamics 365 for Retail, varat reāllaikā pārraudzīt pārdošanu un uzcenojuma veiktspēju.</span><span class="sxs-lookup"><span data-stu-id="34a91-104">You can monitor sales and margin performance in real time using Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="34a91-105">Programmatūrā Dynamics 365 for Retail lietotāji var reāllaikā pārraudzīt tālāk norādīto dimensiju pārdošanas un uzcenojuma veiktspēju dažādos organizācijas hierarhijas līmeņos.</span><span class="sxs-lookup"><span data-stu-id="34a91-105">As part of Dynamics 365 for Retail, users can monitor sales and margin performance in real time across different levels of the organization hierarchy for the following dimensions:</span></span>

-   <span data-ttu-id="34a91-106">Preces</span><span class="sxs-lookup"><span data-stu-id="34a91-106">Products</span></span>
-   <span data-ttu-id="34a91-107">Kategorijas</span><span class="sxs-lookup"><span data-stu-id="34a91-107">Categories</span></span>
-   <span data-ttu-id="34a91-108">Atlaides</span><span class="sxs-lookup"><span data-stu-id="34a91-108">Discounts</span></span>
-   <span data-ttu-id="34a91-109">Gadi kā laika periods</span><span class="sxs-lookup"><span data-stu-id="34a91-109">Years as time period</span></span>
-   <span data-ttu-id="34a91-110">Reģistri/termināļi</span><span class="sxs-lookup"><span data-stu-id="34a91-110">Registers/terminals</span></span>
-   <span data-ttu-id="34a91-111">Personāls/darbinieki</span><span class="sxs-lookup"><span data-stu-id="34a91-111">Staff/employees</span></span>
-   <span data-ttu-id="34a91-112">Debitori</span><span class="sxs-lookup"><span data-stu-id="34a91-112">Customers</span></span>
-   <span data-ttu-id="34a91-113">Pārvaldības struktūrvienības</span><span class="sxs-lookup"><span data-stu-id="34a91-113">Operating units</span></span>

<span data-ttu-id="34a91-114">Turklāt divi unikāli pārskati, kuri izmanto hierarhijas režģa strukturēšanu, ļauj lietotājiem pārraudzīt pārdošanu un uzcenojuma veiktspēju, veicot detalizētu aplūkošanu no augšējā kategorijas līmeņa līdz atsevišķiem kategorijas lapu mezgliem noklusējuma mazumtirdzniecības preces kategorijas hierarhijā.</span><span class="sxs-lookup"><span data-stu-id="34a91-114">Additionally, two unique reports that take advantage of hierarchical grid structuring let users monitor sales and margin performance by drilling down from the top category node to individual leaf nodes of the category in the default retail product category hierarchy.</span></span> <span data-ttu-id="34a91-115">Lietotāji var arī veikt detalizētu aplūkošanu no augšējās pārvaldības struktūrvienības līdz atsevisķam kanālam organizācijas hierarhijā, kas ir definēta kā noklusējuma organizācijas hierarhija mazumtirdzniecības pārskatu veidošanas hierarhijas nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="34a91-115">Users can also drill-down from the top operating unit to an individual channel in the organization hierarchy that is defined as the default organization hierarchy for retail reporting hierarchy purposes.</span></span> <span data-ttu-id="34a91-116">Pārskatus var atvērt no šādām vietām:</span><span class="sxs-lookup"><span data-stu-id="34a91-116">You can open the reports from any of the following locations:</span></span>

-   <span data-ttu-id="34a91-117">Darbvieta **Mazumtirdzniecības veikala pārvaldība** &gt; **Mazumtirdzniecība** &gt; **Kanāli** &gt; **Mazumtirdzniecības veikala pārvaldība** &gt; **Pārskati**</span><span class="sxs-lookup"><span data-stu-id="34a91-117">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports**</span></span>
-   <span data-ttu-id="34a91-118">Darbvieta **Kategorijas un preču pārvaldība** &gt; **Mazumtirdzniecība** &gt; **Preces un kategorijas** &gt; **Mazumtirdzniecības veikala pārvaldība** &gt; **Pārskati**</span><span class="sxs-lookup"><span data-stu-id="34a91-118">**Category and product management** workspace &gt; **Retail** &gt; **Product and categories** &gt; **Retail store management** &gt; **Reports**</span></span>
-   <span data-ttu-id="34a91-119">Darbvieta **Cenu noteikšanas un atlaižu pārvaldība** &gt; **Mazumtirdzniecība** &gt; **Cenu noteikšana un atlaides** &gt; **Mazumtirdzniecības veikala pārvaldība** &gt; **Pārskati**</span><span class="sxs-lookup"><span data-stu-id="34a91-119">**Pricing and discount management** workspace &gt; **Retail** &gt; **Pricing and discounts** &gt; **Retail store management** &gt; **Reports**</span></span>
-   <span data-ttu-id="34a91-120">Sadaļa **Pieprasījumi un pārskati** &gt; **Mazumtirdzniecība** &gt; **Pieprasījumi un pārskati** &gt; **Pārdošanas pārskati**</span><span class="sxs-lookup"><span data-stu-id="34a91-120">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports**</span></span>




---
title: Kreditoru meklēšana
description: Uzziniet kā meklēt kreditorus, balstoties uz noteiktiem kritērijiem.
author: RichardLuan
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendSearchCriterion, VendSearchAddCategory, VendSearchAddReviewCriterionGroup, VendSearchResults, VendSearchAddReviewCriterion
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf93307600aac6fa6e45524092ec4811742010e4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244043"
---
# <a name="search-for-vendors"></a><span data-ttu-id="67efa-103">Kreditoru meklēšana</span><span class="sxs-lookup"><span data-stu-id="67efa-103">Search for vendors</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67efa-104">Uzziniet kā meklēt kreditorus, balstoties uz noteiktiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="67efa-104">Learn how to search for vendors based on specific criteria.</span></span> <span data-ttu-id="67efa-105">Šajā piemērā parādīts, kā meklēt kreditorus, kas ir apstiprināti konkrētai sagādes kategorijai un kuriem primārā adrese atrodas konkrētā valstī.</span><span class="sxs-lookup"><span data-stu-id="67efa-105">This example shows you how to search for vendors that are approved for a particular procurement category and have their primary address in a specific country.</span></span> <span data-ttu-id="67efa-106">Šo procedūru varat izpildīt, izmantojot demonstrācijas datu uzņēmumu USMF vai izmantojot savus datus.</span><span class="sxs-lookup"><span data-stu-id="67efa-106">You can run this procedure in demo data company USMF, or on your own data.</span></span> <span data-ttu-id="67efa-107">Šo uzdevumu parasti veic sagādes speciālists.</span><span class="sxs-lookup"><span data-stu-id="67efa-107">This task would usually be carried out by a procurement professional.</span></span>

1. <span data-ttu-id="67efa-108">Pārejiet uz sadaļu Sagāde un avoti > Kreditori > Kreditoru meklēšana.</span><span class="sxs-lookup"><span data-stu-id="67efa-108">Go to Procurement and sourcing > Vendors > Vendor search.</span></span>
2. <span data-ttu-id="67efa-109">Noklikšķiniet uz Plus ikonas, lai atvērtu lapu Sagādes kategorijas atlase.</span><span class="sxs-lookup"><span data-stu-id="67efa-109">Click on the Plus icon to open the Procurement category selection page.</span></span>  
3. <span data-ttu-id="67efa-110">Koka struktūrā atlasiet "KORP. SAGĀDES KATEGORIJAS\BIROJA APARATŪRA".</span><span class="sxs-lookup"><span data-stu-id="67efa-110">In the tree, select 'CORP PROCUREMENT CATEGORIES\OFFICE MACHINES'.</span></span>
    * <span data-ttu-id="67efa-111">Ja šo procedūru veicāt ka uzdevuma ceļvedi, iespējams, lai šo atlasītu pareizo zaru, jums būs jānoklikšķina uz pogas Atbloķēt.</span><span class="sxs-lookup"><span data-stu-id="67efa-111">If you're running this procedure as a task guide, you may have to click the Unlock button before you can select the correct node.</span></span> <span data-ttu-id="67efa-112">Ja neizmantojat USMF, atlasiet vienu no jums esošām kategorijām.</span><span class="sxs-lookup"><span data-stu-id="67efa-112">If you're not using USMF, select one of the categories that you have.</span></span>  
4. <span data-ttu-id="67efa-113">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="67efa-113">Click Add.</span></span>
    * <span data-ttu-id="67efa-114">Šeit ir iespējams atlasīt vairāk nekā vienu kategoriju.</span><span class="sxs-lookup"><span data-stu-id="67efa-114">It's possible to select more than one category here.</span></span> <span data-ttu-id="67efa-115">Ja to izdarīt, meklēšanas laikā tiks atrasti visi kreditori, kas ir apstiprināti vismaz vienai no kategorijām.</span><span class="sxs-lookup"><span data-stu-id="67efa-115">If you do so, the search will find all the vendors that are approved for at least one of the categories.</span></span>  
5. <span data-ttu-id="67efa-116">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="67efa-116">Click OK.</span></span>
6. <span data-ttu-id="67efa-117">Laukā Valsts/reģions ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="67efa-117">In the Country/region field, type a value.</span></span>
7. <span data-ttu-id="67efa-118">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="67efa-118">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
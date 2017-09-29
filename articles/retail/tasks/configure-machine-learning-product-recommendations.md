--- 
title: " Algoritmiskās mācīšanās produktu ieteikumu konfigurēšana"
description: "Veicot šo procedūru, tiek atjaunoti dati elementu krātuvē, ko izmanto algoritmiskās mācīšanās sistēma, kura nodrošina ieteikumus par preci un pēc tam nodrošina ieteikumus par preci POS klientiem."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e32c7cf1283487cb7a52f7d8e261b6b587b76364
ms.contentlocale: lv-lv
ms.lasthandoff: 08/29/2017

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="0e7cc-103"> Algoritmiskās mācīšanās produktu ieteikumu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="0e7cc-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0e7cc-104">Veicot šo procedūru, tiek atjaunoti dati elementu krātuvē, ko izmanto algoritmiskās mācīšanās sistēma, kura nodrošina ieteikumus par preci un pēc tam nodrošina ieteikumus par preci POS klientiem.</span><span class="sxs-lookup"><span data-stu-id="0e7cc-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="0e7cc-105">Šajā procedūrā tiek izmantoti demonstrācijas uzņēmuma “USRT” dati.</span><span class="sxs-lookup"><span data-stu-id="0e7cc-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="0e7cc-106">Dodieties uz sadaļu Sistēmas administrēšana > Iestatījumi > Elementu krātuve.</span><span class="sxs-lookup"><span data-stu-id="0e7cc-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="0e7cc-107">Sarakstā atrodiet un atlasiet ierakstu RetailSales.</span><span class="sxs-lookup"><span data-stu-id="0e7cc-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="0e7cc-108">Noklikšķiniet uz Atsvaidzināt.</span><span class="sxs-lookup"><span data-stu-id="0e7cc-108">Click Refresh.</span></span>
4. <span data-ttu-id="0e7cc-109">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="0e7cc-109">Click OK.</span></span>
5. <span data-ttu-id="0e7cc-110">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0e7cc-110">Close the page.</span></span>
6. <span data-ttu-id="0e7cc-111">Pārejiet uz sadaļu Mazumtirdzniecība un komercija > Centrālā biroja iestatīšana > Parametri > Mazumtirdzniecības parametri.</span><span class="sxs-lookup"><span data-stu-id="0e7cc-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="0e7cc-112">Noklikšķiniet uz cilnes Algoritmiskā mācīšanās.</span><span class="sxs-lookup"><span data-stu-id="0e7cc-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="0e7cc-113">Laukā Iespējot ieteikumus par preci atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="0e7cc-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="0e7cc-114">Ja tiek parādīts ziņojums “Ieteikumu modeļus nevar izgūt”, tas notiek tāpēc, ka pavisam nesen ir atsvaidzināts elementu krātuve un, iespējams, ka vēl nav pabeigta jauno datu iekļaušana sistēmā.</span><span class="sxs-lookup"><span data-stu-id="0e7cc-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="0e7cc-115">Uzgaidiet 2–3 stundas un mēģiniet vēlreiz.</span><span class="sxs-lookup"><span data-stu-id="0e7cc-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="0e7cc-116">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="0e7cc-116">Click Save.</span></span>
10. <span data-ttu-id="0e7cc-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="0e7cc-117">Close the page.</span></span>



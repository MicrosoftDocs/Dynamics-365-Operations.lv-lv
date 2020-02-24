---
title: Veikala preču klāstā neietvertu preču pārdošana un atgriešana
description: Izmantojot programmu Dynamics 365 Commerce, varat pārdot un atgriezt preces, kas nav ietvertas preču klāstos.
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 86c6ecf9ef67ca3ac4ed3c44d930acaa965112b6
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023311"
---
# <a name="sell-and-return-products-that-arent-part-of-a-stores-assortment"></a><span data-ttu-id="590b8-103">Veikala preču klāstā neietvertu preču pārdošana un atgriešana</span><span class="sxs-lookup"><span data-stu-id="590b8-103">Sell and return products that aren't part of a store's assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="590b8-104">Bieži izmantots scenārijs visiem mazumtirgotājiem ir preču pārdošana saviem klientiem vai atgriezto preču pieņemšana no tiem, pat ja konkrētās preces nav pieejamas veikalā (citiem vārdiem sakot, preces nav veikala sortimentā).</span><span class="sxs-lookup"><span data-stu-id="590b8-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don't carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>

<span data-ttu-id="590b8-105">Tālāk uzskaitīti daži tipiski scenāriji.</span><span class="sxs-lookup"><span data-stu-id="590b8-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="590b8-106">Mazumtirgotājam nav jānodrošina visu savu preču pieejamība konkrētā veikalā.</span><span class="sxs-lookup"><span data-stu-id="590b8-106">A retailer doesn't carry all its products in a specific store.</span></span> <span data-ttu-id="590b8-107">Pārējās preces tiek glabātas noliktavā.</span><span class="sxs-lookup"><span data-stu-id="590b8-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="590b8-108">Veikala darbinieks var palīdzēt klientam meklēt vai pārlūkot preces noliktavā, pievienot tās grozam un veikt norēķināšanos, izvēloties piegādes metodi, piemēram, piegādi uz adresi no noliktavas, vai arī klients preci var saņemt pašreizējā vai citā veikalā.</span><span class="sxs-lookup"><span data-stu-id="590b8-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="590b8-109">Mazumtirgotājam nav jānodrošina konkrētu preču pieejamība veikalā, kuru klients apmeklē, ja preces ir pieejamas citos veikalos.</span><span class="sxs-lookup"><span data-stu-id="590b8-109">A retailer doesn't carry specific products in the store or doesn't have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="590b8-110">Veikala darbinieks var palīdzēt klientam meklēt vai pārlūkot preces citā veikalā, pievienot tās grozam un veikt norēķināšanos, izvēloties piegādes metodi.</span><span class="sxs-lookup"><span data-stu-id="590b8-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="590b8-111">Mazumtirgotājam ir vairāki veikali noteiktā pilsētā un tās tuvumā vai pasta indeksa teritorijā, un mazumtirgotājs nevēlas likt klientiem atgriezt preces tajā pašā veikalā, kurā tās iegādājās.</span><span class="sxs-lookup"><span data-stu-id="590b8-111">A retailer has many stores in and around a specific city or zip code and doesn't want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="590b8-112">Tā vietā klienti var atgriezt preces jebkurā veikalā.</span><span class="sxs-lookup"><span data-stu-id="590b8-112">Instead, customers can return products to any store.</span></span>

<span data-ttu-id="590b8-113">Šie izplatītie scenāriji ir pieejami mazumtirgotājiem, kuri izmanto programmu Commerce.</span><span class="sxs-lookup"><span data-stu-id="590b8-113">Those common scenarios are available for retailers using Commerce.</span></span> <span data-ttu-id="590b8-114">Izmantojot Commerce, var veikt šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="590b8-114">With Commerce, you can:</span></span>

+ <span data-ttu-id="590b8-115">meklēt vai pārlūkot preces citos veikalos;</span><span class="sxs-lookup"><span data-stu-id="590b8-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="590b8-116">meklēt vai pārlūkot visas izlaistās preces;</span><span class="sxs-lookup"><span data-stu-id="590b8-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="590b8-117">izveidot “pārdošana skaidrā naudā bez piegādes” transakcijas vai klientu pasūtījumus;</span><span class="sxs-lookup"><span data-stu-id="590b8-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="590b8-118">atlasīt piegādes opcijas klientu pasūtījumiem;</span><span class="sxs-lookup"><span data-stu-id="590b8-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="590b8-119">izsniegt preces pašreizējā vai citā veikalā;</span><span class="sxs-lookup"><span data-stu-id="590b8-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="590b8-120">atcelt pasūtījumu pašreizējā vai citā veikalā;</span><span class="sxs-lookup"><span data-stu-id="590b8-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="590b8-121">atgriezt pasūtījumu ar vai bez čeka (kvīts) pašreizējā vai citā veikalā.</span><span class="sxs-lookup"><span data-stu-id="590b8-121">Return an order with or without the receipt at the current store or another store.</span></span>

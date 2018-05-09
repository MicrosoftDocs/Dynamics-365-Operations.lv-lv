---
title: "Preču preču klāstā neesošu preču pārdošana un atgriešana"
description: "Izmantojot Dynamics 365 for Retail, varat pārdot un atgriezt preces ārpus preču klāsta."
author: pdp1207
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailAssortmentDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.search.region: Global
ms.search.industry: retail
ms.author: prabhup
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0903879f7fa11c80e695dcb095ce1020984addf6
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="sell-and-return-products-outside-of-an-assortment"></a><span data-ttu-id="44bbe-103">Preču preču klāstā neesošu preču pārdošana un atgriešana</span><span class="sxs-lookup"><span data-stu-id="44bbe-103">Sell and return products outside of an assortment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="44bbe-104">Visbiežākais scenārijs visiem mazumtirgotājiem ir preču pārdošana saviem klientiem vai atgriezto preču pieņemšana no tiem, pat ja konkrētās preces nav pieejamas veikalā (citiem vārdiem sakot, preces nav veikala sortimentā).</span><span class="sxs-lookup"><span data-stu-id="44bbe-104">A common scenario for any retailer is to sell products to their customers or accept returns from their customers even if they don’t carry the specific products in their store (in other words, the products are not assorted to the store).</span></span>
<span data-ttu-id="44bbe-105">Tālāk uzskaitīti daži tipiski scenāriji.</span><span class="sxs-lookup"><span data-stu-id="44bbe-105">Here are some typical scenarios:</span></span>

+ <span data-ttu-id="44bbe-106">Mazumtirgotājam nav jānodrošina visu savu preču pieejamība konkrētā veikalā.</span><span class="sxs-lookup"><span data-stu-id="44bbe-106">A retailer doesn’t carry all its products in a specific store.</span></span> <span data-ttu-id="44bbe-107">Pārējās preces tiek glabātas noliktavā.</span><span class="sxs-lookup"><span data-stu-id="44bbe-107">The remaining products are stored in the warehouse.</span></span> <span data-ttu-id="44bbe-108">Veikala darbinieks var palīdzēt klientam meklēt vai pārlūkot preces noliktavā, pievienot tās grozam un veikt norēķināšanos, izvēloties piegādes metodi, piemēram, piegādi uz adresi no noliktavas, vai arī klients preci var saņemt pašreizējā vai citā veikalā.</span><span class="sxs-lookup"><span data-stu-id="44bbe-108">The store associate can assist the customer by searching or browsing for the products in the warehouse, add them to the cart, and complete the checkout by selecting a delivery method, such as shipping to an address from the warehouse or letting the customer pick up the product from the current store or from another store.</span></span>
+ <span data-ttu-id="44bbe-109">Mazumtirgotājam nav jānodrošina konkrētu preču pieejamība veikalā, kuru klients apmeklē, ja preces ir pieejamas citos veikalos.</span><span class="sxs-lookup"><span data-stu-id="44bbe-109">A retailer doesn’t carry specific products in the store or doesn’t have them in stock at the store the customer visited, but the products are available in other stores.</span></span> <span data-ttu-id="44bbe-110">Veikala darbinieks var palīdzēt klientam meklēt vai pārlūkot preces citā veikalā, pievienot tās grozam un veikt norēķināšanos, izvēloties piegādes metodi.</span><span class="sxs-lookup"><span data-stu-id="44bbe-110">The store associate can assist the customer by searching or browsing the products in the other store, add them to the cart, and complete the checkout by selecting a delivery method.</span></span>
+ <span data-ttu-id="44bbe-111">Mazumtirgotājam ir vairāki veikali noteiktā pilsētā un tās tuvumā vai pasta indeksa teritorijā, un mazumtirgotājs nevēlas likt klientiem atgriezt preces tajā pašā veikalā, kurā tās iegādājās.</span><span class="sxs-lookup"><span data-stu-id="44bbe-111">A retailer has many stores in and around a specific city or zip code and doesn’t want to force the customers to return products to the same store they were purchased in.</span></span> <span data-ttu-id="44bbe-112">Tā vietā klienti var atgriezt preces jebkurā veikalā.</span><span class="sxs-lookup"><span data-stu-id="44bbe-112">Instead, customers can return products to any store.</span></span>


<span data-ttu-id="44bbe-113">Šie visbiežākie scenāriji ir pieejami mazumtirgotājiem, kuri izmanto Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="44bbe-113">Those common scenarios are available for retailers using Dynamics 365 for Retail.</span></span> <span data-ttu-id="44bbe-114">Izmantojot Retail, var veikt šādas darbības:</span><span class="sxs-lookup"><span data-stu-id="44bbe-114">With Retail, you can:</span></span>
+ <span data-ttu-id="44bbe-115">meklēt vai pārlūkot preces citos veikalos;</span><span class="sxs-lookup"><span data-stu-id="44bbe-115">Search or browse products at other stores.</span></span>
+ <span data-ttu-id="44bbe-116">meklēt vai pārlūkot visas izlaistās preces;</span><span class="sxs-lookup"><span data-stu-id="44bbe-116">Search or browse all released products.</span></span>
+ <span data-ttu-id="44bbe-117">izveidot “pārdošana skaidrā naudā bez piegādes” transakcijas vai klientu pasūtījumus;</span><span class="sxs-lookup"><span data-stu-id="44bbe-117">Create cash-and-carry transactions or customer orders.</span></span>
+ <span data-ttu-id="44bbe-118">atlasīt piegādes opcijas klientu pasūtījumiem;</span><span class="sxs-lookup"><span data-stu-id="44bbe-118">Select delivery options for customer orders.</span></span>
+ <span data-ttu-id="44bbe-119">izsniegt preces pašreizējā vai citā veikalā;</span><span class="sxs-lookup"><span data-stu-id="44bbe-119">Pick up products at the current store or another store.</span></span>
+ <span data-ttu-id="44bbe-120">atcelt pasūtījumu pašreizējā vai citā veikalā;</span><span class="sxs-lookup"><span data-stu-id="44bbe-120">Cancel an order at the current store or another store.</span></span>
+ <span data-ttu-id="44bbe-121">atgriezt pasūtījumu ar vai bez čeka (kvīts) pašreizējā vai citā veikalā.</span><span class="sxs-lookup"><span data-stu-id="44bbe-121">Return an order with or without the receipt at the current store or another store.</span></span>


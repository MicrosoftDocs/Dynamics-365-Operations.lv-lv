---
title: EUR-00015 Pušu meklēšana pēc PVN ID
description: Šajā procedūrā ir parādīts, kā pabeigt puses meklēšanu, izmantojot reģistrācijas ID.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DirPartyTable, DirPartTaxRegistrationSearch
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 401971b6f146f1df028291ba0f691ccac5f1966d
ms.sourcegitcommit: b92c3e1b3403d0455fc4e0bf9132d6bc0d7aba5e
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/18/2020
ms.locfileid: "3139001"
---
# <a name="eur-00015-party-search-using-vat-id"></a><span data-ttu-id="8372d-103">EUR-00015 Pušu meklēšana pēc PVN ID</span><span class="sxs-lookup"><span data-stu-id="8372d-103">EUR-00015 Party search using VAT ID</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8372d-104">Šajā procedūrā ir parādīts, kā pabeigt puses meklēšanu, izmantojot reģistrācijas ID.</span><span class="sxs-lookup"><span data-stu-id="8372d-104">This procedure shows how to complete a party search using a registration ID.</span></span> <span data-ttu-id="8372d-105">Lai varētu veikt šo procedūru, jums ir jāiestata PVN ID un jāievada PVN ID kreditoriem, debitoriem vai juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="8372d-105">Before you can complete this procedure, you must set up VAT IDs and enter any VAT IDs for vendors, customers, or legal entities.</span></span>

<span data-ttu-id="8372d-106">Šī procedūra attiecas uz visām Eiropas valstīm/reģioniem.</span><span class="sxs-lookup"><span data-stu-id="8372d-106">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="8372d-107">Šī procedūra ir izveidota, izmantojot demonstrācijas datu uzņēmumu DEMF, kura primārā adrese ir Vācijā.</span><span class="sxs-lookup"><span data-stu-id="8372d-107">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="8372d-108">Šī procedūra ir paredzēta kreditoriem maksājamo parādu vadītājam vai debitoru parādu vadītājam.</span><span class="sxs-lookup"><span data-stu-id="8372d-108">This procedure is intended for an accounts payable manager or accounts receivable manager.</span></span> <span data-ttu-id="8372d-109">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="8372d-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="8372d-110">Dodieties uz Organizācijas administrēšana > Globālā adrešu grāmata > Globālā adrešu grāmata.</span><span class="sxs-lookup"><span data-stu-id="8372d-110">Go to Organization administration > Global address book > Global address book.</span></span>
2. <span data-ttu-id="8372d-111">Noklikšķiniet uz Reģistrācijas ID meklēšana.</span><span class="sxs-lookup"><span data-stu-id="8372d-111">Click Registration ID search.</span></span>
3. <span data-ttu-id="8372d-112">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="8372d-112">Click Add.</span></span>
4. <span data-ttu-id="8372d-113">Laukā Reģistrācijas tips ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8372d-113">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="8372d-114">Piemēram, ja vēlējāties atrastu puses, izmantojot PVN ID tipa reģistrācijas ID, atlasiet PVN ID.</span><span class="sxs-lookup"><span data-stu-id="8372d-114">For example, if you wanted to find parties with a registration ID of type VAT ID, select VAT ID.</span></span>  
5. <span data-ttu-id="8372d-115">Laukā Valsts/reģions ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="8372d-115">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="8372d-116">Piemēram, ievadiet DEU.</span><span class="sxs-lookup"><span data-stu-id="8372d-116">For example, enter DEU.</span></span>  
6. <span data-ttu-id="8372d-117">Laukā Reģistrācijas numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="8372d-117">In the Registration number field, type a value.</span></span>
7. <span data-ttu-id="8372d-118">Noklikšķiniet uz Meklēt.</span><span class="sxs-lookup"><span data-stu-id="8372d-118">Click Find.</span></span>
    * <span data-ttu-id="8372d-119">Tiks parādītas visas puses ar šo reģistrācijas ID.</span><span class="sxs-lookup"><span data-stu-id="8372d-119">All parties with that registration ID will be displayed.</span></span>  


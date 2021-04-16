---
title: EUR-00015 Pušu meklēšana pēc PVN ID
description: Šajā procedūrā ir parādīts, kā pabeigt puses meklēšanu, izmantojot reģistrācijas ID.
author: v-oloski
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DirPartyTable, DirPartTaxRegistrationSearch
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8e5cbbbc15a0e33afb04f00d8b1a0b0cd5cab2c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821790"
---
# <a name="eur-00015-party-search-using-vat-id"></a><span data-ttu-id="2c31c-103">EUR-00015 Pušu meklēšana pēc PVN ID</span><span class="sxs-lookup"><span data-stu-id="2c31c-103">EUR-00015 Party search using VAT ID</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c31c-104">Šajā procedūrā ir parādīts, kā pabeigt puses meklēšanu, izmantojot reģistrācijas ID.</span><span class="sxs-lookup"><span data-stu-id="2c31c-104">This procedure shows how to complete a party search using a registration ID.</span></span> <span data-ttu-id="2c31c-105">Lai varētu veikt šo procedūru, jums ir jāiestata PVN ID un jāievada PVN ID kreditoriem, debitoriem vai juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="2c31c-105">Before you can complete this procedure, you must set up VAT IDs and enter any VAT IDs for vendors, customers, or legal entities.</span></span>

<span data-ttu-id="2c31c-106">Šī procedūra attiecas uz visām Eiropas valstīm/reģioniem.</span><span class="sxs-lookup"><span data-stu-id="2c31c-106">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="2c31c-107">Šī procedūra ir izveidota, izmantojot demonstrācijas datu uzņēmumu DEMF, kura primārā adrese ir Vācijā.</span><span class="sxs-lookup"><span data-stu-id="2c31c-107">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="2c31c-108">Šī procedūra ir paredzēta kreditoriem maksājamo parādu vadītājam vai debitoru parādu vadītājam.</span><span class="sxs-lookup"><span data-stu-id="2c31c-108">This procedure is intended for an accounts payable manager or accounts receivable manager.</span></span> <span data-ttu-id="2c31c-109">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="2c31c-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="2c31c-110">Dodieties uz Organizācijas administrēšana > Globālā adrešu grāmata > Globālā adrešu grāmata.</span><span class="sxs-lookup"><span data-stu-id="2c31c-110">Go to Organization administration > Global address book > Global address book.</span></span>
2. <span data-ttu-id="2c31c-111">Noklikšķiniet uz Reģistrācijas ID meklēšana.</span><span class="sxs-lookup"><span data-stu-id="2c31c-111">Click Registration ID search.</span></span>
3. <span data-ttu-id="2c31c-112">Noklikšķiniet uz Pievienot.</span><span class="sxs-lookup"><span data-stu-id="2c31c-112">Click Add.</span></span>
4. <span data-ttu-id="2c31c-113">Laukā Reģistrācijas tips ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2c31c-113">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="2c31c-114">Piemēram, ja vēlējāties atrastu puses, izmantojot PVN ID tipa reģistrācijas ID, atlasiet PVN ID.</span><span class="sxs-lookup"><span data-stu-id="2c31c-114">For example, if you wanted to find parties with a registration ID of type VAT ID, select VAT ID.</span></span>  
5. <span data-ttu-id="2c31c-115">Laukā Valsts/reģions ievadiet vai atlasiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="2c31c-115">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="2c31c-116">Piemēram, ievadiet DEU.</span><span class="sxs-lookup"><span data-stu-id="2c31c-116">For example, enter DEU.</span></span>  
6. <span data-ttu-id="2c31c-117">Laukā Reģistrācijas numurs ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="2c31c-117">In the Registration number field, type a value.</span></span>
7. <span data-ttu-id="2c31c-118">Noklikšķiniet uz Meklēt.</span><span class="sxs-lookup"><span data-stu-id="2c31c-118">Click Find.</span></span>
    * <span data-ttu-id="2c31c-119">Tiks parādītas visas puses ar šo reģistrācijas ID.</span><span class="sxs-lookup"><span data-stu-id="2c31c-119">All parties with that registration ID will be displayed.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
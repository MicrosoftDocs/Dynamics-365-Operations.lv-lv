---
title: Maksājuma metožu izmantošanas ierobežošana atgriešanām bez kvīts
description: Šajā tēmā ir aprakstīts, kā var ierobežot noteiktu maksājumu veidu izmantošanu atmaksai, ja atgriešanas tiek veiktas bez kvīts.
author: rapraj
manager: AnnBe
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.custom: 15831
ms.assetid: 465893a5-6b4f-4c5f-b305-db071df2d33f
ms.search.region: global
ms.search.industry: Retail
ms.author: yabinl
ms.search.validFrom: 2019-02-01
ms.dyn365.ops.version: AX 10.0.0, Retail Feb 2019 update
ms.openlocfilehash: fc087ea24ebbebd5acd1cf37fdfd5c9422d44be8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5257053"
---
# <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="cbd76-103">Maksājuma metožu izmantošanas ierobežošana atgriešanām bez kvīts</span><span class="sxs-lookup"><span data-stu-id="cbd76-103">Restrict payment methods for returns without a receipt</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cbd76-104">Kad sistēma tiek iestatīta, ir jākonfigurē katrs maksājuma tips, kuru mazumtirgotājs pieņem.</span><span class="sxs-lookup"><span data-stu-id="cbd76-104">Each payment type that a retailer accepts must be configured when the system is set up.</span></span> <span data-ttu-id="cbd76-105">Šajā tēmā ir aprakstīts, kā var ierobežot noteiktu maksājumu veidu izmantošanu atmaksai, ja atgriešanas tiek veiktas bez kvīts.</span><span class="sxs-lookup"><span data-stu-id="cbd76-105">This topic describes how certain payment types can be restricted for refund if the returns are made without a receipt.</span></span>

## <a name="set-up-payment-methods"></a><span data-ttu-id="cbd76-106">Iestatīt maksājuma metodes</span><span class="sxs-lookup"><span data-stu-id="cbd76-106">Set up payment methods</span></span>

<span data-ttu-id="cbd76-107">Lai iestatītu maksājuma metodes, ir jāizpilda tālāk norādītie uzdevumi.</span><span class="sxs-lookup"><span data-stu-id="cbd76-107">To set up payment methods, the following tasks must be completed.</span></span>
1. <span data-ttu-id="cbd76-108">Izveidojiet maksājuma metodes, kas tiek pieņemtas visā organizācijā.</span><span class="sxs-lookup"><span data-stu-id="cbd76-108">Create the payment methods that are accepted by the entire organization.</span></span>
2. <span data-ttu-id="cbd76-109">Izveidojiet uzņēmuma līmeņa karšu veidus un karšu numurus.</span><span class="sxs-lookup"><span data-stu-id="cbd76-109">Create organization-wide card types and card numbers.</span></span> <span data-ttu-id="cbd76-110">Ja tiek pieņemtas kredītkartes vai debetkartes, ir jāizveido viena maksājumu metode maksājumiem ar kartēm un pēc tam ir jāizveido organizācijas līmeņa karšu veidi un karšu numuri.</span><span class="sxs-lookup"><span data-stu-id="cbd76-110">If credit cards or debit cards are accepted, you must create one payment method for cards, and then create the organization-wide card types and card numbers.</span></span>
3. <span data-ttu-id="cbd76-111">Iestatiet veikala maksājuma metodes.</span><span class="sxs-lookup"><span data-stu-id="cbd76-111">Set up store payment methods.</span></span> <span data-ttu-id="cbd76-112">Saistiet maksājuma metodes ar katru veikalu un pēc tam ievadiet veikalam raksturīgos maksājuma metodes iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="cbd76-112">Associate payment methods with each store, and then enter the store-specific settings for each payment method.</span></span>
4. <span data-ttu-id="cbd76-113">Iestatiet veikalu kartes maksājuma metodes.</span><span class="sxs-lookup"><span data-stu-id="cbd76-113">Set up card payment methods for stores.</span></span> <span data-ttu-id="cbd76-114">Veiciet kartes iestatījumus visām kartes maksājuma metodēm, kas tiek pieņemtas veikalā.</span><span class="sxs-lookup"><span data-stu-id="cbd76-114">For any card payment methods that the store accepts, complete the card setup.</span></span>

<span data-ttu-id="cbd76-115">![Veikala iestatīšana](media/NoReceiptReturns1.png "Mazumtirdzniecības veikala iestatīšana")</span><span class="sxs-lookup"><span data-stu-id="cbd76-115">![Store Setup](media/NoReceiptReturns1.png "Retail Store Setup")</span></span> 


## <a name="restrict-payment-methods-for-returns-without-a-receipt"></a><span data-ttu-id="cbd76-116">Maksāšanas metožu ierobežošana atgriešanām bez kvīts</span><span class="sxs-lookup"><span data-stu-id="cbd76-116">Restrict payment methods for returns without a receipt</span></span>

<span data-ttu-id="cbd76-117">Katrai veikala maksājuma metodei lapas **Veikala pārvaldība** sadaļā **Atgriešanas bez kvīts** iestatiet opcijas **Ierobežot izmantošanu atmaksām bez kvīts** vērtību **Jā**.</span><span class="sxs-lookup"><span data-stu-id="cbd76-117">For each store payment method, on the **Store management** page, under **Non receipt returns**, set **Restrict for refunds without receipt** to **Yes**.</span></span> 

<span data-ttu-id="cbd76-118">Pārslēga noklusējuma vērtība ir **Nē**, kas nodrošina, ka maksājuma metodi drīkst izmantot atmaksām.</span><span class="sxs-lookup"><span data-stu-id="cbd76-118">The default value of the toggle is **No**, which ensures that the payment method is allowed for refunds.</span></span> 

<span data-ttu-id="cbd76-119">Ja ir iestatīta opcijas **Ierobežot izmantošanu atmaksām bez kvīts** vērtība **Jā**, atlasīto maksājuma metodi nedrīkst izmantot atmaksām.</span><span class="sxs-lookup"><span data-stu-id="cbd76-119">When **Restrict for refunds without receipt** is set to **Yes**, the selected payment method will not be allowed for refunds.</span></span> 

<span data-ttu-id="cbd76-120">![Veikala maksājuma metode](media/NoReceiptReturns3.png "Mazumtirdzniecības veikala maksājuma metode")</span><span class="sxs-lookup"><span data-stu-id="cbd76-120">![Store payment method](media/NoReceiptReturns3.png "Retail Store Payment Method")</span></span> 

> [!NOTE]
> <span data-ttu-id="cbd76-121">Ja kasieris atlasa maksājuma metodi, kam ir ierobežota izmantošana atmaksai bez kvīts, tiek parādīts ziņojums, kurā var pārbaudīt pieņemamās maksājuma metodes.</span><span class="sxs-lookup"><span data-stu-id="cbd76-121">When a cashier selects a payment method that is restricted for refund without a receipt, a message displays to verify the acceptable payment methods.</span></span>

<span data-ttu-id="cbd76-122">![Pieņemtās maksājumu metodes](media/NoReceiptReturns4.png "Pieņemtās maksājumu metodes")</span><span class="sxs-lookup"><span data-stu-id="cbd76-122">![Acceptable payment methods](media/NoReceiptReturns4.png "Acceptable payment methods")</span></span> 

<span data-ttu-id="cbd76-123">Ja transakcijā ir ietverta gan atgriešana ar kvīti, gan atgriešana bez kvīts, ierobežojuma nosacījumi netiek lietoti, jo transakcijai tiek izmantota atgriešanas darbplūsma ar kvīti.</span><span class="sxs-lookup"><span data-stu-id="cbd76-123">If a transaction has both a receipted return and a return without a receipt, the restriction conditions will not be enforced because the transaction will be a return workflow with a receipt.</span></span> 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Kreditora maksājumu nosacījumu definēšana
description: Šajā tēmā ir izskaidrots, kā iestatīt kreditoru rēķinu apmaksas nosacījumus.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1b69b505996b5536088578885c11a7e8c27f4975
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971857"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="39de9-103">Kreditora maksājumu nosacījumu definēšana</span><span class="sxs-lookup"><span data-stu-id="39de9-103">Define vendor payment terms</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="39de9-104">Šajā tēmā ir izskaidrots, kā iestatīt kreditoru rēķinu apmaksas nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="39de9-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="39de9-105">Šajā uzdevumā tiek izmantots demonstrācijas uzņēmums USMF.</span><span class="sxs-lookup"><span data-stu-id="39de9-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="39de9-106">Pārejiet uz sadaļu **Navigācijas rūts > Moduļi > Kreditori > Maksājuma iestatīšana > Apmaksas nosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="39de9-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="39de9-107">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="39de9-107">Select **New**.</span></span> <span data-ttu-id="39de9-108">Lapa Apmaksas noteikumi tiek izmantota, lai definētu, kā tiks aprēķināts apmaksas termiņš.</span><span class="sxs-lookup"><span data-stu-id="39de9-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="39de9-109">Tā netiek izmantota, lai definētu, kā tiks aprēķināts termiņatlaides datums.</span><span class="sxs-lookup"><span data-stu-id="39de9-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="39de9-110">Ierakstiet vērtību laukā **Apmaksas nosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="39de9-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="39de9-111">Laukā **Apraksts** ierakstiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="39de9-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="39de9-112">Ievadiet skaitli laukā **Dienas**.</span><span class="sxs-lookup"><span data-stu-id="39de9-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="39de9-113">Šeit ievadītais skaitlis tiks izmantots, lai to pieskaitītu apmaksas datumam vai maksāšanas metodē norādītā perioda beigām.</span><span class="sxs-lookup"><span data-stu-id="39de9-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="39de9-114">Piemēram, ja atlasāt **Neto**, skaitlis tiks pieskaitīts apmaksas datumam.</span><span class="sxs-lookup"><span data-stu-id="39de9-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="39de9-115">Ja atlasāt **Pašreizējais mēnesis**, aprēķinot apmaksas datumu, skaitlis tiks pieskaitīts pašreizējā mēneša pēdējai dienai.</span><span class="sxs-lookup"><span data-stu-id="39de9-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="39de9-116">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="39de9-116">Select **Save**.</span></span>
7. <span data-ttu-id="39de9-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="39de9-117">Close the page.</span></span>
8. <span data-ttu-id="39de9-118">Pārejiet uz sadaļu **Kreditori > Maksājuma iestatīšana > Termiņatlaides**.</span><span class="sxs-lookup"><span data-stu-id="39de9-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="39de9-119">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="39de9-119">Select **New**.</span></span>
10. <span data-ttu-id="39de9-120">Ievadiet ID laukā **Termiņatlaide**.</span><span class="sxs-lookup"><span data-stu-id="39de9-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="39de9-121">Laukā **Apraksts** ierakstiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="39de9-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="39de9-122">Ja kreditors piedāvā diferencētas atlaides, atlasiet nākamo termiņatlaidi, kas stājas spēkā, kad pašreizējā vairs nav spēkā.</span><span class="sxs-lookup"><span data-stu-id="39de9-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="39de9-123">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="39de9-123">Close the page.</span></span>
14. <span data-ttu-id="39de9-124">Ievadiet skaitli laukā **Dienas**.</span><span class="sxs-lookup"><span data-stu-id="39de9-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="39de9-125">Daudzums, kas ievadīts laukā **Dienas**, tiks izmantots, lai aprēķinātu termiņatlaides datumu, pamatojoties uz opciju, kas atlasīta laukā **Neto/Pašreizējais**.</span><span class="sxs-lookup"><span data-stu-id="39de9-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="39de9-126">Ja ir atlasīts **Neto**, termiņatlaides datuma aprēķināšanai dienu daudzums tiks pieskaitīts rēķina datumam.</span><span class="sxs-lookup"><span data-stu-id="39de9-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="39de9-127">Ja ir atlasīts **Pašreizējais mēnesis**, termiņatlaides datuma aprēķināšanai dienu daudzums tiks pieskaitīts pašreizējā mēneša beigām.</span><span class="sxs-lookup"><span data-stu-id="39de9-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="39de9-128">Laukā **Atlaide** ievadiet termiņatlaidi procentos.</span><span class="sxs-lookup"><span data-stu-id="39de9-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="39de9-129">Ievadiet galveno kontu, kurā tiks iegrāmatota termiņatlaide debitoru rēķiniem, pēc tam ievadiet galveno kontu, kurā tiks iegrāmatota termiņatlaide kreditoru rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="39de9-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="39de9-130">Ja lauka **Atlaižu korespondējošie konti** vērtība ir **Kreditoru atlaidēm izmantot galveno kontu**, tiks izmantots galvenais konts.</span><span class="sxs-lookup"><span data-stu-id="39de9-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="39de9-131">Ja ir izvēlēta opcija **Konti rēķina rindās**, termiņatlaide tiks iegrāmatota līdzekļu/izdevumu kontos, kuri izmantoti rēķina rindās.</span><span class="sxs-lookup"><span data-stu-id="39de9-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="39de9-132">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="39de9-132">Select **Save**.</span></span>


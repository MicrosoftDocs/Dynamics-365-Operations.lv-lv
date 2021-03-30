---
title: " Mazumtirdzniecības izrakstu maksājumu konfigurācijas"
description: Šajā procedūra ir aprakstītas Commerce veikala maksāšanas metožu konfigurācijas, kas ietekmē Commerce pārskatu izveides un grāmatošanas procesu.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable, RetailStoreTenderTypeTable
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8723f786c2eaf5f045007de32ce5cbe57563eaf9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205701"
---
# <a name="payment-configurations-for-retail-statements"></a><span data-ttu-id="f502f-103"> Mazumtirdzniecības izrakstu maksājumu konfigurācijas</span><span class="sxs-lookup"><span data-stu-id="f502f-103">Payment configurations for Retail statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f502f-104">Šajā procedūra ir aprakstītas Commerce veikala maksāšanas metožu konfigurācijas, kas ietekmē Commerce pārskatu izveides un grāmatošanas procesu.</span><span class="sxs-lookup"><span data-stu-id="f502f-104">This procedure demonstrates configurations for Commerce store payment methods, which affect how statements get created and posted.</span></span>

<span data-ttu-id="f502f-105">Šis paraugs izmanto USRT demonstrācijas uzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="f502f-105">This recording uses the USRT demo company.</span></span>

1. <span data-ttu-id="f502f-106">Parejiet uz Retail un Commerce > Kanāli > Veikali > Visi veikali.</span><span class="sxs-lookup"><span data-stu-id="f502f-106">Go to Retail and Commerce > Channels > Stores > All stores.</span></span>
2. <span data-ttu-id="f502f-107">Sarakstā atrodiet un atlasiet vajadzīgo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="f502f-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="f502f-108">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="f502f-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f502f-109">Darbību rūtī noklikšķiniet uz Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="f502f-109">On the Action Pane, click Set up.</span></span>
5. <span data-ttu-id="f502f-110">Noklikšķiniet uz Maksāšanas metodes.</span><span class="sxs-lookup"><span data-stu-id="f502f-110">Click Payment methods.</span></span>
6. <span data-ttu-id="f502f-111">Izvērsiet vai sakļaujiet sadaļu Grāmatošana.</span><span class="sxs-lookup"><span data-stu-id="f502f-111">Expand or collapse the Posting section.</span></span>
7. <span data-ttu-id="f502f-112">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="f502f-112">Click Edit.</span></span>
    * <span data-ttu-id="f502f-113">Atlasiet, vai summas, kas saņemtas šai maksāšanas metodei, ir jāgrāmato virsgrāmatas kontā vai bankas kontā.</span><span class="sxs-lookup"><span data-stu-id="f502f-113">Select whether the amounts received for this payment method should be posted to a ledger account or bank account.</span></span>  
    * <span data-ttu-id="f502f-114">Atlasiet kontu, kurā jāgrāmato šai maksāšanas metodei saņemtās summas.</span><span class="sxs-lookup"><span data-stu-id="f502f-114">Select the account that amounts received for this payment method should be posted to.</span></span>  
    * <span data-ttu-id="f502f-115">Atlasiet kontu, kurā grāmatot iespējamās transakcijas saņemtās kopsummas un šai maksāšanas metodei aprēķinātās summas starpības.</span><span class="sxs-lookup"><span data-stu-id="f502f-115">Select an account to post possible differences between the total transaction amount received and the amount counted for this payment method.</span></span>  
    * <span data-ttu-id="f502f-116">Šajā laukā var ievadīt kontrolējamo summu, ja starpības summa ir jāgrāmato citā starpību kontā.</span><span class="sxs-lookup"><span data-stu-id="f502f-116">In this field you can enter an amount to control when the difference amount should be posted to another difference account.</span></span> <span data-ttu-id="f502f-117">To var izmantot, lai izsekotu lielas atšķirības.</span><span class="sxs-lookup"><span data-stu-id="f502f-117">You can use this to track big differences.</span></span>  
    * <span data-ttu-id="f502f-118">Atlasiet kontu, kurā grāmatot iespējamās transakcijas saņemtās kopsummas un aprēķinātās summas starpības, ja tas pārsniedz vērtību, kas ir definēta laukā Maksimālā starpības summa.</span><span class="sxs-lookup"><span data-stu-id="f502f-118">Select an account to post possible differences between the total transaction amount received and the amount counted, when it exceeds the value that is defined in the "Maximum difference amount" field.</span></span>  
    * <span data-ttu-id="f502f-119">Atlasiet Jā, lai bankas noguldījuma summas grāmatotu atsevišķā kontā.</span><span class="sxs-lookup"><span data-stu-id="f502f-119">Select "Yes" to post bank drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="f502f-120">Šajā laukā varat atlasīt, vai bankas noguldījuma summas ir jāgrāmato virsgrāmatas kontā vai bankas kontā.</span><span class="sxs-lookup"><span data-stu-id="f502f-120">In this field you can select whether bank drop amounts should be posted to a ledger account or a bank account.</span></span>  
    * <span data-ttu-id="f502f-121">Atlasiet kontu, kurā grāmatot bankas noguldījuma summas.</span><span class="sxs-lookup"><span data-stu-id="f502f-121">Select the account to post bank drop amounts into.</span></span>  
    * <span data-ttu-id="f502f-122">Atlasiet bankas transakcijas veidu, ko izmantot, grāmatojot bankas noguldījuma summas bankas kontā.</span><span class="sxs-lookup"><span data-stu-id="f502f-122">Select the bank transaction type to use when posting bank drop amounts to the bank account.</span></span>  
    * <span data-ttu-id="f502f-123">Atlasiet Jā, lai seifa noguldījuma summas grāmatotu atsevišķā kontā.</span><span class="sxs-lookup"><span data-stu-id="f502f-123">Select "Yes" to post safe drop amounts to a separate account.</span></span>  
    * <span data-ttu-id="f502f-124">Atlasiet, vai seifa noguldījuma summas ir jāgrāmato virsgrāmatas kontā vai bankas kontā.</span><span class="sxs-lookup"><span data-stu-id="f502f-124">Select whether safe drop amounts should be posted to the ledger account or the bank account.</span></span>  
    * <span data-ttu-id="f502f-125">Atlasiet kontu, kurā grāmatot seifa noguldījuma summas.</span><span class="sxs-lookup"><span data-stu-id="f502f-125">Select the account to post safe drop amounts into.</span></span>  
8. <span data-ttu-id="f502f-126">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="f502f-126">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Pamatlīdzekļu iegādes grāmatošanas konti
description: Šajā rakstā ir paskaidrots, kā iestatīt virsgrāmatas grāmatošanas kontus līdzekļu iegādei.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a340df57a6073c6d9b6f2cdaadbf8f21fc11649
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241046"
---
# <a name="fixed-asset-acquisition-posting-accounts"></a><span data-ttu-id="5aa8d-103">Pamatlīdzekļu iegādes grāmatošanas konti</span><span class="sxs-lookup"><span data-stu-id="5aa8d-103">Fixed asset acquisition posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5aa8d-104">Šajā rakstā ir paskaidrots, kā iestatīt virsgrāmatas grāmatošanas kontus līdzekļu iegādei.</span><span class="sxs-lookup"><span data-stu-id="5aa8d-104">This article explains how to set up general ledger posting accounts for acquiring assets.</span></span>

<span data-ttu-id="5aa8d-105">Pamatlīdzekļu iegādes grāmatošanai izmantotie konti ir atkarīgi no metodes, kādā līdzeklis tiek iegādāts.</span><span class="sxs-lookup"><span data-stu-id="5aa8d-105">Accounts used for posting fixed asset acquisitions may vary depending upon the method used to acquire the asset.</span></span> <span data-ttu-id="5aa8d-106">Lapā Pamatlīdzekļu grāmatošanas metodes, cilnē Virsgrāmatas konti atlasiet Iegāde un Iegādes korekcija, lai iestatītu pamatlīdzekļu kontus grāmatošanai virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="5aa8d-106">On the Fixed asset posting profiles page, on the Ledger accounts tab, select Acquisition and Acquisition adjustment to set up fixed asset accounts to post to the ledger.</span></span> 

<span data-ttu-id="5aa8d-107">Žurnālos un pirkšanas pasūtījumos Virsgrāmatas konts parasti ir bilances konts, kur jaunā pamatlīdzekļa iegādes vērtība tiek ierakstīta debetā.</span><span class="sxs-lookup"><span data-stu-id="5aa8d-107">In journals and on purchase orders, Ledger account is typically the balance sheet account, where the acquisition value of the new fixed asset is debited.</span></span> <span data-ttu-id="5aa8d-108">Šis konts netiek parādīts žurnālā un to nevar aizstāt transakcijās.</span><span class="sxs-lookup"><span data-stu-id="5aa8d-108">This account is not displayed in the journal and cannot be replaced in transactions.</span></span> 

<span data-ttu-id="5aa8d-109">Korespondējošais konts ir arī bilances konts.</span><span class="sxs-lookup"><span data-stu-id="5aa8d-109">Offset account is also a balance sheet account.</span></span> <span data-ttu-id="5aa8d-110">Virsgrāmatas žurnālā un pamatlīdzekļu žurnālā šis konts bieži mēdz būt bankas konts, ko lieto, lai maksātu par pamatlīdzekļa iegādi.</span><span class="sxs-lookup"><span data-stu-id="5aa8d-110">In the general journal and in the fixed assets journal, this account often will be the bank account that is used to pay for the acquisition of the asset.</span></span> <span data-ttu-id="5aa8d-111">Korespondējošais konts ir noklusējuma konts, kas tiek norādīts žurnālos.</span><span class="sxs-lookup"><span data-stu-id="5aa8d-111">The offset account is a default account, which is suggested in the journals.</span></span> <span data-ttu-id="5aa8d-112">Žurnālā to var nomainīt ar jebkuru citu kontu no kontu plāna vai ar kreditora kontu, ja pamatlīdzeklis tika pirkts no kreditora.</span><span class="sxs-lookup"><span data-stu-id="5aa8d-112">It can be changed in the journal to any other account from the chart of accounts or to a vendor account, if the fixed asset was purchase from a vendor.</span></span> 

<span data-ttu-id="5aa8d-113">Ja pamatlīdzekļu iegādei modulī Kreditori tiek lietots vienums Rēķinu žurnāls vai Pirkšanas pasūtījumi, tad pamatlīdzekļu transakcijas korespondējošais konts tiek aizstāts ar šai transakcijai atlasīto kreditora kontu.</span><span class="sxs-lookup"><span data-stu-id="5aa8d-113">When Invoice journal or Purchase orders in Accounts payable are used for fixed asset acquisitions, the offset account for the fixed asset transaction is replaced by the vendor account that is selected for the transaction.</span></span>

<span data-ttu-id="5aa8d-114">Iegādēm, kas tiek grāmatotas, virsgrāmatā izmantojot žurnālu Krājumi pamatlīdzekļiem, pamatlīdzekļi netiek pirkti no ārējiem avotiem, bet pārsūtīti no paša uzņēmuma krājumiem.</span><span class="sxs-lookup"><span data-stu-id="5aa8d-114">For acquisitions posted using the Inventory to fixed assets journal in General ledger, the fixed asset is not bought from external sources, but transferred from the company's own inventory.</span></span> <span data-ttu-id="5aa8d-115">Tādējādi korespondējošais konts ir krājumu izejas plūsmas konts krājumu vienībām sadaļā Krājumu pārvaldība.</span><span class="sxs-lookup"><span data-stu-id="5aa8d-115">Therefore, the offset account is an inventory issue account for the inventory item in Inventory management.</span></span>

<span data-ttu-id="5aa8d-116">Papildinformāciju skatiet tēmā [Līdzekļu iegādāšanās, izmantojot iepirkuma procesu](acquire-assets-procurement.md).</span><span class="sxs-lookup"><span data-stu-id="5aa8d-116">For more information, see [Acquire assets through procurement](acquire-assets-procurement.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Sadalīt rēķina funkcionalitāti
description: Šajā tēmā aprakstīta rēķinu sadalījuma iestatīšana un funkcionalitāte pēc piegādes adreses un nodokļu konta numura (TAN).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023423"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="98472-103">Sadalīt rēķina funkcionalitāti</span><span class="sxs-lookup"><span data-stu-id="98472-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98472-104">Šajā tēmā aprakstīta rēķinu sadalījuma iestatīšana un funkcionalitāte pēc piegādes adreses un nodokļu konta numura (TAN).</span><span class="sxs-lookup"><span data-stu-id="98472-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="98472-105">Lapas **Kreditoru parametri** cilnē **Vispārīgi** atlasiet izvēles rūtiņu **Produktu kvīts** vai **Rēķins** lai grāmatotu un sadalītu preču kvīti vai rēķinu, kuram ir atšķirīgas piegādes adreses un TAN lapā **Pirkšanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="98472-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="98472-106">Iegrāmatotais rēķins tiks sadalīts pēc piegādes adreses un TAN.</span><span class="sxs-lookup"><span data-stu-id="98472-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="98472-107">Cilnē **Kopsavilkuma atjauninājums**, kopsavilkuma cilnē **Sadalīt, pamatojoties uz**, rindā **Piegādes informācija** iestatiet opcijas **Apstiprinājums**, **Izdošanas saraksts**, **Pavadzīme** vai **Rēķins** uz **Jā**, lai grāmatotu un sadalītu apstiprinājumu, izdošanas sarakstu, pavadzīmi vai rēķinu, kur dažādas piegādes adreses un rēķini ir definēti dažādām rēķina rindām lapā **Pārdošanas pasūtījums**.</span><span class="sxs-lookup"><span data-stu-id="98472-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="98472-108">Iegrāmatotais rēķins tiks sadalīts vispirms pēc piegādes adreses un tad pēc TAN.</span><span class="sxs-lookup"><span data-stu-id="98472-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="98472-109">Ja **Piegādes informācijas** opcijas nav iestatītas uz **Jā**, rēķins tiks grāmatots kā viens rēķins.</span><span class="sxs-lookup"><span data-stu-id="98472-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="98472-110">Netiek veikta rēķinu sadalīšana.</span><span class="sxs-lookup"><span data-stu-id="98472-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="98472-111">Lai sadalītu un grāmatotu pavadzīmi, kur rēķina rindām ir dažādas piegādes adreses un TAN, jums jāiestata **Pavadzīmes** opcija **Piegādes informācijai** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="98472-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="98472-112">Lai sadalītu un grāmatotu rēķinu, kur rēķina rindām ir dažādas piegādes adreses un TAN, jums jāiestata **Rēķina** opcija **Piegādes informācijai** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="98472-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="98472-113">Lai sadalītu un grāmatotu rēķinu, kur rēķina rindām ir dažādas piegādes adreses, bet viens un tas pats TAN, jums jāiestata **Rēķina** opcija **Piegādes informācijai** uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="98472-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="98472-114">Iegrāmatotais rēķins tiks sadalīts pēc piegādes adreses.</span><span class="sxs-lookup"><span data-stu-id="98472-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="98472-115">Paraugs</span><span class="sxs-lookup"><span data-stu-id="98472-115">Example</span></span>

<span data-ttu-id="98472-116">Šajā piemērā **Rēķina** opcija **Piegādes informācijai** tiek iestatīta uz **Jā** cilnes **Kopsavilkuma atjauninājums** lapā **Debitoru parametri**.</span><span class="sxs-lookup"><span data-stu-id="98472-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="98472-117">Tiek grāmatots pirkšanas rēķins, kam rindās ir šādi iestatījumi piegādes adresēm un TAN:</span><span class="sxs-lookup"><span data-stu-id="98472-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="98472-118">**1. krājumu rinda:** piegādes adrese 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="98472-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="98472-119">**2. krājumu rinda:** piegādes adrese 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="98472-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="98472-120">**3. krājumu rinda:** piegādes adrese 2, TAN-ABCE12345B</span><span class="sxs-lookup"><span data-stu-id="98472-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="98472-121">**4. krājumu rinda:** piegādes adrese 3, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="98472-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="98472-122">Šajā gadījumā oriģinālais rēķins tiek sadalīts divos rēķinos un grāmatots šādā veidā:</span><span class="sxs-lookup"><span data-stu-id="98472-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="98472-123">1. rēķins tiek grāmatots 1. krājuma rindai un 2. krājuma rindai, jo abām rindām ir viena piegādes adrese un TAN.</span><span class="sxs-lookup"><span data-stu-id="98472-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="98472-124">2. rēķins ir grāmatots 3. krājuma rindai.</span><span class="sxs-lookup"><span data-stu-id="98472-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="98472-125">3. rēķins ir grāmatots 4. krājuma rindai.</span><span class="sxs-lookup"><span data-stu-id="98472-125">Invoice 3 is posted for item line 4.</span></span>

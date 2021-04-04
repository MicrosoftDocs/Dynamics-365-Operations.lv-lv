---
title: Kreditora daļējas summas maksājumi
description: Reizēm jūs veicat kreditoram maksājumu, kas ir mazāks par rēķinā norādīto summu. Šajā rakstā ir aprakstītas dažādās opcijas, ko darīt šādās situācijās.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 43b0f4f6a6988f659c957664b140c4b9907ef3d3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255697"
---
# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="b1d34-104">Kreditoru maksājumi par daļēju summu</span><span class="sxs-lookup"><span data-stu-id="b1d34-104">Vendor payments for a partial amount</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1d34-105">Reizēm jūs veicat kreditoram maksājumu, kas ir mazāks par rēķinā norādīto summu.</span><span class="sxs-lookup"><span data-stu-id="b1d34-105">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="b1d34-106">Šajā rakstā ir aprakstītas dažādās opcijas, ko darīt šādās situācijās.</span><span class="sxs-lookup"><span data-stu-id="b1d34-106">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="b1d34-107">Jums pieejamās opcijas ir atkarīgas no jūsu biznesa prasībām un konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="b1d34-107">The options that are available to you depend on your business requirements and configuration.</span></span> 

<a name="cash-discount-amounts"></a><span data-ttu-id="b1d34-108">Termiņatlaides summas</span><span class="sxs-lookup"><span data-stu-id="b1d34-108">Cash discount amounts</span></span>
---------------------

<span data-ttu-id="b1d34-109">Varat piedāvāt kreditoram termiņatlaidi, ja rēķins tiek apmaksāts pirms apmaksas datuma.</span><span class="sxs-lookup"><span data-stu-id="b1d34-109">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="b1d34-110">Piemēram, ja rēķins tiek apmaksāts 10 dienu laikā, jūs ievadiet rēķinu par summu 100,00, kurā norādīta 2 procentu termiņatlaide.</span><span class="sxs-lookup"><span data-stu-id="b1d34-110">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="b1d34-111">Apmaksas termiņš ir 30 dienas.</span><span class="sxs-lookup"><span data-stu-id="b1d34-111">The due date terms are 30 days.</span></span> <span data-ttu-id="b1d34-112">Ja maksājuma piedāvājumā kā rēķina atlases kritērijs ir izmantota termiņatlaide un ja priekšlikums ir spēkā termiņatlaides datumā vai pirms tā, tad šis rēķins tiek atlasīts apmaksai un maksājums tiek veikts par summu 98,00.</span><span class="sxs-lookup"><span data-stu-id="b1d34-112">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="b1d34-113">Termiņatlaidi var piemērot arī vienreizējam maksājumam, kas ir izveidots manuāli.</span><span class="sxs-lookup"><span data-stu-id="b1d34-113">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="b1d34-114">Daļēji maksājumi ar termiņatlaidēm</span><span class="sxs-lookup"><span data-stu-id="b1d34-114">Partial payments with cash discounts</span></span>
<span data-ttu-id="b1d34-115">Ja tiek veikts daļējs maksājums, var ieplānot veikt papildu daļēju maksājumu, lai pilnībā segtu rēķinu.</span><span class="sxs-lookup"><span data-stu-id="b1d34-115">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="b1d34-116">Lai daļējam maksājumam piemērotu termiņatlaidi, opcija **Aprēķināt daļēju maksājumu termiņatlaides** lapā **Debitoru moduļa parametri** ir jāiestata ar vērtību **Jā**.</span><span class="sxs-lookup"><span data-stu-id="b1d34-116">To take a cash discount for a partial payment, you must set the **Calculate cash discounts for partial payments** option to **Yes** on the **Account payable parameters** page.</span></span> 

<span data-ttu-id="b1d34-117">Piemēram, ja rēķins tiek apmaksāts 10 dienu laikā pēc tā izrakstīšanas, jums tiek piedāvāta 2 procentu termiņatlaide.</span><span class="sxs-lookup"><span data-stu-id="b1d34-117">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="b1d34-118">Rēķins ir iegrāmatots par summu 100,00.</span><span class="sxs-lookup"><span data-stu-id="b1d34-118">An invoice is posted for 100.00.</span></span> <span data-ttu-id="b1d34-119">Ja 10 dienu laikā veicat maksājumu par summu 49,00, maksājumu žurnālā ievadiet debeta summu 49,00.</span><span class="sxs-lookup"><span data-stu-id="b1d34-119">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="b1d34-120">Kad daļējais maksājums tiek nosegts lapā **Nosegt atvērtās transakcijas**, laukā **Noņemamā termiņatlaides summa** tiek parādīta vērtība **1,00**.</span><span class="sxs-lookup"><span data-stu-id="b1d34-120">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="b1d34-121">Ja ievadāt daļēju maksājumu un atstājat pilnu rēķina summu laukā **Nosedzamā summa**, tad lauks **Ņemamā termiņatlaides summa** automātiski tiek pārrēķināts, kad grāmatojot transakcijas.</span><span class="sxs-lookup"><span data-stu-id="b1d34-121">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="b1d34-122">Kredīta notas ar temiņatlaidēm</span><span class="sxs-lookup"><span data-stu-id="b1d34-122">Credit notes with cash discounts</span></span>
<span data-ttu-id="b1d34-123">Jūs varat atgriezt dažas rēķinā iekļautās preces un saņemt kredīta notu.</span><span class="sxs-lookup"><span data-stu-id="b1d34-123">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="b1d34-124">Ja termiņatlaide ir piemērota sākotnējam rēķinam, varat atņemt atlaides vērtību un saņemt pareizās summas atmaksu.</span><span class="sxs-lookup"><span data-stu-id="b1d34-124">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="b1d34-125">Ja opcija **Aprēķināt kredīta notu termiņatlaides** lapā **Kreditoru moduļa parametri** ir iestatīta ar vērtību **Jā**, kredīta notai automātiski tiek aprēķināta atlaide.</span><span class="sxs-lookup"><span data-stu-id="b1d34-125">If the **Calculate cash discounts for credit notes** option is set to **Yes** on the **Accounts payable parameters** page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="b1d34-126">Piemēram, ja rēķins tiek apmaksāts 10 dienu laikā pēc tā izrakstīšanas, jums tiek piedāvāta 2 procentu termiņatlaide.</span><span class="sxs-lookup"><span data-stu-id="b1d34-126">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="b1d34-127">Rēķins tiek iegrāmatots par summu 100,00.</span><span class="sxs-lookup"><span data-stu-id="b1d34-127">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="b1d34-128">Ja tiek atgrieztas preces un saņemta kredīta nota, varat ievadīt kredīta notu par sākotnējā rēķina visu summu 100,00 kopā ar 2 procentu termiņatlaidi, kas arī ir norādīta kredītrēķinā.</span><span class="sxs-lookup"><span data-stu-id="b1d34-128">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="b1d34-129">Skatot kredīta notu lapā **Nosegt transakcijas**, summa **98,00** ir redzama laukā **Nosedzamā summa**, un summa **-2,00** ir redzama laukā **Termiņatlaides summa**.</span><span class="sxs-lookup"><span data-stu-id="b1d34-129">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="b1d34-130">Atlaides summa tiek grāmatota uz termiņatlaides kontu.</span><span class="sxs-lookup"><span data-stu-id="b1d34-130">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="b1d34-131">Pārmaksas/nepilnas samaksas summas</span><span class="sxs-lookup"><span data-stu-id="b1d34-131">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="b1d34-132">Ja vēl atlikusī nosedzamā summa ir ļoti neliela, varat veikt daļējo maksājumu.</span><span class="sxs-lookup"><span data-stu-id="b1d34-132">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="b1d34-133">Piemēram, kreditora rēķins summa ir 1000,00, bet jūs veicat maksājumu par summu 999.90.</span><span class="sxs-lookup"><span data-stu-id="b1d34-133">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="b1d34-134">Ja atlikusī summa ir mazāka par summu, kas norādīta pārmaksām vai nepilnām samaksām lapā **Kreditoru moduļa parametri**, starpība tiek automātiski grāmatota uz pārmaksas/nepilnas samaksas virsgrāmatas kontu.</span><span class="sxs-lookup"><span data-stu-id="b1d34-134">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="b1d34-135">Plašāku informāciju skatiet šeit: [Kreditora maksājumu pārskats](../cash-bank-management/tasks/vendor-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b1d34-135">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
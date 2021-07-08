---
title: Piegādātāja kods nav autorizēts noteiktai precei un datumam
description: Mēģinot apstiprināt plānoto pasūtījumu vai pievienot rindu pirkšanas pasūtījumam, tiek parādīts kļūdas ziņojums, kurā norādīts, ka kreditora kods nav autorizēts precei un datumam.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO_ReqTransPoMarkFirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: e6b1189e4fedfdb029f4b4503f0635133df9d87e
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294131"
---
# <a name="vendor-code-isnt-authorized-for-a-specific-product-and-date"></a><span data-ttu-id="4245c-103">Piegādātāja kods nav autorizēts noteiktai precei un datumam</span><span class="sxs-lookup"><span data-stu-id="4245c-103">Vendor code isn't authorized for a specific product and date</span></span>

<span data-ttu-id="4245c-104">Kļūdas kods: SYP4881415</span><span class="sxs-lookup"><span data-stu-id="4245c-104">Error code: SYP4881415</span></span>

## <a name="symptoms"></a><span data-ttu-id="4245c-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="4245c-105">Symptoms</span></span>

<span data-ttu-id="4245c-106">Mēģinot apstiprināt plānoto pasūtījumu vai pievienot rindu pirkšanas pasūtījumam saņemsit šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="4245c-106">When you try to firm a planned order or add a line to a purchase order, you receive the following error message:</span></span>

> <span data-ttu-id="4245c-107">Kreditora kods %1 nav autorizēts lietošanai vienumā %2 šeit: %3.</span><span class="sxs-lookup"><span data-stu-id="4245c-107">Vendor code %1 is not authorized for %2 on %3.</span></span>

## <a name="cause"></a><span data-ttu-id="4245c-108">Iemesls</span><span class="sxs-lookup"><span data-stu-id="4245c-108">Cause</span></span>

<span data-ttu-id="4245c-109">Kļūda rodas, jo norādītajai precei lauks **Apstiprināts piegādātāja pārbaudes metode** ir iestatīts uz *Tikai brīdinājums* vai *Nav atļauts* un kreditors pašlaik nav autorizēts piegādāt šo preci.</span><span class="sxs-lookup"><span data-stu-id="4245c-109">The error occurs because the **Approved vendor check method** field is set to *Warning only* or *Not allowed* for the specified product, and the vendor isn't currently authorized to supply that product.</span></span>

## <a name="resolution"></a><span data-ttu-id="4245c-110">Novēršana</span><span class="sxs-lookup"><span data-stu-id="4245c-110">Resolution</span></span>

<span data-ttu-id="4245c-111">Lai novērstu šo problēmu, deaktivizējiet kreditora pārbaudi atbilstošai precei vai apstipriniet kreditoru.</span><span class="sxs-lookup"><span data-stu-id="4245c-111">To fix this issue, either disable the vendor check for the relevant product or approve the vendor.</span></span>

<span data-ttu-id="4245c-112">Lai atspējotu kreditora pārbaudi precei, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="4245c-112">To disable the vendor check for a product, follow these steps.</span></span>

1. <span data-ttu-id="4245c-113">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="4245c-113">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="4245c-114">Atveriet attiecīgo preci.</span><span class="sxs-lookup"><span data-stu-id="4245c-114">Open the relevant product.</span></span>
1. <span data-ttu-id="4245c-115">Kopsavilkuma cilnē **Pirkums** iestatiet lauku **Apstiprinātais kreditors** uz vērtību, kas nav *Tikai brīdinājums* vai *Nav atļauts*.</span><span class="sxs-lookup"><span data-stu-id="4245c-115">On the **Purchase** FastTab, set the **Approved vendor check method** field to a value other than *Warning only* or *Not allowed*.</span></span>

<span data-ttu-id="4245c-116">Lai apstiprinātu kreditoru precei, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="4245c-116">To approve a vendor for a product, follow these steps.</span></span>

1. <span data-ttu-id="4245c-117">Pārejiet uz sadaļu **Preču informācijas pārvaldība \> Preces \> Izlaistās preces**.</span><span class="sxs-lookup"><span data-stu-id="4245c-117">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="4245c-118">Atveriet attiecīgo krājumu.</span><span class="sxs-lookup"><span data-stu-id="4245c-118">Open the relevant item.</span></span>
1. <span data-ttu-id="4245c-119">Darbību rūtī, cilnē **Pirkšana**, grupā **Apstiprinātais piegādātājs** atlasiet **Iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="4245c-119">On the Action Pane, on the **Purchase** tab, in the **Approved vendor** group, select **Setup**.</span></span>
1. <span data-ttu-id="4245c-120">Darbību rūtī atlasiet saraksta lapu **Apstiprinātais piegādātājs**, pievienojiet rindu režģim, un iestatiet tai šādas vērtības:</span><span class="sxs-lookup"><span data-stu-id="4245c-120">On the **Approved vendor** list page, add a row to the grid, and set the following values for it:</span></span>

    - <span data-ttu-id="4245c-121">**Kreditors** – izvēlieties kreditoru, ko apstiprināt pašreizējai precei.</span><span class="sxs-lookup"><span data-stu-id="4245c-121">**Vendor** – Select the vendor to approve for the current product.</span></span>
    - <span data-ttu-id="4245c-122">**Spēkā stāšanās datums** – izvēlieties pirmo datumu, kuram kreditors ir apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="4245c-122">**Effective date** – Select the first date that the vendor is approved for.</span></span>
    - <span data-ttu-id="4245c-123">**Beigu datums** – izvēlieties pēdējo datumu, kuram kreditors ir apstiprināts.</span><span class="sxs-lookup"><span data-stu-id="4245c-123">**Expiration date** – Select the last date that the vendor is approved for.</span></span>

<span data-ttu-id="4245c-124">Papildinformāciju skatiet [Kreditoru apstiprināšana noteiktām precēm](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span><span class="sxs-lookup"><span data-stu-id="4245c-124">For more information, see [Approve vendors for specific products](/dynamics365/supply-chain/procurement/tasks/approve-vendors-specific-products.md).</span></span>

---
title: Maksājuma rēķinu izveide
description: Šajā tēmā izskaidrots, kā izveidot ikmēneša nomas rēķinus. Varat izveidot rēķinus atsevišķām nomām, vai arī varat izmantot partijas procesu, lai izveidotu tos vairākām nomām.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 32618814d00cb1e1f1082169a64b187cce1e76b4
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445777"
---
# <a name="create-payment-invoices"></a><span data-ttu-id="a6ad9-104">Maksājuma rēķinu izveide</span><span class="sxs-lookup"><span data-stu-id="a6ad9-104">Create payment invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6ad9-105">Varat izveidot ikmēneša rēķinus atsevišķām nomām, vai arī varat izmantot partijas procesu, lai izveidotu tos vairākām nomām.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-105">You can create monthly invoices for individual leases, or you can use a batch process to create them for multiple leases.</span></span> <span data-ttu-id="a6ad9-106">Tālāk minētajā procedūrā ir parādīts, kā izveidot atsevišķu nomas maksājuma ierakstu, ja ir ieslēgts parametrs **Maksāt kreditoram** lapā **Nomas grāmatas iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-106">The following procedure shows how to create an individual lease payment entry when the **Pay to Vendor** parameter on the **Lease book setup** page is turned on.</span></span>

1. <span data-ttu-id="a6ad9-107">Lapā **Nomas kopsavilkums** atlasiet nomu un pēc tam atlasiet **Grāmatas \> Maksājumu grafiks**.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-107">On the **Lease summary** page, select a lease, and then select **Books \> Payment schedule**.</span></span>
2. <span data-ttu-id="a6ad9-108">Atlasiet maksājumu, kas ir jāveic, un pēc tam atlasiet **Izveidot žurnālu**.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-108">Select the payment that must be made, and then select **Create journal**.</span></span> <span data-ttu-id="a6ad9-109">Tiek parādīts ziņojums, ka žurnāls tika izveidots atbilstoši atlasītajam maksājumam.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-109">You receive a message that states that a journal was created against the selected payment.</span></span>
3. <span data-ttu-id="a6ad9-110">Atlasiet **Rēķinu žurnāli** un pēc tam atlasiet rēķinu, kas ir jāsamaksā.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-110">Select **Invoice journals**, and then select the invoice that must be paid.</span></span>
4. <span data-ttu-id="a6ad9-111">Cilnē **Rindas** pārskatiet žurnāla ierakstu, pirms to grāmatot Virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-111">On the **Lines** tab, review the journal entry before you post it to the general ledger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a6ad9-112">Pēc noklusējuma izveidotās kreditora rēķina rindas izmanto kreditoru grāmatošanas profilu no lapas **Kreditora parādu parametri**.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-112">By default, the vendor invoice lines that are created use the vendor posting profile from the **Accounts payable parameters** page.</span></span>

5. <span data-ttu-id="a6ad9-113">Atlasiet pareizo žurnālu un pēc tam atlasiet rēķinu, kas ir jāsamaksā.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-113">Select the correct journal, and then select the invoice that must be paid.</span></span>

    <span data-ttu-id="a6ad9-114">Šajā piemērā nomas grāmatas parametrs **Maksāt kreditoram** ir ieslēgts.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-114">For this example, the **Pay to Vendor** parameter on the lease book is turned on.</span></span> <span data-ttu-id="a6ad9-115">Tāpēc rēķins būs rēķinu žurnālā.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-115">Therefore, the invoice will be in the invoice journal.</span></span> <span data-ttu-id="a6ad9-116">Sadaļā **Pārskats** tiek parādīts žurnāla ieraksta kopsavilkums, un sadaļā **Rindas** tiek parādīta detalizēta informācija par faktiskajām žurnāla rindām.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-116">The **Overview** section shows a summary of the journal entry, and the **Lines** section shows details of the actual journal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a6ad9-117">Ja parametrs **Maksāt kreditoram** ir izslēgts, maksājumu žurnāla ieraksti tiks uzskaitīti nomas grāmatas lapā **Līdzekļa noma**, un sistēma izveidos līdzekļa nomas ierakstu, nevis rēķinu.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-117">If the **Pay to Vendor** parameter is turned off, payment journal entries will be listed on the **Asset leasing** page for the lease book, and the system will create an asset leasing entry instead of an invoice.</span></span> <span data-ttu-id="a6ad9-118">Nomas maksājuma ieraksts tiks grāmatots žurnālā ar nosaukumu, kas norādīts laukā **Ikmēneša nomas žurnāls**.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-118">The lease payment entry will be posted to the journal name that is specified in the **Monthly lease journal** field.</span></span>

6. <span data-ttu-id="a6ad9-119">Kad darījums ir iegrāmatots, varat skatīt informāciju par darījumu un nomas saistību uzskaites vērtību, nomas grāmatā atlasot **Saistību darījumi**.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-119">After the transaction is posted, you can view the transaction information and the carrying value of the lease liability by selecting **Liability transactions** in the lease book.</span></span>

    <span data-ttu-id="a6ad9-120">Maksājumu grafikā būs atlasīta izvēles rūtiņa **Žurnāls grāmatots**, un rindā tiks parādīts rēķinu žurnāla numurs.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-120">In the payment schedule, the **Journal posted** check box will be selected, and the line will show the invoice journal number.</span></span> <span data-ttu-id="a6ad9-121">Pēc tam, kad ir izveidots maksājumu žurnāls un ieraksts šim žurnālam, ieraksts ir jāanulē, pirms to var izveidot atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="a6ad9-121">After a payment journal and an entry for that journal have been created, you must reverse the entry before it can be re-created.</span></span>

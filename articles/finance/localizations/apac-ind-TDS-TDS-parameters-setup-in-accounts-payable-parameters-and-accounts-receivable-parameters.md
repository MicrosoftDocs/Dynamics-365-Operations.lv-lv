---
title: Iestatiet TDS parametrus Kreditoriem un Debitoriem
description: Šajā tēmā skaidrots, kā iestatīt parametrus sadaļā Kreditori un Debitori, lai atbalstītu No kopējo ienākumu summas atskaitīto nodokļu (TDS) ieturējumus.
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
ms.openlocfilehash: 4540cdfff2362d8fb7cc2b4cccf9c340be9750ce
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023418"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a><span data-ttu-id="498da-103">Iestatiet TDS parametrus Kreditoriem un Debitoriem</span><span class="sxs-lookup"><span data-stu-id="498da-103">Set TDS parameters in Accounts payable and Accounts receivable</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="498da-104">Šajā tēmā skaidrots, kā iestatīt parametrus sadaļā Kreditori un Debitori, lai atbalstītu No kopējo ienākumu summas atskaitīto nodokļu (TDS) ieturējumus.</span><span class="sxs-lookup"><span data-stu-id="498da-104">This topic explains how to set parameters in Accounts payable and Accounts receivable to support Tax Deducted at Source (TDS) deductions.</span></span>

1. <span data-ttu-id="498da-105">Dodieties uz **Nodoklis \> Iestatīšana \> Parametri \> Debitoru parādu parametri**.</span><span class="sxs-lookup"><span data-stu-id="498da-105">Go to **Tax \> Setup \> Parameters \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="498da-106">Cilnē **Atjauninājumi** atlasiet **Atjaunināt pasūtījuma rindas**, lai atvērtu dialoglodziņu **Atjaunināt pasūtījuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="498da-106">On the **Updates** tab, select **Update order lines** to open the **Update order lines** dialog box.</span></span>
3. <span data-ttu-id="498da-107">Sadaļas **TDS grupa** laukā **Atjaunināt TDS grupu** norādiet metodi, ko izmantot TDS grupas atjaunināšanai rindas līmenī.</span><span class="sxs-lookup"><span data-stu-id="498da-107">In the **TDS group** section, in the **Updating TDS group** field, specify the method to use to update the TDS group at the line level.</span></span> <span data-ttu-id="498da-108">Šis iestatījums tiek izmantots, kad TDS grupa tiek atjaunināta pasūtījuma galvenē.</span><span class="sxs-lookup"><span data-stu-id="498da-108">This setting is used when the TDS group is updated on an order header.</span></span> <span data-ttu-id="498da-109">Pieejamas šādas opcijas:</span><span class="sxs-lookup"><span data-stu-id="498da-109">The following options are available:</span></span>

    - <span data-ttu-id="498da-110">**Nekad** – TDS grupa netiek atjaunināta pasūtījuma rindās, kad tā tiek atjaunināta pasūtījuma galvenē.</span><span class="sxs-lookup"><span data-stu-id="498da-110">**Never** – The TDS group isn't updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="498da-111">**Vienmēr** – TDS grupa tiek automātiski atjaunināta pasūtījuma rindās, kad tā tiek atjaunināta pasūtījuma galvenē.</span><span class="sxs-lookup"><span data-stu-id="498da-111">**Always** – The TDS group is automatically updated on the order lines when it's updated on the order header.</span></span>
    - <span data-ttu-id="498da-112">**Uzvedne** – lietotāji saņem ziņojumu, kas pieprasa atjaunināt TDS grupu pasūtījuma rindās.</span><span class="sxs-lookup"><span data-stu-id="498da-112">**Prompt** – Users receive a message that prompts them to update the TDS group on the order lines.</span></span>
4. <span data-ttu-id="498da-113">Atlasiet **Labi**.</span><span class="sxs-lookup"><span data-stu-id="498da-113">Select **OK**.</span></span>

    <span data-ttu-id="498da-114">[![Atjaunināt pasūtījuma rindu dialoglodziņš](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span><span class="sxs-lookup"><span data-stu-id="498da-114">[![Update order lines dialog box](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)</span></span>

5. <span data-ttu-id="498da-115">Dodieties uz **Nodoklis \> Iestatīšana \> Parametri \> Kreditoru parādu parametri**.</span><span class="sxs-lookup"><span data-stu-id="498da-115">Go to **Tax \> Setup \> Parameters \> Accounts payable parameters**.</span></span>
6. <span data-ttu-id="498da-116">Cilnes **Vispārīgi** kopsavilkuma cilnē **Sadalīt, pamatojoties uz piegādes informāciju** iestatiet opciju **Produkta kvīts** uz **Jā**, lai grāmatotu un sadalītu produktu kvīti ar dažādām piegādes adresēm un nodokļu konta numuriem (TAN).</span><span class="sxs-lookup"><span data-stu-id="498da-116">On the **General** tab, on the **Split based on delivery information** FastTab, set the **Product receipt** option to **Yes** to post and split a product receipt that has different delivery addresses and tax account numbers (TANs).</span></span> <span data-ttu-id="498da-117">Ja šī opcija ir iestatīta uz **Nē**, nevar grāmatot pirkšanas pavadzīmi ar dažādām piegādes adresēm un TAN.</span><span class="sxs-lookup"><span data-stu-id="498da-117">If this option is set to **No**, you can't post a purchase packing slip that has different delivery addresses and TANs.</span></span>
7. <span data-ttu-id="498da-118">Iestatiet opciju **Rēķins** uz **Jā**, lai grāmatotu un sadalītu pirkšanas rēķinu ar dažādām piegādes adresēm un TAN.</span><span class="sxs-lookup"><span data-stu-id="498da-118">Set the **Invoice** option to **Yes** to post and split a purchase invoice that has different delivery addresses and TANs.</span></span>

    <span data-ttu-id="498da-119">[![Sadalīt, pamatojoties uz kopsavilkuma cilni Piegādes informācija](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span><span class="sxs-lookup"><span data-stu-id="498da-119">[![Split based on delivery information FastTab](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)</span></span>

8. <span data-ttu-id="498da-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="498da-120">Close the page.</span></span>

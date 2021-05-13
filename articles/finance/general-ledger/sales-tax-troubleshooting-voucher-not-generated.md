---
title: Dokuments nav ģenerēts
description: Šajā tēmā ir sniegta traucējummeklēšanas informācija, kas var palīdzēt, kad dokumentam jābūt ģenerētam, bet tas nav.
author: qire
manager: beya
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: eafc9110ec58be5083569188d59b67a62e86c85d
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947676"
---
# <a name="voucher-isnt-generated"></a><span data-ttu-id="9bc85-103">Dokuments nav ģenerēts</span><span class="sxs-lookup"><span data-stu-id="9bc85-103">Voucher isn't generated</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9bc85-104">Ja dokuments ir jāģenerē, bet lapā **Dokumenta transakcijas** netiek rādīts neviens dokuments, dariet, lai novērstu šo problēmu, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="9bc85-104">If a voucher should be generated, but the **Voucher transactions** page doesn't show any vouchers, follow the steps in the following sections as required to troubleshoot this issue.</span></span>

<span data-ttu-id="9bc85-105">[![Dokumentu transakciju lapa, kurā nav dokumentu](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="9bc85-105">[![Voucher transactions page that has no vouchers](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)</span></span>

## <a name="check-the-tax-applicability"></a><span data-ttu-id="9bc85-106">Pārbaudīt nodokļa piemērojamību</span><span class="sxs-lookup"><span data-stu-id="9bc85-106">Check the tax applicability</span></span>

1. <span data-ttu-id="9bc85-107">Doties uz **Nodoklis** \> **Periodiskie uzdevumi** \> **Apakšgrāmatas žurnāla ieraksti periodiskajiem vēl nav pārsūtīti**.</span><span class="sxs-lookup"><span data-stu-id="9bc85-107">Go to **Tax** \> **Periodic tasks** \> **Subledger journal entries not yet transferred**.</span></span>
2. <span data-ttu-id="9bc85-108">Ja ir žurnāla ieraksts, atlasiet to un pēc tam atlasiet **Pārsūtīt tūlīt**.</span><span class="sxs-lookup"><span data-stu-id="9bc85-108">If there is a journal record, select it, and then select **Transfer now**.</span></span>

    <span data-ttu-id="9bc85-109">[![Poga Pārsūtīt tūlīt apakšgrāmatas žurnāla ierakstos, kas vēl nav pārsūtīti lapā](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="9bc85-109">[![Transfer now button on the Subledger journal entries not yet transferred page](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)</span></span>

3. <span data-ttu-id="9bc85-110">Atveriet lapu **Dokumentu transakcijas** vēlreiz, lai redzētu, vai dokuments ir ģenerēts.</span><span class="sxs-lookup"><span data-stu-id="9bc85-110">Open the **Voucher transactions** page again to see whether the voucher was generated.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="9bc85-111">Noteikt, vai pielāgojums pastāv</span><span class="sxs-lookup"><span data-stu-id="9bc85-111">Determine whether customization exists</span></span>

<span data-ttu-id="9bc85-112">Ja esat pabeidzis iepriekšējā sadaļā norādītās darbības, bet nav atraduši nekādu problēmu, nosakiet, vai pielāgošana eksistē.</span><span class="sxs-lookup"><span data-stu-id="9bc85-112">If you've completed the steps in the previous section but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="9bc85-113">Ja pielāgošana nepastāv, izveidojiet Microsoft pakalpojuma pieprasījumu turpmākam atbalstam.</span><span class="sxs-lookup"><span data-stu-id="9bc85-113">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

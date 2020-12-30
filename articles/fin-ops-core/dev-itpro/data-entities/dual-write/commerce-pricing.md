---
title: Dynamics 365 Commerce cenu noteikšanas programmas izmantošana ar Dynamics 365 Sales
description: Šajā tēmā aprakstīts, kā izmantot Microsoft Dynamics 365 Commerce cenu noteikšanas programmu, lai izveidotu pārdošanas piedāvājumus Dynamics 365 Sales.
author: ShalabhjainMSFT
manager: AnnBe
ms.date: 11/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: shajain
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-11-03
ms.openlocfilehash: fad5c21d75db62b85efe803f1667dd3f9164a5fc
ms.sourcegitcommit: 597476103bb695e3cbe6d9ffcd7a466400346636
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/20/2020
ms.locfileid: "4594922"
---
# <a name="use-the-dynamics-365-commerce-pricing-engine-with-dynamics-365-sales"></a><span data-ttu-id="34536-103">Dynamics 365 Commerce cenu noteikšanas programmas izmantošana ar Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="34536-103">Use the Dynamics 365 Commerce pricing engine with Dynamics 365 Sales</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34536-104">Šajā tēmā aprakstīts, kā izmantot Microsoft Dynamics 365 Commerce cenu noteikšanas programmu, lai izveidotu pārdošanas piedāvājumus Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="34536-104">This topic describes how to use the Microsoft Dynamics 365 Commerce pricing engine to create sales quotations in Dynamics 365 Sales.</span></span>

<span data-ttu-id="34536-105">Dynamics 365 Commerce cenu noteikšanas programma atbalsta lielāko daļu no uzņēmuma līdz patērētājam (B2C) cenu noteikšanas scenāriju, piemēram, veikala līmeņa cenu noteikšanu, uz piederību un lojalitāti balstītu cenu noteikšanu, atlaides dažādām vienas kolekcijas precēm, apjoma atlaides un atlaides par iztērētu noteiktu summu.</span><span class="sxs-lookup"><span data-stu-id="34536-105">The Dynamics 365 Commerce pricing engine supports most business-to-consumer (B2C) pricing scenarios, such as store-level pricing, affiliation-based and loyalty-based pricing, mix-and-match discounts, quantity discounts, and threshold discounts.</span></span> <span data-ttu-id="34536-106">Cenu noteikšanas programma izmanto kompleksas kārtulas, lai noteiktu labāko cenu dotajam piedāvājumam vai pasūtījumam.</span><span class="sxs-lookup"><span data-stu-id="34536-106">The pricing engine uses complex rules to determine the best price for a given quotation or order.</span></span>

<span data-ttu-id="34536-107">Izmantojot [duālo rakstīšanu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), cenu noteikšanas vajadzībām ir pieejamas trīs opcijas.</span><span class="sxs-lookup"><span data-stu-id="34536-107">When you use [dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), you have three options for your pricing needs.</span></span> <span data-ttu-id="34536-108">Varat izmantot statisko cenu noteikšanu, kas tiek iegūta no cenrāža Dynamics 365 Sales, cenu noteikšanas programmu Dynamics 365 Supply Chain Management vai cenu noteikšanas programmu Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="34536-108">You can use the static pricing that comes from the price list in Dynamics 365 Sales, the pricing engine in Dynamics 365 Supply Chain Management, or the pricing engine in Dynamics 365 Commerce.</span></span> <span data-ttu-id="34536-109">No šīm opcijām Commerce cenu noteikšanas programma ir vislabāk piemērota B2C scenārijiem.</span><span class="sxs-lookup"><span data-stu-id="34536-109">Among these options, the Commerce pricing engine is best suited to B2C scenarios.</span></span>

## <a name="use-the-commerce-pricing-engine-in-sales"></a><span data-ttu-id="34536-110">Commerce cenu noteikšanas programmas izmantošana Sales</span><span class="sxs-lookup"><span data-stu-id="34536-110">Use the Commerce pricing engine in Sales</span></span>

> [!NOTE]
> <span data-ttu-id="34536-111">Pašlaik Commerce cenu noteikšanas programmu var izmantot tikai piedāvājuma izveidei Sales.</span><span class="sxs-lookup"><span data-stu-id="34536-111">Currently, the Commerce pricing engine can be used only for quotation creation in the Sales.</span></span> <span data-ttu-id="34536-112">Pārdošanas pasūtījuma integrācija ar Commerce cenu noteikšanas programmu vēl nav pieejama.</span><span class="sxs-lookup"><span data-stu-id="34536-112">Sales order integration with the Commerce pricing engine isn't yet available.</span></span>

<span data-ttu-id="34536-113">Kad lietotāji uzsāk piedāvājumu Sales, duālās rakstīšanas struktūra kopē detalizētu informāciju par piedāvājumu uz Commerce.</span><span class="sxs-lookup"><span data-stu-id="34536-113">When users initiate a quotation in Sales, the dual-write framework copies the quotation details to Commerce.</span></span> <span data-ttu-id="34536-114">Visas izmaiņas esošajās piedāvājuma rindās vai jebkādas nesen pievienotās piedāvājuma rindas Sales tiek kopētas uz Commerce.</span><span class="sxs-lookup"><span data-stu-id="34536-114">Any changes to existing quotation lines or any newly added quotation lines in Sales are copied to Commerce.</span></span> <span data-ttu-id="34536-115">Kad lietotāji vēlas izmantot Commerce cenu noteikšanas programmu, lai noteiktu cenu piedāvājumam, tie var atlasīt **Cenas piedāvājums**, lai atjauninātu piedāvājuma cenas, pamatojoties uz Commerce cenu noteikšanas programmu.</span><span class="sxs-lookup"><span data-stu-id="34536-115">When users want to use the Commerce pricing engine to price the quotation, they can select **Price quote** to update the prices of the quotation, based on the Commerce pricing engine.</span></span> <span data-ttu-id="34536-116">Šajā gadījumā cenas automātiski tiek atjauninātas gan Sales, gan Commerce.</span><span class="sxs-lookup"><span data-stu-id="34536-116">Prices are then automatically updated in both Sales and Commerce.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="34536-117">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="34536-117">Prerequisites</span></span>

- <span data-ttu-id="34536-118">Pirms varat izmantot Commerce cenu noteikšanas programmu Sales, jāseko darbībām, kas norādītas [Potenciālais klients līdz naudai duālajā rakstīšanā](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span><span class="sxs-lookup"><span data-stu-id="34536-118">Before you can use the Commerce pricing engine in Sales, you must follow the steps in [Prospect-to-cash in dual-write](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/).</span></span>
- <span data-ttu-id="34536-119">Lai veiktu manuālu ievadi, jāizslēdz tirdzniecības līgumu novērtēšana, veicot tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="34536-119">You must turn off trade agreement evaluation for manual entry by following these steps:</span></span>

    1. <span data-ttu-id="34536-120">Savā Commerce vidē dodieties uz **Debitoru parādi \> Iestatīšana \> Debitoru parādu parametri**.</span><span class="sxs-lookup"><span data-stu-id="34536-120">In your Commerce environment, go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
    1. <span data-ttu-id="34536-121">Cilnē **Cenas**, kas atrodas kopsavilkuma cilnē **Tirdzniecības līguma novērtēšana**, nodzēsiet izvēles rūtiņu **Manuālā ievade**.</span><span class="sxs-lookup"><span data-stu-id="34536-121">On the **Prices** tab, on the **Trade agreement evaluation** FastTab, clear the **Manual entry** check box.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34536-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="34536-122">Additional resources</span></span>

[<span data-ttu-id="34536-123">Potenciālā klienta-naudas duālais ieraksts</span><span class="sxs-lookup"><span data-stu-id="34536-123">Prospect-to-cash in dual-write</span></span>](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-prospect-to-cash/)

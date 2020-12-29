---
title: Preču konfiguratora problēmu novēršana
description: Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar preču konfiguratoru.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: dacc7205eaf2084f6fbd3be9d8ac0572f9e1bcde
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516831"
---
# <a name="troubleshoot-the-product-configurator"></a><span data-ttu-id="c5c3e-103">Preču konfiguratora problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="c5c3e-103">Troubleshoot the product configurator</span></span>

<span data-ttu-id="c5c3e-104">Šajā tēmā ir aprakstīts, kā labot problēmas, kas var rasties, strādājot ar preču konfiguratoru.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-104">This topic describes how to fix issues that you might encounter while you work with the product configurator.</span></span>

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a><span data-ttu-id="c5c3e-105">Krājuma teksts tiek pārrakstīts, konfigurējot preci pārdošanas pasūtījuma rindā.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-105">Item text is overwritten when I configure a product on a sales order line.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c5c3e-106">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="c5c3e-106">Issue description</span></span>

<span data-ttu-id="c5c3e-107">Šī problēma rodas, veidojot pārdošanas pasūtījuma rindu konfigurējamam krājumam un pēc tam modificējot krājuma tekstu.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-107">This issue occurs when you create a sales order line for a configurable item and then modify the item text.</span></span> <span data-ttu-id="c5c3e-108">Konfigurējot krājumu un pēc tam atlasot **Labi**, teksts tiek pārrakstīts ar standarta tekstu.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-108">When you configure the item and then select **OK**, the text is overwritten with the standard text.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c5c3e-109">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="c5c3e-109">Issue resolution</span></span>

<span data-ttu-id="c5c3e-110">Šāda darbība ir paredzama.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-110">This behavior is expected.</span></span> <span data-ttu-id="c5c3e-111">Teksta lauks ietver varianta nosaukumu, kas tiek aizpildīts tikai pēc rindas konfigurēšanas.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-111">The text field includes the variant name, which is filled in only after you configure the line.</span></span> <span data-ttu-id="c5c3e-112">Tāpēc teksts ir jāmaina pēc rindas konfigurācijas, nevis pirms tam.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-112">Therefore, you must change the text after you've configured the line, not before.</span></span>

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a><span data-ttu-id="c5c3e-113">Ja tiek aprēķināti preču konfigurācijas modeļi, tiek nepareizi noapaļoti veseli skaitļi.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-113">Integer attributes are incorrectly rounded when product configuration models are calculated.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c5c3e-114">Problēmas apraksts</span><span class="sxs-lookup"><span data-stu-id="c5c3e-114">Issue description</span></span>

<span data-ttu-id="c5c3e-115">Šī problēma var rasties, veicot šādas darbību sērijas:</span><span class="sxs-lookup"><span data-stu-id="c5c3e-115">This issue can occur when you perform the following series of actions:</span></span>

1. <span data-ttu-id="c5c3e-116">Iestatiet šādus atribūtus ražošanas konfigurācijas modelim:</span><span class="sxs-lookup"><span data-stu-id="c5c3e-116">Set up the following attributes on a production configuration model:</span></span>

    - <span data-ttu-id="c5c3e-117">Ievade (vesels skaitlis)</span><span class="sxs-lookup"><span data-stu-id="c5c3e-117">Input (integer)</span></span>
    - <span data-ttu-id="c5c3e-118">Procenti (decimāls)</span><span class="sxs-lookup"><span data-stu-id="c5c3e-118">Percent (decimal)</span></span>
    - <span data-ttu-id="c5c3e-119">Rezultāts (vesels skaitlis)</span><span class="sxs-lookup"><span data-stu-id="c5c3e-119">Result (integer)</span></span>

2. <span data-ttu-id="c5c3e-120">Izveidojiet aprēķinu, kam ir turpmāk aprakstītā izteiksme:</span><span class="sxs-lookup"><span data-stu-id="c5c3e-120">Create a calculation that has the following expression:</span></span>

    <span data-ttu-id="c5c3e-121">*Rezultāts* = *Ievade* x *Procenti* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="c5c3e-121">*Result* = *Input* × *Percent* ÷ 100</span></span>

<span data-ttu-id="c5c3e-122">Šādā gadījumā veselā skaitļa rezultāts ne vienmēr tiek noapaļots.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-122">In this case, the integer result isn't always correctly rounded.</span></span> <span data-ttu-id="c5c3e-123">Piemēram, ievade ir 1000, un procentuālā vērtība ir 2,40.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-123">For example, the input is 1,000, and the percentage is 2.40.</span></span> <span data-ttu-id="c5c3e-124">Tāpēc paredzams, ka veselā skaitļa rezultāts ir 24, jo 2,40 procenti no 1000 ir 24 (vai 24,00 decimālā formā).</span><span class="sxs-lookup"><span data-stu-id="c5c3e-124">Therefore, you expect the integer result to be 24, because 2.40 percent of 1,000 is 24 (or 24.00 in decimal form).</span></span> <span data-ttu-id="c5c3e-125">Tā vietā rezultāts tiek attēlots kā 23.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-125">Instead, the result is shown as 23.</span></span> <span data-ttu-id="c5c3e-126">Tomēr, ja procentuālais daudzums ir 2,39, aprēķins tiek noapaļots uz 24, nevis 23.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-126">However, when the percentage is 2.39, the calculation is rounded to 24 instead of 23.</span></span> <span data-ttu-id="c5c3e-127">Kad procentuālais daudzums ir 2,50, aprēķins tiek noapaļots uz 25, kā paredzēts.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-127">When the percentage is 2.50, the calculation is rounded to 25, as expected.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c5c3e-128">Problēmas risinājums</span><span class="sxs-lookup"><span data-stu-id="c5c3e-128">Issue resolution</span></span>

<span data-ttu-id="c5c3e-129">Šī problēma rodas tādēļ, ka Microsoft Solver Foundation iekšēji ataino skaitļus, izmantojot daļskaitļus.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-129">This issue occurs because of the way that Microsoft Solver Foundation internally represents numbers by using fractions.</span></span> <span data-ttu-id="c5c3e-130">Iepriekšējā piemērā aprēķina rezultāts, kur procentuālā vērtība ir 2,40, tiek parādīts kā 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-130">For the preceding example, the result of the calculation where the percentage is 2.40 is represented as 27021597764222975 ÷ 1125899906842624 = 23.99999999999999911182158029987476766109466552734375.</span></span> <span data-ttu-id="c5c3e-131">Kad .NET šo vērtību izmanto kā veselu skaitli, tas atgriezīs 23.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-131">When .NET casts this value as an integer, it will return 23.</span></span>

<span data-ttu-id="c5c3e-132">Šo darbību nevar mainīt, jo no tās ir atkarīgi citi scenāriji.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-132">This behavior won't be changed, because other scenarios depend on it.</span></span> <span data-ttu-id="c5c3e-133">Iepriekšējā piemērā varat novērst problēmu, ieviešot papildu decimālu atribūtu un aprēķinu.</span><span class="sxs-lookup"><span data-stu-id="c5c3e-133">For the preceding example, you can fix the issue by introducing an additional decimal attribute and a calculation.</span></span>

<span data-ttu-id="c5c3e-134">Piemēram, varat iestatīt šādus atribūtus ražošanas konfigurācijas modelim:</span><span class="sxs-lookup"><span data-stu-id="c5c3e-134">For example, you can set up the following attributes on a production configuration model:</span></span>

- <span data-ttu-id="c5c3e-135">Ievade (vesels skaitlis)</span><span class="sxs-lookup"><span data-stu-id="c5c3e-135">Input (integer)</span></span>
- <span data-ttu-id="c5c3e-136">Procenti (decimāls)</span><span class="sxs-lookup"><span data-stu-id="c5c3e-136">Percent (decimal)</span></span>
- <span data-ttu-id="c5c3e-137">ResultDecimal (decimāls)</span><span class="sxs-lookup"><span data-stu-id="c5c3e-137">ResultDecimal (decimal)</span></span>
- <span data-ttu-id="c5c3e-138">ResultInteger (vesels skaitlis)</span><span class="sxs-lookup"><span data-stu-id="c5c3e-138">ResultInteger (integer)</span></span>

<span data-ttu-id="c5c3e-139">Varat pievienot šādus aprēķinus:</span><span class="sxs-lookup"><span data-stu-id="c5c3e-139">You can then add the following calculations:</span></span>

- <span data-ttu-id="c5c3e-140">*ResultDecimal* = *Ievade* x *Procenti* ÷ 100</span><span class="sxs-lookup"><span data-stu-id="c5c3e-140">*ResultDecimal* = *Input* × *Percent* ÷ 100</span></span>
- <span data-ttu-id="c5c3e-141">*ResultInteger* = *ResultDecimal*</span><span class="sxs-lookup"><span data-stu-id="c5c3e-141">*ResultInteger* = *ResultDecimal*</span></span>

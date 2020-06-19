---
title: Izveidot un lietot kreditoru maksājumu ieturējumu nosacījumus
description: Šajā tēmā ir sniegta informācija par to, kā iestatīt un uzturēt ieturējumu nosacījumus kreditoru maksājumiem.
author: kfend
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 0e14050a79220b5d02763a025040edb934489d00
ms.sourcegitcommit: cecd97fd74ff7b31f1a677e8fdf3e233aa28ef5a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/28/2020
ms.locfileid: "3410245"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="d0aa9-103">Izveidot un lietot kreditoru maksājumu ieturējumu nosacījumus</span><span class="sxs-lookup"><span data-stu-id="d0aa9-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="d0aa9-104">Kreditora maksājuma ieturējuma nosacījumu iestatīšana projektam ir noderīga, ja jūsu organizācija vēlas saglabāt daļu no kreditoriem veiktajiem maksājumiem.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="d0aa9-105">Piemēram, ja vēlaties aizturēt maksājumu kreditoram, līdz piegādātās preces atbilst jūsu vēlmēm.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="d0aa9-106">Kreditora maksājuma nosacījumus varat norādīt, kad vienojaties par kreditora līgumu.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="d0aa9-107">Kreditora maksājuma ieturējumu nosacījumu izveide</span><span class="sxs-lookup"><span data-stu-id="d0aa9-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="d0aa9-108">Var ievadīt procentuālo daļu, kas ir jāietur no maksājuma kreditoram, un iepriekš ieturēto summu procentuālo daļu, kas ir jānodod izpildei.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="d0aa9-109">Summas tiek automātiski ieturētas no kreditora rēķiniem, līdz ir sasniegts līgumā norādītais pabeigtības stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="d0aa9-110">Kad kreditora ieturējumu nosacījumi ir iestatīti, tos var lietot jebkurā projektā šim kreditoram.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="d0aa9-111">Izmantojiet tālāk minētās darbības, lai iestatītu un uzturētu ieturējumu nosacījumus maksājumiem, kas veicami kreditoram.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="d0aa9-112">Dodieties uz **Projektu vadība un uzskaite** > **Ieturējumi** > **Kreditora maksājumu ieturējumu nosacījumi**.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="d0aa9-113">Atlasiet **Jauns**, lai pievienotu jaunu kreditora ieturējumu nosacījumu.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="d0aa9-114">Jaunā nosacījuma vērtība **Kārtulas ID** tiek ievadīta automātiski.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="d0aa9-115">Ievadiet īsu aprakstu laukā **Apraksts** un kopsavilkuma cilnē **Nosacījumi** atlasiet vienumu **Pievienot rindu**, lai ievadītu terminu vērtības tālāk minētajam.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="d0aa9-116">**Piegādāto vienību procentuālā daļa**: ievadiet procentuālo daļu, kuru sasniedzot nosacījums ir jāizpilda.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="d0aa9-117">Summas tiek automātiski ieturētas no kreditora rēķiniem, līdz projekta pabeigtības posms ir vienāds ar norādīto procentuālo daļu.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="d0aa9-118">Piemēram, ja ievadāt 50,00 procentus, summa tiek saglabāta kā ieturēta līdz brīdim, kad projekta pabeigtība sasniegs 50 procentus.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="d0aa9-119">**Uzkrājamie procenti**: ievadiet procentuālo daļu, kas ir ieturama no kreditora rēķina summas.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="d0aa9-120">Piemēram, ja ievadāt 10.00, tad 10 procenti no kreditora rēķinu summas tiek ieturēti, līdz projektā ir sasniegts pabeigtības stāvoklis, ko atlasījāt kā iestatītu **Piegādāto vienību procentuālās daļas lauks**.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="d0aa9-121">**Procentuālā daļa, kas jānodod izpildei**: atlasiet **Pievienot rindu**, lai ievadītu iepriekš ieturēto summu procentuālo daļu, kas ir jānodod izpildei, kad projektā ir sasniegts pabeigtības stāvoklis.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="d0aa9-122">Ja dažādos projekta līmeņos ir iestatīti dažādi pabeigtības stāvokļi, katrai ieturējumu kārtulai ievadiet atsevišķu rindu ar kreditora ieturējumu nosacījumiem.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="d0aa9-123">Katrā rindā var norādīt atšķirīgu ieturamo procentuālo daļu un atšķirīgu procentuālo daļu, kas ir jānodod izpildei, katrā projekta pabeigtības līmenī.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="d0aa9-124">Kad kreditora ieturējumu nosacījumi ir izveidoti, varat lietot šos nosacījumus projektam.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="d0aa9-125">Kreditora ieturējumu nosacījumu lietošana projektam</span><span class="sxs-lookup"><span data-stu-id="d0aa9-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="d0aa9-126">Dodieties uz **Projektu vadība un uzskaite** > **Projekti** > **Visi projekti** un projektu saraksta lapā atveriet projektu.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="d0aa9-127">Kopsavilkuma cilnē **Kreditora līgumi** atlasiet **Pievienot rindu**.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="d0aa9-128">Laukā **Konta kods** atlasiet kādu no tālāk minētajām opcijām.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="d0aa9-129">**Tabula**: kreditora ieturējumu nosacījumi attiecas uz vienu kreditoru.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="d0aa9-130">**Grupa**: kreditora ieturējumu nosacījumi attiecas uz visiem kreditoriem kreditoru grupā.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="d0aa9-131">**Visi**: kreditora ieturējumu nosacījumi attiecas uz visiem kreditoriem.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="d0aa9-132">Laukā **Kreditors/kreditoru grupa** atlasiet kreditoru vai kreditoru grupu, uz kuru attiecas kreditora ieturējumu nosacījumi.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="d0aa9-133">Šis lauks nav pieejams, ja iepriekšējā transakcijā izvēlējāties **Visi**.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="d0aa9-134">Laukā **Kreditora ieturējumu nosacījumi** atlasiet ieturējumu nosacījumus, kurus izveidojāt iepriekšējā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="d0aa9-135">Ja projektā kreditoram ir iestatīti “apmaksāt pēc apmaksas” (PWP — pay-when-paid) veida nosacījumi, laukā **PWP sliekšņa procentuālā vērtība** ievadiet projekta sliekšņa procentuālo vērtību.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="d0aa9-136">Kreditora ieturējumu nosacījumi tiek parādīti arī pirkšanas pasūtījumos, ko izveidojat kreditoram.</span><span class="sxs-lookup"><span data-stu-id="d0aa9-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>

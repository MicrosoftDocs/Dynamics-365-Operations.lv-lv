---
title: Sākotnējā rēķina atsauces kredīta notās
description: Šajā tēmā ir paskaidrots, kā iestatīt un drukāt sākotnējo rēķinu numurus saistītajās kredīta notās.
author: ilkond
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 04a4fc96cb7de60052b17e36c33ad5d5be322be4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207355"
---
# <a name="references-to-original-invoices-in-credit-notes"></a><span data-ttu-id="36902-103">Sākotnējā rēķina atsauces kredīta notās</span><span class="sxs-lookup"><span data-stu-id="36902-103">References to original invoices in credit notes</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="36902-104">Dažās valstīs un reģionos pastāv juridiska prasība, ka drukātajās kredīta notās jāietver atsauces uz sākotnējiem rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="36902-104">In some countries and regions, there is a legal requirement that printed credit notes include references to the original invoices.</span></span> <span data-ttu-id="36902-105">Šajā tēmā ir paskaidrots, kā iestatīt un drukāt sākotnējo rēķinu numurus saistītajās kredīta notās.</span><span class="sxs-lookup"><span data-stu-id="36902-105">This topic explains how to set up and print the original invoice numbers in related credit notes.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="36902-106">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="36902-106">Prerequisites</span></span>

- <span data-ttu-id="36902-107">Darbvietā **Līdzekļu pārvaldība** ieslēdziet līdzekli **Kredīta rēķinu izkārtojums pārdošanas un projekta rēķinu atskaitēs**.</span><span class="sxs-lookup"><span data-stu-id="36902-107">In the **Feature management** workspace, turn on the **Credit invoicing layout for sales and project invoice reports** feature.</span></span> <span data-ttu-id="36902-108">Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="36902-108">For more information, see [Feature management overview](../../fin-and-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="36902-109">Nepieciešamo dokumentu drukājamie formāti ir jākonfigurē Drukas pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="36902-109">The printable formats of the required documents must be configured in Print management.</span></span>

<span data-ttu-id="36902-110">Šajā tēmā aprakstītā funkcionalitāte attiecas uz šādiem dokumentiem:</span><span class="sxs-lookup"><span data-stu-id="36902-110">The functionality that is described in this topic applies to the following documents:</span></span>

<span data-ttu-id="36902-111">**Debitori**</span><span class="sxs-lookup"><span data-stu-id="36902-111">**Accounts receivable**</span></span>

- <span data-ttu-id="36902-112">Brīva teksta kredīta nota</span><span class="sxs-lookup"><span data-stu-id="36902-112">Free text credit note</span></span>
- <span data-ttu-id="36902-113">Debitora kredīta nota</span><span class="sxs-lookup"><span data-stu-id="36902-113">Customer credit note</span></span>

<span data-ttu-id="36902-114">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="36902-114">**Project management and accounting**</span></span>

- <span data-ttu-id="36902-115">Projekta kredīta nota</span><span class="sxs-lookup"><span data-stu-id="36902-115">Project credit note</span></span>

## <a name="configure-accounts-receivable-parameters"></a><span data-ttu-id="36902-116">Debitoru parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="36902-116">Configure Accounts receivable parameters</span></span>

<span data-ttu-id="36902-117">Izpildiet šīs darbības, lai iestatītu parametru, kas kontrolē, vai atsauces uz sākotnējiem rēķiniem tiek drukātas saistītajās kredīta notās.</span><span class="sxs-lookup"><span data-stu-id="36902-117">Follow these steps to set the parameter that controls whether references to the original invoices are printed in related credit notes.</span></span>

1. <span data-ttu-id="36902-118">Dodieties uz **Debitori** \> **Iestatīšana** \> **Debitoru parametri**.</span><span class="sxs-lookup"><span data-stu-id="36902-118">Go to **Accounts receivable** \> **Setup** \> **Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="36902-119">Cilnes **Atjauninājumi** kopsavilkuma cilnē **Rēķins** iestatiet opciju **Lietot kredīta rēķinu izrakstīšanas izkārtojumu pārdošanas un projektu rēķinu pārskatos** uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="36902-119">On the **Updates** tab, on the **Invoice** FastTab, set the **Apply the credit invoicing layout into sales and project invoice reports** option to **Yes**.</span></span>

![Debitoru parametru konfigurēšana](media/original-invoice-number-in-credit-note.jpg)

## <a name="define-references-to-original-invoices"></a><span data-ttu-id="36902-121">Atsauču definēšana sākotnējiem rēķiniem</span><span class="sxs-lookup"><span data-stu-id="36902-121">Define references to original invoices</span></span>

<span data-ttu-id="36902-122">Izmantojiet tālāk uzskaitītās procedūras, lai definētu atsauces sākotnējiem rēķiniem, pamatojoties uz dokumenta veidu.</span><span class="sxs-lookup"><span data-stu-id="36902-122">Use the following procedures to define references to original invoices, based on the document type.</span></span>

### <a name="free-text-credit-note"></a><span data-ttu-id="36902-123">Brīva teksta kredīta nota</span><span class="sxs-lookup"><span data-stu-id="36902-123">Free text credit note</span></span>

1. <span data-ttu-id="36902-124">Atveriet sadaļas **Debitoru parādi** \> **Rēķini** \> **Visi brīvā teksta rēķini**.</span><span class="sxs-lookup"><span data-stu-id="36902-124">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="36902-125">Izveidojiet jaunu kredīta notu vai atlasiet esošu kredīta notu.</span><span class="sxs-lookup"><span data-stu-id="36902-125">Create a new credit note, or select an existing credit note.</span></span>
3. <span data-ttu-id="36902-126">Atveriet rēķinu.</span><span class="sxs-lookup"><span data-stu-id="36902-126">Open the invoice.</span></span>
4. <span data-ttu-id="36902-127">Darbību rūtī, cilnē **Rēķins**, grupā **Funkcijas** atlasiet **Kredīta rēķinu izrakstīšana**.</span><span class="sxs-lookup"><span data-stu-id="36902-127">On the Action Pane, on the **Invoice** tab, in the **Functions** group, select **Credit invoicing**.</span></span>
5. <span data-ttu-id="36902-128">Ievadiet atsauci uz sākotnējo rēķinu un atlasiet labojuma pamatojumu.</span><span class="sxs-lookup"><span data-stu-id="36902-128">Enter the reference to the original invoice, and select the reason for the correction.</span></span>

![Atsauču definēšana brīva teksta rēķinam](media/reference-original-invoice-FTI.jpg)

### <a name="customer-credit-note"></a><span data-ttu-id="36902-130">Debitora kredīta nota</span><span class="sxs-lookup"><span data-stu-id="36902-130">Customer credit note</span></span>

1. <span data-ttu-id="36902-131">Doties uz **Debitori** \> **Pasūtījumi** \> **Visi pārdošanas pasūtījumi**.</span><span class="sxs-lookup"><span data-stu-id="36902-131">Go to **Accounts receivable** \> **Orders** \> **All sales orders**.</span></span>
2. <span data-ttu-id="36902-132">Atlasiet un atveriet rēķinā iekļauto pārdošanas pasūtījumu, kas ir jālabo.</span><span class="sxs-lookup"><span data-stu-id="36902-132">Select and open the invoiced sales order that must be corrected.</span></span>
3. <span data-ttu-id="36902-133">Darbību rūtī, cilnē **Pārdošana**, grupā **Kredīta nota** atlasiet **Kredīta nota**.</span><span class="sxs-lookup"><span data-stu-id="36902-133">On the Action Pane, on the **Sell** tab, in the **Credit note** group, select **Credit note**.</span></span>
4. <span data-ttu-id="36902-134">Ievadiet labošanas iemeslu.</span><span class="sxs-lookup"><span data-stu-id="36902-134">Enter the reason for the correction.</span></span> <span data-ttu-id="36902-135">Atsauce uz sākotnējo rēķinu tiek izveidota automātiski.</span><span class="sxs-lookup"><span data-stu-id="36902-135">The reference to the original invoice is automatically established.</span></span>

![Atsauču definēšana pārdošanas pasūtījumam](media/reference-original-invoice-SO.jpg)

### <a name="project-credit-note"></a><span data-ttu-id="36902-137">Projekta kredīta nota</span><span class="sxs-lookup"><span data-stu-id="36902-137">Project credit note</span></span>

1. <span data-ttu-id="36902-138">Dodieties uz **Projektu pārvaldība un uzskaite** \> **Projekta rēķini** \> **Projekta rēķini**.</span><span class="sxs-lookup"><span data-stu-id="36902-138">Go to **Project management and accounting** \> **Project invoices** \> **Project invoices**.</span></span>
2. <span data-ttu-id="36902-139">Atlasiet un atveriet projekta rēķinu, kas ir jālabo.</span><span class="sxs-lookup"><span data-stu-id="36902-139">Select and open the project invoice that must be corrected.</span></span>
3. <span data-ttu-id="36902-140">Darbību rūtī, cilnē **Projekta rēķins**, grupā **Funkcijas** atlasiet **Atlasīt kredīta notai**.</span><span class="sxs-lookup"><span data-stu-id="36902-140">On the Action Pane, on the **Project invoice** tab, in the **Functions** group, select **Select for credit note**.</span></span>
4. <span data-ttu-id="36902-141">Atlasiet **Kredīta rēķina izrakstīšana**.</span><span class="sxs-lookup"><span data-stu-id="36902-141">Select **Credit invoicing**.</span></span>
5. <span data-ttu-id="36902-142">Ievadiet labošanas iemeslu.</span><span class="sxs-lookup"><span data-stu-id="36902-142">Enter the reason for the correction.</span></span> <span data-ttu-id="36902-143">Atsauce uz sākotnējo rēķinu tiek izveidota automātiski.</span><span class="sxs-lookup"><span data-stu-id="36902-143">The reference to the original invoice is automatically established.</span></span>

![Atsauču definēšana projekta rēķinam](media/reference-original-invoice-project.jpg)

## <a name="printing-credit-notes"></a><span data-ttu-id="36902-145">Kredīta notu drukāšana</span><span class="sxs-lookup"><span data-stu-id="36902-145">Printing credit notes</span></span>

<span data-ttu-id="36902-146">Drukājot brīvā teksta, klienta un projekta kredīta notas, tajās tiks iekļauta atsauce uz sākotnējo rēķinu un labošanas iemeslu.</span><span class="sxs-lookup"><span data-stu-id="36902-146">When you print free text, customer, and project credit notes, they will include the reference to the original invoice and the correction reason.</span></span>

![Drukāta kredīta nota](media/credit-note-FTI.jpg)

> [!NOTE]
> <span data-ttu-id="36902-148">Pārliecinieties, vai dokumentu drukājamie formāti ir pareizi konfigurēti, pieņemot, ka tiks drukātas atsauces uz sākotnējiem rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="36902-148">Make sure that the printable formats of the documents are correctly configured, on the assumption that references to original invoices will be printed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
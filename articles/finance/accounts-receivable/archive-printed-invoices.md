---
title: Izdrukātie debitoru rēķini ar jaukšanas numuriem — arhivēšana
description: Šajā tēmā paskaidrots, kā iespējot arhivēšanu, lai glabātu drukātos klientu rēķinus ar jaukšanas numuriem.
author: ilyako
manager: AnnBe
ms.date: 03/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 539093
ms.search.region: Global
ms.author: ilyako
ms.search.validFrom: 2021-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: d502ec5d286573c72e207419b66f283183009c09
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557484"
---
# <a name="archive-printed-customer-invoices-with-hash-numbers"></a><span data-ttu-id="71450-103">Izdrukātie debitoru rēķini ar jaukšanas numuriem — arhivēšana</span><span class="sxs-lookup"><span data-stu-id="71450-103">Archive printed customer invoices with hash numbers</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="71450-104">Dažās valstīs pastāv tiesiska prasība glabāt aprēķinātos jauktos numurus sistēmā kopā ar dažu dokumentu izdrukām.</span><span class="sxs-lookup"><span data-stu-id="71450-104">In some countries, there is a legal requirement to store calculated hash numbers in the system together with printouts of some documents.</span></span> <span data-ttu-id="71450-105">Jauktos numurus var izmantot, lai ziņotu iestādēm, un auditu laikā.</span><span class="sxs-lookup"><span data-stu-id="71450-105">Hash numbers can be used for reporting to authorities and during audits.</span></span>

<span data-ttu-id="71450-106">Šajā tēmā paskaidrots, kā konfigurēt arhivēšanu, lai glabātu drukātos klientu rēķinus ar jaukšanas numuriem.</span><span class="sxs-lookup"><span data-stu-id="71450-106">This topic explains how to configure archiving in order to store printed customer invoices with hash numbers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="71450-107">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="71450-107">Prerequisites</span></span>

- <span data-ttu-id="71450-108">Darbvietā **Līdzekļu pārvaldība** iespējojiet līdzekli **Arhivēt drukātos klientu rēķinus ar jauktajiem numuriem**.</span><span class="sxs-lookup"><span data-stu-id="71450-108">In the **Feature management** workspace, turn on the feature, **Archive printed customer invoices with hash numbers**.</span></span> <span data-ttu-id="71450-109">Papildinformāciju skatiet [Līdzekļu pārvaldības pārskatā](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="71450-109">For more information, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
- <span data-ttu-id="71450-110">Konfigurējiet nepieciešamo dokumentu drukājamos formātus **Drukāšanas pārvaldībā**.</span><span class="sxs-lookup"><span data-stu-id="71450-110">Configure the printable formats of required documents in **Print management**.</span></span>

<span data-ttu-id="71450-111">Šī funkcionalitāte ir piemērojama šādiem dokumentiem:</span><span class="sxs-lookup"><span data-stu-id="71450-111">This functionality is applicable to the following documents.</span></span>

<span data-ttu-id="71450-112">**Debitori**</span><span class="sxs-lookup"><span data-stu-id="71450-112">**Accounts receivable**</span></span>
- <span data-ttu-id="71450-113">Rēķins debitoram</span><span class="sxs-lookup"><span data-stu-id="71450-113">Customer invoice</span></span>
- <span data-ttu-id="71450-114">Debitora kredīta nota</span><span class="sxs-lookup"><span data-stu-id="71450-114">Customer credit note</span></span>
- <span data-ttu-id="71450-115">Brīva teksta rēķins</span><span class="sxs-lookup"><span data-stu-id="71450-115">Free text invoice</span></span>
- <span data-ttu-id="71450-116">Kredīta nota brīvā tekstā</span><span class="sxs-lookup"><span data-stu-id="71450-116">Free text credit note</span></span>

<span data-ttu-id="71450-117">**Projektu pārvaldība un uzskaite**</span><span class="sxs-lookup"><span data-stu-id="71450-117">**Project management and accounting**</span></span>
- <span data-ttu-id="71450-118">Projekta rēķins</span><span class="sxs-lookup"><span data-stu-id="71450-118">Project invoice</span></span>
- <span data-ttu-id="71450-119">Projekta kredīta nota</span><span class="sxs-lookup"><span data-stu-id="71450-119">Project credit note</span></span>

## <a name="configure-customer-master-data"></a><span data-ttu-id="71450-120">Klienta pamatdatu konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="71450-120">Configure customer master data</span></span>
<span data-ttu-id="71450-121">Izpildiet šīs darbības, lai konfigurētu klienta datus un iespējotu iespēju automātiski saglabāt drukātos rēķinus kā pielikumus.</span><span class="sxs-lookup"><span data-stu-id="71450-121">Complete the following steps to configure customer data and turn on the ability to automatically save printed invoices as attachments.</span></span>

1. <span data-ttu-id="71450-122">Dodieties uz **Debitori** > **Visi klienti**.</span><span class="sxs-lookup"><span data-stu-id="71450-122">Go to **Accounts receivable** > **All customers**.</span></span> 
2. <span data-ttu-id="71450-123">Atlasiet klientu un kopsavilkuma cilnē **Rēķins un piegāde**, sadaļā **Elektroniskais rēķins**, laukā **Elektroniskā rēķina pielikums** atlasiet **Jā**.</span><span class="sxs-lookup"><span data-stu-id="71450-123">Select a customer, and on the **Invoice and delivery** FastTab, in the **E-INVOCE** section, in the **eInvoice attachment** field, select **Yes**.</span></span>

## <a name="print-invoices"></a><span data-ttu-id="71450-124">Rēķinu drukāšana</span><span class="sxs-lookup"><span data-stu-id="71450-124">Print invoices</span></span>
<span data-ttu-id="71450-125">Jūs varat izvietot un drukāt jebkuru brīvā teksta, klienta un projekta rēķinu vai kredīta notu klientam, kas konfigurēts iepriekšējā procedūrā.</span><span class="sxs-lookup"><span data-stu-id="71450-125">You can post and print any free text, customer, and project invoice or credit note for the customer configured in the previous procedure.</span></span>

<span data-ttu-id="71450-126">Atveriet drukātā rēķina lapu **Pielikumi**.</span><span class="sxs-lookup"><span data-stu-id="71450-126">Open the **Attachments** page for the printed invoice.</span></span> <span data-ttu-id="71450-127">Kopsavilkuma cilnē **Pielikums**, lauka grupā **Papildu informācija**, laukā **Dokumenta jauktais numurs** atrodiet glabāto jaukto numuru, kas aprēķināts drukātajam rēķinam.</span><span class="sxs-lookup"><span data-stu-id="71450-127">On the **Attachment** FastTab, in the **Additional details** field group, in **Document hash number** field, find the stored hash number calculated for the printed invoice.</span></span>

![Pielikuma jauktais numurs](media/attach-hash-num.jpg)

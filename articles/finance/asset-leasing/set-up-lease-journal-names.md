---
title: Nomas žurnālu nosaukumu iestatīšana
description: Šajā tēmā skaidrots, kā definēt nomas žurnāla nosaukumus. Nomas žurnāla nosaukumi norāda žurnālus, kuros tiek grāmatoti ieraksti, kas radušies līdzekļu nomā.
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
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 89c5fc768aafe9e5de9adcde32e7b4d0a084941b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990921"
---
# <a name="set-up-lease-journal-names"></a><span data-ttu-id="31556-104">Nomas žurnālu nosaukumu iestatīšana</span><span class="sxs-lookup"><span data-stu-id="31556-104">Set up lease journal names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="31556-105">Nomas žurnāla nosaukumi norāda žurnālus, kuros tiek grāmatoti līdzekļu nomas darījumi.</span><span class="sxs-lookup"><span data-stu-id="31556-105">Lease journal names specify the journals that Asset leasing transactions are posted to.</span></span> <span data-ttu-id="31556-106">Tikai tie žurnālu nosaukumi, kas ir piešķirti žurnāla tipam **Līdzekļu noma**, tiek parādīti laukos **Sākotnējā atzīšana** un **Ikmēneša žurnāla nosaukums**, kas atrodas lapā **Līdzekļu nomas parametri**.</span><span class="sxs-lookup"><span data-stu-id="31556-106">Only journal names that are assigned to the **Asset leasing** journal type appear in the **Initial Recognition** and **Monthly Journal Name** fields on the **Asset leasing parameters** page.</span></span> <span data-ttu-id="31556-107">Laukam **Rēķina žurnāla nosaukums** var piešķirt tikai žurnāla tipu **Kreditora žurnāla ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="31556-107">Only **vendor invoice recording** journal type can be assigned to the **Invoice journal name** field.</span></span>

<span data-ttu-id="31556-108">Lai konfigurētu nomas žurnālu nosaukumus, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="31556-108">To configure lease journal names, follow these steps.</span></span>

1. <span data-ttu-id="31556-109">Dodieties uz **Līdzekļu noma \> Iestatījumi \> Līdzekļu nomas parametri**.</span><span class="sxs-lookup"><span data-stu-id="31556-109">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="31556-110">Cilnes **Vispārīgi** laukā **Sākotnējais atzīšanas žurnāla nosaukums** atlasiet žurnālu.</span><span class="sxs-lookup"><span data-stu-id="31556-110">On the **General** tab, in the **Initial recognition journal name** field, and select a journal.</span></span> <span data-ttu-id="31556-111">Visi sākotnējās atzīšanas žurnāla ieraksti tiks grāmatoti šajā žurnāla nosaukumā.</span><span class="sxs-lookup"><span data-stu-id="31556-111">All initial recognition journal entries will be posted to this journal name.</span></span>
3. <span data-ttu-id="31556-112">Laukā **Rēķina žurnāla nosaukums** atlasiet žurnālu.</span><span class="sxs-lookup"><span data-stu-id="31556-112">In the **Invoice journal name** field, select a journal.</span></span> <span data-ttu-id="31556-113">Ja opcija **Maksāt kreditoram** ir iestatīta uz **Jā** nomas grāmatai, nomas un izdevumu maksājumu rēķini tiks grāmatoti šajā žurnāla nosaukumā.</span><span class="sxs-lookup"><span data-stu-id="31556-113">If the **Pay to vendor** option is set to **Yes** for the lease book, lease and expense payment invoices will be posted to this journal name.</span></span>
4. <span data-ttu-id="31556-114">Laukā **Nomas žurnāla nosaukums** atlasiet žurnālu.</span><span class="sxs-lookup"><span data-stu-id="31556-114">In the **Lease journal name** field, select a journal.</span></span> <span data-ttu-id="31556-115">Visi nolietojuma, procentu un īstermiņa pārklasificēšanas ieraksti tiks grāmatoti šajā žurnāla nosaukumā.</span><span class="sxs-lookup"><span data-stu-id="31556-115">All depreciation, interest, and short-term reclassification entries will be posted to this journal name.</span></span> <span data-ttu-id="31556-116">Ja opcija **Maksāt kreditoram** ir iestatīta uz **Nē** nomas grāmatai, nomas maksājumu un izdevumu ieraksti arī tiks grāmatoti šajā žurnāla nosaukumā.</span><span class="sxs-lookup"><span data-stu-id="31556-116">If the **Pay to vendor** option is set to **No** for the lease book, lease payments and expense payment entries will also be posted to this journal name.</span></span>

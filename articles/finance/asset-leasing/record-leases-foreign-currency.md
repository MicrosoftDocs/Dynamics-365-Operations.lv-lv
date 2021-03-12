---
title: Nomu reģistrēšana ārvalstu valūtās
description: Šajā tēmā skaidrots, kā reģistrēt nomu valūtā, kas nav uzskaites vai pārskata valūta.
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
ms.openlocfilehash: 92177d4f808bfec88dabe9277c3d584ed02e401e
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/28/2020
ms.locfileid: "4445784"
---
# <a name="record-leases-in-foreign-currencies"></a><span data-ttu-id="98873-103">Nomu reģistrēšana ārvalstu valūtās</span><span class="sxs-lookup"><span data-stu-id="98873-103">Record leases in foreign currencies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98873-104">Līdzekļu līzinga konti nomai, kas ir valūtās, kas nav uzskaites valūta vai pārskata valūta, ir izveidoti **Virsgrāmatas iestatīšanas** lapā.</span><span class="sxs-lookup"><span data-stu-id="98873-104">Asset leasing accounts for leases that are in currencies other than the accounting currency or the reporting currency are established on the **Ledger setup** page.</span></span> <span data-ttu-id="98873-105">Visas nomas jāievada to darījumu valūtā.</span><span class="sxs-lookup"><span data-stu-id="98873-105">All leases should be entered in their transaction currency.</span></span> <span data-ttu-id="98873-106">Citiem vārdiem sakot, tie jāievada valūtā, kas norādīta nomas līgumā.</span><span class="sxs-lookup"><span data-stu-id="98873-106">In other words, they should be entered in the currency that is specified in the lease contract.</span></span> <span data-ttu-id="98873-107">Šajā tēmā skaidrots, kā reģistrēt nomu valūtā, kas nav uzskaites vai pārskata valūta.</span><span class="sxs-lookup"><span data-stu-id="98873-107">This topic explains how to record leases in currencies other than the accounting or reporting currency.</span></span>

<span data-ttu-id="98873-108">Ja ievadāt nomu ārvalstu valūtā, LLT tiek nolietots gan uzskaites valūtā, gan pārskata valūtā.</span><span class="sxs-lookup"><span data-stu-id="98873-108">If you enter a lease in a foreign currency, the right-of-use (ROU) asset is depreciated in both the accounting currency and the reporting currency.</span></span> <span data-ttu-id="98873-109">Šīs valūtas tiek konfigurētas lapā **Virsgrāmatas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="98873-109">These currencies are configured on the **Ledger setup** page.</span></span> <span data-ttu-id="98873-110">Šo darbību izmanto arī pamatlīdzekļos.</span><span class="sxs-lookup"><span data-stu-id="98873-110">This behavior is also used in Fixed assets.</span></span> <span data-ttu-id="98873-111">Kad jūs izveidojat nomu ārzemju valūtā, laukā **Valūta** atlasiet darījumu valūtu.</span><span class="sxs-lookup"><span data-stu-id="98873-111">When you create a lease in a foreign currency, select the transaction currency in the **Currency** field.</span></span>

<span data-ttu-id="98873-112">Uzskaites valūtas maiņas kurss ir noklusējuma vērtība **uzskaites valūtas maiņas kursa** laukā.</span><span class="sxs-lookup"><span data-stu-id="98873-112">The exchange rate of the accounting currency is the default value in **Accounting currency exchange rate** field.</span></span> <span data-ttu-id="98873-113">Pārskata valūtas maiņas kurss ir noklusējuma vērtība **pārskata valūtas maiņas kursa** laukā.</span><span class="sxs-lookup"><span data-stu-id="98873-113">The exchange rate of the reporting currency is the default value in the **Reporting currency exchange rate** field.</span></span> <span data-ttu-id="98873-114">Šie maiņas kursi bija spēkā nomas sākuma datumā.</span><span class="sxs-lookup"><span data-stu-id="98873-114">These exchange rates were effective on the commencement date of the lease.</span></span> <span data-ttu-id="98873-115">Lauki **Uzskaites valūtas maiņas kurss** un **Pārskata valūtas maiņas kurss** ir kopsavilkuma cilnē **Finanšu un pārskatu maiņas informācija**, kas atrodas lapā **Nomas informācija**.</span><span class="sxs-lookup"><span data-stu-id="98873-115">The **Accounting currency exchange rate** and **Reporting currency exchange rate** fields, are in the **Financial and reporting exchange information** FastTab, on the **Lease details** page.</span></span>

1. <span data-ttu-id="98873-116">Atzīmējiet izvēles rūtiņu **Fiksēts kurss**, lai ignorētu automātiski ievadīto maiņas kursu, un pēc tam ievadiet jauno kursu.</span><span class="sxs-lookup"><span data-stu-id="98873-116">Select the **Fixed rate** check box to override the exchange rate that was automatically entered, and then enter the new rate.</span></span>
2. <span data-ttu-id="98873-117">Citos laukos ievadiet informāciju, kas nepieciešama nomai, un pēc tam atlasiet **Izveidot grafikus**.</span><span class="sxs-lookup"><span data-stu-id="98873-117">In the other fields, enter the information that is required for the lease, and then select **Create schedules**.</span></span>
3. <span data-ttu-id="98873-118">Jaunajā lapā **Nomas informācija** atlasiet **Grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="98873-118">On the new **Lease details** page, select **Books**.</span></span>
4. <span data-ttu-id="98873-119">Lapas **Nomas grāmata** cilnē **Finanšu un pārskatu maiņas kursa informācija** pārbaudiet lauku **Uzskaites valūtas vērtības sākotnējās līdzekļa lietošanas tiesības** un **Pārskata valūtas sākotnējās līdzekļa lietošanas tiesības**.</span><span class="sxs-lookup"><span data-stu-id="98873-119">On the **Lease book** page, on the **Financial and reporting exchange information** tab, verify the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span> <span data-ttu-id="98873-120">Katrs no šiem laukiem parāda tulkoto LLT bilanci atbilstošajā valūtā.</span><span class="sxs-lookup"><span data-stu-id="98873-120">Each of these fields shows the translated ROU asset balance in the corresponding currency.</span></span> <span data-ttu-id="98873-121">Šie lauki tiek atjaunināti ik reizi, kad maināt finansiālu informāciju.</span><span class="sxs-lookup"><span data-stu-id="98873-121">These fields are updated whenever you change any financial information.</span></span> <span data-ttu-id="98873-122">Atlasiet **Izveidot grafikus**, pirms apstiprināt maksājumu grafiku.</span><span class="sxs-lookup"><span data-stu-id="98873-122">Select **Create schedules** before you confirm the payment schedule.</span></span>

    <span data-ttu-id="98873-123">Sākotnējais atzīšanas žurnāla ieraksts reģistrē LLT, kas izmanto nomas maksai norādītos valūtas maiņas kursus.</span><span class="sxs-lookup"><span data-stu-id="98873-123">The initial recognition journal entry records the ROU asset that uses the currency exchange rates that are listed on the lease.</span></span> <span data-ttu-id="98873-124">Žurnāla ierakstā ir iekļautas arī lauku **Uzskaites valūtas sākotnējās līdzekļa lietošanas tiesības** un **Pārskata valūtas sākotnējās līdzekļa lietošanas tiesības**.</span><span class="sxs-lookup"><span data-stu-id="98873-124">The journal entry also includes the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

## <a name="subsequent-measurement-for-foreign-currency-leases"></a><span data-ttu-id="98873-125">Ārvalstu valūtas nomu turpmākā novērtēšana</span><span class="sxs-lookup"><span data-stu-id="98873-125">Subsequent measurement for foreign currency leases</span></span>

<span data-ttu-id="98873-126">Nolietojuma grafiks parāda prognozēto nolietojuma izdevumu summas pārskata valūtā, uzskaites valūtā un darījuma valūtā.</span><span class="sxs-lookup"><span data-stu-id="98873-126">The depreciation schedule shows the expected depreciation expense amounts in the reporting currency, the accounting currency, and the transaction currency.</span></span>

<span data-ttu-id="98873-127">Lai skatītu LLT bilances un nolietojuma summas pārskata valūtā vai uzskaites valūtā, atveriet lapu **Līdzekļa nolietojuma grafiks** un atzīmējiet izvēles rūtiņu **Rādīt uzskaites valūtas summas** vai **Rādīt pārskata valūtas summas**.</span><span class="sxs-lookup"><span data-stu-id="98873-127">To view the ROU asset balances and depreciation amounts in either the reporting currency or the accounting currency, open the **Asset depreciation schedule** page, and select the **Show accounting currency amounts** or **Show reporting currency amounts** check box.</span></span>

<span data-ttu-id="98873-128">Kad tiek veidoti nolietojuma izdevumu žurnāla ieraksti nomai, kas izteikta ārzemju valūtā, ieraksts izmanto valūtas maiņas kursus, kas norādīti nomā.</span><span class="sxs-lookup"><span data-stu-id="98873-128">When you create the depreciation expense journal entries against a lease that is denominated in a foreign currency, the entry uses the exchange rates that are listed on the lease.</span></span> <span data-ttu-id="98873-129">Tas izmanto arī lauku **Uzskaites valūtas sākotnējās līdzekļa lietošanas tiesības** un **Pārskata valūtas sākotnējās līdzekļa lietošanas tiesības** vērtības.</span><span class="sxs-lookup"><span data-stu-id="98873-129">It also uses the values of the **Accounting currency initial right-of-use asset** and **Reporting currency initial right-of-use asset** fields.</span></span>

<span data-ttu-id="98873-130">Galīgo nolietojuma izdevumu summu var aprēķināt, izmantojot nedaudz atšķirīgu maiņas kursu, lai LLT būtu pilnībā nolietots gan uzskaites valūtā, gan pārskata valūtā.</span><span class="sxs-lookup"><span data-stu-id="98873-130">The final depreciation expense amount can be calculated by using a slightly different exchange rate, so that the ROU asset is fully depreciated in both the accounting currency and the reporting currency.</span></span>

<span data-ttu-id="98873-131">Ja noma pārklasificēta kā **Atliktā nomas maksa**, sistēma automātiski notīra uzskaites un pārskata valūtas maiņas kursus, ja tie jau ir definēti.</span><span class="sxs-lookup"><span data-stu-id="98873-131">If the lease has been reclassified as **Deferred rent**, the system automatically clears the exchange rates of the accounting and reporting currencies, if they have already been defined.</span></span>
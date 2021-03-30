---
title: Nomas parametru konfigurēšana (priekšskatījums)
description: Šajā tēmā ir aprakstīti konfigurācijas iestatījumi Līdzekļu nomai, piemēram, drošības informācija un uzskaites iestatījumi.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4bb8372c5e4a1d7183b5d793b142fed92e833d5a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210437"
---
# <a name="configure-lease-parameters"></a><span data-ttu-id="57321-103">Nomas parametru konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="57321-103">Configure lease parameters</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="57321-104">Vairāki konfigurācijas iestatījumi ietekmē Līdzekļu nomas darbību.</span><span class="sxs-lookup"><span data-stu-id="57321-104">Several configuration settings affect how Asset leasing behaves.</span></span> <span data-ttu-id="57321-105">Šie iestatījumi ietver žurnālu nosaukumus, vispārīgos parametrus un grāmatošanas profila iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="57321-105">These settings include journal names, general parameters, and posting profile settings.</span></span>

1. <span data-ttu-id="57321-106">Dodieties uz **Līdzekļu noma \> Iestatījumi \> Līdzekļu nomas parametri**.</span><span class="sxs-lookup"><span data-stu-id="57321-106">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="57321-107">Cilnē **Nomas** atlasiet kopsavilkuma cilni **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="57321-107">On the **Leases** tab, select the **General** FastTab.</span></span>

    <span data-ttu-id="57321-108">Parametrs **Atļaut manuālās klasifikācijas pārlabošanu** nosaka, vai nomas klasifikāciju var pārlabot pirms maksājumu grafika apstiprināšanas.</span><span class="sxs-lookup"><span data-stu-id="57321-108">The **Allow manual classification override** parameter determines whether the lease classification can be overridden before the payment schedule is confirmed.</span></span>

    <span data-ttu-id="57321-109">Parametrs **Partija no dažādiem elementiem** nosaka, vai varat grāmatot citās juridiskajās personās no esošās juridiskās personas.</span><span class="sxs-lookup"><span data-stu-id="57321-109">The **Cross-entity batch** parameter determines whether you can post to other legal entities from the current legal entity.</span></span> <span data-ttu-id="57321-110">Ja šis parametrs ir ieslēgts, varat izveidot žurnāla ierakstus juridiskām personām, kurām jums ir piekļuve.</span><span class="sxs-lookup"><span data-stu-id="57321-110">If this parameter is turned on, you can create journal entries for the legal entities that you have access to.</span></span>

3. <span data-ttu-id="57321-111">Iestatiet opciju **Atļaut dzēst apstiprinātās nomas** uz **Jā**, lai atļautu dzēst nomas, kam ir apstiprināti maksājumu grafiki.</span><span class="sxs-lookup"><span data-stu-id="57321-111">Set the **Allow delete of confirmed leases** option to **Yes** to allow leases that have confirmed payment schedules to be deleted.</span></span> <span data-ttu-id="57321-112">Nomu nevar dzēst, ja ar tām ir saistītas grāmatoti vai negrāmatoti darījumi, neatkarīgi no šīs opcijas iestatījuma.</span><span class="sxs-lookup"><span data-stu-id="57321-112">Leases can't be deleted if posted or unposted transactions are associated with them, regardless of the setting of this option.</span></span> <span data-ttu-id="57321-113">Nav iespējams atjaunot nomas ierakstu pēc tā dzēšanas.</span><span class="sxs-lookup"><span data-stu-id="57321-113">You can't restore a lease record after it's deleted.</span></span> <span data-ttu-id="57321-114">Ja augšupielādējiet jebkādus ierakstus par dzēstu nomu vai nu manuāli, vai izmantojot datu entītijas, augšupielādētā informācija tiek uzskatīta par jaunu, nevis esošas nomas atjauninājumu.</span><span class="sxs-lookup"><span data-stu-id="57321-114">If you upload any records for a deleted lease, either manually or through data entities, the uploaded information is treated as new, not as an update to an existing lease.</span></span>

    <span data-ttu-id="57321-115">Iestatot šo opciju kā **Jā** un grāmatas pārejas veidu kā **Kumulatīvās izlīdzināšanas opcija A vai B**, sistēma iestata lauku **Salīdzināmā aizņēmuma procentu likme** uz lauka **Salīdzināmā aizņēmuma procentu likme pārejas laikā** vērtību lapā **Grāmatas iestatījumi**.</span><span class="sxs-lookup"><span data-stu-id="57321-115">If you set this option to **Yes**, and the transition type of the book is **Cumulative Catchup Option A or B**, the system sets the **Incremental borrowing rate** field to the value of the **Incremental borrowing rate at transition** field on the **Book setup** page.</span></span> <span data-ttu-id="57321-116">Ja šī opcija ir iestatīta uz **Nē**, neatkarīgi no grāmatas pārejas veida galvenās nomas likme ir iestatīta uz vērtību laukā **Salīdzināmā aizņēmuma procentu likme** lapā **Detalizēta informācija par grāmatu**.</span><span class="sxs-lookup"><span data-stu-id="57321-116">If this option is set to **No**, the rate on the head lease is set to the value of the **Incremental borrowing rate** field on the **Book details** page, regardless of the transition type of the book.</span></span>

4. <span data-ttu-id="57321-117">Iestatiet opciju **Atļaut nolietojuma anulēšanu slēgtā grāmatas versijā** uz **Jā**, atļautu nolietojuma izdevumu darījumu anulēšanu.</span><span class="sxs-lookup"><span data-stu-id="57321-117">Set the **Allow depreciation reversals on closed book version** option to **Yes** to allow depreciation expense transactions to be reversed.</span></span> <span data-ttu-id="57321-118">Izdevumu darījumus var anulēt pat tad, ja grāmatas versija ir slēgta.</span><span class="sxs-lookup"><span data-stu-id="57321-118">Expense transactions can be reversed even when the book version is closed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="57321-119">Ieteicams saglabāt šo opciju iestatītu uz **Nē**.</span><span class="sxs-lookup"><span data-stu-id="57321-119">We recommend that you keep this option set to **No**.</span></span> <span data-ttu-id="57321-120">Šīs opcijas iestatījums tiek izmantots kā validācija un kontrole, lai novērstu, ka slēgtas grāmatas versijā nolietojums tiek piemērots nejauši.</span><span class="sxs-lookup"><span data-stu-id="57321-120">The setting of this option is used as a validation and control to prevent a closed book version from being accidently depreciated.</span></span> <span data-ttu-id="57321-121">Saglabājot opciju iestatītu uz **Nē**, varat nodrošināt precīzu atlikušo vērtību un nākotnes nolietojuma aprēķinus.</span><span class="sxs-lookup"><span data-stu-id="57321-121">By keeping the option set to **No**, you help keep the net book value and future depreciation calculations accurate.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
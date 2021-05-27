---
title: MK līniju skalošanas principa iestatījumi netiek ievēroti
description: Materiālu komplekta (MK) līniju skalošanas principa iestatījumi netiek ievēroti.
author: johanhoffmann
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: PurchTable,ProdParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 84a84728016119a2a02f59f6903171afbceb48e7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026713"
---
# <a name="flushing-principle-settings-on-bom-lines-arent-respected"></a><span data-ttu-id="a962e-103">MK līniju skalošanas principa iestatījumi netiek ievēroti</span><span class="sxs-lookup"><span data-stu-id="a962e-103">Flushing principle settings on BOM lines aren't respected</span></span>

<span data-ttu-id="a962e-104">KB numurs: 4612725</span><span class="sxs-lookup"><span data-stu-id="a962e-104">KB number: 4612725</span></span>

## <a name="symptoms"></a><span data-ttu-id="a962e-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="a962e-105">Symptoms</span></span>

<span data-ttu-id="a962e-106">Šī problēma rodas, ja **Automātiskā MK patēriņa** lauks cilnē **Automātiska atjaunināšana**, lapā **Ražošanas kontroles parametri** ir iestatīts uz *Tīrīšanas principu*.</span><span class="sxs-lookup"><span data-stu-id="a962e-106">This issue occurs when the **Automatic BOM consumption** field on the **Automatic update** tab of the **Production control parameters** page is set to *Flushing principle*.</span></span> <span data-ttu-id="a962e-107">Šis iestatījums norāda, ka visas materiālu komplekta (MK) rindas ir automātiski jāpatērē, kad ir saņemts pirkšanas pasūtījums.</span><span class="sxs-lookup"><span data-stu-id="a962e-107">This setting indicates that all bill of materials (BOM) lines should automatically be consumed when a purchase order is received.</span></span> <span data-ttu-id="a962e-108">Ja **Tīrīšanas principa** lauks MK rindās ir skaidri iestatīts uz *Manuāli*, var būt paredzams, ka MK rindas netiks automātiski patērētas.</span><span class="sxs-lookup"><span data-stu-id="a962e-108">If the **Flushing principle** field on BOM lines is explicitly set to *Manual*, you might expect that the BOM lines won't automatically be consumed.</span></span> <span data-ttu-id="a962e-109">Tomēr, kad rodas šī problēma, MK rindas, kur **Tīrīšanas principa** lauks ir iestatīts uz *Manuāli*, vienalga tiek automātiski patērētas.</span><span class="sxs-lookup"><span data-stu-id="a962e-109">However, when this issue occurs, BOM lines where the **Flushing principle** field is set to *Manual* are automatically consumed anyway.</span></span>

## <a name="resolution"></a><span data-ttu-id="a962e-110">Novēršana</span><span class="sxs-lookup"><span data-stu-id="a962e-110">Resolution</span></span>

<span data-ttu-id="a962e-111">Ja rodas šī problēma, iespējams, ražošanas kontroles parametri ir iestatīti, lai ignorētu **Tīrīšanas principa** iestatījumu MK rindās.</span><span class="sxs-lookup"><span data-stu-id="a962e-111">If you're experiencing this issue, your production control parameters might be set up to override the **Flushing principle** setting on BOM lines.</span></span> <span data-ttu-id="a962e-112">Lapā **Ražošanas kontroles parametri**, cilnē **Automātiskā atjaunināšana** pārbaudiet lauku **Automātiskais MK patēriņš**.</span><span class="sxs-lookup"><span data-stu-id="a962e-112">On the **Production control parameters** page, on the **Automatic update** tab, check the value of the **Automatic BOM consumption** field.</span></span> <span data-ttu-id="a962e-113">Ja tas ir iestatīts uz *Vienmēr*, sistēma ignorēs **Tīrīšanas principa** iestatījumu visās MK rindās un vienmēr iztukšos rindas.</span><span class="sxs-lookup"><span data-stu-id="a962e-113">If it's set to *Always*, the system will disregard the **Flushing principle** setting on all BOM lines and will always flush the lines.</span></span> <span data-ttu-id="a962e-114">Lai sistēmā būtu atbilstība MK rindu **Tīrīšanas principa** iestatījumam, mainiet lauka **Automātisks MK patēriņš** vērtību uz *Tīrīšanas princips*.</span><span class="sxs-lookup"><span data-stu-id="a962e-114">To make the system respect the **Flushing principle** setting on BOM lines, change the value of the **Automatic BOM consumption** field to *Flushing principle*.</span></span>

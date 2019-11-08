---
title: Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 24. septembris)
description: Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Microsoft Dynamics 365 Talent — Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 078b513b828b97a5cfaf613970edd581fb091f9e
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551340"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-24-2018"></a><span data-ttu-id="ad363-103">Jaunumi un izmaiņas programmā Dynamics 365 Talent — Core HR (2018. gada 24. septembris)</span><span class="sxs-lookup"><span data-stu-id="ad363-103">What's new or changed in Dynamics 365 Talent - Core HR (September 24, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ad363-104">**8.1.1015.0 būvējums**</span><span class="sxs-lookup"><span data-stu-id="ad363-104">**Build 8.1.1015.0**</span></span>

<span data-ttu-id="ad363-105">Šajā sadaļā ir aprakstīti līdzekļi, kas ir vai nu jauni, vai kas ir mainīti programmā Core HR.</span><span class="sxs-lookup"><span data-stu-id="ad363-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="currency-added-to-benefits"></a><span data-ttu-id="ad363-106">Atvieglojumiem pievienota valūta</span><span class="sxs-lookup"><span data-stu-id="ad363-106">Currency added to Benefits</span></span>

<span data-ttu-id="ad363-107">Atvieglojumu plāns ir atjaunināts, iekļaujot atvieglojumu valūtu.</span><span class="sxs-lookup"><span data-stu-id="ad363-107">Benefit plans have been updated to include the currency of the benefit.</span></span> <span data-ttu-id="ad363-108">Šis jaunais lauks ir pieejams nodarbinātajam reģistrētajos atvieglojumos.</span><span class="sxs-lookup"><span data-stu-id="ad363-108">This new field is also available on worker enrolled benefits.</span></span> <span data-ttu-id="ad363-109">Jauns lauks ir iekļauts sadaļā Atvieglojumu uzturēšana un Skatīt atvieglojumu drošības privilēģiju sarakstu.</span><span class="sxs-lookup"><span data-stu-id="ad363-109">This new field is part of the Maintain benefits and View a list of benefits security privilege.</span></span>

## <a name="update-proration-process--leave-and-absence"></a><span data-ttu-id="ad363-110">Proporcionalitātes sadales procesa atjaunināšana — atvaļinājums un prombūtne</span><span class="sxs-lookup"><span data-stu-id="ad363-110">Update proration process – Leave and Absence</span></span>

<span data-ttu-id="ad363-111">Organizācijas piešķir prombūtnes laiku dažādi atkarībā no tā, kad darbinieks ir pievienojies uzņēmumam vai atstājis to.</span><span class="sxs-lookup"><span data-stu-id="ad363-111">Organizations award time off differently based on when employees join and leave the company.</span></span> <span data-ttu-id="ad363-112">Dažiem darbiniekiem, kuri atstāj organizāciju, var būt nepieciešams pārtraukt piemaksas aprēķināšanu darba attiecību pārtraukšanas dienā, bet citi izmanto pēdējo nostrādāto dienu, lai apturētu uzkrāšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="ad363-112">For employees leaving the organization, some may need to end the award on the termination date, while others rely on the last day worked to stop the accrual process.</span></span> <span data-ttu-id="ad363-113">Šīs izmaiņas nodrošina uzņēmumiem iespēju izvēlēties reģistrācijas pārtraukšanas brīdi darba attiecību pārtraukšanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="ad363-113">These changes provide organizations the ability to choose when to end enrollment during the termination process.</span></span> <span data-ttu-id="ad363-114">Šīs jaunās opcijas ir ietvertas darba attiecību pārtraukšanas ar nodarbināto un darba attiecību pārtraukšana ar nodarbināto, izmantojot vadītāja patstāvīgi izmantojamo pakalpojumu, privilēģijās.</span><span class="sxs-lookup"><span data-stu-id="ad363-114">These new options are part of the privileges for Terminate a worker and Terminate a worker from manager self service.</span></span> 

## <a name="other-changes"></a><span data-ttu-id="ad363-115">Cita izmaiņas</span><span class="sxs-lookup"><span data-stu-id="ad363-115">Other changes</span></span>

<span data-ttu-id="ad363-116">Šis laidiens ietver vairākus papildu kļūdu labojumus.</span><span class="sxs-lookup"><span data-stu-id="ad363-116">This release includes several additional bug fixes.</span></span>

## <a name="known-issue"></a><span data-ttu-id="ad363-117">Zināma problēma</span><span class="sxs-lookup"><span data-stu-id="ad363-117">Known Issue</span></span>

-   <span data-ttu-id="ad363-118">**Problēma:** pievienojot nodarbinātajam jaunu pielikumu, tiek deaktivizēta poga **Jauns** un **Rediģēt**. **Risinājums:** pirms pielikuma lapas atvēršanas pārbaudiet, vai lapā **Nodarbinātais** ir aizvērta papildinformācija.</span><span class="sxs-lookup"><span data-stu-id="ad363-118">**Issue:** When adding a new attachment to a worker, the **New** and **Edit** buttons are grayed out. **Workaround:** Before opening the attachment page, make sure that the fact boxes on the **Worker** page are closed.</span></span> <span data-ttu-id="ad363-119">Ja, ielādējot lapu **Nodarbinātais**, papildinformācija ir aizvērta, pielikumu pogas tiek iespējotas.</span><span class="sxs-lookup"><span data-stu-id="ad363-119">If the fact boxes are closed when the **Worker** page is loaded, the attachments buttons will be enabled.</span></span> <span data-ttu-id="ad363-120">(Šī problēma tiks novērsta nākamajā platformas atjauninājumā.)</span><span class="sxs-lookup"><span data-stu-id="ad363-120">(This issue will be fixed in the next platform update.)</span></span>

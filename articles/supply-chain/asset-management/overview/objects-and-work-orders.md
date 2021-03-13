---
title: Līdzekļi un darba pasūtījumi
description: Šajā tēmā aprakstīti līdzekļi un darba pasūtījumi Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0cddb0a25286c8ce9d72aef0b835809705ad577a
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/16/2021
ms.locfileid: "5020943"
---
# <a name="assets-and-work-orders"></a><span data-ttu-id="c6046-103">Līdzekļi un darba pasūtījumi</span><span class="sxs-lookup"><span data-stu-id="c6046-103">Assets and work orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="c6046-104">Šajā tēmā aprakstīti līdzekļi un darba pasūtījumi Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="c6046-104">This topic describes assets and work orders in Asset Management.</span></span> <span data-ttu-id="c6046-105">Līdzekļi un darba pasūtījumi ir Līdzekļu pārvaldības centrālās daļas.</span><span class="sxs-lookup"><span data-stu-id="c6046-105">Assets and work orders are the central parts of Asset Management.</span></span> <span data-ttu-id="c6046-106">*Līdzeklis* ir mašīna vai mašīnas daļa, kam nepieciešama nepārtraukta uzturēšana un apkope.</span><span class="sxs-lookup"><span data-stu-id="c6046-106">An *asset* is a machine or machine part that requires continuous maintenance and service.</span></span> <span data-ttu-id="c6046-107">Līdzekļus var izveidot hierarhiskā struktūrā, un tie var būt saistīti ar funkcionālajiem novietojumiem.</span><span class="sxs-lookup"><span data-stu-id="c6046-107">Assets can be created in a hierarchical structure, and they can be related to functional locations.</span></span> <span data-ttu-id="c6046-108">Uzturēšanas darbus līdzekļu struktūrā var plānot visos līmeņos.</span><span class="sxs-lookup"><span data-stu-id="c6046-108">Maintenance jobs can be planned at all levels in the asset structure.</span></span>

<span data-ttu-id="c6046-109">Katram līdzeklim tiek iestatīti dažādi dati, piemēram, informācija par preci un līdzekļa specifikācija, un nepieciešamie uzturēšanas plāni.</span><span class="sxs-lookup"><span data-stu-id="c6046-109">Various data, such as product information and asset specification, and required maintenance plans are set up on each asset.</span></span> <span data-ttu-id="c6046-110">Nākamajā attēlā ir redzams pārskats par līdzekļu datiem un līdzekļu piederību darba veidiem.</span><span class="sxs-lookup"><span data-stu-id="c6046-110">The following illustration shows an overview of asset data and the affiliation of assets to job types.</span></span> <span data-ttu-id="c6046-111">Sarkanaiss teksts tiek izmantots piemēriem, kas parāda pārmantošanu un atkarības.</span><span class="sxs-lookup"><span data-stu-id="c6046-111">Red text is used for examples that show inheritance and dependencies.</span></span>

![Shēmā ir parādīti līdzekļu dati saistībā ar darbu veidiem](media/05-overview-image.png)

<span data-ttu-id="c6046-113">Katram darba pasūtījumam ir darba pasūtījuma veids, šāda profilaktiska uzturēšana, koriģējoša uzturēšana vai pārbaude.</span><span class="sxs-lookup"><span data-stu-id="c6046-113">Every work order has a work order type, such preventive maintenance, corrective maintenance, or inspection.</span></span> <span data-ttu-id="c6046-114">Darba pasūtījumā ir viens vai vairāki darba pasūtījuma darbi.</span><span class="sxs-lookup"><span data-stu-id="c6046-114">The work order contains one or more work order jobs.</span></span> <span data-ttu-id="c6046-115">Katrs darba pasūtījuma darbs definē darbu, kas jāveic līdzeklim, un saistīto darba veidu.</span><span class="sxs-lookup"><span data-stu-id="c6046-115">Every work order job defines a job that must be performed on an asset and a related job type.</span></span> <span data-ttu-id="c6046-116">Saistīto darba veidu piemēri ietver 10 000 km, 50 000 km, 1 gada kapitālremontu un drošības pārbaudi.</span><span class="sxs-lookup"><span data-stu-id="c6046-116">Examples of related job types include 10,000 km, 50,000 km, 1-year overhaul, and safety inspection.</span></span> <span data-ttu-id="c6046-117">Viens darba pasūtījums var būt saistīts ar vairākiem līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="c6046-117">One work order can be related to multiple assets.</span></span>

<span data-ttu-id="c6046-118">Nākamajā attēlā ir parādīts pārskats par galvenajiem datiem darba pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="c6046-118">The following illustration shows an overview of the key data in a work order.</span></span>

![Shēmā ir redzami darba pasūtījuma galvenie dati](media/06-overview-image.png)

<span data-ttu-id="c6046-120">Darba pasūtījums var būt saistīts ar citu darba pasūtījumu, un darba veidos var ietilpt secīgi darbi, kas veido darba pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="c6046-120">A work order can be related to another work order, and job types can contain succeeding jobs that create a work order.</span></span> <span data-ttu-id="c6046-121">Parasti starp darba pasūtījumiem nav atkarību.</span><span class="sxs-lookup"><span data-stu-id="c6046-121">In general, there are no dependencies between work orders.</span></span> <span data-ttu-id="c6046-122">Tāpēc tie var mainīt savu darba pasūtījuma dzīves cikla stāvokli, un tos var ieplānot neatkarīgi vienu no otra.</span><span class="sxs-lookup"><span data-stu-id="c6046-122">Therefore, they can change their work order lifecycle state and can be scheduled independently of each other.</span></span>

<span data-ttu-id="c6046-123">Darba pasūtījumus var veidot dažādos veidos, kas ir saistīti ar koriģējošu, preventīvu vai reaktīvu uzturēšanu.</span><span class="sxs-lookup"><span data-stu-id="c6046-123">Work orders can be created in various ways that are related to corrective, preventive, or reactive maintenance.</span></span> <span data-ttu-id="c6046-124">Darba pasūtījumus var izveidot arī manuāli.</span><span class="sxs-lookup"><span data-stu-id="c6046-124">You can also create work orders manually.</span></span> <span data-ttu-id="c6046-125">Nākamajā attēlā ir parādīts apskats par procesu automātiskai vai manuālai darba pasūtījumu izveidei.</span><span class="sxs-lookup"><span data-stu-id="c6046-125">The following illustration shows an overview of the process for automatic or manual creation of work orders.</span></span>

![Shēmā ir parādīta automātiska vai manuāla darba pasūtījumu izveide](media/07-overview-image.png)

<span data-ttu-id="c6046-127">Ja vēlaties plānot un izpildīt uzturēšanas darbu darba pasūtījumā, ir jāizpilda vairākas darbības.</span><span class="sxs-lookup"><span data-stu-id="c6046-127">Several steps must be completed when you want to schedule and run a maintenance job on a work order.</span></span> <span data-ttu-id="c6046-128">Nākamajā attēlā ir parādīts pārskats par darba pasūtījum apstrādi.</span><span class="sxs-lookup"><span data-stu-id="c6046-128">The following illustration shows an overview of the processing for a work order.</span></span>

![Shēmā ir parādīts darba pasūtījuma apstrādes pārskats](media/08-overview-image.png)

> [!NOTE]
> <span data-ttu-id="c6046-130">Parasti, strādājot programmā Dynamics 365 Supply Chain Management un modulī **Līdzekļu pārvaldība**, jūs atlasāt **Jauns**, lai izveidotu jaunu ierakstu, atlasāt **RediģētEdit**, lai atjauninātu esošu ierakstu, un atlasāt **Saglabāt**, lai saglabātu jaunus vai rediģētus datus.</span><span class="sxs-lookup"><span data-stu-id="c6046-130">In general, when you work in Dynamics 365 Supply Chain Management and the **Asset Management** module, you select **New** to create a new record, you select **Edit** to update an existing record, and you select **Save** to save new or edited data.</span></span>

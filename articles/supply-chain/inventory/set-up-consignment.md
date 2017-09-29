---
title: "Sūtījuma iestatīšana"
description: "Šajā tēmā ir paskaidrots, kā konfigurēt ienākošo sūtījumu krājumu darbības."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventJournalOwnershipChange, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220804
ms.assetid: 88822f78-4de5-462c-a55f-1f766c572719
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 41c1b8de0aae24efb30a670d3109b6d65e6abd9c
ms.contentlocale: lv-lv
ms.lasthandoff: 09/12/2017

---

# <a name="set-up-consignment"></a><span data-ttu-id="8d22e-103">Sūtījuma iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8d22e-103">Set up consignment</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="8d22e-104">Šajā tēmā ir paskaidrots, kā konfigurēt ienākošo sūtījumu krājumu darbības.</span><span class="sxs-lookup"><span data-stu-id="8d22e-104">This topic explains how to configure inbound consignment inventory operations.</span></span>

<span data-ttu-id="8d22e-105">Sūtījuma krājumi ir krājumi, kas pieder kreditoram, bet tiek glabāti jūsu bāzes vietā.</span><span class="sxs-lookup"><span data-stu-id="8d22e-105">Consignment inventory is inventory that’s owned by a vendor, but stored at your site.</span></span> <span data-ttu-id="8d22e-106">Kad esat gatavs patērēt vai izmantot krājumu, jūs pārņemat krājuma īpašumtiesības.</span><span class="sxs-lookup"><span data-stu-id="8d22e-106">When you’re ready to consume or use the inventory, you take over the ownership of the inventory.</span></span> <span data-ttu-id="8d22e-107">Šajā tēmā ir aprakstīta iestatīšana, kas ir nepieciešama, lai nodrošinātu sūtījuma procesus.</span><span class="sxs-lookup"><span data-stu-id="8d22e-107">This topic describes the setup needed to enable consignment processes.</span></span> <span data-ttu-id="8d22e-108">Plašāku informāciju par sūtījuma procesiem skatiet sadaļā [Sūtījums](consignment.md).</span><span class="sxs-lookup"><span data-stu-id="8d22e-108">For more information about consignment processes, see [Consignment](consignment.md).</span></span>

## <a name="inventory-owners"></a><span data-ttu-id="8d22e-109">Krājumu īpašnieki</span><span class="sxs-lookup"><span data-stu-id="8d22e-109">Inventory owners</span></span>
<span data-ttu-id="8d22e-110">Lai ierakstītu fizisko ienākošo sūtījumu krājumu, nepieciešams definēt kreditora īpašnieku.</span><span class="sxs-lookup"><span data-stu-id="8d22e-110">In order to record physical inbound consignment inventory, you need to define a vendor owner.</span></span> <span data-ttu-id="8d22e-111">Tas tiek veikts lapā **Krājumu īpašnieks**.</span><span class="sxs-lookup"><span data-stu-id="8d22e-111">This is done on the **Inventory owner** page.</span></span> <span data-ttu-id="8d22e-112">Atlasot **Kreditora konts**, tiek izveidotas noklusētās vērtības laukiem **Nosaukums** un **Īpašnieks**.</span><span class="sxs-lookup"><span data-stu-id="8d22e-112">When you select a **Vendor account** this generates default values for the **Name** and **Owner** fields.</span></span> <span data-ttu-id="8d22e-113">Vērtība laukā **Īpašnieks** būs redzama kreditoram, tāpēc jūs varētu vēlēties to mainīt, ja jūsu kreditora kontu nosaukumi nav viegli atpazīstami citiem cilvēkiem.</span><span class="sxs-lookup"><span data-stu-id="8d22e-113">The value in the **Owner** field will be visible to the vendor, so you might want to change it if your vendor account names aren’t easy for external people to recognize.</span></span> <span data-ttu-id="8d22e-114">Iespējams rediģēt lauku **Īpašnieks**, bet tikai līdz brīdim, kad saglabājat ierakstu **Krājumu īpašnieks**.</span><span class="sxs-lookup"><span data-stu-id="8d22e-114">It’s possible to edit the **Owner** field, but only up to the point when you save the **Inventory owner** record.</span></span> <span data-ttu-id="8d22e-115">Lauks **Nosaukums** tiek aizpildīts ar puses nosaukumu, ar kuru ir saistīts kreditora konts, un to nevar mainīt.</span><span class="sxs-lookup"><span data-stu-id="8d22e-115">The **Name** field is populated with the name of the party that the vendor account is associated with, and this cannot be changed.</span></span>

<span data-ttu-id="8d22e-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span><span class="sxs-lookup"><span data-stu-id="8d22e-116">[![inventory-owners](./media/inventory-owners.png)](./media/inventory-owners.png)</span></span>

## <a name="tracking-dimension-group"></a><span data-ttu-id="8d22e-117">Izsekošanas dimensijas grupa</span><span class="sxs-lookup"><span data-stu-id="8d22e-117">Tracking dimension group</span></span>
<span data-ttu-id="8d22e-118">Krājumus, kas tiks izmantoti sūtījuma procesos, nepieciešams saistīt ar **Izsekošanas dimensijas grupa**, kur dimensija **Īpašnieks** ir iestatīta uz **Aktīvs**.</span><span class="sxs-lookup"><span data-stu-id="8d22e-118">Items that are going to be used in consignment processes must be associated with a **Tracking dimension group** where the **Owner** dimension is set to **Active**.</span></span> <span data-ttu-id="8d22e-119">Īpašnieka dimensijai vienmēr ir atlasītas opcijas **Fiziskie krājumi** un **Finanšu krājumi**.</span><span class="sxs-lookup"><span data-stu-id="8d22e-119">The Owner dimension always has the **Physical inventory** and **Financial inventory** options selected.</span></span> <span data-ttu-id="8d22e-120">**Vajadzības plāns pa dimensijām** nekad netiek atlasīts.</span><span class="sxs-lookup"><span data-stu-id="8d22e-120">The **Coverage plan by dimension** is never selected.</span></span>

<span data-ttu-id="8d22e-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span><span class="sxs-lookup"><span data-stu-id="8d22e-121">[![tracking-dimension-group](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)</span></span>

## <a name="inventory-ownership-change-journal"></a><span data-ttu-id="8d22e-122">Krājumu īpašumtiesību izmaiņu žurnāls</span><span class="sxs-lookup"><span data-stu-id="8d22e-122">Inventory ownership change journal</span></span>
<span data-ttu-id="8d22e-123">**Krājumu īpašumtiesību izmaiņu**žurnāls tiek izmantots, lai ierakstītu sūtījuma krājumu īpašumtiesību maiņu no kreditora uz pašreizējo juridisko personu, kas to patērē.</span><span class="sxs-lookup"><span data-stu-id="8d22e-123">The **Inventory ownership change** journal is used to record the transfer of ownership of consignment inventory from the vendor to the legal entity that’s consuming it.</span></span> <span data-ttu-id="8d22e-124">Kā jebkuram krājumu žurnālam, tam jābūt norādītam Krājumu žurnāla nosaukumam.</span><span class="sxs-lookup"><span data-stu-id="8d22e-124">Like any inventory journal, it must be identified with an Inventory journal name.</span></span> <span data-ttu-id="8d22e-125">Šie nosaukumi tiek izveidoti lapā **Krājumu žurnālu nosaukumi**, un **Žurnāla tips** jābūt iestatītam uz **Īpašumtiesību izmaiņa**.</span><span class="sxs-lookup"><span data-stu-id="8d22e-125">These names are created on the **Inventory journal names** page, and the **Journal type** must be set to **Ownership change**.</span></span>

<span data-ttu-id="8d22e-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span><span class="sxs-lookup"><span data-stu-id="8d22e-126">[![inventory-ownership-change-journal](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)</span></span>

## <a name="vendor-collaboration-in-consignment-processes"></a><span data-ttu-id="8d22e-127">Kreditora sadarbība sūtījuma procesos</span><span class="sxs-lookup"><span data-stu-id="8d22e-127">Vendor collaboration in consignment processes</span></span>
<span data-ttu-id="8d22e-128">Ja jūsu kreditoriem ir kreditoru sadarbības interfeiss, viņi var izmantot šo, lai pārraudzītu krājumu patēriņu jūsu bāzes vietā.</span><span class="sxs-lookup"><span data-stu-id="8d22e-128">If your vendors are using the vendor collaboration interface, they can use this to monitor the consumption of inventory at your site.</span></span> <span data-ttu-id="8d22e-129">Lai iegūtu papildu informāciju par kreditoru iestatīšanu kreditoru sadarbības izmantošanai, skatiet [Drošības konfigurācija kreditoru sadarbības lietotājiem](../procurement/configure-security-vendor-portal-users.md).</span><span class="sxs-lookup"><span data-stu-id="8d22e-129">For more information about setting up vendors to use vendor collaboration, see [Configuration of security for vendor collaboration users](../procurement/configure-security-vendor-portal-users.md).</span></span>


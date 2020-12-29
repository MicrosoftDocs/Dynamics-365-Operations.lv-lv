---
title: Izveidot mazumtirdzniecības funkcionalitātes profilu
description: Šajā tēmā aprakstīts, kā izveidot funkcionalitātes profilu programmā Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 6bee51eb25b04eb65e588dd4cf54a0cef587aa15
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413920"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="143fb-103">Izveidot mazumtirdzniecības funkcionalitātes profilu</span><span class="sxs-lookup"><span data-stu-id="143fb-103">Create a retail functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="143fb-104">Šajā tēmā aprakstīts, kā izveidot funkcionalitātes profilu programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="143fb-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="143fb-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="143fb-105">Overview</span></span>

<span data-ttu-id="143fb-106">Komercijas funkcionalitātes profilā ir sniegti dažādi tiešsaistes kanāliem izmantotie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="143fb-106">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="143fb-107">Katram kanālam jānorāda funkcionalitātes profils.</span><span class="sxs-lookup"><span data-stu-id="143fb-107">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="143fb-108">Izveidot funkcionalitātes profilu</span><span class="sxs-lookup"><span data-stu-id="143fb-108">Create a functionality profile</span></span>

<span data-ttu-id="143fb-109">Lai izveidotu jaunu funkcionalitāti, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="143fb-109">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="143fb-110">Navigācijas rūtī atveriet **Moduļi \> Kanāla iestatīšana \> POS profili \> Funkcionalitātes profili**.</span><span class="sxs-lookup"><span data-stu-id="143fb-110">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="143fb-111">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="143fb-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="143fb-112">Laukā **Profils** ievadiet profila ID ("FN006" zemāk esošā attēla piemērā).</span><span class="sxs-lookup"><span data-stu-id="143fb-112">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="143fb-113">Laukā **Apraksts** ievadiet vērtību ("Adventure Works profilu" piemērā zemāk esošajā attēlā).</span><span class="sxs-lookup"><span data-stu-id="143fb-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="143fb-114">Sadaļā **Vispārīgi** atlasiet **ISO** lokalizācijas valsti.</span><span class="sxs-lookup"><span data-stu-id="143fb-114">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="143fb-115">Sadaļā **Vispārīgi** pēc nepieciešamības modificējiet citus iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="143fb-115">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="143fb-116">Sadaļā **Vispārīgi** atlasiet **Saņemšanas profila ID** e-pasta kvītīm.</span><span class="sxs-lookup"><span data-stu-id="143fb-116">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="143fb-117">Sadaļā **Funkcijas** pēc nepieciešamības modificējiet iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="143fb-117">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="143fb-118">Sadaļā **Summa** pēc nepieciešamības modificējiet iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="143fb-118">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="143fb-119">Sadaļā **Informācijas kodi** pēc nepieciešamības modificējiet iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="143fb-119">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="143fb-120">Sadaļā **Kvīšu numerācija** pēc nepieciešamības modificējiet citus iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="143fb-120">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="143fb-121">Šajā attēlā ir parādīts funkcionalitātes piemērs.</span><span class="sxs-lookup"><span data-stu-id="143fb-121">The following image shows an example functionality profile.</span></span>
  
![Funkcionalitātes profila piemērs](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="143fb-123">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="143fb-123">Additional resources</span></span>

[<span data-ttu-id="143fb-124">Informācijas kodi un informācijas kodu grupas</span><span class="sxs-lookup"><span data-stu-id="143fb-124">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="143fb-125">Izveidot jaunu adrešu grāmatu</span><span class="sxs-lookup"><span data-stu-id="143fb-125">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="143fb-126">Ekrāna izkārtojuma pārskats</span><span class="sxs-lookup"><span data-stu-id="143fb-126">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="143fb-127">Retail Hardware Station konfigurēšana un instalēšana</span><span class="sxs-lookup"><span data-stu-id="143fb-127">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 

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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 14da5fd2b409790de2269036ccb941ffa6d3311c
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478312"
---
# <a name="create-a-retail-functionality-profile"></a><span data-ttu-id="af8b3-103">Izveidot mazumtirdzniecības funkcionalitātes profilu</span><span class="sxs-lookup"><span data-stu-id="af8b3-103">Create a retail functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="af8b3-104">Šajā tēmā aprakstīts, kā izveidot funkcionalitātes profilu programmā Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="af8b3-104">This topic describes how to create a functionality profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="af8b3-105">Komercijas funkcionalitātes profilā ir sniegti dažādi tiešsaistes kanāliem izmantotie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="af8b3-105">The commerce functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="af8b3-106">Katram kanālam jānorāda funkcionalitātes profils.</span><span class="sxs-lookup"><span data-stu-id="af8b3-106">Each channel must specify a functionality profile.</span></span>

## <a name="create-a-functionality-profile"></a><span data-ttu-id="af8b3-107">Izveidot funkcionalitātes profilu</span><span class="sxs-lookup"><span data-stu-id="af8b3-107">Create a functionality profile</span></span>

<span data-ttu-id="af8b3-108">Lai izveidotu jaunu funkcionalitāti, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="af8b3-108">To create a functionality profile, follow these steps.</span></span>

1. <span data-ttu-id="af8b3-109">Navigācijas rūtī atveriet **Moduļi \> Kanāla iestatīšana \> POS profili \> Funkcionalitātes profili**.</span><span class="sxs-lookup"><span data-stu-id="af8b3-109">In the navigation pane, go to **Modules \> Channel setup \> POS profiles \> Functionality profiles**.</span></span>
1. <span data-ttu-id="af8b3-110">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="af8b3-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="af8b3-111">Laukā **Profils** ievadiet profila ID ("FN006" zemāk esošā attēla piemērā).</span><span class="sxs-lookup"><span data-stu-id="af8b3-111">In the **Profile** field, enter an ID for the profile ("FN006" in the example image below).</span></span>
1. <span data-ttu-id="af8b3-112">Laukā **Apraksts** ievadiet vērtību ("Adventure Works profilu" piemērā zemāk esošajā attēlā).</span><span class="sxs-lookup"><span data-stu-id="af8b3-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="af8b3-113">Sadaļā **Vispārīgi** atlasiet **ISO** lokalizācijas valsti.</span><span class="sxs-lookup"><span data-stu-id="af8b3-113">In the **General** section, select a country for the **ISO** locale.</span></span>
1. <span data-ttu-id="af8b3-114">Sadaļā **Vispārīgi** pēc nepieciešamības modificējiet citus iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="af8b3-114">In the **General** section, modify other settings, as needed.</span></span>
1. <span data-ttu-id="af8b3-115">Sadaļā **Vispārīgi** atlasiet **Saņemšanas profila ID** e-pasta kvītīm.</span><span class="sxs-lookup"><span data-stu-id="af8b3-115">In the **General** section, select a **Receipt profile ID** for email receipts.</span></span>
1. <span data-ttu-id="af8b3-116">Sadaļā **Funkcijas** pēc nepieciešamības modificējiet iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="af8b3-116">In the **Functions** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="af8b3-117">Sadaļā **Summa** pēc nepieciešamības modificējiet iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="af8b3-117">In the **Amount** section, modify settings as, needed.</span></span>
1. <span data-ttu-id="af8b3-118">Sadaļā **Informācijas kodi** pēc nepieciešamības modificējiet iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="af8b3-118">In the **Info Codes** section, modify settings, as needed.</span></span>
1. <span data-ttu-id="af8b3-119">Sadaļā **Kvīšu numerācija** pēc nepieciešamības modificējiet citus iestatījumus.</span><span class="sxs-lookup"><span data-stu-id="af8b3-119">In the **Receipt numbering** section, modify settings, as needed.</span></span> 
  
<span data-ttu-id="af8b3-120">Šajā attēlā ir parādīts funkcionalitātes piemērs.</span><span class="sxs-lookup"><span data-stu-id="af8b3-120">The following image shows an example functionality profile.</span></span>
  
![Funkcionalitātes profila piemērs](media/retail-functionality-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="af8b3-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="af8b3-122">Additional resources</span></span>

[<span data-ttu-id="af8b3-123">Informācijas kodi un informācijas kodu grupas</span><span class="sxs-lookup"><span data-stu-id="af8b3-123">Info codes and info code groups</span></span>](info-codes-retail.md)           

[<span data-ttu-id="af8b3-124">Izveidot jaunu adrešu grāmatu</span><span class="sxs-lookup"><span data-stu-id="af8b3-124">Create new address book</span></span>](new-address-book.md) 

[<span data-ttu-id="af8b3-125">Ekrāna izkārtojuma pārskats</span><span class="sxs-lookup"><span data-stu-id="af8b3-125">Screen layout overview</span></span>](pos-screen-layouts.md)       

[<span data-ttu-id="af8b3-126">Retail Hardware Station konfigurēšana un instalēšana</span><span class="sxs-lookup"><span data-stu-id="af8b3-126">Configure and install Retail hardware station</span></span>](retail-hardware-station-configuration-installation.md) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

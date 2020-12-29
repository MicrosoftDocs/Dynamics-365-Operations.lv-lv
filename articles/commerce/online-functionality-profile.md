---
title: Izveidot tiešsaistes funkcionalitātes profilu
description: Šajā tēmā aprakstīts, kā izveidot tiešsaistes funkcionalitātes profilu programmā Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 5ecbfcf3fa78ad2909a7cc9988ab1edaf2b98376
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414172"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="ee965-103">Izveidot tiešsaistes funkcionalitātes profilu</span><span class="sxs-lookup"><span data-stu-id="ee965-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ee965-104">Šajā tēmā sniegts pārskats par tiešsaistes funkcionalitātes profila iestatīšanu programmai Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ee965-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ee965-105">Pārskats</span><span class="sxs-lookup"><span data-stu-id="ee965-105">Overview</span></span>

<span data-ttu-id="ee965-106">Tiešsaistes funkcionalitātes profilā ir sniegti dažādi tiešsaistes kanāliem izmantotie iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="ee965-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="ee965-107">Katram tiešsaistes kanālam jānorāda tiešsaistes funkcionalitātes profils.</span><span class="sxs-lookup"><span data-stu-id="ee965-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="ee965-108">Izveidot tiešsaistes funkcionalitātes profilu</span><span class="sxs-lookup"><span data-stu-id="ee965-108">Create an online functionality profile</span></span>

<span data-ttu-id="ee965-109">Šī procedūra izskaidro, kā izveidot tiešsaistes funkcionalitātes profilu programmā Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="ee965-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="ee965-110">Navigācijas rūtī atveriet **Moduļi \> Kanāla iestatīšana \> Tiešsaistes veikala iestatīšana \> Funkcionalitātes profili**.</span><span class="sxs-lookup"><span data-stu-id="ee965-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="ee965-111">Darbību rūtī atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="ee965-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ee965-112">Laukā **Profils** ievadiet profila ID.</span><span class="sxs-lookup"><span data-stu-id="ee965-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="ee965-113">Laukā **Apraksts** ievadiet vērtību ("Adventure Works profilu" piemērā zemāk esošajā attēlā).</span><span class="sxs-lookup"><span data-stu-id="ee965-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="ee965-114">Sadaļā **Funkcijas** pēc nepieciešamības modificējiet iestatījumus **GROZS**, **MAZUMTIRDZNIECĪBAS KLIENTI** vai **IZRAKSTĪŠANĀS**.</span><span class="sxs-lookup"><span data-stu-id="ee965-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="ee965-115">Darbību rūtī atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="ee965-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ee965-116">Šajā attēlā ir parādīts tiešsaistes funkcionalitātes piemērs.</span><span class="sxs-lookup"><span data-stu-id="ee965-116">The following image shows an example online functionality profile.</span></span>
  
![Tiešsaistes funkcionalitātes profila piemērs](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="ee965-118">Funkcijas</span><span class="sxs-lookup"><span data-stu-id="ee965-118">Functions</span></span>

- <span data-ttu-id="ee965-119">**Apkopot preces**: Ja aktivizēta, šī funkcija ļauj grozam atjaunināt daudzumu, kad viens un tas pats krājums tiek pievienots vairākkārt.</span><span class="sxs-lookup"><span data-stu-id="ee965-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="ee965-120">**Atļaut izrakstīšanos bez maksājumiem**: Ja aktivizēta, šī funkcija apstrādā scenāriju, kad grozam pievienotajām precēm ir cena $0.00.</span><span class="sxs-lookup"><span data-stu-id="ee965-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="ee965-121">**Izveidot debitoru async režīmā**: Šis ir mantojuma iestatījums, kas piemērojams trešās puses e-komercijas kanāliem, un tas neattiecas uz Dynamics 365 e-commerce vietni.</span><span class="sxs-lookup"><span data-stu-id="ee965-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ee965-122">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="ee965-122">Additional resources</span></span>

[<span data-ttu-id="ee965-123">Kanālu apskats</span><span class="sxs-lookup"><span data-stu-id="ee965-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="ee965-124">Kanālu iestatīšanas priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="ee965-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="ee965-125">Tiešsaistes veikala iestatīšana</span><span class="sxs-lookup"><span data-stu-id="ee965-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="ee965-126">Mazumtirdzniecības kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="ee965-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="ee965-127">Zvanu centra kanāla iestatīšana</span><span class="sxs-lookup"><span data-stu-id="ee965-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)

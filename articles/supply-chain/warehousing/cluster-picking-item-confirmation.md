---
title: Preces apstiprināšana klastera izdošanai
description: Šajā tēmā ir aprakstīts, kā varat iestatīt krājuma pārbaudi kopā ar klastera izdošanu.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272c3a13b68e2b862faf20cc269ca790322b61de
ms.sourcegitcommit: 89022f39502b19c24c0997ae3a01a64b93280f42
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2020
ms.locfileid: "3367296"
---
# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="8aaa6-103">Preces apstiprināšana klastera izdošanai</span><span class="sxs-lookup"><span data-stu-id="8aaa6-103">Product confirmation for cluster picking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8aaa6-104">Klastera izdošanas sniedz iespēju vienlaikus izdot vairāku pasūtījumu krājumus.</span><span class="sxs-lookup"><span data-stu-id="8aaa6-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="8aaa6-105">Ja tiek lietota klasteru izdošana, ir svarīgi veikt krājumu apstiprināšanu, lai pārbaudītu klasteriem pievienotos krājumus.</span><span class="sxs-lookup"><span data-stu-id="8aaa6-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="8aaa6-106">Varat pārbaudīt klastera izdošanā ietvertos krājumus klastera izdošanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="8aaa6-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="8aaa6-107">Darbības tvērums</span><span class="sxs-lookup"><span data-stu-id="8aaa6-107">Where it applies</span></span>

<span data-ttu-id="8aaa6-108">Krājumu pārbaude klastera izdošanai notiek tādā pašā veidā kā krājumu pārbaude ar klasteriem nesaistītas izdošanas procesa ietvaros.</span><span class="sxs-lookup"><span data-stu-id="8aaa6-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="8aaa6-109">Iestatīšana tiek veikta, pamatojoties uz preču svītrkodu iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="8aaa6-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="8aaa6-110">Krājumu pārbaudes klastera izdošanai iestatīšana</span><span class="sxs-lookup"><span data-stu-id="8aaa6-110">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="8aaa6-111">Mobilās ierīces izvēlnes vienumā atveriet iestatīšanas formu darba apstiprināšanai: **Noliktavas pārvaldība** > **Noliktavas pārvaldība** > **Iestatījumi** > **Mobilā ierīce** > **Mobilās ierīces izvēlnes vienumi**</span><span class="sxs-lookup"><span data-stu-id="8aaa6-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
1. <span data-ttu-id="8aaa6-112">Mobilās ierīces izvēlnes vienumā atveriet sadaļu **Darba apstiprinājuma iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="8aaa6-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

|        <span data-ttu-id="8aaa6-113">Opcija</span><span class="sxs-lookup"><span data-stu-id="8aaa6-113">Option</span></span>        |                                    <span data-ttu-id="8aaa6-114">Apraksts</span><span class="sxs-lookup"><span data-stu-id="8aaa6-114">Description</span></span>                                    |
|----------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8aaa6-115">Preces apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="8aaa6-115">Product confirmation</span></span> | <span data-ttu-id="8aaa6-116">Sniedz iespēju mobilajā ierīcē pārbaudīt katru krājumu vienību, veicot skenēšanu.</span><span class="sxs-lookup"><span data-stu-id="8aaa6-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span> |

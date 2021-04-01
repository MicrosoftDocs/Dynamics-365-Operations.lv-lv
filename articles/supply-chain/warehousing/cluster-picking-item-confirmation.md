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
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e30022377cb02e7516cb98f48dc12e4f9e2ce172
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233035"
---
# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="ca50b-103">Preces apstiprināšana klastera izdošanai</span><span class="sxs-lookup"><span data-stu-id="ca50b-103">Product confirmation for cluster picking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca50b-104">Klastera izdošanas sniedz iespēju vienlaikus izdot vairāku pasūtījumu krājumus.</span><span class="sxs-lookup"><span data-stu-id="ca50b-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="ca50b-105">Ja tiek lietota klasteru izdošana, ir svarīgi veikt krājumu apstiprināšanu, lai pārbaudītu klasteriem pievienotos krājumus.</span><span class="sxs-lookup"><span data-stu-id="ca50b-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="ca50b-106">Varat pārbaudīt klastera izdošanā ietvertos krājumus klastera izdošanas procesa laikā.</span><span class="sxs-lookup"><span data-stu-id="ca50b-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="ca50b-107">Darbības tvērums</span><span class="sxs-lookup"><span data-stu-id="ca50b-107">Where it applies</span></span>

<span data-ttu-id="ca50b-108">Krājumu pārbaude klastera izdošanai notiek tādā pašā veidā kā krājumu pārbaude ar klasteriem nesaistītas izdošanas procesa ietvaros.</span><span class="sxs-lookup"><span data-stu-id="ca50b-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="ca50b-109">Iestatīšana tiek veikta, pamatojoties uz preču svītrkodu iestatījumiem.</span><span class="sxs-lookup"><span data-stu-id="ca50b-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="ca50b-110">Krājumu pārbaudes klastera izdošanai iestatīšana</span><span class="sxs-lookup"><span data-stu-id="ca50b-110">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="ca50b-111">Mobilās ierīces izvēlnes vienumā atveriet iestatīšanas formu darba apstiprināšanai: **Noliktavas pārvaldība** > **Noliktavas pārvaldība** > **Iestatījumi** > **Mobilā ierīce** > **Mobilās ierīces izvēlnes vienumi**</span><span class="sxs-lookup"><span data-stu-id="ca50b-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
1. <span data-ttu-id="ca50b-112">Mobilās ierīces izvēlnes vienumā atveriet sadaļu **Darba apstiprinājuma iestatīšana**.</span><span class="sxs-lookup"><span data-stu-id="ca50b-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

|        <span data-ttu-id="ca50b-113">Opcija</span><span class="sxs-lookup"><span data-stu-id="ca50b-113">Option</span></span>        |                                    <span data-ttu-id="ca50b-114">Apraksts</span><span class="sxs-lookup"><span data-stu-id="ca50b-114">Description</span></span>                                    |
|----------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ca50b-115">Preces apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="ca50b-115">Product confirmation</span></span> | <span data-ttu-id="ca50b-116">Sniedz iespēju mobilajā ierīcē pārbaudīt katru krājumu vienību, veicot skenēšanu.</span><span class="sxs-lookup"><span data-stu-id="ca50b-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
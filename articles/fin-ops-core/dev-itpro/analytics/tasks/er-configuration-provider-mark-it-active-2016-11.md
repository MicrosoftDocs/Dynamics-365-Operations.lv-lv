---
title: Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus
description: Šajā tēmā ir paskaidrots, kā lietotājs, kuram ir piešķirta loma “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs”, var izveidot konfigurācijas nodrošinātāju.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERVendorTable
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 11ff1d531b0467cf75ec98b092fe6010f4fa95c0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569791"
---
# <a name="create-configuration-providers-and-mark-them-as-active"></a><span data-ttu-id="e869b-103">Izveidot konfigurācijas nodrošinātājus un atzīmēt tos kā aktīvus</span><span class="sxs-lookup"><span data-stu-id="e869b-103">Create configuration providers and mark them as active</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e869b-104">Šajā tēmā ir paskaidrots, kā lietotājs, kuram ir piešķirta loma “Sistēmas administrators” vai “Elektronisko pārskatu izstrādātājs”, var izveidot konfigurācijas nodrošinātāju elektroniskajiem pārskatiem (Electronic reporting — ER).</span><span class="sxs-lookup"><span data-stu-id="e869b-104">This topic explains how a user assigned to the System Administrator or Electronic Reporting Developer role can create a configuration provider for Electronic reporting (ER).</span></span> <span data-ttu-id="e869b-105">Katra ER konfigurācija atsauksies uz nodrošinātāju kā konfigurācijas autoru.</span><span class="sxs-lookup"><span data-stu-id="e869b-105">Each ER configuration will refer to the provider as the author of the configuration.</span></span> <span data-ttu-id="e869b-106">Šajā piemērā tiek izveidots konfigurēšanas pakalpojuma sniedzējs parauga uzņēmumam Litware, Inc. Šīs darbības var veikt jebkurā uzņēmumā, jo ER konfigurēšanas pakalpojuma sniedzēji ir kopīgi visiem uzņēmumiem.</span><span class="sxs-lookup"><span data-stu-id="e869b-106">In this example, you will create a configuration provider for sample company, Litware, Inc. These steps can be performed in any company as ER configuration providers are shared among all companies.</span></span>

## <a name="create-a-provider"></a><span data-ttu-id="e869b-107">Nodrošinātāja izveide</span><span class="sxs-lookup"><span data-stu-id="e869b-107">Create a provider</span></span>
1. <span data-ttu-id="e869b-108">Dodieties uz sadaļu **Navigācijas rūts** augšējā kreisajā stūrī un atlasiet **Organizācijas administrēšana.**</span><span class="sxs-lookup"><span data-stu-id="e869b-108">Go to the **navigation pane** in the upper left corner and select **Organization administration**.</span></span>
2. <span data-ttu-id="e869b-109">Dodieties uz **Darbvietas > Elektroniskie pārskati**.</span><span class="sxs-lookup"><span data-stu-id="e869b-109">Go to **Workspaces > Electronic reporting**.</span></span>
3. <span data-ttu-id="e869b-110">Dodieties uz **Saistītās saites > Konfigurācijas nodrošinātāji**.</span><span class="sxs-lookup"><span data-stu-id="e869b-110">Go to **Related links > Configuration providers**.</span></span>
4. <span data-ttu-id="e869b-111">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="e869b-111">Select **New**.</span></span>
    - <span data-ttu-id="e869b-112">Nodrošinātāja ierakstam ir unikāls nosaukums un URL.</span><span class="sxs-lookup"><span data-stu-id="e869b-112">A provider record has a unique name and URL.</span></span> <span data-ttu-id="e869b-113">Pārskatiet šīs lapas saturu un izlaidiet šo procedūru, ja “Litware, Inc.” (https://www.litware.com) ieraksts jau pastāv.</span><span class="sxs-lookup"><span data-stu-id="e869b-113">Review the content of this page and skip this procedure if a record for Litware, Inc. (https://www.litware.com) already exists.</span></span>  
5. <span data-ttu-id="e869b-114">Laukā Nosaukums ierakstiet `Litware, Inc.`.</span><span class="sxs-lookup"><span data-stu-id="e869b-114">In the Name field, type `Litware, Inc.`.</span></span>
6. <span data-ttu-id="e869b-115">Laukā Interneta adrese ierakstiet `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="e869b-115">In the Internet address field, type `https://www.litware.com`.</span></span>
7. <span data-ttu-id="e869b-116">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="e869b-116">Select **Save**.</span></span>
8. <span data-ttu-id="e869b-117">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="e869b-117">Close the page.</span></span>

## <a name="select-as-an-active-provider"></a><span data-ttu-id="e869b-118">Atlasiet kā aktīvu nodrošinātāju</span><span class="sxs-lookup"><span data-stu-id="e869b-118">Select as an active provider</span></span>
1. <span data-ttu-id="e869b-119">Atlasiet pakalpojumu sniedzēju Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="e869b-119">Select the Litware, Inc. provider.</span></span>
2. <span data-ttu-id="e869b-120">Atlasiet **Iestatīt kā aktīvu**.</span><span class="sxs-lookup"><span data-stu-id="e869b-120">Select **Set active**.</span></span>

![Elektronisko pārskatu darbvietas lapa](../media/GER-Task-ActiveProvider-1.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
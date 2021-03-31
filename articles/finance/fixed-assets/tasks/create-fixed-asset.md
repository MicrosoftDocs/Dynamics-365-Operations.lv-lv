---
title: Pamatlīdzekļa izveide
description: Šajā tēmā ir paskaidrots, kā izveidot jaunu pamatlīdzekļa ierakstu no lapas Pamatlīdzekļu saraksts.
author: moaamer
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bbbafb1732a9628cb90ad284fce224e3d8172afd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227044"
---
# <a name="create-a-fixed-asset"></a><span data-ttu-id="53f72-103">Pamatlīdzekļa izveide</span><span class="sxs-lookup"><span data-stu-id="53f72-103">Create a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="53f72-104">Šajā tēmā ir paskaidrots, kā izveidot jaunu pamatlīdzekļa ierakstu no saraksta lapas **Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="53f72-104">This topic explains how to create a new fixed asset record from the **Fixed asset** list page.</span></span>

<span data-ttu-id="53f72-105">Sistēma piešķir līdzekļa numuru, pamatojoties uz numuru sēriju, kas piešķirta pamatlīdzekļu grupai.</span><span class="sxs-lookup"><span data-stu-id="53f72-105">The system assigns the asset number, based on the number sequence that is assigned to the fixed asset group.</span></span> <span data-ttu-id="53f72-106">Ja izmantojat pamatlīdzekļa veidni līdzekļu importēšanai, izmantojot Microsoft Excel pievienojumprogrammu, vai arī, ja izmantojat citu importēšanas darbu, sistēma automātiski izveido pamatlīdzekļu ierakstus un palielina līdzekļa numuru.</span><span class="sxs-lookup"><span data-stu-id="53f72-106">If you use the fixed asset template to import assets via the Microsoft Excel add-in, or if you use another import job, the system automatically creates fixed asset records and increments the asset number.</span></span>

<span data-ttu-id="53f72-107">Lai manuāli izveidotu līdzekļa ierakstu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="53f72-107">To manually create an asset record, follow these steps.</span></span>

1. <span data-ttu-id="53f72-108">Dodieties uz **Navigācijas rūts \> Moduļi \> Pamatlīdzekļi \> Pamatlīdzekļi \> Pamatlīdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="53f72-108">Go to **Navigation pane \> Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="53f72-109">Cilnē **Darbību rūts** atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="53f72-109">On the **Action pane**, select **New**.</span></span>
3. <span data-ttu-id="53f72-110">Ievadiet vai atlasiet vērtību laukā **Pamatlīdzekļa grupa**.</span><span class="sxs-lookup"><span data-stu-id="53f72-110">In **the Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="53f72-111">Lauks **Numurs** izmantos noklusējuma vērtību, ja esat iespējojis **Pamatlīdzekļu funkcionalitātes automātiska numurēšana** **Pamatlīdzekļu parametros** un **Pamatlīdzekļu grupā**.</span><span class="sxs-lookup"><span data-stu-id="53f72-111">The **Number** field will default if you have enabled **Autonumber fixed assets functionality** in the **Fixed assets parameters** and the **Fixed asset group**.</span></span> <span data-ttu-id="53f72-112">Ja tā nav, Jums jāievada unikāls kods pamatlīdzekļa identificēšanai.</span><span class="sxs-lookup"><span data-stu-id="53f72-112">If not, you must enter a unique number to identify the fixed asset.</span></span>
4. <span data-ttu-id="53f72-113">Laukā **Nosaukums** ievadiet vērtību.</span><span class="sxs-lookup"><span data-stu-id="53f72-113">In the **Name** field, enter a value.</span></span> <span data-ttu-id="53f72-114">Ievadiet papildu informāciju, kas jūsu uzņēmumam ir nepieciešama par šo līdzekli.</span><span class="sxs-lookup"><span data-stu-id="53f72-114">Enter the additional information that your business needs for this asset.</span></span>
5. <span data-ttu-id="53f72-115">Cilnē **Darbību rūts** atlasiet **Grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="53f72-115">On the **Action pane**, select **Books**.</span></span>
6. <span data-ttu-id="53f72-116">Laukā **Iegādes datums** ievadiet datumu.</span><span class="sxs-lookup"><span data-stu-id="53f72-116">In the **Acquisition date** field, enter a date.</span></span>
7. <span data-ttu-id="53f72-117">Laukā **Iegādes cena** ievadiet skaitli.</span><span class="sxs-lookup"><span data-stu-id="53f72-117">In the **Acquisition price** field, enter a number.</span></span>

    - <span data-ttu-id="53f72-118">Ievadiet papildinformāciju, kas jūsu uzņēmumam ir nepieciešama par šo grāmatu.</span><span class="sxs-lookup"><span data-stu-id="53f72-118">Enter the additional information that your business needs for this book.</span></span>
    - <span data-ttu-id="53f72-119">Ievadiet papildinformāciju, kas jūsu uzņēmumam ir nepieciešama par atlikušajām grāmatām.</span><span class="sxs-lookup"><span data-stu-id="53f72-119">Enter the additional information that your business needs for the remaining books.</span></span>

8. <span data-ttu-id="53f72-120">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="53f72-120">Close the page.</span></span>

<span data-ttu-id="53f72-121">Varat arī importēt pamatlīdzekļus, izmantojot Excel pievienojumprogrammu vai izpildot importēšanas darbu no darbvietas **Datu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="53f72-121">You can also import fixed assets by using the Excel add-in or by running an import job from the **Data management** workspace.</span></span> <span data-ttu-id="53f72-122">Pirms importa palaišanas ievadiet vērtības obligātajiem laukiem veidnē.</span><span class="sxs-lookup"><span data-stu-id="53f72-122">Before you run the import, enter the values for required fields in the template.</span></span>

<span data-ttu-id="53f72-123">Ja nedefinējāt pamatlīdzekļa numuru Excel pievienojumprogrammas veidnē vai Datu vadībā, sistēma katram importētajam pamatlīdzeklim izveido pamatlīdzekļa numuru un automātiski katram pamatlīdzeklim palielina numura secību.</span><span class="sxs-lookup"><span data-stu-id="53f72-123">If you didn't define the fixed asset number in the template of the Excel add-in, or in Data management, the system creates a fixed asset number for each imported asset and automatically increments the number sequence for each.</span></span> <span data-ttu-id="53f72-124">Tomēr, ja importējat līdzekļus un definējat līdzekļu numurus veidnē, sistēma automātiski **nepalielina** numuru secību.</span><span class="sxs-lookup"><span data-stu-id="53f72-124">However, if you import assets and define asset numbers in the template, the system does **not** automatically increment the number sequence.</span></span> <span data-ttu-id="53f72-125">Šādā gadījumā administratoram, iespējams, būs manuāli jāatjaunina numuru secība.</span><span class="sxs-lookup"><span data-stu-id="53f72-125">In this case, an admin might have to manually update the number sequence.</span></span> <span data-ttu-id="53f72-126">Ja definējāt pamatlīdzekļa numuru Excel pievienojumprogrammas veidnē, sistēma izmanto definēto pamatlīdzekļa numuru un palielina numuru secību.</span><span class="sxs-lookup"><span data-stu-id="53f72-126">If you defined the fixed asset number in the template of the Excel add-in, the system uses the defined fixed asset number and increments the number sequence.</span></span>

> [!NOTE]                                                                                                         
> <span data-ttu-id="53f72-127">Pēc nolietojuma grāmatošanas lauki **Nodots lietošanā** un **Nolietojuma aprēķināšanas datums** lapā **Grāmata** tiks bloķēti.</span><span class="sxs-lookup"><span data-stu-id="53f72-127">After posting the depreciation, the **Placed in service** and **Depreciation run date** fields will be locked on the **Book** page.</span></span> <span data-ttu-id="53f72-128">Turklāt neviens no laukiem netiks atjaunināts no datu elementa.</span><span class="sxs-lookup"><span data-stu-id="53f72-128">Also, both neither field will be updated from the data entity.</span></span>

> [!WARNING]
> <span data-ttu-id="53f72-129">Fiksētais līdzekļa ieraksts netiks dzēsts, ja darījumi tika grāmatoti saistītajā grāmatā vai ja jaunizveidotais fiksētais līdzeklis ir ievadīts žurnāla rindā, bet nav grāmatots.</span><span class="sxs-lookup"><span data-stu-id="53f72-129">The fixed asset record won't be deleted if transactions were posted to the associated book, or if the newly created fixed asset is entered on a journal line but not posted.</span></span> 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
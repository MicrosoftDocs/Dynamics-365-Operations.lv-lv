---
title: Izveidot līdzekļus, pamatojoties uz pirkšanas pasūtījumiem
description: Šajā tēmā ir paskaidrots, kā var izveidot to līdzekļu vienību sarakstu, kurus var izmantot par pamatu uzturēšanas darbu līdzekļu veidošanai Līdzekļu pārvaldībā.
author: josaw1
manager: tfehr
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectItem, EntAssetPendingAssets
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 54c129d93e13e032cc5526a91c73d3363ed183db
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432725"
---
# <a name="create-assets-based-on-purchase-orders"></a><span data-ttu-id="41b27-103">Izveidot līdzekļus, pamatojoties uz pirkšanas pasūtījumiem</span><span class="sxs-lookup"><span data-stu-id="41b27-103">Create assets based on purchase orders</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="41b27-104">Šajā tēmā ir paskaidrots, kā var izveidot to līdzekļu vienību sarakstu, kurus var izmantot par pamatu uzturēšanas darbu līdzekļu veidošanai Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="41b27-104">This topic explains how you can create a list of asset items that can be used as a basis for creating assets for maintenance jobs in Asset Management.</span></span> <span data-ttu-id="41b27-105">Pamatojoties uz līdzekļu vienībām, varat skatīt to pirkšanas pasūtījuma rindu sarakstu, kuras ir izveidotas šīm vienībām.</span><span class="sxs-lookup"><span data-stu-id="41b27-105">Based on the asset items, you are able to view a list of the purchase order lines that have been created on those items.</span></span> <span data-ttu-id="41b27-106">Šīs funkcionalitātes nolūks ir viegli izveidot līdzekli Līdzekļu pārvaldībā, pamatojoties uz pirkšanas pasūtījumu.</span><span class="sxs-lookup"><span data-stu-id="41b27-106">The purpose of this functionality is to easily create an asset in Asset Management based on a purchase order.</span></span>

<span data-ttu-id="41b27-107">Vispirms iestatiet vienības, kas jāizmanto līdzekļu veidošanai no pirkšanas pasūtījuma **Līdzekļu vienībās**.</span><span class="sxs-lookup"><span data-stu-id="41b27-107">First, you set up the items to be used for creating assets from a purchase order in **Asset items**.</span></span> <span data-ttu-id="41b27-108">Pēc pirkšanas pasūtījuma rindas izveidošanas jūs veidojat līdzekļus **Gaidošie līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="41b27-108">After creating a purchase order line, you create the assets in **Pending assets**.</span></span> <span data-ttu-id="41b27-109">Ir iespējams izlemt, kurā pirkšanas pasūtījuma stadijā līdzeklis būtu jāizveido.</span><span class="sxs-lookup"><span data-stu-id="41b27-109">It is possible to decide at which stage of the purchase order the asset should be created.</span></span>


## <a name="select-asset-items"></a><span data-ttu-id="41b27-110">Atlasīt līdzekļa vienības</span><span class="sxs-lookup"><span data-stu-id="41b27-110">Select asset items</span></span>

1. <span data-ttu-id="41b27-111">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļi** > **Vienības**.</span><span class="sxs-lookup"><span data-stu-id="41b27-111">Click **Asset management** > **Setup** > **Assets** > **Items**.</span></span>
2. <span data-ttu-id="41b27-112">Noklikšķiniet uz **Jauns**, lai izveidotu jaunu līdzekļa vienību.</span><span class="sxs-lookup"><span data-stu-id="41b27-112">Click **New** to create a new asset item.</span></span>
3. <span data-ttu-id="41b27-113">Atlasiet vienību laukā **Vienības kods**.</span><span class="sxs-lookup"><span data-stu-id="41b27-113">Select the item in the **Item number** field.</span></span> <span data-ttu-id="41b27-114">Izejot no šī lauka, vienības nosaukums tiek automātiski ievietots laukā **Preces nosaukums.**</span><span class="sxs-lookup"><span data-stu-id="41b27-114">When you leave that field, the item name is automatically inserted in the **Product name** field.</span></span>
4. <span data-ttu-id="41b27-115">Kopsavilkuma cilnē **Vispārīgi** atlasiet vienības līdzekļa tipu.</span><span class="sxs-lookup"><span data-stu-id="41b27-115">On the **General** FastTab, select an asset type for the item.</span></span>
5. <span data-ttu-id="41b27-116">Atlasiet vienības līdzekļa ražotāju un modeli.</span><span class="sxs-lookup"><span data-stu-id="41b27-116">Select asset manufacturer and model for the item.</span></span>
6. <span data-ttu-id="41b27-117">Saglabājiet vienību.</span><span class="sxs-lookup"><span data-stu-id="41b27-117">Save the item.</span></span>


## <a name="create-assets-from-pending-assets"></a><span data-ttu-id="41b27-118">Līdzekļu izveide no gaidošiem līdzekļiem</span><span class="sxs-lookup"><span data-stu-id="41b27-118">Create assets from pending assets</span></span>

1. <span data-ttu-id="41b27-119">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Kopīgi** > **Līdzekļi** > **Gaidošie līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="41b27-119">Click **Asset management** > **Common** > **Assets** > **Pending Assets**.</span></span>
2. <span data-ttu-id="41b27-120">Tiks parādīts pirkšanas pasūtījumu atjaunināts saraksts, pamatojoties uz vienībām, kas atlasītas laukā **Līdzekļu vienības**.</span><span class="sxs-lookup"><span data-stu-id="41b27-120">You will see an updated list of the purchase orders based on the items selected in **Asset items**.</span></span>
3. <span data-ttu-id="41b27-121">Varat filtrēt pirkšanas pasūtījumu statusu, lai atlasītu, kurā dzīves cikla stāvoklī šis līdzeklis ir jāizveido.</span><span class="sxs-lookup"><span data-stu-id="41b27-121">You can filter the status of purchase orders to select at which lifecycle state the asset should be created.</span></span> <span data-ttu-id="41b27-122">Piemēram, varat izveidot līdzekļus tikai tad, ja preču ieejas plūsma ir iegrāmatota pirkšanas pasūtījumā.</span><span class="sxs-lookup"><span data-stu-id="41b27-122">For example, you may only want to create assets when a product receipt has been posted on a purchase order.</span></span>
4. <span data-ttu-id="41b27-123">Pirkšanas pasūtījuma rindā atlasiet saiti **Atsauces numurs**, lai skatītu detalizētu informāciju par vienību.</span><span class="sxs-lookup"><span data-stu-id="41b27-123">Select the **Reference number** link on a purchase order line to view detailed information about the item.</span></span>
5. <span data-ttu-id="41b27-124">Ja vēlaties rediģēt, kuras dimensijas tiek rādītas kopsavilkuma cilnē **Krājumu dimensijas**, noklikšķiniet uz pogas **Rādīt dimensijas** un veiciet atlasi.</span><span class="sxs-lookup"><span data-stu-id="41b27-124">If you want to edit which dimensions are displayed on the **Inventory dimensions** FastTab, click the **Display Dimensions** button, and make your selections.</span></span>
6. <span data-ttu-id="41b27-125">Ja vēlaties izveidot līdzekli, kura pamatā ir pirkšanas pasūtījuma rinda, saraksta lapā atzīmējiet izvēles rūtiņu kolonnā **Atzīmēt** un noklikšķiniet uz **Izveidot līdzekļus**.</span><span class="sxs-lookup"><span data-stu-id="41b27-125">If you want to create an asset based on a purchase order line, select the check box in the **Mark** column for that line on the list page, and click **Create assets**.</span></span> <span data-ttu-id="41b27-126">Tiks parādīts ziņojums, informējot jūs par līdzekļa ID.</span><span class="sxs-lookup"><span data-stu-id="41b27-126">A message will be displayed informing you of the asset ID.</span></span>
7. <span data-ttu-id="41b27-127">Atlasiet līdzekli sarakstā **Visi līdzekļi** un noklikšķiniet uz pogas **Rediģēt**, lai pievienotu līdzeklim vairāk informācijas.</span><span class="sxs-lookup"><span data-stu-id="41b27-127">Select the asset in the **All assets** list and click **Edit** to add more information to the asset.</span></span>
8. <span data-ttu-id="41b27-128">Laukā **Gaidošie līdzekļi**, ja vēlaties dzēst rindu, jo nevēlaties izveidot līdzekli, atlasiet izvēles rūtiņu rindas kolonnā **Atzīmēt** un noklikšķiniet uz **Atmest gaidošos līdzekļus**.</span><span class="sxs-lookup"><span data-stu-id="41b27-128">In **Pending assets**, if you want to delete a line because you don't want to create an asset, select the check box in the **Mark** column for that line, and click **Discard pending assets**.</span></span> <span data-ttu-id="41b27-129">Tiks parādīts ziņojums, informējot jūs par līdzekļa ID.</span><span class="sxs-lookup"><span data-stu-id="41b27-129">A message will be displayed informing you of the asset ID.</span></span> <span data-ttu-id="41b27-130">Jūs nedzēšat pirkšanas pasūtījumu vai pārdošanas pasūtījumu — tikai to ierakstu, no kura jūs varētu būt izveidojis līdzekli **Līdzekļu pārvaldībā**.</span><span class="sxs-lookup"><span data-stu-id="41b27-130">You are not deleting the purchase order or sales order, just the record from which you could have created an asset in **Asset Management**.</span></span>

>[!NOTE]
><span data-ttu-id="41b27-131">Visas preces dimensijas (izmērs, krāsa, konfigurācija utt.) tiek automātiski pārsūtītas uz līdzekļa atribūtiem.</span><span class="sxs-lookup"><span data-stu-id="41b27-131">All product dimensions (size, color, configuration etc.) are automatically transferred to the asset attributes.</span></span> <span data-ttu-id="41b27-132">Izsekošanas dimensijas (sērijas numurs) tiek glabātas tieši uz līdzekļa, kad līdzeklis ir izveidots.</span><span class="sxs-lookup"><span data-stu-id="41b27-132">Tracking dimensions (serial number) are stored directly on the asset when the asset is created.</span></span>


## <a name="find-pending-assets"></a><span data-ttu-id="41b27-133">Atrast gaidošos līdzekļus</span><span class="sxs-lookup"><span data-stu-id="41b27-133">Find pending assets</span></span>

<span data-ttu-id="41b27-134">Varat palaist **Gaidošo līdzekļu skaitīšanu**, lai pārbaudītu, vai nav gaidošo līdzekļu.</span><span class="sxs-lookup"><span data-stu-id="41b27-134">You can run a **Pending asset count** to check for pending assets.</span></span> <span data-ttu-id="41b27-135">Piemēram, šo funkciju var izmantot, lai saņemtu paziņojumu katru reizi, kad gaidošie līdzekļi ir gatavi, lai tos izveidotu kā līdzekli.</span><span class="sxs-lookup"><span data-stu-id="41b27-135">For example, this function can be used for receiving a notification each time a pending asset is ready to be created as an asset.</span></span>

1. <span data-ttu-id="41b27-136">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Periodiski** > **Līdzekļi** > **Gaidošo līdzekļu skaitīšana**.</span><span class="sxs-lookup"><span data-stu-id="41b27-136">Click **Asset management** > **Periodic** > **Assets** > **Pending asset count**.</span></span>
2. <span data-ttu-id="41b27-137">Noklikšķiniet uz **Labi**, lai palaistu darbu un atjauninātu sarakstu **Gaidošajos līdzekļos**.</span><span class="sxs-lookup"><span data-stu-id="41b27-137">Click **OK** to run the job and update the list in **Pending assets**.</span></span>
3. <span data-ttu-id="41b27-138">Šo darbu var iestatīt, lai palaistu kā pakešuzdevumu, piemēram, reizi dienā.</span><span class="sxs-lookup"><span data-stu-id="41b27-138">You can set up this job to run as a batch job, for example, once each day.</span></span>

<span data-ttu-id="41b27-139">**Brīdinājums:** ja dati pirkšanas pasūtījumā tiek mainīti *pēc tam*, kad līdzeklis ir izveidots, pamatojoties uz atbilstīgo vienību, šīs izmaiņas līdzeklim netiks atspoguļotas.</span><span class="sxs-lookup"><span data-stu-id="41b27-139">**Caution:** If data is changed on a purchase order *after* you have created an asset based on the appertaining item, those changes will not be reflected on the asset.</span></span>

---
title: Kvalitātes pārvaldības krājumu paraugu ņemšana
description: Šajā tēmā ir aprakstīts, kā iestatīt krājumu paraugu ņemšanu.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventItemSampling
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ae8bfd329ca0d7c30adcd93a759ee6bea7b76278
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022232"
---
# <a name="quality-management-item-sampling"></a><span data-ttu-id="efc83-103">Kvalitātes pārvaldības krājumu paraugu ņemšana</span><span class="sxs-lookup"><span data-stu-id="efc83-103">Quality management item sampling</span></span>

<span data-ttu-id="efc83-104">Krājumu paraugu ņemšana tiek izmantota kā daļa no kvalitātes saistības.</span><span class="sxs-lookup"><span data-stu-id="efc83-104">Item sampling is used as part of a quality association.</span></span> <span data-ttu-id="efc83-105">Tas nosaka pašreizējā krājuma apjomu, kas jāpārbauda.</span><span class="sxs-lookup"><span data-stu-id="efc83-105">It defines the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="efc83-106">Paraugu nodošana var būt balstīta uz fiksētiem daudzumiem, procentiem vai pilnu numura zīmi.</span><span class="sxs-lookup"><span data-stu-id="efc83-106">Sampling can be based on fixed quantities, a percentage, or a full license plate.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="efc83-107">Krājuma paraugu izveides iestatīšana</span><span class="sxs-lookup"><span data-stu-id="efc83-107">Set up item sampling</span></span>

<span data-ttu-id="efc83-108">Lai iestatītu krājuma paraugu ņemšanu, rīkojieties šādi.</span><span class="sxs-lookup"><span data-stu-id="efc83-108">Follow these steps to set up item sampling.</span></span>

1. <span data-ttu-id="efc83-109">Dodieties uz **Krājumu pārvaldība \> Iestatījumi \> Kvalitātes kontrole \> Krājumu iztveršana**.</span><span class="sxs-lookup"><span data-stu-id="efc83-109">Go to **Inventory management \> Setup \> Quality control \> Item sampling**.</span></span>
1. <span data-ttu-id="efc83-110">Atlasiet **Jauns**.</span><span class="sxs-lookup"><span data-stu-id="efc83-110">Select **New**.</span></span>
1. <span data-ttu-id="efc83-111">Ievadiet vērtību laukā **Krājumu paraugu ņemšana**.</span><span class="sxs-lookup"><span data-stu-id="efc83-111">In the **Item sampling** field, enter a value.</span></span>
1. <span data-ttu-id="efc83-112">Laukā **Apraksts** ievadiet kādu vērtību.</span><span class="sxs-lookup"><span data-stu-id="efc83-112">In the **Description** field, enter a value.</span></span>
1. <span data-ttu-id="efc83-113">Ievadiet skaitli laukā **Vērtība**.</span><span class="sxs-lookup"><span data-stu-id="efc83-113">In the **Value** field, enter a number.</span></span> <span data-ttu-id="efc83-114">Šī vērtība attiecas uz daudzuma specifikācijas vērtību, kas atlasīta blakus esošajā laukā.</span><span class="sxs-lookup"><span data-stu-id="efc83-114">This value is related to the quantity specification value that is selected in the adjacent field.</span></span>
1. <span data-ttu-id="efc83-115">Sadaļā **Process** atzīmējiet izvēles rūtiņu **Pilna bloķēšana**, ja testa kļūmes gadījumā ir jābloķē viss partijas vai pasūtījuma rindas daudzums.</span><span class="sxs-lookup"><span data-stu-id="efc83-115">In the **Process** section, select the **Full blocking** check box if the whole lot or order line quantity should be blocked if a test is failed.</span></span> <span data-ttu-id="efc83-116">Ja šī izvēles rūtiņa ir notīrīta, tikai krājumi kvalitātes pasūtījumā tiks bloķēti, ja tests nav izdevies.</span><span class="sxs-lookup"><span data-stu-id="efc83-116">If this check box is cleared, only the items in the quality order will be blocked if a test is failed.</span></span>
1. <span data-ttu-id="efc83-117">Atlasiet **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="efc83-117">Select **Save**.</span></span>
1. <span data-ttu-id="efc83-118">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="efc83-118">Close the page.</span></span>

> [!NOTE]
> <span data-ttu-id="efc83-119">Funkcija *Kvalitātes pārvaldība noliktavas procesiem* nodrošina papildu krājumu paraugu ņemšanas iespējas.</span><span class="sxs-lookup"><span data-stu-id="efc83-119">The *Quality management for warehouse processes* feature provides additional item sampling capabilities.</span></span> <span data-ttu-id="efc83-120">Tas pievieno *preču paraugu ņemšanas tvēruma* koncepciju un ļauj noteikt pilnu numura zīmi kā daudzuma specifikāciju.</span><span class="sxs-lookup"><span data-stu-id="efc83-120">It adds the concept of *item sampling scope* and lets you define a full license plate as the quantity specification.</span></span> <span data-ttu-id="efc83-121">Ja esat ieslēdzis šo līdzekli, tad skatiet sadaļu [Kvalitātes pārvaldība noliktavas procesiem](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="efc83-121">If you've turned on this feature, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

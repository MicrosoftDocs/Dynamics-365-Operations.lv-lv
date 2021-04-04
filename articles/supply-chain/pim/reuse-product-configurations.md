---
title: Preču konfigurāciju atkārtota izmantošana
description: Varat norādīt, ka vēlaties automātiski atkārtoti izmantot esošu konfigurāciju kādai precei. Kad lietotājs ir pabeidzis konfigurācijas sesiju, sistēma pārbauda, vai jau pastāv lietotāja atlasēm atbilstoša konfigurācija. Ja tiek atrasta atbilstoša konfigurācija, tad konfigurācijas ID, atbilstošais materiālu komplekts (MK) un maršruts tiek izmantoti atkārtoti.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 21dc25b878ff65b57b060fe3d74b5d120fa4b5cd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260603"
---
# <a name="reuse-product-configurations"></a><span data-ttu-id="83c2f-105">Preču konfigurāciju atkārtota izmantošana</span><span class="sxs-lookup"><span data-stu-id="83c2f-105">Reuse product configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83c2f-106">Varat norādīt, ka vēlaties automātiski atkārtoti izmantot esošu konfigurāciju kādai precei.</span><span class="sxs-lookup"><span data-stu-id="83c2f-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="83c2f-107">Kad lietotājs ir pabeidzis konfigurācijas sesiju, sistēma pārbauda, vai jau pastāv lietotāja atlasēm atbilstoša konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="83c2f-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="83c2f-108">Ja tiek atrasta atbilstoša konfigurācija, tad konfigurācijas ID, atbilstošais materiālu komplekts (MK) un maršruts tiek izmantoti atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="83c2f-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="83c2f-109">Prasības konfigurāciju atkārtotai izmantošanai</span><span class="sxs-lookup"><span data-stu-id="83c2f-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="83c2f-110">Lai iespējotu konfigurāciju atkārtotu izmantošanu, lapā **Detalizēta informācija par preces konfigurācijas modeli** komponentiem un atribūtiem ir jānorāda tālāk aprakstītā informācija.</span><span class="sxs-lookup"><span data-stu-id="83c2f-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="83c2f-111">**Komponenti un apakškomponenti** — kopsavilkuma cilnē **Vispārīgi**, laukā **Atkārtoti izmantot konfigurācijas** atlasiet vērtību **Jā**.</span><span class="sxs-lookup"><span data-stu-id="83c2f-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="83c2f-112">**Atribūti** — kopsavilkuma cilnē **Atribūti** atlasiet opciju **Iekļaut atkārtotā izmantošanā**.</span><span class="sxs-lookup"><span data-stu-id="83c2f-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="83c2f-113">Šī opcija ir redzama tikai tad, ja saistītais komponents ir iespējots atkārtotai izmantošanai.</span><span class="sxs-lookup"><span data-stu-id="83c2f-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="83c2f-114">Ja atkārtotai izmantošanai neatlasāt nevienu komponentu, šī konfigurācija vienmēr tiek izmantoti atkārtoti, neatkarīgi no lietotāja konfigurācijas sesijas laikā veiktās atlases.</span><span class="sxs-lookup"><span data-stu-id="83c2f-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="83c2f-115">Esošās konfigurācijas atribūtu vērtībām ir jāatbilst lietotāja atlasēm.</span><span class="sxs-lookup"><span data-stu-id="83c2f-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="83c2f-116">Piemēram, ja konfigurācijas sesijas laikā lietotājs kā krāsu atlasa **Zilā krāsā**, tad sistēma pārbauda, vai esošajā šī komponenta konfigurācijā ir zila krāsa.</span><span class="sxs-lookup"><span data-stu-id="83c2f-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="83c2f-117">Konfigurācijas atkārtotas izmantošanas atiestatīšana</span><span class="sxs-lookup"><span data-stu-id="83c2f-117">Resetting configuration reuse</span></span>
<span data-ttu-id="83c2f-118">Kad atlasāt konfigurācijas atkārtota izmantošanas atiestatīšanu, iepriekš izveidotās konfigurācijas vairs netiek ņemtas vērā.</span><span class="sxs-lookup"><span data-stu-id="83c2f-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="83c2f-119">Konfigurāciju atkārtotu izmantošanu varat vēlēties atiestatīt, ja ir mainīts MK vai maršruts, bet nav mainīti saistītie atribūti.</span><span class="sxs-lookup"><span data-stu-id="83c2f-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="83c2f-120">Konfigurācijas atkārtotu izmantošanu komponentam varat atiestatīt kopsavilkuma cilnē **Vispārīgi**.</span><span class="sxs-lookup"><span data-stu-id="83c2f-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
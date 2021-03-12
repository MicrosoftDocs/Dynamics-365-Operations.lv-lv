---
title: Kopuma darbību kodi
description: Šajā tēmā sniegts kopuma darbību kodu apskats, un kā tie tiek izmantoti.
author: josaw1
manager: tfehr
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveStepCode, WHSReplenishmentTemplates, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 08b40c076e288592f6a4cd628b9acd8a2eaedb7e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998407"
---
# <a name="wave-step-codes"></a><span data-ttu-id="2cf89-103">Kopuma darbību kodi</span><span class="sxs-lookup"><span data-stu-id="2cf89-103">Wave step codes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2cf89-104">Kopuma darbību kodi ir kodi, ko lietotāji var iestatīt un izmantot, lai saistītu konkrētas kopuma metodes atbilstošajai veidnei.</span><span class="sxs-lookup"><span data-stu-id="2cf89-104">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="2cf89-105">Veidnēs ir ietvertas papildināšanas, konteinerizēšanas, etiķešu drukāšanas, noslodzes veidošanas un kārtošanas veidnes.</span><span class="sxs-lookup"><span data-stu-id="2cf89-105">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="2cf89-106">Kad netiek lietoti kopuma darbību kodi, lietotājiem jāievada brīvs teksts, lai atsauktos uz noteiktu veidni no kopuma metodes instances.</span><span class="sxs-lookup"><span data-stu-id="2cf89-106">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="2cf89-107">Brīvajam tekstam ir nosliece uz kļūdām, jo lietotājiem ir jāpārliecinās, vai kopuma darbību teksts, ko lietotāji pievieno noteiktai kopuma darbību metodei kopuma veidnē, tieši atbilst kopuma darbību tekstam mērķa veidnē.</span><span class="sxs-lookup"><span data-stu-id="2cf89-107">Free text is prone to errors because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="2cf89-108">Kopuma darbību kodi noteiktam kopuma darbību tipam ir iestatīti atsevišķā lapā.</span><span class="sxs-lookup"><span data-stu-id="2cf89-108">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="2cf89-109">Katrai kopuma darbību metodes instancei kopuma veidnē, kas pieprasa kopuma darbību kodu, nolaižamajā sarakstā jābūt atlasītam kopuma darbību kodam.</span><span class="sxs-lookup"><span data-stu-id="2cf89-109">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="2cf89-110">Atlase nolaižamajā sarakstā aizstāj brīvā teksta ievadi un palīdz samazināt cilvēka kļūdas risku un ietekmi.</span><span class="sxs-lookup"><span data-stu-id="2cf89-110">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="2cf89-111">Iestatīšanas kodus lieto, lai veidotu saiti uz kopuma darbību metodi kopuma veidnē uz metodi mērķa veidnē.</span><span class="sxs-lookup"><span data-stu-id="2cf89-111">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="2cf89-112">Kopuma darbību kodu līdzekļa izmantošana nav obligāta.</span><span class="sxs-lookup"><span data-stu-id="2cf89-112">Use of the wave step codes feature is optional.</span></span> <span data-ttu-id="2cf89-113">Visām juridiskajām personām tā ir iespējota organizācijas līmenī.</span><span class="sxs-lookup"><span data-stu-id="2cf89-113">It is enabled organization-wide for all legal entities.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="2cf89-114">Iestatīt demonstrāciju</span><span class="sxs-lookup"><span data-stu-id="2cf89-114">Setup demo</span></span> 

<span data-ttu-id="2cf89-115">Šai demonstrācijai ir jābūt instalētiem demo datiem, un jums ir jāizmanto **USMF** demo datu uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="2cf89-115">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="2cf89-116">Iespējot kopuma darbību kodus</span><span class="sxs-lookup"><span data-stu-id="2cf89-116">Enable wave step codes</span></span>

<span data-ttu-id="2cf89-117">Sekojiet šiem soļiem, lai ieslēgtu kopuma darbību kodu līdzekli.</span><span class="sxs-lookup"><span data-stu-id="2cf89-117">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="2cf89-118">Dodieties uz **Līdzekļu pārvaldība**.</span><span class="sxs-lookup"><span data-stu-id="2cf89-118">Go to **Feature Management**.</span></span>
2. <span data-ttu-id="2cf89-119">Atlasiet, lai iespējotu līdzekli ar nosaukumu **Organizācijas līmeņa kopuma darbību kods**.</span><span class="sxs-lookup"><span data-stu-id="2cf89-119">Select to enable the feature called **Organization-wide Wave Step Code**.</span></span>

<span data-ttu-id="2cf89-120">Visi esošie kopuma darbību brīvie teksti visās juridiskajās personās tiek jaunināti uz jauno struktūru.</span><span class="sxs-lookup"><span data-stu-id="2cf89-120">All existing wave step free texts in all legal entities are upgraded to the new structure.</span></span> <span data-ttu-id="2cf89-121">Pēc šīs jaunināšanas pabeigšanas visām juridiskajām personām, līdzeklis tiek iespējots.</span><span class="sxs-lookup"><span data-stu-id="2cf89-121">After this upgrade is completed for all legal entities, then the feature is enabled.</span></span> <span data-ttu-id="2cf89-122">Ja līdzekli nevar iespējot vienai vai vairākām juridiskajām personām, līdzeklis nav iespējots nevienai no juridiskajām personām.</span><span class="sxs-lookup"><span data-stu-id="2cf89-122">If the feature cannot be enabled for one or more legal entities, then the feature is not enabled for any legal entities.</span></span>

<span data-ttu-id="2cf89-123">Iespējošanas laikā validācijas tiek veiktas datu jaunināšanas laikā.</span><span class="sxs-lookup"><span data-stu-id="2cf89-123">During the enablement, validations are done during the data upgrade.</span></span> <span data-ttu-id="2cf89-124">Ja jaunināšana neizdodas, tiek parādīts kļūdas ziņojums.</span><span class="sxs-lookup"><span data-stu-id="2cf89-124">If the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="2cf89-125">Jaunināšana var neizdoties, jo pastāv šādi konflikti:</span><span class="sxs-lookup"><span data-stu-id="2cf89-125">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="2cf89-126">Pastāv kopuma darbību brīvā teksta dublikāts.</span><span class="sxs-lookup"><span data-stu-id="2cf89-126">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="2cf89-127">Pastāv pielāgojumi.</span><span class="sxs-lookup"><span data-stu-id="2cf89-127">Customizations exist.</span></span>
- <span data-ttu-id="2cf89-128">Kopuma darbību brīvais teksts, kas ir saistīts ar metodes instanci, neatbilst paredzētajam veidnes tipam.</span><span class="sxs-lookup"><span data-stu-id="2cf89-128">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="2cf89-129">Pēc tam, kad esat atrisinājis konfliktus, kas ir identificēti validācijas laikā, varat atkārtoti mēģināt iespējot šo līdzekli.</span><span class="sxs-lookup"><span data-stu-id="2cf89-129">After you've resolved any conflicts that are identified during the validations, you can retry to enable the feature.</span></span>

<span data-ttu-id="2cf89-130">Kad līdzeklis ir iespējots, kļūst pieejama lapa **Kopuma darbību kodi** (**Noliktavas pārvaldība \> Iestatīšana \> Kopumi \> Kopuma darbību kodi**).</span><span class="sxs-lookup"><span data-stu-id="2cf89-130">When the feature has been enabled, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="2cf89-131">Šajā lapā ir uzskaitīti kopuma darbību kodi, kas tika atjaunināti, kad tika iespējots organizācijas līmeņa kopuma darbību koda līdzeklis.</span><span class="sxs-lookup"><span data-stu-id="2cf89-131">This page lists the wave step codes that were upgraded when the Organization-wide Wave Step Code feature was enabled.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="2cf89-132">Izveidot jauna kopuma darbību kodus</span><span class="sxs-lookup"><span data-stu-id="2cf89-132">Create new wave step codes</span></span>

<span data-ttu-id="2cf89-133">Varat izmantot lapu **Kopuma darbību kodi**, lai izveidotu un dzēstu kopuma darbību kodus.</span><span class="sxs-lookup"><span data-stu-id="2cf89-133">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="2cf89-134">Katram jaunam kopuma darbību kodam un ar to saistītajam ID ir jābūt unikālam visos kopuma darbību tipos, un tie ir jādefinē konkrētam kopuma darbību tipam.</span><span class="sxs-lookup"><span data-stu-id="2cf89-134">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="2cf89-135">Pielietot kopuma darbību kodus</span><span class="sxs-lookup"><span data-stu-id="2cf89-135">Apply wave step codes</span></span>

<span data-ttu-id="2cf89-136">Pēc tam, kad esat definējis piemērotus kopuma darbību kodus, tos var lietot kopuma procesa metodēm.</span><span class="sxs-lookup"><span data-stu-id="2cf89-136">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="2cf89-137">Lai pielietotu kopuma darbību kodus, dodieties uz atbilstošo mērķa veidni.</span><span class="sxs-lookup"><span data-stu-id="2cf89-137">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="2cf89-138">Šeit ir mērķa veidnes, kam kopuma darbību kodi ir izveidoti, lai norādītu uz:</span><span class="sxs-lookup"><span data-stu-id="2cf89-138">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="2cf89-139">**Papildināšanas veidnes.:** Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Papildināšanas veidnes</span><span class="sxs-lookup"><span data-stu-id="2cf89-139">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="2cf89-140">**Noslodzes būvējuma veidnes:** Noliktavas pārvaldība \>Iestatīšana \>noslodzes kompilācijas veidnes \> </span><span class="sxs-lookup"><span data-stu-id="2cf89-140">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="2cf89-141">**Kārtot veidnes:** Noliktavas pārvaldība \>Iestatīšana \>Iepakošana \>Nosūtīšanas kārtošanas veidnes</span><span class="sxs-lookup"><span data-stu-id="2cf89-141">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="2cf89-142">**Konteinerizēšanas veidnes:** Noliktavas pārvaldība \> Iestatīšana \> Konteineri \> Konteineru būvējuma veidnes</span><span class="sxs-lookup"><span data-stu-id="2cf89-142">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="2cf89-143">**Etiķešu drukāšanas veidnes:** Noliktavas pārvaldība \>Uzstādīšana \>Dokumenta maršrutēšana \>Kopuma etiķešu veidnes</span><span class="sxs-lookup"><span data-stu-id="2cf89-143">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="2cf89-144">Šajā sarakstā iekļautās veidnes tiek piemērotas, kad tās ir norādītas no kopuma procesa metodes, kas ir atlasītas kopuma veidnēs.</span><span class="sxs-lookup"><span data-stu-id="2cf89-144">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="2cf89-145">Kad kopuma darbību kods procesa metodē kopuma veidnē atbilst tā darbību kodam vienā no veidņu tipiem, tiek lietota veidne.</span><span class="sxs-lookup"><span data-stu-id="2cf89-145">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="2cf89-146">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="2cf89-146">Sample scenario</span></span>

<span data-ttu-id="2cf89-147">Šī procedūra palīdz garantēt, ka izveidotā papildināšanas veidne tiks lietota kopuma veidnei.</span><span class="sxs-lookup"><span data-stu-id="2cf89-147">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="2cf89-148">Dodieties uz **Noliktavas pārvaldība \>Iestatīšana \>Kopumi \>Kopuma darbību kodi** un izveidojiet kopuma darbību kodu **Papildināšanas** tipam.</span><span class="sxs-lookup"><span data-stu-id="2cf89-148">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="2cf89-149">Dodieties uz **Noliktavu pārvaldība\> Iestatīšana \> Papildināšana \> Papildināšanas veidnes** un izveidojiet papildināšanas veidni.</span><span class="sxs-lookup"><span data-stu-id="2cf89-149">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="2cf89-150">Papildināšanas veidnē atlasiet kopuma darbības kodu, ko izveidojāt **Papildināšanas** tipam.</span><span class="sxs-lookup"><span data-stu-id="2cf89-150">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="2cf89-151">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \>Kopumi \>Kopuma veidnes** un atlasiet kopuma veidni, ko plānojat izmantot.</span><span class="sxs-lookup"><span data-stu-id="2cf89-151">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="2cf89-152">Veidnē kopsavilkuma cilnē **Metodes** atlasiet **Papildināšanas** metodi.</span><span class="sxs-lookup"><span data-stu-id="2cf89-152">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="2cf89-153">Laukā **Kopuma darbības kodi** atlasiet kopuma darbības kodu, ko izvēlējāties papildināšanas veidnē.</span><span class="sxs-lookup"><span data-stu-id="2cf89-153">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

<span data-ttu-id="2cf89-154">Veiciet šīs darbības katrai juridiskajai personai.</span><span class="sxs-lookup"><span data-stu-id="2cf89-154">You perform these steps for each legal entity.</span></span>

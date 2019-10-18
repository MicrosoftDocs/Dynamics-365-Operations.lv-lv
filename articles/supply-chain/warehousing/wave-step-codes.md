---
title: Kopuma darbību kodi
description: Šajā tēmā sniegts kopuma darbību kodu apskats, un kā tie tiek izmantoti.
author: josaw1
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 0f89c6098db9e2e3a9aa4ee3666e4b9ae608f054
ms.sourcegitcommit: d8f1135cdbc2deca70bc4b2805a0519253c9a31f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/06/2019
ms.locfileid: "1992361"
---
# <a name="wave-step-codes"></a><span data-ttu-id="575df-103">Kopuma darbību kodi</span><span class="sxs-lookup"><span data-stu-id="575df-103">Wave step codes</span></span>

[!include [banner](../includes/preview-banner.md)]
[!include [banner](../includes/banner.md)]

## <a name="about-wave-step-codes"></a><span data-ttu-id="575df-104">Par kopuma darbību kodiem</span><span class="sxs-lookup"><span data-stu-id="575df-104">About wave step codes</span></span>

<span data-ttu-id="575df-105">Kopuma darbību kodi ir kodi, ko lietotāji var iestatīt un izmantot, lai saistītu konkrētas kopuma metodes atbilstošajai veidnei.</span><span class="sxs-lookup"><span data-stu-id="575df-105">Wave step codes are codes that users can set up and use to link specific instances of wave methods to a corresponding template.</span></span> <span data-ttu-id="575df-106">Veidnēs ir ietvertas papildināšanas, konteinerizēšanas, etiķešu drukāšanas, noslodzes veidošanas un kārtošanas veidnes.</span><span class="sxs-lookup"><span data-stu-id="575df-106">The templates include templates for replenishment, containerization, label printing, load building, and sorting.</span></span>

<span data-ttu-id="575df-107">Kad netiek lietoti kopuma darbību kodi, lietotājiem jāievada brīvs teksts, lai atsauktos uz noteiktu veidni no kopuma metodes instances.</span><span class="sxs-lookup"><span data-stu-id="575df-107">When wave step codes aren't used, users must enter free text to reference a specific template from the wave method instance.</span></span> <span data-ttu-id="575df-108">Brīvajam tekstam ir nosliece uz kļūdu, jo lietotājiem ir jāpārliecinās, vai kopuma darbību teksts, ko lietotāji pievieno noteiktai kopuma darbību metodei kopuma veidnē, tieši atbilst kopuma darbību tekstam mērķa veidnē.</span><span class="sxs-lookup"><span data-stu-id="575df-108">Free text is prone to error, because users must make sure that the wave step text that they add for a specific wave step method in a wave template exactly matches the wave step text in the target template.</span></span>

<span data-ttu-id="575df-109">Kopuma darbību kodi noteiktam kopuma darbību tipam ir iestatīti atsevišķā lapā.</span><span class="sxs-lookup"><span data-stu-id="575df-109">Wave step codes for a specific wave step type are set up on a separate page.</span></span> <span data-ttu-id="575df-110">Katrai kopuma darbību metodes instancei kopuma veidnē, kas pieprasa kopuma darbību kodu, nolaižamajā sarakstā jābūt atlasītam kopuma darbību kodam.</span><span class="sxs-lookup"><span data-stu-id="575df-110">For every wave step method instance in a wave template that requires a wave step code, the wave step code must be selected in a drop-down list.</span></span> <span data-ttu-id="575df-111">Atlase nolaižamajā sarakstā aizstāj brīvā teksta ievadi un palīdz samazināt cilvēka kļūdas risku un ietekmi.</span><span class="sxs-lookup"><span data-stu-id="575df-111">Selection in a drop-down list replaces free text entry and helps reduce the risk and impact of human error.</span></span> <span data-ttu-id="575df-112">Iestatīšanas kodus lieto, lai veidotu saiti uz kopuma darbību metodi kopuma veidnē uz metodi mērķa veidnē.</span><span class="sxs-lookup"><span data-stu-id="575df-112">Setup codes are used to link a wave step method in a wave template to a target template for the method.</span></span>

> [!NOTE]
> <span data-ttu-id="575df-113">Kopuma soļu kodu funkcijas lietošana ir neobligāta, un uzņemšana ir uz juridisku personu.</span><span class="sxs-lookup"><span data-stu-id="575df-113">Use of the wave step codes feature is optional, and uptake is per legal entity.</span></span> <span data-ttu-id="575df-114">Tādēļ, ja noteikta juridiska persona izmanto šo funkciju, visi esošie kopuma darbību kodi šai juridiskajai personai tiek jaunināti uz jauno struktūru.</span><span class="sxs-lookup"><span data-stu-id="575df-114">Therefore, if a specific legal entity uses the feature, all existing wave step codes in that legal entity are upgraded to the new structure.</span></span>

## <a name="setup-demo"></a><span data-ttu-id="575df-115">Iestatīt demonstrāciju</span><span class="sxs-lookup"><span data-stu-id="575df-115">Setup demo</span></span> 

<span data-ttu-id="575df-116">Šai demonstrācijai ir jābūt instalētiem demo datiem, un jums ir jāizmanto **USMF** demo datu uzņēmums.</span><span class="sxs-lookup"><span data-stu-id="575df-116">For this demo, demo data must be installed, and you must use the **USMF** demo data company.</span></span>

### <a name="enable-wave-step-codes"></a><span data-ttu-id="575df-117">Iespējot kopuma darbību kodus</span><span class="sxs-lookup"><span data-stu-id="575df-117">Enable wave step codes</span></span>

<span data-ttu-id="575df-118">Sekojiet šiem soļiem, lai ieslēgtu kopuma darbību kodu līdzekli.</span><span class="sxs-lookup"><span data-stu-id="575df-118">Follow these steps to turn on the wave step codes feature.</span></span>

1. <span data-ttu-id="575df-119">Doties uz **Noliktavas vadība\> Iestatīšana \> Noliktavas vadības parametri**.</span><span class="sxs-lookup"><span data-stu-id="575df-119">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
2. <span data-ttu-id="575df-120">Cilnē **Vispārīgi** **Kopuma apstiprināšana** kopsavilkuma cilnē iestatiet opciju **Iespējot kopumu kodus** vērtību uz **Jā**.</span><span class="sxs-lookup"><span data-stu-id="575df-120">On the **General** tab, on the **Wave processing** FastTab, set the **Enable wave step codes** option to **Yes**.</span></span>

<span data-ttu-id="575df-121">Visi esošie kopuma darbību brīvie teksti tiek jaunināti uz jauno struktūru.</span><span class="sxs-lookup"><span data-stu-id="575df-121">All existing wave step free texts are upgraded to the new structure.</span></span> <span data-ttu-id="575df-122">Pēc tam, kad šis jauninājums ir izpildīts juridiskai personai, opcija **Iespējot kopuma darbību kodus** vairs nav pieejama **Noliktavas pārvaldības parametru** lapā.</span><span class="sxs-lookup"><span data-stu-id="575df-122">After this upgrade is completed for a legal entity, the **Enable wave step codes** option is no longer available on the **Warehouse management parameters** page.</span></span>

<span data-ttu-id="575df-123">Pārbaudes tiek veiktas jaunināšanas laikā, un, ja jaunināšana neizdodas, saņemsiet kļūdas ziņojumu.</span><span class="sxs-lookup"><span data-stu-id="575df-123">Validations are done during the upgrade, and if the upgrade fails, you receive an error message.</span></span> <span data-ttu-id="575df-124">Jaunināšana var neizdoties, jo pastāv šādi konflikti:</span><span class="sxs-lookup"><span data-stu-id="575df-124">An upgrade might fail because of the following conflicts:</span></span>

- <span data-ttu-id="575df-125">Pastāv kopuma darbību brīvā teksta dublikāts.</span><span class="sxs-lookup"><span data-stu-id="575df-125">Duplicate wave step free texts exist.</span></span>
- <span data-ttu-id="575df-126">Pastāv pielāgojumi.</span><span class="sxs-lookup"><span data-stu-id="575df-126">Customizations exist.</span></span>
- <span data-ttu-id="575df-127">Kopuma darbību brīvais teksts, kas ir saistīts ar metodes instanci, neatbilst paredzētajam veidnes tipam.</span><span class="sxs-lookup"><span data-stu-id="575df-127">A wave step free text that is associated with a wave step method instance doesn't match the expected template type.</span></span>

<span data-ttu-id="575df-128">Pēc tam, kad esat atrisinājis konfliktus, kas ir identificēti pārbaudes laikā, varat palaist jaunināšanas procesu.</span><span class="sxs-lookup"><span data-stu-id="575df-128">After you've resolved any conflicts that are identified during the validations, you can rerun the upgrade process.</span></span>

<span data-ttu-id="575df-129">Kad jaunināšana ir sekmīga, **Kopuma darbību kodu** lapa (**Noliktavas pārvaldība\>Iestatīšana \>Kopumi \>Kopuma darbību kodi**) kļūst pieejama.</span><span class="sxs-lookup"><span data-stu-id="575df-129">When the upgrade succeeds, the **Wave step codes** page (**Warehouse management \> Setup \> Waves \> Wave step codes**) becomes available.</span></span> <span data-ttu-id="575df-130">Šajā lapā ir uzskaitīti kopuma darbību kodi, kas tika atjaunināti, kad kopuma darbību kodu līdzeklis tika ieslēgts.</span><span class="sxs-lookup"><span data-stu-id="575df-130">This page lists the wave step codes that were upgraded when the wave step codes feature was turned on.</span></span>

### <a name="create-new-wave-step-codes"></a><span data-ttu-id="575df-131">Izveidot jauna kopuma darbību kodus</span><span class="sxs-lookup"><span data-stu-id="575df-131">Create new wave step codes</span></span>

<span data-ttu-id="575df-132">Varat izmantot lapu **Kopuma darbību kodi**, lai izveidotu un dzēstu kopuma darbību kodus.</span><span class="sxs-lookup"><span data-stu-id="575df-132">You can use the **Wave step codes** page to create and delete wave step codes.</span></span>

<span data-ttu-id="575df-133">Katram jaunam kopuma darbību kodam un ar to saistītajam ID ir jābūt unikālam visos kopuma darbību tipos, un tie ir jādefinē konkrētam kopuma darbību tipam.</span><span class="sxs-lookup"><span data-stu-id="575df-133">Every new wave step code and its associated ID must be unique across all wave step types, and they must be defined for a specific wave step type.</span></span>

### <a name="apply-wave-step-codes"></a><span data-ttu-id="575df-134">Pielietot kopuma darbību kodus</span><span class="sxs-lookup"><span data-stu-id="575df-134">Apply wave step codes</span></span>

<span data-ttu-id="575df-135">Pēc tam, kad esat definējis piemērotus kopuma darbību kodus, tos var lietot kopuma procesa metodēm.</span><span class="sxs-lookup"><span data-stu-id="575df-135">After you've defined the appropriate wave step codes, they can be applied to the wave process methods.</span></span>

<span data-ttu-id="575df-136">Lai pielietotu kopuma darbību kodus, dodieties uz atbilstošo mērķa veidni.</span><span class="sxs-lookup"><span data-stu-id="575df-136">To apply wave step codes, go to the appropriate target template.</span></span> <span data-ttu-id="575df-137">Šeit ir mērķa veidnes, kam kopuma darbību kodi ir izveidoti, lai norādītu uz:</span><span class="sxs-lookup"><span data-stu-id="575df-137">Here are the target templates that the wave step codes are designated to point to:</span></span>

- <span data-ttu-id="575df-138">**Papildināšanas veidnes.:** Noliktavas pārvaldība \> Iestatīšana \> Papildināšana \> Papildināšanas veidnes</span><span class="sxs-lookup"><span data-stu-id="575df-138">**Replenishment templates:** Warehouse management \> Setup \> Replenishment \> Replenishment templates</span></span>
- <span data-ttu-id="575df-139">**Noslodzes būvējuma veidnes:** Noliktavas pārvaldība \>Iestatīšana \>noslodzes kompilācijas veidnes \> </span><span class="sxs-lookup"><span data-stu-id="575df-139">**Load build templates:** Warehouse management \> Setup \> Load \> Load build templates</span></span>
- <span data-ttu-id="575df-140">**Kārtot veidnes:** Noliktavas pārvaldība \>Iestatīšana \>Iepakošana \>Nosūtīšanas kārtošanas veidnes</span><span class="sxs-lookup"><span data-stu-id="575df-140">**Sort templates:** Warehouse management \> Setup \> Packing \> Outbound sorting templates</span></span>
- <span data-ttu-id="575df-141">**Konteinerizēšanas veidnes:** Noliktavas pārvaldība \> Iestatīšana \> Konteineri \> Konteineru būvējuma veidnes</span><span class="sxs-lookup"><span data-stu-id="575df-141">**Containerization templates:** Warehouse management \> Setup \> Containers \> Container build templates</span></span>
- <span data-ttu-id="575df-142">**Etiķešu drukāšanas veidnes:** Noliktavas pārvaldība \>Uzstādīšana \>Dokumenta maršrutēšana \>Kopuma etiķešu veidnes</span><span class="sxs-lookup"><span data-stu-id="575df-142">**Label printing templates:** Warehouse management \> Setup \> Document routing \> Wave label templates</span></span>

<span data-ttu-id="575df-143">Šajā sarakstā iekļautās veidnes tiek piemērotas, kad tās ir norādītas no kopuma procesa metodes, kas ir atlasītas kopuma veidnēs.</span><span class="sxs-lookup"><span data-stu-id="575df-143">The templates in this list are applied when they are referenced from a wave process method that is selected in a wave template.</span></span> <span data-ttu-id="575df-144">Kad kopuma darbību kods procesa metodē kopuma veidnē atbilst tā darbību kodam vienā no veidņu tipiem, tiek lietota veidne.</span><span class="sxs-lookup"><span data-stu-id="575df-144">When the wave step code on a wave process method in a wave template matches the wave step code in one of the templates types, the template is applied.</span></span>

### <a name="sample-scenario"></a><span data-ttu-id="575df-145">Piemēra situācija</span><span class="sxs-lookup"><span data-stu-id="575df-145">Sample scenario</span></span>

<span data-ttu-id="575df-146">Šī procedūra palīdz garantēt, ka izveidotā papildināšanas veidne tiks lietota kopuma veidnei.</span><span class="sxs-lookup"><span data-stu-id="575df-146">The following procedure helps guarantee that the replenishment template that you created will be applied for the wave template.</span></span>

1. <span data-ttu-id="575df-147">Dodieties uz **Noliktavas pārvaldība \>Iestatīšana \>Kopumi \>Kopuma darbību kodi** un izveidojiet kopuma darbību kodu **Papildināšanas** tipam.</span><span class="sxs-lookup"><span data-stu-id="575df-147">Go to **Warehouse management \> Setup \> Waves \> Wave step codes**, and create a wave step code for the **Replenishment** type.</span></span>
2. <span data-ttu-id="575df-148">Dodieties uz **Noliktavu pārvaldība\> Iestatīšana \> Papildināšana \> Papildināšanas veidnes** un izveidojiet papildināšanas veidni.</span><span class="sxs-lookup"><span data-stu-id="575df-148">Go to **Warehouse management \> Setup \> Replenishment \> Replenishment templates**, and create a replenishment template.</span></span>
3. <span data-ttu-id="575df-149">Papildināšanas veidnē atlasiet kopuma darbības kodu, ko izveidojāt **Papildināšanas** tipam.</span><span class="sxs-lookup"><span data-stu-id="575df-149">In the replenishment template, select the wave step code that you created for the **Replenishment** type.</span></span>
4. <span data-ttu-id="575df-150">Dodieties uz **Noliktavas pārvaldība \> Iestatīšana \>Kopumi \>Kopuma veidnes** un atlasiet kopuma veidni, ko plānojat izmantot.</span><span class="sxs-lookup"><span data-stu-id="575df-150">Go to **Warehouse management \> Setup \> Waves \> Wave templates**, and select the wave template that you intend to use.</span></span>
5. <span data-ttu-id="575df-151">Veidnē kopsavilkuma cilnē **Metodes** atlasiet **Papildināšanas** metodi.</span><span class="sxs-lookup"><span data-stu-id="575df-151">In the template, on the **Methods** FastTab, select the **Replenishment** method.</span></span>
6. <span data-ttu-id="575df-152">Laukā **Kopuma darbības kodi** atlasiet kopuma darbības kodu, ko izvēlējāties papildināšanas veidnē.</span><span class="sxs-lookup"><span data-stu-id="575df-152">In the **Wave step code** field, select the wave step code that you selected in the replenishment template.</span></span>

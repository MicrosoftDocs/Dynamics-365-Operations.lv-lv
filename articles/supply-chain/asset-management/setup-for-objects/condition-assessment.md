---
title: Nosacījumu novērtējums
description: Šajā tēmā ir paskaidrots, kā izveidot nosacījuma novērtējuma veidni un reģistrēt līdzekli Līdzekļu pārvaldībā.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetObjectCondition, EntAssetConditionTemplate
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 082a2bfd8818e511095e9ab2dcc22de59eb98d31
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808428"
---
# <a name="condition-assessment"></a><span data-ttu-id="0af2d-103">Nosacījumu novērtējums</span><span class="sxs-lookup"><span data-stu-id="0af2d-103">Condition assessment</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="0af2d-104">Šajā tēmā ir paskaidrots, kā izveidot nosacījuma novērtējuma veidni un reģistrēt līdzekli Līdzekļu pārvaldībā.</span><span class="sxs-lookup"><span data-stu-id="0af2d-104">This topic explains how to create a condition assessment template and registration on an asset in Asset Management.</span></span> <span data-ttu-id="0af2d-105">Nosacījumu novērtējumu veic regulāri, un primārais mērķis ir izveidot un uzturēt nosacījumu datus par līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="0af2d-105">Condition assessment is performed at regular intervals, and the primary objective is to create and maintain condition data on assets.</span></span> <span data-ttu-id="0af2d-106">Raugoties no profilaktiskās uzturēšanas perspektīvas, ir svarīgi pārraudzīt svarīgāko informāciju, piemēram, pašreizējo stāvokli un atlikušo mūža ilgumu.</span><span class="sxs-lookup"><span data-stu-id="0af2d-106">Seen from a preventive maintenance perspective, it is important to monitor key information such as current condition, and remaining life span.</span></span> <span data-ttu-id="0af2d-107">Turklāt, ja regulāri veicat nosacījumu novērtējumu, jūs varēsit pārraudzīt un salīdzināt iekārtu nosacījumus jūsu rūpnīcā.</span><span class="sxs-lookup"><span data-stu-id="0af2d-107">Furthermore, if you carry out condition assessment at regular intervals, you will be able to monitor and compare conditions on the machinery in your factory.</span></span>

<span data-ttu-id="0af2d-108">Nosacījumu novērtējumu var izmantot, lai izmērītu un uzraudzītu daudzus jūsu iekārtu nosacījumus.</span><span class="sxs-lookup"><span data-stu-id="0af2d-108">Condition assessment can be used to measure and monitor many conditions on your equipment.</span></span> <span data-ttu-id="0af2d-109">Piemērs: jūs varētu mērīt jūsu mašīnu vibrācijas.</span><span class="sxs-lookup"><span data-stu-id="0af2d-109">Example: You could measure vibrations on your machinery.</span></span> <span data-ttu-id="0af2d-110">Kad esat reģistrējis vibrācijas mērījumus Līdzekļu pārvaldībā par dažādu veidu iekārtām, varat meklēt jaunāko reģistrēto novērtējumu un skatīt vibrācijas mērījumus.</span><span class="sxs-lookup"><span data-stu-id="0af2d-110">After you have registered vibration measurements in Asset Management on various types of equipment, you can search for the latest registered assessment and view vibration measurements.</span></span>

<span data-ttu-id="0af2d-111">Nosacījumu novērtējums tiek veidots par līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="0af2d-111">Condition assessment is created on assets.</span></span> <span data-ttu-id="0af2d-112">Pirms veicat nosacījumu novērtēšanas procedūru, ir jāiestata nosacījumu novērtējuma veidne līdzekļa veidam.</span><span class="sxs-lookup"><span data-stu-id="0af2d-112">You set up a condition assessment template on an asset type before you carry out the condition assessment procedure.</span></span> <span data-ttu-id="0af2d-113">Veidņu izmantošanas nosacījumu novērtēšanai iemesls ir novērst izvairīties no nosacījumu datu variantiem par līdzīgiem līdzekļiem.</span><span class="sxs-lookup"><span data-stu-id="0af2d-113">The reason for using templates for condition assessment is to avoid variation of condition data on similar assets.</span></span> <span data-ttu-id="0af2d-114">Nosacījumu novērtējuma iestatīšanas un izmantošanas secība Līdzekļu pārvaldībā ir: vispirms iestatiet nepieciešamās nosacījumu novērtēšanas veidnes.</span><span class="sxs-lookup"><span data-stu-id="0af2d-114">The sequence for setting up and using condition assessment in Asset Management is: First you set up the required condition assessment templates.</span></span> <span data-ttu-id="0af2d-115">Pēc tam saistiet veidnes ar līdzekļu veidiem veidlapā **Līdzekļu veidi**.</span><span class="sxs-lookup"><span data-stu-id="0af2d-115">Next, you associate templates with asset types in the **Asset types** form.</span></span> <span data-ttu-id="0af2d-116">Visbeidzot varat izveidot nosacījumu novērtēšanas reģistrācijas par līdzekli veidlapā **Līdzeklis**.</span><span class="sxs-lookup"><span data-stu-id="0af2d-116">Finally, you can create condition assessment registrations on an asset in the **Asset** form.</span></span>

## <a name="create-a-condition-assessment-template"></a><span data-ttu-id="0af2d-117">Nosacījumu novērtējuma veidnes izveide</span><span class="sxs-lookup"><span data-stu-id="0af2d-117">Create a condition assessment template</span></span>

1. <span data-ttu-id="0af2d-118">Atlasiet **Līdzekļu pārvaldība** > **Iestatīšana** > **Līdzekļu veidi** > **Nosacījumu novērtējums**.</span><span class="sxs-lookup"><span data-stu-id="0af2d-118">Select **Asset management** > **Setup** > **Asset types** > **Condition assessment**.</span></span>
2. <span data-ttu-id="0af2d-119">Atlasiet **Jauns**, lai izveidotu jaunu veidni.</span><span class="sxs-lookup"><span data-stu-id="0af2d-119">Select **New** to create a new template.</span></span>
3. <span data-ttu-id="0af2d-120">Laukā **Veidne** ievadiet veidnes ID.</span><span class="sxs-lookup"><span data-stu-id="0af2d-120">Insert and ID for the template in the **Template** field.</span></span>
4. <span data-ttu-id="0af2d-121">Laukā **Nosaukums** ievadiet veidnes nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="0af2d-121">Insert a name for the template in the **Name** field.</span></span>
5. <span data-ttu-id="0af2d-122">Kopsavilkuma cilnē **Nosacījumu novērtējuma rindas** pievienojiet nosacījumu novērtējumam nepieciešamās rindas, tostarp atbilstošā nosacījumu veida un mērvienību atlasi.</span><span class="sxs-lookup"><span data-stu-id="0af2d-122">On the **Condition assessment lines** FastFab, add the lines required for the condition assessment, including selection of the appropriate condition type and measurement unit.</span></span>
6. <span data-ttu-id="0af2d-123">Kopsavilkuma cilnē **Līdzekļu veidi** pievienojiet līdzekļu veidus, kuriem jāizmanto nosacījumu novērtējuma veidne.</span><span class="sxs-lookup"><span data-stu-id="0af2d-123">On the **Asset types** FastTab, add the asset types that should use the condition assessment template.</span></span>
7. <span data-ttu-id="0af2d-124">Laukos **Rindas** un **Līdzekļu veidi**, kas atrodas grupā ekrāna augšdaļā **Detalizēta informācija**, redzēsit novērtēšanas rindu un līdzekļu veidu skaitu, kas saistīti ar atlasīto nosacījumu novērtējuma veidni.</span><span class="sxs-lookup"><span data-stu-id="0af2d-124">In the **Lines** and **Asset types** fields in the **Details** group at the top of the screen, you will see the number of assessment lines and asset types related to the selected condition assessment template.</span></span>


## <a name="create-condition-assessment-registration-on-an-asset"></a><span data-ttu-id="0af2d-125">Nosacījumu novērtējuma reģistrācijas izveide līdzeklim</span><span class="sxs-lookup"><span data-stu-id="0af2d-125">Create condition assessment registration on an asset</span></span>

1. <span data-ttu-id="0af2d-126">Atlasiet **Līdzekļu pārvaldība** > **Kopīgi** > **Līdzekļi** > **Visi līdzekļi**.</span><span class="sxs-lookup"><span data-stu-id="0af2d-126">Select **Asset management** > **Common** > **Assets** > **All Assets**.</span></span>
2. <span data-ttu-id="0af2d-127">Sarakstā atlasiet līdzekli, kuram vēlaties izveidot nosacījumu novērtējuma reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="0af2d-127">In the list, select the asset for which you want to create a condition assessment registration.</span></span>
3. <span data-ttu-id="0af2d-128">Cilnē **Vispārīgie iestatījumi** noklikšķiniet uz **Nosacījumu novērtējums**.</span><span class="sxs-lookup"><span data-stu-id="0af2d-128">On the **General** tab, click **Condition assessment**.</span></span>
4. <span data-ttu-id="0af2d-129">Noklikšķiniet uz **Jauns**, lai veiktu jaunu reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="0af2d-129">Click **New** to make a new registration.</span></span>
5. <span data-ttu-id="0af2d-130">Laukā **Datums** atlasiet nosacījumu novērtējuma datumu.</span><span class="sxs-lookup"><span data-stu-id="0af2d-130">Select the date for the condition assessment in the **Date** field.</span></span>
6. <span data-ttu-id="0af2d-131">Laukā **Darbinieks** atlasiet tā darbinieka vārdu, kurš veica novērtējuma reģistrāciju.</span><span class="sxs-lookup"><span data-stu-id="0af2d-131">Select the name of the worker who carried out the assessment registration in the **Worker** field.</span></span>
7. <span data-ttu-id="0af2d-132">Laukā **Rindas** ir redzams nosacījumu novērtējumam iestatīto novērtējuma rindu skaitu.</span><span class="sxs-lookup"><span data-stu-id="0af2d-132">In the **Lines** field, you see the number of assessment lines set up on the condition assessment.</span></span>
8. <span data-ttu-id="0af2d-133">Laukā **Veidne** atlasiet nosacījumu novērtējuma veidni.</span><span class="sxs-lookup"><span data-stu-id="0af2d-133">Select a template for the condition assessment in the **Template** field.</span></span> <span data-ttu-id="0af2d-134">Veidnes nosaukums tiek automātiski ievietots laukā **Nosaukums**, un saistītās reģistrācijas rindas tiek ievietotas kopsavilkuma cilnē **Nosacījumu novērtējuma rindas**.</span><span class="sxs-lookup"><span data-stu-id="0af2d-134">The name of the template is automatically inserted in the **Name** field, and the related registration lines are inserted on the **Condition assessment lines** FastTab.</span></span>
9. <span data-ttu-id="0af2d-135">Kopsavilkuma cilnē **Piezīmes** var ievietot piezīmes, kas attiecas uz atlasīto nosacījumu novērtējumu.</span><span class="sxs-lookup"><span data-stu-id="0af2d-135">You can insert notes relating to the selected condition assessment on the **Notes** FastTab.</span></span>
10. <span data-ttu-id="0af2d-136">Katrai nosacījumu novērtējuma rindai ievadiet mērījumu datus laukā **Vērtība.**</span><span class="sxs-lookup"><span data-stu-id="0af2d-136">For each condition assessment line, insert measurement data in the **Value** field.</span></span>
11. <span data-ttu-id="0af2d-137">Varat ievietot komentāru, kas attiecas uz atlasīto reģistrācijas rindu kopsavilkuma cilnes **Nosacījumu novērtējuma rindas** laukā > **Komentāri**.</span><span class="sxs-lookup"><span data-stu-id="0af2d-137">You can insert a comment relating to the selected registration line on the **Condition assessment lines** FastTab > **Comments** field.</span></span> <span data-ttu-id="0af2d-138">Ja rindā pievienojat komentāru, automātiski tiek atlasīta izvēles rūtiņa **Komentārs**.</span><span class="sxs-lookup"><span data-stu-id="0af2d-138">If you add a comment on a line, the **Comment** check box is automatically selected.</span></span>

<span data-ttu-id="0af2d-139">Kad esat veicis nosacījumu novērtējuma reģistrēšanu līdzeklim, varat izdrukāt nosacījumu novērtējuma atskaiti.</span><span class="sxs-lookup"><span data-stu-id="0af2d-139">After you have made a condition assessment registration on an asset, you can print a condition assessment report.</span></span>

>[!NOTE]
><span data-ttu-id="0af2d-140">Varat arī reģistrēt nosacījumu novērtējumu darba pasūtījumā (**Līdzekļu pārvaldība** > **Kopīgi** > **Darba pasūtījumi** > **Visi darba pasūtījumi** > **Nosacījumu novērtējuma** poga.)</span><span class="sxs-lookup"><span data-stu-id="0af2d-140">You can also register condition assessment on a work order (**Asset management** > **Common** > **Work orders** > **All Work orders** > **Condition assessment** button.)</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
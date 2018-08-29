--- 
title: "Konfigurāciju pārskatīšana pārskatu ģenerēšanai Office formātā, kurā ir iegultie attēli"
description: "Lai veiktu šīs darbības, vispirms jāveic darbības, kas aprakstītas uzdevuma ceļvedī “ER: veikt pārskatus MS Office formātos ar iegultiem attēliem (1. daļa: iestatīt parametrus)”."
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 8f3462f16ad7638071ab0aa2175d0bc291eeae89
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="90ecb-103">Konfigurāciju pārskatīšana pārskatu ģenerēšanai Office formātā, kurā ir iegultie attēli</span><span class="sxs-lookup"><span data-stu-id="90ecb-103">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="90ecb-104">Lai veiktu šīs darbības, vispirms jāveic darbības, kas aprakstītas uzdevuma ceļvedī “ER: veikt pārskatus MS Office formātos ar iegultiem attēliem (1. daļa: iestatīt parametrus)”.</span><span class="sxs-lookup"><span data-stu-id="90ecb-104">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)” task guide.</span></span>

<span data-ttu-id="90ecb-105">Šajā procedūrā parādīts, kā veidot elektronisko pārskatu (ER) konfigurācijas, lai programmā Microsoft Excel un Microsoft Word ģenerētu elektroniskos dokumentus, kas satur iegultos attēlus.</span><span class="sxs-lookup"><span data-stu-id="90ecb-105">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="90ecb-106">Šajā piemērā jūs pārskatīsit parauga uzņēmuma “Litware, Inc.” ER konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="90ecb-106">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="90ecb-107">Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.</span><span class="sxs-lookup"><span data-stu-id="90ecb-107">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="90ecb-108">Šīs darbības var veikt, izmantojot USMF datu kopu.</span><span class="sxs-lookup"><span data-stu-id="90ecb-108">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="90ecb-109">Pārskatīt importēto datu modeli</span><span class="sxs-lookup"><span data-stu-id="90ecb-109">Review the imported data model</span></span>
1. <span data-ttu-id="90ecb-110">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="90ecb-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="90ecb-111">Koka struktūrā atlasiet “Čeku modelis”.</span><span class="sxs-lookup"><span data-stu-id="90ecb-111">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="90ecb-112">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="90ecb-112">Click Designer.</span></span>
    * <span data-ttu-id="90ecb-113">Šis modelis ir paredzēts, lai parādītu maksājumu čekus no biznesa viedokļa un šī modeļa kartējumu programmas datu avotiem.</span><span class="sxs-lookup"><span data-stu-id="90ecb-113">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application’s data sources.</span></span> <span data-ttu-id="90ecb-114">Pārskatiet šo modeli, izmantojot ER operāciju veidotāju.</span><span class="sxs-lookup"><span data-stu-id="90ecb-114">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="90ecb-115">Ņemiet vērā, ka tiek rādīti šādi modeļa elementu atribūti: struktūra, nosaukums, apraksts, datu tips u.t.t.</span><span class="sxs-lookup"><span data-stu-id="90ecb-115">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="90ecb-116">Kokā izvērsiet elementu “sakne”.</span><span class="sxs-lookup"><span data-stu-id="90ecb-116">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="90ecb-117">Kokā atlasiet 'root\cheques'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-117">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="90ecb-118">Kokā izvērsiet 'root\cheques'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-118">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="90ecb-119">Kokā izvērsiet 'root\cheques\attributes'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-119">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="90ecb-120">Kokā izvērsiet 'root\payer'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-120">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="90ecb-121">Kokā atlasiet 'root\istestrun'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-121">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="90ecb-122">Kokā atlasiet 'root\layout'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-122">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="90ecb-123">Šī modeļa izkārtojuma elements parāda detalizētu informāciju par čeku drukāšanas formas izkārtojumu atlasītajam bankas kontam.</span><span class="sxs-lookup"><span data-stu-id="90ecb-123">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="90ecb-124">Tajā ir iekļauti arī divi mezgli ar datu tipu “Konteiners”, lai glabātu attēlus.</span><span class="sxs-lookup"><span data-stu-id="90ecb-124">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="90ecb-125">Kokā izvērsiet 'root\layout'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-125">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="90ecb-126">Kokā atlasiet 'root\layout\company logo'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-126">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="90ecb-127">Kokā izvērsiet 'root\layout\company logo'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-127">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="90ecb-128">Kokā atlasiet 'root\layout\company logo\image'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-128">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="90ecb-129">Kokā atlasiet 'root\layout\company logo\isprinted'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-129">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="90ecb-130">Kokā atlasiet 'root\layout\signature'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-130">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="90ecb-131">Kokā izvērsiet 'root\layout\signature'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-131">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="90ecb-132">Kokā atlasiet 'root\layout\signature\image'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-132">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="90ecb-133">Kokā atlasiet 'root\layout\signature\isprinted'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-133">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="90ecb-134">Ņemiet vērā, ka divi attēla datu modeļa elementi ir saistīti ar tabulu laukiem, kas satur uzņēmuma logotipa un pilnvarotas personas paraksta attēlus binārā formātā.</span><span class="sxs-lookup"><span data-stu-id="90ecb-134">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person’s signature in binary format.</span></span>  
20. <span data-ttu-id="90ecb-135">Kokā izvērsiet 'root\layout\watermark'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-135">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="90ecb-136">Noklikšķiniet uz Kartēšanas modelis datu avotam.</span><span class="sxs-lookup"><span data-stu-id="90ecb-136">Click Map model to datasource.</span></span>
22. <span data-ttu-id="90ecb-137">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="90ecb-137">Click Designer.</span></span>
23. <span data-ttu-id="90ecb-138">Kokā izvērsiet “chequesselected”.</span><span class="sxs-lookup"><span data-stu-id="90ecb-138">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="90ecb-139">Kokā izvērsiet elementu “izkārtojums”.</span><span class="sxs-lookup"><span data-stu-id="90ecb-139">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="90ecb-140">Kokā izvērsiet 'layout\company logo'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-140">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="90ecb-141">Kokā izvērsiet 'layout\signature'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-141">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="90ecb-142">Kokā izvērsiet 'layout\watermark'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-142">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="90ecb-143">Ieslēdziet opciju “Rādīt detalizēti”.</span><span class="sxs-lookup"><span data-stu-id="90ecb-143">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="90ecb-144">Ņemiet vērā, ka čeku datu modeļa elements ir saistīts ar tabulu TmpChequePrintout, kura izpildlaikā saturēs čeku ierakstus, kurus lietotājs ir atlasījis drukāšanai.</span><span class="sxs-lookup"><span data-stu-id="90ecb-144">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="90ecb-145">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="90ecb-145">Close the page.</span></span>
30. <span data-ttu-id="90ecb-146">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="90ecb-146">Close the page.</span></span>
31. <span data-ttu-id="90ecb-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="90ecb-147">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="90ecb-148">Pārskatīt importēto formātu</span><span class="sxs-lookup"><span data-stu-id="90ecb-148">Review the imported format</span></span>
1. <span data-ttu-id="90ecb-149">Koka struktūrā izvērsiet “Čeku modelis”.</span><span class="sxs-lookup"><span data-stu-id="90ecb-149">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="90ecb-150">Kokā atlasiet 'Model for cheques\Cheques printing format'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-150">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="90ecb-151">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="90ecb-151">Click Designer.</span></span>
4. <span data-ttu-id="90ecb-152">Noklikšķiniet uz Pielikumi.</span><span class="sxs-lookup"><span data-stu-id="90ecb-152">Click Attachments.</span></span>
5. <span data-ttu-id="90ecb-153">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="90ecb-153">Click Open.</span></span>
    * <span data-ttu-id="90ecb-154">Atveriet pievienoto pārskata veidni programmā Excel.</span><span class="sxs-lookup"><span data-stu-id="90ecb-154">Open the attached report’s template in Excel.</span></span>  
    * <span data-ttu-id="90ecb-155">Pārskatiet pievienoto pārskata Excel veidni, kas tiks izmantota, lai drukātu čekus.</span><span class="sxs-lookup"><span data-stu-id="90ecb-155">Review the attached report’s Excel template that will be used to print cheques.</span></span> <span data-ttu-id="90ecb-156">Veidne satur divus čekus katrā lapā un ir paredzēta, lai izdrukātu čekus iepriekš izdrukātā veidlapā.</span><span class="sxs-lookup"><span data-stu-id="90ecb-156">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="90ecb-157">Ņemiet vērā, ka ir iegulti divi tukši attēli.</span><span class="sxs-lookup"><span data-stu-id="90ecb-157">Note that two blank images are embedded.</span></span> <span data-ttu-id="90ecb-158">Šie tukšie attēli ir paredzēti uzņēmuma logotipam un tās personas parakstam, kas pilnvaro maksājumu.</span><span class="sxs-lookup"><span data-stu-id="90ecb-158">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="90ecb-159">Pārbaudiet, vai attēlu nosaukumi programmā Excel ir attiecīgi CompLogo un SignatureImage.</span><span class="sxs-lookup"><span data-stu-id="90ecb-159">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="90ecb-160">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="90ecb-160">Close the page.</span></span>
7. <span data-ttu-id="90ecb-161">Kokā izvērsiet “Pārskats”.</span><span class="sxs-lookup"><span data-stu-id="90ecb-161">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="90ecb-162">Kokā izversiet 'Report\ChequeLines'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-162">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="90ecb-163">Kokā izvērsiet 'Report\ChequeLines\CompLogo'.</span><span class="sxs-lookup"><span data-stu-id="90ecb-163">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="90ecb-164">Ieslēdziet opciju “Rādīt detalizēti”.</span><span class="sxs-lookup"><span data-stu-id="90ecb-164">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="90ecb-165">Ņemiet vērā, ka “CompLogo” formāta šūnas elements ir Excel vienums, kas tiek izmantots, lai aizpildītu uzņēmuma logotipa attēlu pārskatā.</span><span class="sxs-lookup"><span data-stu-id="90ecb-165">Note that the ‘CompLogo’ format’s cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="90ecb-166">Šis formāta elements ir saistīts ar attēlu datu modeļa elementu, kas izpildlaikā satur uzņēmuma logotipa attēlu binārā formātā.</span><span class="sxs-lookup"><span data-stu-id="90ecb-166">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="90ecb-167">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="90ecb-167">Click the Mapping tab.</span></span>
12. <span data-ttu-id="90ecb-168">Noklikšķiniet uz Rediģēšana iespējota.</span><span class="sxs-lookup"><span data-stu-id="90ecb-168">Click Edit enabled.</span></span>
    * <span data-ttu-id="90ecb-169">Ņemiet vērā, ka varat pārveidot 'CompLogo' formāta šūnas elementu, lai tas vairs nebūtu aktivizēts.</span><span class="sxs-lookup"><span data-stu-id="90ecb-169">Note that you can make the ‘CompLogo’ format’s cell element so that it’s no longer enabled.</span></span> <span data-ttu-id="90ecb-170">Tādā gadījumā saistītais Excel attēla elements paslēps uzņēmuma logotipu ģenerētajā pārskatā.</span><span class="sxs-lookup"><span data-stu-id="90ecb-170">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="90ecb-171">Ja aktivizētā izteiksme atgriež vērtību TRUE un definētā saistība neparāda attēlu, saistītais Excel attēla elements rāda attēlu, kas ir saglabāts Excel veidnē.</span><span class="sxs-lookup"><span data-stu-id="90ecb-171">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="90ecb-172">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="90ecb-172">Close the page.</span></span>
14. <span data-ttu-id="90ecb-173">Kokā izvērsiet “etiķetes: Konteiners”.</span><span class="sxs-lookup"><span data-stu-id="90ecb-173">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="90ecb-174">Dažas etiķetes, kas ir redzamas iepriekš izdrukātā čeka veidlapā, tiks iekļautas pārskatā, veidojot to testēšanas nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="90ecb-174">Some labels that are presented in the preprinted cheque form will be included in the report when it’s created for testing purposes.</span></span> <span data-ttu-id="90ecb-175">Tomēr šīs etiķetes netiks drukātas īstās drukāšanas laikā, jo tās jau ir ietvertas iepriekš izdrukātajā veidlapā.</span><span class="sxs-lookup"><span data-stu-id="90ecb-175">However, those labels won’t be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="90ecb-176">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="90ecb-176">Close the page.</span></span>



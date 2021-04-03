---
title: Konfigurāciju pārskatīšana pārskatu ģenerēšanai Office formātā, kurā ir iegultie attēli
description: Šajā procedūrā ir parādīts, kā noformēt elektroniskās atskaišu veidošanas (ER) konfigurācijas, kas satur iegultus attēlus. (1. daļa - parametru iestatīšana).
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6aa5c4d45f9139c65f3aaf1ae392829e3e4967df
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569441"
---
# <a name="review-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="17c34-104">Konfigurāciju pārskatīšana pārskatu ģenerēšanai Office formātā, kurā ir iegultie attēli</span><span class="sxs-lookup"><span data-stu-id="17c34-104">Review configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="17c34-105">Lai veiktu šīs darbības, vispirms jāveic darbības, kas aprakstītas uzdevuma ceļvedī "ER: veikt pārskatus MS Office formātos ar iegultiem attēliem (1. daļa: iestatīt parametrus)".</span><span class="sxs-lookup"><span data-stu-id="17c34-105">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 1: Set up parameters)" task guide.</span></span>

<span data-ttu-id="17c34-106">Šīs procedūras aprakstā ir paskaidrots, kā izstrādāt elektronisko pārskatu izveides (Electronic reporting — ER) konfigurācijas, lai ģenerētu iegultus attēlus saturošus elektroniskos dokumentus programmās Microsoft Excel un Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="17c34-106">This procedure shows how to design Electronic reporting (ER) configurations to generate electronic documents that contain embedded images in Microsoft Excel and Microsoft Word.</span></span> <span data-ttu-id="17c34-107">Šajā piemērā jūs pārskatīsit parauga uzņēmuma “Litware, Inc.” ER konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="17c34-107">In this example, you will review ER configurations for the sample company Litware, Inc.</span></span> 

<span data-ttu-id="17c34-108">Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.</span><span class="sxs-lookup"><span data-stu-id="17c34-108">This procedure is intended for users who have the System administrator or Electronic reporting developer role assigned to them.</span></span> <span data-ttu-id="17c34-109">Šīs darbības var veikt, izmantojot USMF datu kopu.</span><span class="sxs-lookup"><span data-stu-id="17c34-109">The steps can be completed by using the USMF data set.</span></span>


## <a name="review-the-imported-data-model"></a><span data-ttu-id="17c34-110">Pārskatīt importēto datu modeli</span><span class="sxs-lookup"><span data-stu-id="17c34-110">Review the imported data model</span></span>
1. <span data-ttu-id="17c34-111">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="17c34-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="17c34-112">Koka struktūrā atlasiet “Čeku modelis”.</span><span class="sxs-lookup"><span data-stu-id="17c34-112">In the tree, select 'Model for cheques'.</span></span>
3. <span data-ttu-id="17c34-113">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="17c34-113">Click Designer.</span></span>
    * <span data-ttu-id="17c34-114">Šis modelis ir paredzēts, lai parādītu maksājumu čekus no biznesa viedokļa un šī modeļa kartējumu programmas datu avotiem.</span><span class="sxs-lookup"><span data-stu-id="17c34-114">This model is designed to represent payment cheques from the business standpoint and the mapping of this model to the application's data sources.</span></span> <span data-ttu-id="17c34-115">Pārskatiet šo modeli, izmantojot ER operāciju veidotāju.</span><span class="sxs-lookup"><span data-stu-id="17c34-115">Review this model by the ER Operations designer.</span></span> <span data-ttu-id="17c34-116">Ņemiet vērā, ka tiek rādīti šādi modeļa elementu atribūti: struktūra, nosaukums, apraksts, datu tips u.t.t.</span><span class="sxs-lookup"><span data-stu-id="17c34-116">Note the attributes of the model elements that are presented: structure, name, description, data type, and so on.</span></span>   
4. <span data-ttu-id="17c34-117">Kokā izvērsiet elementu “sakne”.</span><span class="sxs-lookup"><span data-stu-id="17c34-117">In the tree, expand 'root'.</span></span>
5. <span data-ttu-id="17c34-118">Kokā atlasiet 'root\cheques'.</span><span class="sxs-lookup"><span data-stu-id="17c34-118">In the tree, select 'root\cheques'.</span></span>
6. <span data-ttu-id="17c34-119">Kokā izvērsiet 'root\cheques'.</span><span class="sxs-lookup"><span data-stu-id="17c34-119">In the tree, expand 'root\cheques'.</span></span>
7. <span data-ttu-id="17c34-120">Kokā izvērsiet 'root\cheques\attributes'.</span><span class="sxs-lookup"><span data-stu-id="17c34-120">In the tree, expand 'root\cheques\attributes'.</span></span>
8. <span data-ttu-id="17c34-121">Kokā izvērsiet 'root\payer'.</span><span class="sxs-lookup"><span data-stu-id="17c34-121">In the tree, expand 'root\payer'.</span></span>
9. <span data-ttu-id="17c34-122">Kokā atlasiet 'root\istestrun'.</span><span class="sxs-lookup"><span data-stu-id="17c34-122">In the tree, select 'root\istestrun'.</span></span>
10. <span data-ttu-id="17c34-123">Kokā atlasiet 'root\layout'.</span><span class="sxs-lookup"><span data-stu-id="17c34-123">In the tree, select 'root\layout'.</span></span>
    * <span data-ttu-id="17c34-124">Šī modeļa izkārtojuma elements parāda detalizētu informāciju par čeku drukāšanas formas izkārtojumu atlasītajam bankas kontam.</span><span class="sxs-lookup"><span data-stu-id="17c34-124">The layout element of this model represents the details of the printing cheque form layout for the selected bank account.</span></span> <span data-ttu-id="17c34-125">Tajā ir iekļauti arī divi mezgli ar datu tipu “Konteiners”, lai glabātu attēlus.</span><span class="sxs-lookup"><span data-stu-id="17c34-125">It also includes two nodes of the Container data type to store images.</span></span>   
11. <span data-ttu-id="17c34-126">Kokā izvērsiet 'root\layout'.</span><span class="sxs-lookup"><span data-stu-id="17c34-126">In the tree, expand 'root\layout'.</span></span>
12. <span data-ttu-id="17c34-127">Kokā atlasiet 'root\layout\company logo'.</span><span class="sxs-lookup"><span data-stu-id="17c34-127">In the tree, select 'root\layout\company logo'.</span></span>
13. <span data-ttu-id="17c34-128">Kokā izvērsiet 'root\layout\company logo'.</span><span class="sxs-lookup"><span data-stu-id="17c34-128">In the tree, expand 'root\layout\company logo'.</span></span>
14. <span data-ttu-id="17c34-129">Kokā atlasiet 'root\layout\company logo\image'.</span><span class="sxs-lookup"><span data-stu-id="17c34-129">In the tree, select 'root\layout\company logo\image'.</span></span>
15. <span data-ttu-id="17c34-130">Kokā atlasiet 'root\layout\company logo\isprinted'.</span><span class="sxs-lookup"><span data-stu-id="17c34-130">In the tree, select 'root\layout\company logo\isprinted'.</span></span>
16. <span data-ttu-id="17c34-131">Kokā atlasiet 'root\layout\signature'.</span><span class="sxs-lookup"><span data-stu-id="17c34-131">In the tree, select 'root\layout\signature'.</span></span>
17. <span data-ttu-id="17c34-132">Kokā izvērsiet 'root\layout\signature'.</span><span class="sxs-lookup"><span data-stu-id="17c34-132">In the tree, expand 'root\layout\signature'.</span></span>
18. <span data-ttu-id="17c34-133">Kokā atlasiet 'root\layout\signature\image'.</span><span class="sxs-lookup"><span data-stu-id="17c34-133">In the tree, select 'root\layout\signature\image'.</span></span>
19. <span data-ttu-id="17c34-134">Kokā atlasiet 'root\layout\signature\isprinted'.</span><span class="sxs-lookup"><span data-stu-id="17c34-134">In the tree, select 'root\layout\signature\isprinted'.</span></span>
    * <span data-ttu-id="17c34-135">Ņemiet vērā, ka divi attēla datu modeļa elementi ir saistīti ar tabulu laukiem, kas satur uzņēmuma logotipa un pilnvarotas personas paraksta attēlus binārā formātā.</span><span class="sxs-lookup"><span data-stu-id="17c34-135">Note that two image data model elements are bound to the fields of the tables that contain images of the company logo and the authorized person's signature in binary format.</span></span>  
20. <span data-ttu-id="17c34-136">Kokā izvērsiet 'root\layout\watermark'.</span><span class="sxs-lookup"><span data-stu-id="17c34-136">In the tree, expand 'root\layout\watermark'.</span></span>
21. <span data-ttu-id="17c34-137">Noklikšķiniet uz Kartēšanas modelis datu avotam.</span><span class="sxs-lookup"><span data-stu-id="17c34-137">Click Map model to datasource.</span></span>
22. <span data-ttu-id="17c34-138">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="17c34-138">Click Designer.</span></span>
23. <span data-ttu-id="17c34-139">Kokā izvērsiet “chequesselected”.</span><span class="sxs-lookup"><span data-stu-id="17c34-139">In the tree, expand 'chequesselected'.</span></span>
24. <span data-ttu-id="17c34-140">Kokā izvērsiet elementu “izkārtojums”.</span><span class="sxs-lookup"><span data-stu-id="17c34-140">In the tree, expand 'layout'.</span></span>
25. <span data-ttu-id="17c34-141">Kokā izvērsiet 'layout\company logo'.</span><span class="sxs-lookup"><span data-stu-id="17c34-141">In the tree, expand 'layout\company logo'.</span></span>
26. <span data-ttu-id="17c34-142">Kokā izvērsiet 'layout\signature'.</span><span class="sxs-lookup"><span data-stu-id="17c34-142">In the tree, expand 'layout\signature'.</span></span>
27. <span data-ttu-id="17c34-143">Kokā izvērsiet 'layout\watermark'.</span><span class="sxs-lookup"><span data-stu-id="17c34-143">In the tree, expand 'layout\watermark'.</span></span>
28. <span data-ttu-id="17c34-144">Ieslēdziet opciju “Rādīt detalizēti”.</span><span class="sxs-lookup"><span data-stu-id="17c34-144">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="17c34-145">Ņemiet vērā, ka čeku datu modeļa elements ir saistīts ar tabulu TmpChequePrintout, kura izpildlaikā saturēs čeku ierakstus, kurus lietotājs ir atlasījis drukāšanai.</span><span class="sxs-lookup"><span data-stu-id="17c34-145">Note that the cheques data model element is bound to the TmpChequePrintout table that, at runtime, will contain records for cheques that the user has selected for printing.</span></span>   
29. <span data-ttu-id="17c34-146">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="17c34-146">Close the page.</span></span>
30. <span data-ttu-id="17c34-147">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="17c34-147">Close the page.</span></span>
31. <span data-ttu-id="17c34-148">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="17c34-148">Close the page.</span></span>

## <a name="review-the-imported-format"></a><span data-ttu-id="17c34-149">Pārskatīt importēto formātu</span><span class="sxs-lookup"><span data-stu-id="17c34-149">Review the imported format</span></span>
1. <span data-ttu-id="17c34-150">Koka struktūrā izvērsiet “Čeku modelis”.</span><span class="sxs-lookup"><span data-stu-id="17c34-150">In the tree, expand 'Model for cheques'.</span></span>
2. <span data-ttu-id="17c34-151">Kokā atlasiet 'Model for cheques\Cheques printing format'.</span><span class="sxs-lookup"><span data-stu-id="17c34-151">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
3. <span data-ttu-id="17c34-152">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="17c34-152">Click Designer.</span></span>
4. <span data-ttu-id="17c34-153">Noklikšķiniet uz Pielikumi.</span><span class="sxs-lookup"><span data-stu-id="17c34-153">Click Attachments.</span></span>
5. <span data-ttu-id="17c34-154">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="17c34-154">Click Open.</span></span>
    * <span data-ttu-id="17c34-155">Atveriet pievienoto pārskata veidni programmā Excel.</span><span class="sxs-lookup"><span data-stu-id="17c34-155">Open the attached report's template in Excel.</span></span>  
    * <span data-ttu-id="17c34-156">Pārskatiet pievienoto pārskata Excel veidni, kas tiks izmantota, lai drukātu čekus.</span><span class="sxs-lookup"><span data-stu-id="17c34-156">Review the attached report's Excel template that will be used to print cheques.</span></span> <span data-ttu-id="17c34-157">Veidne satur divus čekus katrā lapā un ir paredzēta, lai izdrukātu čekus iepriekš izdrukātā veidlapā.</span><span class="sxs-lookup"><span data-stu-id="17c34-157">The template contains two cheques per page and is designed to print cheques to the preprinted form.</span></span> <span data-ttu-id="17c34-158">Ņemiet vērā, ka ir iegulti divi tukši attēli.</span><span class="sxs-lookup"><span data-stu-id="17c34-158">Note that two blank images are embedded.</span></span> <span data-ttu-id="17c34-159">Šie tukšie attēli ir paredzēti uzņēmuma logotipam un tās personas parakstam, kas pilnvaro maksājumu.</span><span class="sxs-lookup"><span data-stu-id="17c34-159">These blank images are for the company logo and the signature of the person who is authorizing a payment.</span></span> <span data-ttu-id="17c34-160">Pārbaudiet, vai attēlu nosaukumi programmā Excel ir attiecīgi CompLogo un SignatureImage.</span><span class="sxs-lookup"><span data-stu-id="17c34-160">Verify that the images are named CompLogo and SignatureImage, respectively, in Excel.</span></span>   
6. <span data-ttu-id="17c34-161">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="17c34-161">Close the page.</span></span>
7. <span data-ttu-id="17c34-162">Kokā izvērsiet “Pārskats”.</span><span class="sxs-lookup"><span data-stu-id="17c34-162">In the tree, expand 'Report'.</span></span>
8. <span data-ttu-id="17c34-163">Kokā izversiet 'Report\ChequeLines'.</span><span class="sxs-lookup"><span data-stu-id="17c34-163">In the tree, expand 'Report\ChequeLines'.</span></span>
9. <span data-ttu-id="17c34-164">Kokā izvērsiet 'Report\ChequeLines\CompLogo'.</span><span class="sxs-lookup"><span data-stu-id="17c34-164">In the tree, select 'Report\ChequeLines\CompLogo'.</span></span>
10. <span data-ttu-id="17c34-165">Ieslēdziet opciju “Rādīt detalizēti”.</span><span class="sxs-lookup"><span data-stu-id="17c34-165">Toggle 'Show details' on.</span></span>
    * <span data-ttu-id="17c34-166">Ņemiet vērā, ka 'CompLogo' formāta šūnas elements ir Excel vienums, kas tiek izmantots, lai aizpildītu uzņēmuma logotipa attēlu pārskatā.</span><span class="sxs-lookup"><span data-stu-id="17c34-166">Note that the 'CompLogo' format's cell element represents the Excel item that is used to populate the company logo image in the report.</span></span> <span data-ttu-id="17c34-167">Šis formāta elements ir saistīts ar attēlu datu modeļa elementu, kas izpildlaikā satur uzņēmuma logotipa attēlu binārā formātā.</span><span class="sxs-lookup"><span data-stu-id="17c34-167">This format element is bound to the image data model element that, at runtime, contains a company logo image in binary format.</span></span>   
11. <span data-ttu-id="17c34-168">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="17c34-168">Click the Mapping tab.</span></span>
12. <span data-ttu-id="17c34-169">Noklikšķiniet uz Rediģēšana iespējota.</span><span class="sxs-lookup"><span data-stu-id="17c34-169">Click Edit enabled.</span></span>
    * <span data-ttu-id="17c34-170">Ņemiet vērā, ka varat pārveidot 'CompLogo' formāta šūnas elementu, lai tas vairs nebūtu aktivizēts.</span><span class="sxs-lookup"><span data-stu-id="17c34-170">Note that you can make the 'CompLogo' format's cell element so that it's no longer enabled.</span></span> <span data-ttu-id="17c34-171">Tādā gadījumā saistītais Excel attēla elements paslēps uzņēmuma logotipu ģenerētajā pārskatā.</span><span class="sxs-lookup"><span data-stu-id="17c34-171">In this case, the associated Excel image element will hide a company logo in the generated report.</span></span> <span data-ttu-id="17c34-172">Ja aktivizētā izteiksme atgriež vērtību TRUE un definētā saistība neparāda attēlu, saistītais Excel attēla elements rāda attēlu, kas ir saglabāts Excel veidnē.</span><span class="sxs-lookup"><span data-stu-id="17c34-172">If the enabled expression returns TRUE and the defined binding brings no image, the associated Excel image element will show an image that has been saved in the Excel template.</span></span>   
13. <span data-ttu-id="17c34-173">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="17c34-173">Close the page.</span></span>
14. <span data-ttu-id="17c34-174">Kokā izvērsiet “etiķetes: Konteiners”.</span><span class="sxs-lookup"><span data-stu-id="17c34-174">In the tree, expand 'labels: Container'.</span></span>
    * <span data-ttu-id="17c34-175">Dažas etiķetes, kas ir redzamas iepriekš izdrukātā čeka veidlapā, tiks iekļautas pārskatā, veidojot to testēšanas nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="17c34-175">Some labels that are presented in the preprinted cheque form will be included in the report when it's created for testing purposes.</span></span> <span data-ttu-id="17c34-176">Tomēr šīs etiķetes netiks drukātas īstās drukāšanas laikā, jo tās jau ir ietvertas iepriekš izdrukātajā veidlapā.</span><span class="sxs-lookup"><span data-stu-id="17c34-176">However, those labels won't be printed during real printing, because the preprinted form already includes them.</span></span>  
15. <span data-ttu-id="17c34-177">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="17c34-177">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
--- 
title: "Pārskatu ģenerēšana Office formātā, kurā ir iegultie attēli"
description: "Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var izveidot elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas, lai veidotu elektroniskos dokumentus ar iegultiem attēliem MS Office formātos (Excel un Word)."
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
ms.openlocfilehash: 5ef7ec2f8b5b7fdf456ebb71b863e620ae21e6b5
ms.contentlocale: lv-lv
ms.lasthandoff: 08/09/2018

---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="d2a5d-103">Pārskatu ģenerēšana Office formātā, kurā ir iegultie attēli</span><span class="sxs-lookup"><span data-stu-id="d2a5d-103">Generate reports in Office format that have embedded images</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d2a5d-104">Tālāk ir paskaidrots, kā lietotājs ar lomu Sistēmas administrators vai Elektronisko atskaišu izstrādātājs var izveidot elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas, lai veidotu elektroniskos dokumentus ar iegultiem attēliem MS Office formātos (Excel un Word).</span><span class="sxs-lookup"><span data-stu-id="d2a5d-104">The following steps explain how a user playing either ‘System administrator’ or ‘Electronic reporting developer’ role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="d2a5d-105">Šajā piemērā jūs izmantosit parauga uzņēmumam “Litware, Inc.” izveidotās ER konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-105">In this example, you will use created ER configurations for sample company, ‘Litware, Inc.’.</span></span>  <span data-ttu-id="d2a5d-106">Lai veiktu šīs darbības, vispirms jāveic darbības, kas aprakstītas uzdevuma ceļvedī “ER: veikt pārskatus MS Office formātos ar iegultiem attēliem (2. daļa: pārskatīt konfigurācijas)”.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-106">To complete these steps, you must first complete the steps in the “ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)” task guide.</span></span> <span data-ttu-id="d2a5d-107">Šīs darbības var veikt uzņēmumā USMF.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-107">These steps can be performed in ‘USMF’ company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="d2a5d-108">Formāta palaišana ar sākotnējo modeļa kartējumu</span><span class="sxs-lookup"><span data-stu-id="d2a5d-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="d2a5d-109">Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="d2a5d-110">Izmantojiet ātro filtru, lai filtrētu pēc lauka Bankas konts vērtības USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="d2a5d-111">Darbību rūtī noklikšķiniet uz Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="d2a5d-112">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-112">Click Check.</span></span>
5. <span data-ttu-id="d2a5d-113">Noklikšķiniet uz Drukāt paraugu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-113">Click Print test.</span></span>
    * <span data-ttu-id="d2a5d-114">Palaidiet formātu testēšanas nolūkā.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="d2a5d-115">Laukā Maksājumu čeka formāts atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="d2a5d-116">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-116">Click OK.</span></span>
    * <span data-ttu-id="d2a5d-117">Pārskatiet izveidoto izvadi.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-117">Review the created output.</span></span> <span data-ttu-id="d2a5d-118">Ņemiet vērā, ka pārskatā ir iekļauts gan uzņēmuma logotips, gan pilnvarotās personas paraksts.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-118">Note that the company logo is presented in the report as well as the authorized person’s signature.</span></span> <span data-ttu-id="d2a5d-119">Paraksta attēls tiek ņemts no čeka izkārtojuma ieraksta lauka ar datu tipu "Konteiners", kas ir saistīts ar atlasīto bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-119">The signature image is taken from the field of the ‘Container’ data type of the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="d2a5d-120">Izvērsiet sadaļu Kopijas.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="d2a5d-121">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-121">Click Edit.</span></span>
10. <span data-ttu-id="d2a5d-122">Laukā Ūdenszīme ievadiet “Drukāt ūdenszīmi kā Anulēts”.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="d2a5d-123">Mainiet ūdenszīmes izkārtojuma iestatījumu, lai parādītu ūdenszīmes tekstu, ģenerējot dokumentu Excel formas elementā.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="d2a5d-124">Noklikšķiniet uz Drukāt paraugu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-124">Click Print test.</span></span>
12. <span data-ttu-id="d2a5d-125">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-125">Click OK.</span></span>
    * <span data-ttu-id="d2a5d-126">Pārskatiet izveidoto izvadi.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-126">Review the created output.</span></span> <span data-ttu-id="d2a5d-127">Ņemiet vērā, ka ūdenszīme izveidotajā pārskatā tiek rādīta atbilstoši atlasītajai opcijai.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-127">Note that the watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="d2a5d-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-128">Close the page.</span></span>
14. <span data-ttu-id="d2a5d-129">Darbību rūtī noklikšķiniet uz Pārvaldīt maksājumus.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="d2a5d-130">Noklikšķiniet uz Čeki.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-130">Click Checks.</span></span>
16. <span data-ttu-id="d2a5d-131">Noklikšķiniet uz Rādīt filtrus.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-131">Click Show filters.</span></span>
17. <span data-ttu-id="d2a5d-132">Lietojiet šādus filtrus: laukā “Čeka numurs” ievadiet filtra vērtību “381”,“385”,“389”, izmantojot filtra operatoru “ir viens no”.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="d2a5d-133">Sarakstā atzīmējiet visas rindas.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="d2a5d-134">Noklikšķiniet uz Drukāt čeka kopiju.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-134">Click Print check copy.</span></span>
    * <span data-ttu-id="d2a5d-135">Palaidiet formātu, lai atkārtoti drukātu atlasītos čekus.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-135">Run the format to re-print the selected cheques.</span></span>  
    * <span data-ttu-id="d2a5d-136">Pārskatiet izveidoto izvadi.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-136">Review the created output.</span></span> <span data-ttu-id="d2a5d-137">Ņemiet vērā, ka atlasītie čeki ir izdrukāti atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-137">Note that the selected cheques have been re-printed.</span></span> <span data-ttu-id="d2a5d-138">Uzņēmuma logotips un etiķetes netiek drukātas, jo tās jau ir redzamas iepriekš izdrukātajā veidlapā.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="d2a5d-139">Importētā datu modeļa kartējuma modificēšana</span><span class="sxs-lookup"><span data-stu-id="d2a5d-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="d2a5d-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-140">Close the page.</span></span>
2. <span data-ttu-id="d2a5d-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-141">Close the page.</span></span>
3. <span data-ttu-id="d2a5d-142">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="d2a5d-143">Koka struktūrā atlasiet “Čeku modelis”.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="d2a5d-144">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-144">Click Designer.</span></span>
6. <span data-ttu-id="d2a5d-145">Noklikšķiniet uz Kartēšanas modelis datu avotam.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="d2a5d-146">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-146">Click Designer.</span></span>
    * <span data-ttu-id="d2a5d-147">Mēs mainīsim datu modeļa paraksta vienuma saistījumu, lai iegūtu paraksta attēlu no faila, kas pievienots čeku izkārtojuma ierakstam, kurš ir saistīts ar atlasīto bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-147">We will change the binding of the data model’s signature item to get the signature image from the file that has been attached to the cheque layout record which is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="d2a5d-148">Izslēdziet opciju Rādīt detalizēti.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-148">Turn Show details off.</span></span>
9. <span data-ttu-id="d2a5d-149">Kokā izvērsiet elementu “izkārtojums”.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="d2a5d-150">Kokā izvērsiet 'layout\signature'.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="d2a5d-151">Kokā atlasiet 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="d2a5d-152">Kokā izvērsiet sadaļu “chequesaccount”.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="d2a5d-153">Kokā izvērsiet 'chequesaccount\<Relations'.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="d2a5d-154">Kokā izvērsiet 'chequesaccount\<Relations\BankChequeLayout'.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="d2a5d-155">Kokā izvērsiet 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="d2a5d-156">Kokā izvērsiet 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="d2a5d-157">Kokā atlasiet 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="d2a5d-158">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-158">Click Bind.</span></span>
19. <span data-ttu-id="d2a5d-159">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-159">Click Save.</span></span>
20. <span data-ttu-id="d2a5d-160">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-160">Close the page.</span></span>
21. <span data-ttu-id="d2a5d-161">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-161">Close the page.</span></span>
22. <span data-ttu-id="d2a5d-162">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-162">Close the page.</span></span>
23. <span data-ttu-id="d2a5d-163">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="d2a5d-164">Formāta palaišana, izmantojot pielāgoto modeļa kartējumu</span><span class="sxs-lookup"><span data-stu-id="d2a5d-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="d2a5d-165">Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="d2a5d-166">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d2a5d-167">Piemēram, filtrējiet pēc lauka Bankas konts vērtības “USMF OPER”.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="d2a5d-168">Darbību rūtī noklikšķiniet uz Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="d2a5d-169">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-169">Click Check.</span></span>
5. <span data-ttu-id="d2a5d-170">Noklikšķiniet uz Drukāt paraugu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-170">Click Print test.</span></span>
6. <span data-ttu-id="d2a5d-171">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-171">Click OK.</span></span>
    * <span data-ttu-id="d2a5d-172">Pārskatiet izveidoto izvadi.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-172">Review the created output.</span></span> <span data-ttu-id="d2a5d-173">Ņemiet vērā, ka attēls no dokumentu pārvaldības pielikuma tiek izmantots kā pilnvarotas personas paraksts.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-173">Note that the image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="d2a5d-174">Izmantot MS Word dokumentu kā veidni importētajā formātā</span><span class="sxs-lookup"><span data-stu-id="d2a5d-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="d2a5d-175">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-175">Close the page.</span></span>
2. <span data-ttu-id="d2a5d-176">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-176">Close the page.</span></span>
3. <span data-ttu-id="d2a5d-177">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="d2a5d-178">Koka struktūrā izvērsiet “Čeku modelis”.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="d2a5d-179">Kokā atlasiet 'Model for cheques\Cheques printing format'.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="d2a5d-180">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-180">Click Designer.</span></span>
7. <span data-ttu-id="d2a5d-181">Noklikšķiniet uz Pielikumi.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-181">Click Attachments.</span></span>
8. <span data-ttu-id="d2a5d-182">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-182">Click Delete.</span></span>
9. <span data-ttu-id="d2a5d-183">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-183">Click Yes.</span></span>
10. <span data-ttu-id="d2a5d-184">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-184">Click New.</span></span>
11. <span data-ttu-id="d2a5d-185">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-185">Click File.</span></span>
    * <span data-ttu-id="d2a5d-186">Noklikšķiniet uz Pārlūkot un atlasiet iepriekš lejupielādēto failu “Čeku veidne Word.docx”.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-186">Click Browse and select the downloaded in advance ‘Cheque template Word.docx’ file.</span></span>  
12. <span data-ttu-id="d2a5d-187">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-187">Close the page.</span></span>
13. <span data-ttu-id="d2a5d-188">Ievadiet vai atlasiet kādu vērtību laukā Veidne.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="d2a5d-189">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-189">Click Save.</span></span>
15. <span data-ttu-id="d2a5d-190">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-190">Close the page.</span></span>
16. <span data-ttu-id="d2a5d-191">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-191">Click Edit.</span></span>
17. <span data-ttu-id="d2a5d-192">Laukā Palaist melnrakstu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="d2a5d-193">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-193">Close the page.</span></span>
19. <span data-ttu-id="d2a5d-194">Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="d2a5d-195">Izmantojiet ātro filtru, lai filtrētu pēc lauka Bankas konts vērtības USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="d2a5d-196">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-196">Click Check.</span></span>
22. <span data-ttu-id="d2a5d-197">Noklikšķiniet uz Drukāt paraugu.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-197">Click Print test.</span></span>
23. <span data-ttu-id="d2a5d-198">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-198">Click OK.</span></span>
    * <span data-ttu-id="d2a5d-199">Pārskatiet izveidoto izvadi.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-199">Review the created output.</span></span> <span data-ttu-id="d2a5d-200">Ņemiet vērā, ka izvade ir izveidota kā MS Word dokuments ar iegultiem attēliem, kuros redzams uzņēmuma logotips, pilnvarotas personas paraksts un atlasītais ūdenszīmes teksts.</span><span class="sxs-lookup"><span data-stu-id="d2a5d-200">Note that the output has been generated as a MS Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  



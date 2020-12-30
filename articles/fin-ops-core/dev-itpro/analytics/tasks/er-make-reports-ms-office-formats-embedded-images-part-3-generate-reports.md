---
title: Pārskatu ģenerēšana Office formātā, kurā ir iegultie attēli
description: Tālāk ir paskaidrots, kā lietotājs ar lomu 'Sistēmas administrators' vai 'Elektronisko atskaišu izstrādātājs' var izveidot elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas, lai veidotu elektroniskos dokumentus ar iegultiem attēliem MS Office formātos (Excel un Word).
author: NickSelin
manager: AnnBe
ms.date: 06/13/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78dcdbd83dc717104d437662f7f451c9ecb714cf
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684383"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="bab91-103">Pārskatu ģenerēšana Office formātā, kurā ir iegultie attēli</span><span class="sxs-lookup"><span data-stu-id="bab91-103">Generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bab91-104">Tālāk ir paskaidrots, kā lietotājs ar lomu 'Sistēmas administrators' vai 'Elektronisko atskaišu izstrādātājs' var izveidot elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas, lai veidotu elektroniskos dokumentus ar iegultiem attēliem MS Office formātos (Excel un Word).</span><span class="sxs-lookup"><span data-stu-id="bab91-104">The following steps explain how a user playing either 'System administrator' or 'Electronic reporting developer' role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="bab91-105">Šajā piemērā jūs izmantosit parauga uzņēmumam 'Litware, Inc.' izveidotās ER konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="bab91-105">In this example, you will use created ER configurations for sample company, 'Litware, Inc.'.</span></span>  <span data-ttu-id="bab91-106">Lai veiktu šīs darbības, vispirms jāveic darbības, kas aprakstītas uzdevuma ceļvedī "ER: veikt pārskatus MS Office formātos ar iegultiem attēliem (2. daļa: pārskatīt konfigurācijas)".</span><span class="sxs-lookup"><span data-stu-id="bab91-106">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)" task guide.</span></span> <span data-ttu-id="bab91-107">Šīs darbības var veikt uzņēmumā 'USMF'.</span><span class="sxs-lookup"><span data-stu-id="bab91-107">These steps can be performed in 'USMF' company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="bab91-108">Formāta palaišana ar sākotnējo modeļa kartējumu</span><span class="sxs-lookup"><span data-stu-id="bab91-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="bab91-109">Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.</span><span class="sxs-lookup"><span data-stu-id="bab91-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="bab91-110">Izmantojiet ātro filtru, lai filtrētu pēc lauka Bankas konts vērtības USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="bab91-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="bab91-111">Darbību rūtī noklikšķiniet uz Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="bab91-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="bab91-112">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="bab91-112">Click Check.</span></span>
5. <span data-ttu-id="bab91-113">Noklikšķiniet uz Drukāt paraugu.</span><span class="sxs-lookup"><span data-stu-id="bab91-113">Click Print test.</span></span>
    * <span data-ttu-id="bab91-114">Palaidiet formātu testēšanas nolūkā.</span><span class="sxs-lookup"><span data-stu-id="bab91-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="bab91-115">Laukā Maksājumu čeka formāts atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="bab91-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="bab91-116">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="bab91-116">Click OK.</span></span>
    * <span data-ttu-id="bab91-117">Pārskatiet izveidoto izvadi.</span><span class="sxs-lookup"><span data-stu-id="bab91-117">Review the created output.</span></span> <span data-ttu-id="bab91-118">Pārskatā ir iekļauts gan uzņēmuma logotips, gan pilnvarotās personas paraksts.</span><span class="sxs-lookup"><span data-stu-id="bab91-118">The company logo is presented in the report as well as the authorized person's signature.</span></span> <span data-ttu-id="bab91-119">Paraksta attēls tiek ņemts no čeka izkārtojuma ieraksta lauka ar datu tipu “Konteiners”, kas ir saistīts ar atlasīto bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="bab91-119">The signature image is taken from the field of the 'Container' data type of the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="bab91-120">Izvērsiet sadaļu Kopijas.</span><span class="sxs-lookup"><span data-stu-id="bab91-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="bab91-121">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="bab91-121">Click Edit.</span></span>
10. <span data-ttu-id="bab91-122">Laukā Ūdenszīme ievadiet “Drukāt ūdenszīmi kā Anulēts”.</span><span class="sxs-lookup"><span data-stu-id="bab91-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="bab91-123">Mainiet ūdenszīmes izkārtojuma iestatījumu, lai parādītu ūdenszīmes tekstu, ģenerējot dokumentu Excel formas elementā.</span><span class="sxs-lookup"><span data-stu-id="bab91-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="bab91-124">Noklikšķiniet uz Drukāt paraugu.</span><span class="sxs-lookup"><span data-stu-id="bab91-124">Click Print test.</span></span>
12. <span data-ttu-id="bab91-125">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="bab91-125">Click OK.</span></span>
    * <span data-ttu-id="bab91-126">Pārskatiet izveidoto izvadi.</span><span class="sxs-lookup"><span data-stu-id="bab91-126">Review the created output.</span></span> <span data-ttu-id="bab91-127">Ūdenszīme izveidotajā pārskatā tiek rādīta atbilstoši atlasītajai opcijai.</span><span class="sxs-lookup"><span data-stu-id="bab91-127">The watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="bab91-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bab91-128">Close the page.</span></span>
14. <span data-ttu-id="bab91-129">Darbību rūtī noklikšķiniet uz Pārvaldīt maksājumus.</span><span class="sxs-lookup"><span data-stu-id="bab91-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="bab91-130">Noklikšķiniet uz Čeki.</span><span class="sxs-lookup"><span data-stu-id="bab91-130">Click Checks.</span></span>
16. <span data-ttu-id="bab91-131">Noklikšķiniet uz Rādīt filtrus.</span><span class="sxs-lookup"><span data-stu-id="bab91-131">Click Show filters.</span></span>
17. <span data-ttu-id="bab91-132">Lietojiet šādus filtrus: laukā “Čeka numurs” ievadiet filtra vērtību “381”,“385”,“389”, izmantojot filtra operatoru “ir viens no”.</span><span class="sxs-lookup"><span data-stu-id="bab91-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="bab91-133">Sarakstā atzīmējiet visas rindas.</span><span class="sxs-lookup"><span data-stu-id="bab91-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="bab91-134">Noklikšķiniet uz Drukāt čeka kopiju.</span><span class="sxs-lookup"><span data-stu-id="bab91-134">Click Print check copy.</span></span>
    * <span data-ttu-id="bab91-135">Palaidiet formātu, lai atkārtoti drukātu atlasītos čekus.</span><span class="sxs-lookup"><span data-stu-id="bab91-135">Run the format to reprint the selected cheques.</span></span>  
    * <span data-ttu-id="bab91-136">Pārskatiet izveidoto izvadi.</span><span class="sxs-lookup"><span data-stu-id="bab91-136">Review the created output.</span></span> <span data-ttu-id="bab91-137">Atlasītie čeki ir izdrukāti atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="bab91-137">The selected cheques have been reprinted.</span></span> <span data-ttu-id="bab91-138">Uzņēmuma logotips un etiķetes netiek drukātas, jo tās jau ir redzamas iepriekš izdrukātajā veidlapā.</span><span class="sxs-lookup"><span data-stu-id="bab91-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="bab91-139">Importētā datu modeļa kartējuma modificēšana</span><span class="sxs-lookup"><span data-stu-id="bab91-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="bab91-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bab91-140">Close the page.</span></span>
2. <span data-ttu-id="bab91-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bab91-141">Close the page.</span></span>
3. <span data-ttu-id="bab91-142">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="bab91-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="bab91-143">Koka struktūrā atlasiet “Čeku modelis”.</span><span class="sxs-lookup"><span data-stu-id="bab91-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="bab91-144">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="bab91-144">Click Designer.</span></span>
6. <span data-ttu-id="bab91-145">Noklikšķiniet uz Kartēšanas modelis datu avotam.</span><span class="sxs-lookup"><span data-stu-id="bab91-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="bab91-146">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="bab91-146">Click Designer.</span></span>
    * <span data-ttu-id="bab91-147">Mēs mainīsim datu modeļa paraksta vienuma saistījumu, lai iegūtu paraksta attēlu no faila, kas pievienots čeku izkārtojuma ierakstam, kurš ir saistīts ar atlasīto bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="bab91-147">We will change the binding of the data model's signature item to get the signature image from the file that has been attached to the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="bab91-148">Izslēdziet opciju Rādīt detalizēti.</span><span class="sxs-lookup"><span data-stu-id="bab91-148">Turn off Show details.</span></span>
9. <span data-ttu-id="bab91-149">Kokā izvērsiet elementu “izkārtojums”.</span><span class="sxs-lookup"><span data-stu-id="bab91-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="bab91-150">Kokā izvērsiet 'layout\signature'.</span><span class="sxs-lookup"><span data-stu-id="bab91-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="bab91-151">Kokā atlasiet 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span><span class="sxs-lookup"><span data-stu-id="bab91-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="bab91-152">Kokā izvērsiet sadaļu “chequesaccount”.</span><span class="sxs-lookup"><span data-stu-id="bab91-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="bab91-153">Kokā izvērsiet 'chequesaccount\<Relations'.</span><span class="sxs-lookup"><span data-stu-id="bab91-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="bab91-154">Kokā izvērsiet 'chequesaccount\<Relations\BankChequeLayout'.</span><span class="sxs-lookup"><span data-stu-id="bab91-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="bab91-155">Kokā izvērsiet 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span><span class="sxs-lookup"><span data-stu-id="bab91-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="bab91-156">Kokā izvērsiet 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span><span class="sxs-lookup"><span data-stu-id="bab91-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="bab91-157">Kokā atlasiet 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span><span class="sxs-lookup"><span data-stu-id="bab91-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="bab91-158">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="bab91-158">Click Bind.</span></span>
19. <span data-ttu-id="bab91-159">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="bab91-159">Click Save.</span></span>
20. <span data-ttu-id="bab91-160">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bab91-160">Close the page.</span></span>
21. <span data-ttu-id="bab91-161">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bab91-161">Close the page.</span></span>
22. <span data-ttu-id="bab91-162">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bab91-162">Close the page.</span></span>
23. <span data-ttu-id="bab91-163">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bab91-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="bab91-164">Formāta palaišana, izmantojot pielāgoto modeļa kartējumu</span><span class="sxs-lookup"><span data-stu-id="bab91-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="bab91-165">Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.</span><span class="sxs-lookup"><span data-stu-id="bab91-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="bab91-166">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="bab91-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="bab91-167">Piemēram, filtrējiet pēc lauka Bankas konts vērtības “USMF OPER”.</span><span class="sxs-lookup"><span data-stu-id="bab91-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="bab91-168">Darbību rūtī noklikšķiniet uz Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="bab91-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="bab91-169">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="bab91-169">Click Check.</span></span>
5. <span data-ttu-id="bab91-170">Noklikšķiniet uz Drukāt paraugu.</span><span class="sxs-lookup"><span data-stu-id="bab91-170">Click Print test.</span></span>
6. <span data-ttu-id="bab91-171">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="bab91-171">Click OK.</span></span>
    * <span data-ttu-id="bab91-172">Pārskatiet izveidoto izvadi.</span><span class="sxs-lookup"><span data-stu-id="bab91-172">Review the created output.</span></span> <span data-ttu-id="bab91-173">Attēls no dokumentu pārvaldības pielikuma tiek izmantots kā pilnvarotas personas paraksts.</span><span class="sxs-lookup"><span data-stu-id="bab91-173">The image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="bab91-174">Izmantot MS Word dokumentu kā veidni importētajā formātā</span><span class="sxs-lookup"><span data-stu-id="bab91-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="bab91-175">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bab91-175">Close the page.</span></span>
2. <span data-ttu-id="bab91-176">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bab91-176">Close the page.</span></span>
3. <span data-ttu-id="bab91-177">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="bab91-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="bab91-178">Koka struktūrā izvērsiet “Čeku modelis”.</span><span class="sxs-lookup"><span data-stu-id="bab91-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="bab91-179">Kokā atlasiet 'Model for cheques\Cheques printing format'.</span><span class="sxs-lookup"><span data-stu-id="bab91-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="bab91-180">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="bab91-180">Click Designer.</span></span>
7. <span data-ttu-id="bab91-181">Noklikšķiniet uz Pielikumi.</span><span class="sxs-lookup"><span data-stu-id="bab91-181">Click Attachments.</span></span>
8. <span data-ttu-id="bab91-182">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="bab91-182">Click Delete.</span></span>
9. <span data-ttu-id="bab91-183">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="bab91-183">Click Yes.</span></span>
10. <span data-ttu-id="bab91-184">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="bab91-184">Click New.</span></span>
11. <span data-ttu-id="bab91-185">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="bab91-185">Click File.</span></span>
    * <span data-ttu-id="bab91-186">Noklikšķiniet uz Pārlūkot un atlasiet iepriekš lejupielādēto failu 'Čeku veidne Word.docx'.</span><span class="sxs-lookup"><span data-stu-id="bab91-186">Click Browse and select the downloaded in advance 'Cheque template Word.docx' file.</span></span>  
12. <span data-ttu-id="bab91-187">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bab91-187">Close the page.</span></span>
13. <span data-ttu-id="bab91-188">Ievadiet vai atlasiet kādu vērtību laukā Veidne.</span><span class="sxs-lookup"><span data-stu-id="bab91-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="bab91-189">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="bab91-189">Click Save.</span></span>
15. <span data-ttu-id="bab91-190">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bab91-190">Close the page.</span></span>
16. <span data-ttu-id="bab91-191">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="bab91-191">Click Edit.</span></span>
17. <span data-ttu-id="bab91-192">Laukā Palaist melnrakstu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="bab91-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="bab91-193">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="bab91-193">Close the page.</span></span>
19. <span data-ttu-id="bab91-194">Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.</span><span class="sxs-lookup"><span data-stu-id="bab91-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="bab91-195">Izmantojiet ātro filtru, lai filtrētu pēc lauka Bankas konts vērtības USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="bab91-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="bab91-196">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="bab91-196">Click Check.</span></span>
22. <span data-ttu-id="bab91-197">Noklikšķiniet uz Drukāt paraugu.</span><span class="sxs-lookup"><span data-stu-id="bab91-197">Click Print test.</span></span>
23. <span data-ttu-id="bab91-198">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="bab91-198">Click OK.</span></span>
    * <span data-ttu-id="bab91-199">Pārskatiet izveidoto izvadi.</span><span class="sxs-lookup"><span data-stu-id="bab91-199">Review the created output.</span></span> <span data-ttu-id="bab91-200">Izvade ir izveidota kā Word dokuments ar iegultiem attēliem, kuros redzams uzņēmuma logotips, pilnvarotas personas paraksts un atlasītais ūdenszīmes teksts.</span><span class="sxs-lookup"><span data-stu-id="bab91-200">The output has been generated as a Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  


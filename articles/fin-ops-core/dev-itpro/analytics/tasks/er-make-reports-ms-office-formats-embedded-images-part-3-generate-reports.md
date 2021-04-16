---
title: Pārskatu ģenerēšana Office formātā, kurā ir iegultie attēli
description: Šīs procedūras aprakstā ir paskaidrots, kā izstrādāt elektronisko pārskatu izveides (Electronic reporting — ER) konfigurācijas, lai ģenerētu iegultus attēlus saturošus elektroniskos dokumentus.
author: NickSelin
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
ms.openlocfilehash: 81b93c14fc4819fffd322a1b364feac3d25a0d24
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751562"
---
# <a name="generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="d9d2a-103">Pārskatu ģenerēšana Office formātā, kurā ir iegultie attēli</span><span class="sxs-lookup"><span data-stu-id="d9d2a-103">Generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d9d2a-104">Tālāk ir paskaidrots, kā lietotājs ar lomu 'Sistēmas administrators' vai 'Elektronisko atskaišu izstrādātājs' var izveidot elektronisko atskaišu veidošanas (Electronic Reporting — ER) konfigurācijas, lai veidotu elektroniskos dokumentus ar iegultiem attēliem MS Office formātos (Excel un Word).</span><span class="sxs-lookup"><span data-stu-id="d9d2a-104">The following steps explain how a user playing either 'System administrator' or 'Electronic reporting developer' role can design Electronic reporting (ER) configurations to generate electronic documents in MS office formats (Excel and Word) containing embedded images.</span></span>

<span data-ttu-id="d9d2a-105">Šajā piemērā jūs izmantosit parauga uzņēmumam 'Litware, Inc.' izveidotās ER konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-105">In this example, you will use created ER configurations for sample company, 'Litware, Inc.'.</span></span>  <span data-ttu-id="d9d2a-106">Lai veiktu šīs darbības, vispirms jāveic darbības, kas aprakstītas uzdevuma ceļvedī "ER: veikt pārskatus MS Office formātos ar iegultiem attēliem (2. daļa: pārskatīt konfigurācijas)".</span><span class="sxs-lookup"><span data-stu-id="d9d2a-106">To complete these steps, you must first complete the steps in the "ER Make reports in MS Office formats with embedded images (Part 2: Review configurations)" task guide.</span></span> <span data-ttu-id="d9d2a-107">Šīs darbības var veikt uzņēmumā 'USMF'.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-107">These steps can be performed in 'USMF' company.</span></span>


## <a name="run-format-with-initial-model-mapping"></a><span data-ttu-id="d9d2a-108">Formāta palaišana ar sākotnējo modeļa kartējumu</span><span class="sxs-lookup"><span data-stu-id="d9d2a-108">Run format with initial model mapping</span></span>
1. <span data-ttu-id="d9d2a-109">Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-109">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="d9d2a-110">Izmantojiet ātro filtru, lai filtrētu pēc lauka Bankas konts vērtības USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-110">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="d9d2a-111">Darbību rūtī noklikšķiniet uz Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-111">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="d9d2a-112">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-112">Click Check.</span></span>
5. <span data-ttu-id="d9d2a-113">Noklikšķiniet uz Drukāt paraugu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-113">Click Print test.</span></span>
    * <span data-ttu-id="d9d2a-114">Palaidiet formātu testēšanas nolūkā.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-114">Run the format for testing purposes.</span></span>  
6. <span data-ttu-id="d9d2a-115">Laukā Maksājumu čeka formāts atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-115">Select Yes in the Negotiable check format field.</span></span>
7. <span data-ttu-id="d9d2a-116">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-116">Click OK.</span></span>
    * <span data-ttu-id="d9d2a-117">Pārskatiet izveidoto izvadi.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-117">Review the created output.</span></span> <span data-ttu-id="d9d2a-118">Pārskatā ir iekļauts gan uzņēmuma logotips, gan pilnvarotās personas paraksts.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-118">The company logo is presented in the report as well as the authorized person's signature.</span></span> <span data-ttu-id="d9d2a-119">Paraksta attēls tiek ņemts no čeka izkārtojuma ieraksta lauka ar datu tipu “Konteiners”, kas ir saistīts ar atlasīto bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-119">The signature image is taken from the field of the 'Container' data type of the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="d9d2a-120">Izvērsiet sadaļu Kopijas.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-120">Expand the Copies section.</span></span>
9. <span data-ttu-id="d9d2a-121">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-121">Click Edit.</span></span>
10. <span data-ttu-id="d9d2a-122">Laukā Ūdenszīme ievadiet “Drukāt ūdenszīmi kā Anulēts”.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-122">In the Watermark field, enter 'Print watermark as Void'.</span></span>
    * <span data-ttu-id="d9d2a-123">Mainiet ūdenszīmes izkārtojuma iestatījumu, lai parādītu ūdenszīmes tekstu, ģenerējot dokumentu Excel formas elementā.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-123">Change the watermark layout setting to show the watermark text in generating document in an Excel shape element.</span></span>  
11. <span data-ttu-id="d9d2a-124">Noklikšķiniet uz Drukāt paraugu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-124">Click Print test.</span></span>
12. <span data-ttu-id="d9d2a-125">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-125">Click OK.</span></span>
    * <span data-ttu-id="d9d2a-126">Pārskatiet izveidoto izvadi.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-126">Review the created output.</span></span> <span data-ttu-id="d9d2a-127">Ūdenszīme izveidotajā pārskatā tiek rādīta atbilstoši atlasītajai opcijai.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-127">The watermark is shown in the created report in accordance to the selection option.</span></span>  
13. <span data-ttu-id="d9d2a-128">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-128">Close the page.</span></span>
14. <span data-ttu-id="d9d2a-129">Darbību rūtī noklikšķiniet uz Pārvaldīt maksājumus.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-129">On the Action Pane, click Manage payments.</span></span>
15. <span data-ttu-id="d9d2a-130">Noklikšķiniet uz Čeki.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-130">Click Checks.</span></span>
16. <span data-ttu-id="d9d2a-131">Noklikšķiniet uz Rādīt filtrus.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-131">Click Show filters.</span></span>
17. <span data-ttu-id="d9d2a-132">Lietojiet šādus filtrus: laukā “Čeka numurs” ievadiet filtra vērtību “381”,“385”,“389”, izmantojot filtra operatoru “ir viens no”.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-132">Apply the following filters: Enter a filter value of "381","385","389" on the "Check number" field using the "is one of" filter operator.</span></span>
18. <span data-ttu-id="d9d2a-133">Sarakstā atzīmējiet visas rindas.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-133">In the list, mark all rows.</span></span>
19. <span data-ttu-id="d9d2a-134">Noklikšķiniet uz Drukāt čeka kopiju.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-134">Click Print check copy.</span></span>
    * <span data-ttu-id="d9d2a-135">Palaidiet formātu, lai atkārtoti drukātu atlasītos čekus.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-135">Run the format to reprint the selected cheques.</span></span>  
    * <span data-ttu-id="d9d2a-136">Pārskatiet izveidoto izvadi.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-136">Review the created output.</span></span> <span data-ttu-id="d9d2a-137">Atlasītie čeki ir izdrukāti atkārtoti.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-137">The selected cheques have been reprinted.</span></span> <span data-ttu-id="d9d2a-138">Uzņēmuma logotips un etiķetes netiek drukātas, jo tās jau ir redzamas iepriekš izdrukātajā veidlapā.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-138">The company logo and labels are not printed out since they are presented on the pre-printed form.</span></span>  

## <a name="modify-the-mapping-of-the-imported-data-model"></a><span data-ttu-id="d9d2a-139">Importētā datu modeļa kartējuma modificēšana</span><span class="sxs-lookup"><span data-stu-id="d9d2a-139">Modify the mapping of the imported data model</span></span>
1. <span data-ttu-id="d9d2a-140">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-140">Close the page.</span></span>
2. <span data-ttu-id="d9d2a-141">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-141">Close the page.</span></span>
3. <span data-ttu-id="d9d2a-142">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-142">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="d9d2a-143">Koka struktūrā atlasiet “Čeku modelis”.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-143">In the tree, select 'Model for cheques'.</span></span>
5. <span data-ttu-id="d9d2a-144">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-144">Click Designer.</span></span>
6. <span data-ttu-id="d9d2a-145">Noklikšķiniet uz Kartēšanas modelis datu avotam.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-145">Click Map model to datasource.</span></span>
7. <span data-ttu-id="d9d2a-146">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-146">Click Designer.</span></span>
    * <span data-ttu-id="d9d2a-147">Mēs mainīsim datu modeļa paraksta vienuma saistījumu, lai iegūtu paraksta attēlu no faila, kas pievienots čeku izkārtojuma ierakstam, kurš ir saistīts ar atlasīto bankas kontu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-147">We will change the binding of the data model's signature item to get the signature image from the file that has been attached to the cheque layout record that is associated with the selected bank account.</span></span>  
8. <span data-ttu-id="d9d2a-148">Izslēdziet opciju Rādīt detalizēti.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-148">Turn off Show details.</span></span>
9. <span data-ttu-id="d9d2a-149">Kokā izvērsiet elementu “izkārtojums”.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-149">In the tree, expand 'layout'.</span></span>
10. <span data-ttu-id="d9d2a-150">Kokā izvērsiet 'layout\signature'.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-150">In the tree, expand 'layout\signature'.</span></span>
11. <span data-ttu-id="d9d2a-151">Kokā atlasiet 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-151">In the tree, select 'layout\signature\image = chequesaccount.'<Relations'.BankChequeLayout.Signature1Bmp'.</span></span>
12. <span data-ttu-id="d9d2a-152">Kokā izvērsiet sadaļu “chequesaccount”.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-152">In the tree, expand 'chequesaccount'.</span></span>
13. <span data-ttu-id="d9d2a-153">Kokā izvērsiet 'chequesaccount\<Relations'.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-153">In the tree, expand 'chequesaccount\<Relations'.</span></span>
14. <span data-ttu-id="d9d2a-154">Kokā izvērsiet 'chequesaccount\<Relations\BankChequeLayout'.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-154">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout'.</span></span>
15. <span data-ttu-id="d9d2a-155">Kokā izvērsiet 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-155">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations'.</span></span>
16. <span data-ttu-id="d9d2a-156">Kokā izvērsiet 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-156">In the tree, expand 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents'.</span></span>
17. <span data-ttu-id="d9d2a-157">Kokā atlasiet 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-157">In the tree, select 'chequesaccount\<Relations\BankChequeLayout\<Relations\<Documents\getFileContentAsContainer()'.</span></span>
18. <span data-ttu-id="d9d2a-158">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-158">Click Bind.</span></span>
19. <span data-ttu-id="d9d2a-159">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-159">Click Save.</span></span>
20. <span data-ttu-id="d9d2a-160">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-160">Close the page.</span></span>
21. <span data-ttu-id="d9d2a-161">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-161">Close the page.</span></span>
22. <span data-ttu-id="d9d2a-162">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-162">Close the page.</span></span>
23. <span data-ttu-id="d9d2a-163">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-163">Close the page.</span></span>

## <a name="run-format-using-the-adjusted-model-mapping"></a><span data-ttu-id="d9d2a-164">Formāta palaišana, izmantojot pielāgoto modeļa kartējumu</span><span class="sxs-lookup"><span data-stu-id="d9d2a-164">Run format using the adjusted model mapping</span></span>
1. <span data-ttu-id="d9d2a-165">Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-165">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
2. <span data-ttu-id="d9d2a-166">Izmantojiet līdzekli Ātrais filtrs, lai atrastu ierakstus.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-166">Use the Quick Filter to find records.</span></span> <span data-ttu-id="d9d2a-167">Piemēram, filtrējiet pēc lauka Bankas konts vērtības “USMF OPER”.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-167">For example, filter on the Bank account field with a value of 'USMF OPER'.</span></span>
3. <span data-ttu-id="d9d2a-168">Darbību rūtī noklikšķiniet uz Iestatīt.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-168">On the Action Pane, click Set up.</span></span>
4. <span data-ttu-id="d9d2a-169">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-169">Click Check.</span></span>
5. <span data-ttu-id="d9d2a-170">Noklikšķiniet uz Drukāt paraugu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-170">Click Print test.</span></span>
6. <span data-ttu-id="d9d2a-171">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-171">Click OK.</span></span>
    * <span data-ttu-id="d9d2a-172">Pārskatiet izveidoto izvadi.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-172">Review the created output.</span></span> <span data-ttu-id="d9d2a-173">Attēls no dokumentu pārvaldības pielikuma tiek izmantots kā pilnvarotas personas paraksts.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-173">The image from the Document Management attachment is presented as the signature of an authorized person.</span></span>  

## <a name="use-ms-word-document-as-a-template-in-the-imported-format"></a><span data-ttu-id="d9d2a-174">Izmantot MS Word dokumentu kā veidni importētajā formātā</span><span class="sxs-lookup"><span data-stu-id="d9d2a-174">Use MS Word document as a template in the imported format</span></span>
1. <span data-ttu-id="d9d2a-175">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-175">Close the page.</span></span>
2. <span data-ttu-id="d9d2a-176">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-176">Close the page.</span></span>
3. <span data-ttu-id="d9d2a-177">Dodieties uz Organizācijas administrēšana > Elektronisko atskaišu veidošana > Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-177">Go to Organization administration > Electronic reporting > Configurations.</span></span>
4. <span data-ttu-id="d9d2a-178">Koka struktūrā izvērsiet “Čeku modelis”.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-178">In the tree, expand 'Model for cheques'.</span></span>
5. <span data-ttu-id="d9d2a-179">Kokā atlasiet 'Model for cheques\Cheques printing format'.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-179">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>
6. <span data-ttu-id="d9d2a-180">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-180">Click Designer.</span></span>
7. <span data-ttu-id="d9d2a-181">Noklikšķiniet uz Pielikumi.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-181">Click Attachments.</span></span>
8. <span data-ttu-id="d9d2a-182">Noklikšķiniet uz Dzēst.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-182">Click Delete.</span></span>
9. <span data-ttu-id="d9d2a-183">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-183">Click Yes.</span></span>
10. <span data-ttu-id="d9d2a-184">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-184">Click New.</span></span>
11. <span data-ttu-id="d9d2a-185">Noklikšķiniet uz Fails.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-185">Click File.</span></span>
    * <span data-ttu-id="d9d2a-186">Noklikšķiniet uz Pārlūkot un atlasiet iepriekš lejupielādēto failu 'Čeku veidne Word.docx'.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-186">Click Browse and select the downloaded in advance 'Cheque template Word.docx' file.</span></span>  
12. <span data-ttu-id="d9d2a-187">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-187">Close the page.</span></span>
13. <span data-ttu-id="d9d2a-188">Ievadiet vai atlasiet kādu vērtību laukā Veidne.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-188">In the Template field, enter or select a value.</span></span>
14. <span data-ttu-id="d9d2a-189">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-189">Click Save.</span></span>
15. <span data-ttu-id="d9d2a-190">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-190">Close the page.</span></span>
16. <span data-ttu-id="d9d2a-191">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-191">Click Edit.</span></span>
17. <span data-ttu-id="d9d2a-192">Laukā Palaist melnrakstu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-192">Select Yes in the Run Draft field.</span></span>
18. <span data-ttu-id="d9d2a-193">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-193">Close the page.</span></span>
19. <span data-ttu-id="d9d2a-194">Dodieties uz Kases un bankas vadība > Banku konti > Banku konti.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-194">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>
20. <span data-ttu-id="d9d2a-195">Izmantojiet ātro filtru, lai filtrētu pēc lauka Bankas konts vērtības USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-195">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>
21. <span data-ttu-id="d9d2a-196">Noklikšķiniet uz Pārbaudīt.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-196">Click Check.</span></span>
22. <span data-ttu-id="d9d2a-197">Noklikšķiniet uz Drukāt paraugu.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-197">Click Print test.</span></span>
23. <span data-ttu-id="d9d2a-198">Noklikšķiniet uz Labi.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-198">Click OK.</span></span>
    * <span data-ttu-id="d9d2a-199">Pārskatiet izveidoto izvadi.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-199">Review the created output.</span></span> <span data-ttu-id="d9d2a-200">Izvade ir izveidota kā Word dokuments ar iegultiem attēliem, kuros redzams uzņēmuma logotips, pilnvarotas personas paraksts un atlasītais ūdenszīmes teksts.</span><span class="sxs-lookup"><span data-stu-id="d9d2a-200">The output has been generated as a Word document with embedded images presenting the company logo, the signature of an authorized person and the selected text of the watermark.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
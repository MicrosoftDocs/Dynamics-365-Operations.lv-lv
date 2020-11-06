---
title: Formātu modificēšana, atkārtoti lietojot Excel veidnes
description: Lai veiktu šīs procedūras darbības, jums vispirms ir jāizpilda procedūra “ER Noformēt konfigurāciju pārskatu ģenerēšanai formātā OPENXML”.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 255e45ec724eb4e6a4a87c65f62867eb50c7df93
ms.sourcegitcommit: cb94f16d69455cbf6fd059f9f394e7623810c924
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/15/2020
ms.locfileid: "4011613"
---
# <a name="modify-formats-by-reapplying-excel-templates"></a><span data-ttu-id="02c24-103">Formātu modificēšana, atkārtoti lietojot Excel veidnes</span><span class="sxs-lookup"><span data-stu-id="02c24-103">Modify formats by reapplying Excel templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02c24-104">Lai veiktu šīs procedūras darbības, jums vispirms ir jāizpilda procedūra “ER Noformēt konfigurāciju pārskatu ģenerēšanai formātā OPENXML”.</span><span class="sxs-lookup"><span data-stu-id="02c24-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="02c24-105">Šīs procedūras aprakstā ir paskaidrots, kā izmainīt elektronisko pārskatu izveides (Electronic reporting — ER) formāta konfigurāciju, atkārtoti lietojot izmainītu Microsoft Excel veidni.</span><span class="sxs-lookup"><span data-stu-id="02c24-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="02c24-106">Šajā procedūrā importēsiet modificētu Excel veidni ER formāta konfigurācijās, kuras ir izveidotas parauga uzņēmumam “Litware, Inc.”, un pēc tam ģenerēsit elektroniskos dokumentus.</span><span class="sxs-lookup"><span data-stu-id="02c24-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="02c24-107">Šī procedūra ir paredzēta lietotājiem, kuriem ir piešķirta sistēmas administratora vai elektroniskā pārskata izstrādātāja loma.</span><span class="sxs-lookup"><span data-stu-id="02c24-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="02c24-108">Šīs darbības var veikt, izmantojot GBSI datu kopu.</span><span class="sxs-lookup"><span data-stu-id="02c24-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="02c24-109">Pirms darba sākšanas lejupielādējiet un saglabājiet failu SampleVendPaymWsReport2.xlsx, kurš ir norādīts palīdzības tēmā “Elektronisko pārskatu veidošanas formāta mainīšana, atkārtoti pielietojot Excel veidni” (modify-electronic-reporting-format-reapply-excel-template/).</span><span class="sxs-lookup"><span data-stu-id="02c24-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="02c24-110">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="02c24-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="02c24-111">Pārliecinieties, vai konfigurācijas nodrošinātājs parauga uzņēmumam “Litware, Inc.” ir pieejams un ir atzīmēts kā aktīvs.</span><span class="sxs-lookup"><span data-stu-id="02c24-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="02c24-112">Ja neredzat šo konfigurācijas nodrošinātāju, jums vispirms ir jāizpilda darbības, kas aprakstītas procedūrā “Izveidot konfigurācijas nodrošinātāju un atzīmēt to kā aktīvu”.</span><span class="sxs-lookup"><span data-stu-id="02c24-112">If you don't see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="02c24-113">Atlasīt ER formātu</span><span class="sxs-lookup"><span data-stu-id="02c24-113">Select the ER format</span></span>
1. <span data-ttu-id="02c24-114">Noklikšķiniet uz Pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="02c24-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="02c24-115">Kokā struktūra izvērsiet sadaļu “Maksājuma modelis”.</span><span class="sxs-lookup"><span data-stu-id="02c24-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="02c24-116">Koka struktūrā atlasiet “Maksājuma modelis\Parauga darblapas atskaite”.</span><span class="sxs-lookup"><span data-stu-id="02c24-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="02c24-117">Noklikšķiniet uz Pielikumi.</span><span class="sxs-lookup"><span data-stu-id="02c24-117">Click Attachments.</span></span>
    * <span data-ttu-id="02c24-118">Ņemiet vērā, ka Excel fails SampleVendPaymWsReport.xlsx pašlaik tiek izmantots kā veidne maksājumu žurnālu apstrādei.</span><span class="sxs-lookup"><span data-stu-id="02c24-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="02c24-119">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="02c24-119">Click Open.</span></span>
    * <span data-ttu-id="02c24-120">Noklikšķiniet uz Atvērt, lai izpētītu Excel veidnes izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="02c24-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="02c24-121">Pārskatiet veidni.</span><span class="sxs-lookup"><span data-stu-id="02c24-121">Review the template.</span></span> <span data-ttu-id="02c24-122">Ņemiet vērā, ka tajā pašlaik ietverta šāda informācija par katru maksājuma rindu: kreditora konta numurs, kreditora nosaukums, banka, reģistrācijas numurs, konta numurs, debets, kredīts un valūta.</span><span class="sxs-lookup"><span data-stu-id="02c24-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="02c24-123">Šajā piemērā mēs vēlamies paplašināt šo sarakstu, pievienojot detalizētu informāciju par maksājuma datumu.</span><span class="sxs-lookup"><span data-stu-id="02c24-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="02c24-124">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="02c24-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="02c24-125">Atkārtoti lietot jaunu Excel veidni ER formātam</span><span class="sxs-lookup"><span data-stu-id="02c24-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="02c24-126">Noklikšķiniet uz Veidotājs.</span><span class="sxs-lookup"><span data-stu-id="02c24-126">Click Designer.</span></span>
    * <span data-ttu-id="02c24-127">Atveriet atlasītā ER formāta melnraksta versiju rediģēšanai.</span><span class="sxs-lookup"><span data-stu-id="02c24-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="02c24-128">Darbību rūtī noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="02c24-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="02c24-129">Noklikšķiniet uz Atjaunināt no Excel.</span><span class="sxs-lookup"><span data-stu-id="02c24-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="02c24-130">Noklikšķiniet uz 'Atjaunināt veidni' un pēc tam atlasiet failu SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="02c24-130">Click 'Update template', and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="02c24-131">Noklikšķiniet uz Atjaunināt veidni un pārlūkojiet līdz iepriekš lejupielādētajam failam SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="02c24-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="02c24-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="02c24-132">Click OK.</span></span>
    * <span data-ttu-id="02c24-133">Tiek lietota veidne SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="02c24-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="02c24-134">ER formāta struktūra ir sinhronizēta ar tās veidnes saturu, kuras elementi tiek pievienoti ER formātam.</span><span class="sxs-lookup"><span data-stu-id="02c24-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="02c24-135">Visi esošie ER formāta elementi, kas nav iekļauti veidnē, tiek noņemti no formāta definīcijas.</span><span class="sxs-lookup"><span data-stu-id="02c24-135">Any existing elements in the ER format that aren't included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="02c24-136">Kokā atlasiet “Excel”.</span><span class="sxs-lookup"><span data-stu-id="02c24-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="02c24-137">Ņemiet vērā, ka lauks Veidne tagad satur atsauci uz jauno veidni.</span><span class="sxs-lookup"><span data-stu-id="02c24-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="02c24-138">Noklikšķiniet uz Pielikumi.</span><span class="sxs-lookup"><span data-stu-id="02c24-138">Click Attachments.</span></span>
7. <span data-ttu-id="02c24-139">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="02c24-139">Click Open.</span></span>
    * <span data-ttu-id="02c24-140">Noklikšķiniet uz Atvērt, lai izpētītu modificētās Excel veidnes izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="02c24-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="02c24-141">Pārskatiet veidni.</span><span class="sxs-lookup"><span data-stu-id="02c24-141">Review the template.</span></span> <span data-ttu-id="02c24-142">Ņemiet vērā, ka tas tagad satur maksājuma datuma rindu.</span><span class="sxs-lookup"><span data-stu-id="02c24-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="02c24-143">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="02c24-143">Close the page.</span></span>
9. <span data-ttu-id="02c24-144">Kokā izvērsiet “Excel”.</span><span class="sxs-lookup"><span data-stu-id="02c24-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="02c24-145">Koka struktūrā izvērsiet zaru “Excel\PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="02c24-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="02c24-146">Kokā atlasiet 'Excel\PaymLines\PaymDate'.</span><span class="sxs-lookup"><span data-stu-id="02c24-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="02c24-147">Ņemiet vērā, ka ER formāts tagad satur vienu papildu vienumu.</span><span class="sxs-lookup"><span data-stu-id="02c24-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="02c24-148">Excel veidnei ir pievienota šūna PaymDate.</span><span class="sxs-lookup"><span data-stu-id="02c24-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="02c24-149">Noklikšķiniet uz cilnes Kartēšana.</span><span class="sxs-lookup"><span data-stu-id="02c24-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="02c24-150">Koka struktūrā izvērsiet elementu “modelis”.</span><span class="sxs-lookup"><span data-stu-id="02c24-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="02c24-151">Kokā izvērsiet sadaļu “modelis\Maksājumi”.</span><span class="sxs-lookup"><span data-stu-id="02c24-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="02c24-152">Kokā atlasiet "modelis\Maksājumi\Transakcijas datums(TransactionDate)".</span><span class="sxs-lookup"><span data-stu-id="02c24-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="02c24-153">Noklikšķiniet uz Saistīt.</span><span class="sxs-lookup"><span data-stu-id="02c24-153">Click Bind.</span></span>
    * <span data-ttu-id="02c24-154">Norādiet, kādi dati jāpievieno jaunajai šūnai izpildlaikā.</span><span class="sxs-lookup"><span data-stu-id="02c24-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="02c24-155">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="02c24-155">Click Save.</span></span>
18. <span data-ttu-id="02c24-156">Aizvērt lapu.</span><span class="sxs-lookup"><span data-stu-id="02c24-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="02c24-157">Iespējot ER formāta modificēto melnraksta versiju lietošanai maksājumu žurnāla apstrādei</span><span class="sxs-lookup"><span data-stu-id="02c24-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="02c24-158">Darbību rūtī noklikšķiniet uz Konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="02c24-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="02c24-159">Noklikšķiniet uz Lietotāja parametri.</span><span class="sxs-lookup"><span data-stu-id="02c24-159">Click User parameters.</span></span>
3. <span data-ttu-id="02c24-160">Laukā Palaist iestatījumus atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="02c24-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="02c24-161">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="02c24-161">Click OK.</span></span>
5. <span data-ttu-id="02c24-162">Noklikšķiniet uz Rediģēt.</span><span class="sxs-lookup"><span data-stu-id="02c24-162">Click Edit.</span></span>
6. <span data-ttu-id="02c24-163">Laukā Palaist melnrakstu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="02c24-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="02c24-164">Izmantot ER formāta modificēto melnraksta versiju lietošanai maksājumu žurnāla apstrādei</span><span class="sxs-lookup"><span data-stu-id="02c24-164">Use the modified draft version of the ER format for payment journal processing</span></span>

<span data-ttu-id="02c24-165">Pārskatiet izveidoto darblapu, ieskaitot jauno maksājuma informācijas rindu — maksājuma datumu.</span><span class="sxs-lookup"><span data-stu-id="02c24-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  

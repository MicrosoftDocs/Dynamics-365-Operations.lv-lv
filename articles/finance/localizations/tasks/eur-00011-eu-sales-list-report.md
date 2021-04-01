---
title: EUR-00011 Ģenerēt ES pārdošanas saraksta atskaiti
description: Šajā procedūrā tiek izklāstīta ES pārdošanas saraksta pārskata izveide.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesEditLines,  EUSalesList, EUSalesListSelection, SysQueryForm, SysLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fdedf153ae17ac90032e8998ce3b97ba9b734b64
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227983"
---
# <a name="eur-00011-generate-the-eu-sales-list-report"></a><span data-ttu-id="03398-103">EUR-00011 Ģenerēt ES pārdošanas saraksta atskaiti</span><span class="sxs-lookup"><span data-stu-id="03398-103">EUR-00011 Generate the EU sales list report</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="03398-104">Šajā procedūrā tiek izklāstīta ES pārdošanas saraksta pārskata izveide.</span><span class="sxs-lookup"><span data-stu-id="03398-104">This procedure walks you through generating the EU sales list report.</span></span> <span data-ttu-id="03398-105">Tā ietver EK iekšējo tirdzniecības transakciju pārsūtīšanu uz ES pārdošanas sarakstu un pārskata izveidi.</span><span class="sxs-lookup"><span data-stu-id="03398-105">This includes transferring intra-community trade transactions to the EU sales list and running the report.</span></span> <span data-ttu-id="03398-106">Šī procedūra ietver arī kopienas iekšējo tirdzniecības transakciju izveidošanu demonstrācijas nolūkiem.</span><span class="sxs-lookup"><span data-stu-id="03398-106">This procedure also includes creating an intra-community trade transaction for demo purposes.</span></span> <span data-ttu-id="03398-107">Lai iegūtu plašāku informāciju par ES pārdošanas saraksta pārskatu, tai skaitā nepieciešamajiem priekšnoteikumiem, skatiet sadaļu Palīdzība.</span><span class="sxs-lookup"><span data-stu-id="03398-107">For more information about EU Sales list reporting, including required prerequisites, refer to Help.</span></span>

<span data-ttu-id="03398-108">Šī procedūra attiecas uz visām Eiropas valstīm/reģioniem.</span><span class="sxs-lookup"><span data-stu-id="03398-108">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="03398-109">Šī procedūra tika izveidota, izmantojot demonstrācijas datu uzņēmumu DEMF un tādējādi Vācijā tiek izmantota kā iekšzemes valsts/reģiona piemērs.</span><span class="sxs-lookup"><span data-stu-id="03398-109">The procedure was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="03398-110">Šajā procedūrā kā ES valsts/reģiona piemērs tiek izmantota arī Portugāle.</span><span class="sxs-lookup"><span data-stu-id="03398-110">The procedure also uses Portugal as an exemplar EU country/region.</span></span> <span data-ttu-id="03398-111">Lai varētu veikt šo procedūru, ir jākonfigurē ES pārdošanas saraksta pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="03398-111">Before you can complete this procedure, you must configure EU sales list reporting.</span></span>

<span data-ttu-id="03398-112">Šī procedūra ir paredzēta grāmatvežiem.</span><span class="sxs-lookup"><span data-stu-id="03398-112">This procedure is intended for accountants.</span></span>


## <a name="create-an-intra-community-sales-transaction-for-demo-purposes"></a><span data-ttu-id="03398-113">EK iekšējās tirdzniecības transakcijas izveide demonstrācijas nolūkiem</span><span class="sxs-lookup"><span data-stu-id="03398-113">Create an intra-community sales transaction for demo purposes</span></span>
1. <span data-ttu-id="03398-114">Pārejiet uz sadaļu Debitori > Pasūtījumi > Visi pārdošanas pasūtījumi.</span><span class="sxs-lookup"><span data-stu-id="03398-114">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="03398-115">Noklikšķiniet uz Jauns.</span><span class="sxs-lookup"><span data-stu-id="03398-115">Click New.</span></span>
3. <span data-ttu-id="03398-116">Laukā Debitora konts ierakstiet "PRT-001".</span><span class="sxs-lookup"><span data-stu-id="03398-116">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="03398-117">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="03398-117">Click OK.</span></span>
5. <span data-ttu-id="03398-118">Laukā Krājuma kods ierakstiet D0001.</span><span class="sxs-lookup"><span data-stu-id="03398-118">In the Item number field, type 'D0001'.</span></span>
6. <span data-ttu-id="03398-119">Izvērsiet sadaļu Detalizēta informācija par rindu.</span><span class="sxs-lookup"><span data-stu-id="03398-119">Expand the Line details section.</span></span>
7. <span data-ttu-id="03398-120">Noklikšķiniet uz cilnes Iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="03398-120">Click the Setup tab.</span></span>
8. <span data-ttu-id="03398-121">Laukā Krājumu PVN grupa ierakstiet vērtību "PILNS".</span><span class="sxs-lookup"><span data-stu-id="03398-121">In the Item sales tax group field, type 'FULL'.</span></span>
9. <span data-ttu-id="03398-122">Noklikšķiniet uz Pievienot rindu.</span><span class="sxs-lookup"><span data-stu-id="03398-122">Click Add line.</span></span>
10. <span data-ttu-id="03398-123">Laukā Krājuma kods ierakstiet D0003.</span><span class="sxs-lookup"><span data-stu-id="03398-123">In the Item number field, type 'D0003'.</span></span>
11. <span data-ttu-id="03398-124">Laukā Krājumu PVN grupa ierakstiet vērtību "SARKANS".</span><span class="sxs-lookup"><span data-stu-id="03398-124">In the Item sales tax group field, type 'RED'.</span></span>
12. <span data-ttu-id="03398-125">Noklikšķiniet uz Saglabāt.</span><span class="sxs-lookup"><span data-stu-id="03398-125">Click Save.</span></span>
13. <span data-ttu-id="03398-126">Darbību rūtī noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="03398-126">On the Action Pane, click Invoice.</span></span>
14. <span data-ttu-id="03398-127">Noklikšķiniet uz Rēķins.</span><span class="sxs-lookup"><span data-stu-id="03398-127">Click Invoice.</span></span>
15. <span data-ttu-id="03398-128">Izvērsiet sadaļu Parametri.</span><span class="sxs-lookup"><span data-stu-id="03398-128">Expand the Parameters section.</span></span>
16. <span data-ttu-id="03398-129">Laukā Daudzums atlasiet vērtību Visi.</span><span class="sxs-lookup"><span data-stu-id="03398-129">In the Quantity field, select 'All'.</span></span>
17. <span data-ttu-id="03398-130">Izvērsiet sadaļu Iestatīšana.</span><span class="sxs-lookup"><span data-stu-id="03398-130">Expand the Setup section.</span></span>
18. <span data-ttu-id="03398-131">Laukā Rēķina datums iestatiet datumu “11.01.2016.”.</span><span class="sxs-lookup"><span data-stu-id="03398-131">In the Invoice date field, set the date to '01/11/2016'.</span></span>
19. <span data-ttu-id="03398-132">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="03398-132">Click OK.</span></span>
20. <span data-ttu-id="03398-133">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="03398-133">Click OK.</span></span>

## <a name="transfer-intra-community-trade-transactions-to-the-eu-sales-list"></a><span data-ttu-id="03398-134">EK iekšējo tirdzniecības transakciju pārsūtīšana uz ES pārdošanas sarakstu</span><span class="sxs-lookup"><span data-stu-id="03398-134">Transfer intra-community trade transactions to the EU sales list</span></span>
1. <span data-ttu-id="03398-135">Dodieties uz Nodokļi > Deklarācijas > Ārējā tirdzniecība > ES pārdošanas saraksts.</span><span class="sxs-lookup"><span data-stu-id="03398-135">Go to Tax > Declarations > Foreign trade > EU sales list.</span></span>
2. <span data-ttu-id="03398-136">Noklikšķiniet uz Pārvest.</span><span class="sxs-lookup"><span data-stu-id="03398-136">Click Transfer.</span></span>
3. <span data-ttu-id="03398-137">Laukā Krājums atlasiet Jā, lai pārsūtītu krājuma darbības.</span><span class="sxs-lookup"><span data-stu-id="03398-137">Select Yes in the Item field to transfer item transactions.</span></span>
4. <span data-ttu-id="03398-138">Laukā Pakalpojums atlasiet Jā, lai pārsūtītu pakalpojum darbības.</span><span class="sxs-lookup"><span data-stu-id="03398-138">Select Yes in the Service field to transfer service transactions.</span></span>
    * <span data-ttu-id="03398-139">Varat arī norādīt papildu filtrus attiecībā uz EK iekšējām tirdzniecības transakcijām, kas jāpārsūta.</span><span class="sxs-lookup"><span data-stu-id="03398-139">You can also specify additional filters on intra-community trade transactions to transfer.</span></span>  
5. <span data-ttu-id="03398-140">Noklikšķiniet uz Pārvest.</span><span class="sxs-lookup"><span data-stu-id="03398-140">Click Transfer.</span></span>
    * <span data-ttu-id="03398-141">Apstipriniet, ka EK iekšējās tirdzniecības transakcijas ir veiksmīgi pārsūtītas uz ES pārdošanas sarakstu.</span><span class="sxs-lookup"><span data-stu-id="03398-141">Verify that the intra-community sales transaction is successfully transferred to the EU sales list.</span></span>  

## <a name="generate-the-eu-sales-list-report"></a><span data-ttu-id="03398-142">Ģenerēt ES pārdošanas sarakstu pārskatu</span><span class="sxs-lookup"><span data-stu-id="03398-142">Generate the EU sales list report</span></span>
1. <span data-ttu-id="03398-143">Noklikšķiniet uz Atskaišu veidošana.</span><span class="sxs-lookup"><span data-stu-id="03398-143">Click Reporting.</span></span>
2. <span data-ttu-id="03398-144">Laukā Pārskata periods atlasiet vienumu Mēneša.</span><span class="sxs-lookup"><span data-stu-id="03398-144">In the Reporting period field, select 'Monthly'.</span></span>
3. <span data-ttu-id="03398-145">Laukā No datuma iestatiet datumu “01.01.2016.”.</span><span class="sxs-lookup"><span data-stu-id="03398-145">In the From date field, set the date to '01/01/2016'.</span></span>
4. <span data-ttu-id="03398-146">Laukā Ģenerēt failu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="03398-146">Select Yes in the Generate file field.</span></span>
5. <span data-ttu-id="03398-147">Laukā Ģenerēt pārskatu atlasiet Jā.</span><span class="sxs-lookup"><span data-stu-id="03398-147">Select Yes in the Generate report field.</span></span>
6. <span data-ttu-id="03398-148">Laukā Faila nosaukums ierakstiet "EUSalesList".</span><span class="sxs-lookup"><span data-stu-id="03398-148">In the File name field, type 'EUSalesList'.</span></span>
7. <span data-ttu-id="03398-149">Laukā Pārskata faila nosaukums ierakstiet "EUSalesList".</span><span class="sxs-lookup"><span data-stu-id="03398-149">In the Report file name field, type 'EUSalesList'.</span></span>
8. <span data-ttu-id="03398-150">Laukā ES pārdošanas saraksta reģistrācijas ID ierakstiet "123".</span><span class="sxs-lookup"><span data-stu-id="03398-150">In the EU Sales List Registration ID field, type '123'.</span></span>
    * <span data-ttu-id="03398-151">Šis lauks ir pieejams tikai Vācijai.</span><span class="sxs-lookup"><span data-stu-id="03398-151">This field is only available for Germany.</span></span>  
    * <span data-ttu-id="03398-152">Varat arī norādīt pārsūtīšanai papildu filtrus attiecībā uz EK iekšējām tirdzniecības transakcijām, kas jāiekļauj pārskatā.</span><span class="sxs-lookup"><span data-stu-id="03398-152">You can also specify additional filters on intra-community trade transactions to include in the report.</span></span>  
9. <span data-ttu-id="03398-153">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="03398-153">Click OK.</span></span>
    * <span data-ttu-id="03398-154">Pārliecinieties, ka tiek parādīti uznirstošie logi, lai apstiprinātu, ka tiek lejupielādēts fails un kontroles pārskats.</span><span class="sxs-lookup"><span data-stu-id="03398-154">Verify that pop-up windows appear to confirm that the file and the control report are being downloaded.</span></span>  

## <a name="mark-eu-sales-list-lines-as-reported"></a><span data-ttu-id="03398-155">ES pārdošanas saraksta rindu atzīmēšana kā iekļautas pārskatā</span><span class="sxs-lookup"><span data-stu-id="03398-155">Mark EU sales list lines as Reported</span></span>
1. <span data-ttu-id="03398-156">Noklikšķiniet uz Atzīmēt.</span><span class="sxs-lookup"><span data-stu-id="03398-156">Click Mark.</span></span>
2. <span data-ttu-id="03398-157">Noklikšķiniet uz Iezīmēt pārskatam.</span><span class="sxs-lookup"><span data-stu-id="03398-157">Click Mark as reported.</span></span>
3. <span data-ttu-id="03398-158">Sarakstā atlasiet rindu laukam Rēķina datums.</span><span class="sxs-lookup"><span data-stu-id="03398-158">In the list, select the row for the Invoice date field.</span></span>
4. <span data-ttu-id="03398-159">Laukā Kritēriji ierakstiet "01.01.2016.–31.01.2016.".</span><span class="sxs-lookup"><span data-stu-id="03398-159">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="03398-160">Sarakstā atlasiet rindu laukam Pārskata statuss.</span><span class="sxs-lookup"><span data-stu-id="03398-160">In the list, select the row for the Reporting status field.</span></span>
6. <span data-ttu-id="03398-161">Laukā Kritēriji atlasiet vienumu Iekļauts.</span><span class="sxs-lookup"><span data-stu-id="03398-161">In the Criteria field, select 'Included'.</span></span>
    * <span data-ttu-id="03398-162">Varat arī norādīt papildu filtrus attiecībā uz EK iekšējām tirdzniecības transakcijām, kas jāatzīmē kā iekļautas pārskatā.</span><span class="sxs-lookup"><span data-stu-id="03398-162">You can also specify additional filters on intra-community trade transactions to mark as Reported.</span></span>  
7. <span data-ttu-id="03398-163">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="03398-163">Click OK.</span></span>
8. <span data-ttu-id="03398-164">Laukā Atlase izvēlieties vienumu Iekļauti pārskatā.</span><span class="sxs-lookup"><span data-stu-id="03398-164">In the Selection field, select 'Reported'.</span></span>

## <a name="mark-eu-sales-list-lines-as-closed"></a><span data-ttu-id="03398-165">ES pārdošanas saraksta rindu atzīmēšana kā slēgtas</span><span class="sxs-lookup"><span data-stu-id="03398-165">Mark EU sales list lines as Closed</span></span>
1. <span data-ttu-id="03398-166">Noklikšķiniet uz Atzīmēt.</span><span class="sxs-lookup"><span data-stu-id="03398-166">Click Mark.</span></span>
2. <span data-ttu-id="03398-167">Noklikšķiniet uz Iezīmēt kā aizvērtu.</span><span class="sxs-lookup"><span data-stu-id="03398-167">Click Mark as closed.</span></span>
3. <span data-ttu-id="03398-168">Sarakstā atzīmējiet rindu laukam Rēķina datums.</span><span class="sxs-lookup"><span data-stu-id="03398-168">In the list, mark the row for the Invoice date field.</span></span>
4. <span data-ttu-id="03398-169">Laukā Kritēriji ierakstiet "01.01.2016.–31.01.2016.".</span><span class="sxs-lookup"><span data-stu-id="03398-169">In the Criteria field, type '01/01/2016..01/31/2016'.</span></span>
5. <span data-ttu-id="03398-170">Sarakstā atzīmējiet rindu laukam Pārskata statuss.</span><span class="sxs-lookup"><span data-stu-id="03398-170">In the list, mark the row for the Reporting status field.</span></span>
6. <span data-ttu-id="03398-171">Laukā Kritēriji atlasiet vienumu ' Iekļauti pārskatā'.</span><span class="sxs-lookup"><span data-stu-id="03398-171">In the Criteria field, select 'Reported'.</span></span>
    * <span data-ttu-id="03398-172">Varat arī norādīt papildu filtrus attiecībā uz EK iekšējām tirdzniecības transakcijām, kas jāatzīmē kā slēgtas.</span><span class="sxs-lookup"><span data-stu-id="03398-172">You can also specify additional filters on intra-community trade transactions to mark as Closed.</span></span>  
7. <span data-ttu-id="03398-173">Noklikšķiniet uz OK.</span><span class="sxs-lookup"><span data-stu-id="03398-173">Click OK.</span></span>
8. <span data-ttu-id="03398-174">Laukā Atlase izvēlieties vienumu Slēgts.</span><span class="sxs-lookup"><span data-stu-id="03398-174">In the Selection field, select 'Closed'.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
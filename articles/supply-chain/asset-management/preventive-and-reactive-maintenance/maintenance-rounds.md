---
title: Uzturēšanas cikls
description: Šajā tēmā ir uzturēšanas cikli programmā Asset Management.
author: josaw1
manager: AnnBe
ms.date: 08/27/2019
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
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 4c9a2fee7d43142f8bb17f4e819c9949a2a20c41
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570034"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="9a26e-103">Uzturēšanas cikls</span><span class="sxs-lookup"><span data-stu-id="9a26e-103">Maintenance rounds</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="9a26e-104">Programmā **Asset Management** jūs varat izveidot uzturēšanas ciklus dažādiem līdzekļiem, kuriem jums ir regulāros intervālos jāveic līdzīgs uzdevums.</span><span class="sxs-lookup"><span data-stu-id="9a26e-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="9a26e-105">Piemēram, ieeļļošanas darbus vai drošības pārbaudes darbus, kuri ir jāveic vairākām iekārtām vienādos intervālos.</span><span class="sxs-lookup"><span data-stu-id="9a26e-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="9a26e-106">Pirmā darbībā ir uzturēšanas cikla izveide, ieskaitot līdzekļus, kuriem ir nepieciešams viena un tāda paša veida uzturēšanas darbs.</span><span class="sxs-lookup"><span data-stu-id="9a26e-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="9a26e-107">Pēc tam jūs ieplānojat uzturēšanas ciklus.</span><span class="sxs-lookup"><span data-stu-id="9a26e-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="9a26e-108">Kad esat aizpildījis uzturēšanas ciklu grafiku, jūs varat redzēt visus darba ierakstus, kas saistīti ar raundu sadaļās **Visi uzturēšanas grafiki** un **Atvērt uzturēšanas saraksta rindas**.</span><span class="sxs-lookup"><span data-stu-id="9a26e-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="9a26e-109">Uzturēšanas ciklus var arī uzstādīt funkcionālajam novietojumam, kurš ir jāpabeidz līdzekļos, kuri instalēti funkcionālajā novietojumā ciklā bāzēta darba pasūtījuma izveidošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="9a26e-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="9a26e-110">Skatiet [Izveidot funkcionālo novietojumu](../functional-locations/create-functional-locations.md), lai iegūtu vairāk informācijas par uzturēšanas ciklu uzstādīšanu funkcionālajā novietojumā.</span><span class="sxs-lookup"><span data-stu-id="9a26e-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="9a26e-111">Uzturēšanas cikla uzstādīšana</span><span class="sxs-lookup"><span data-stu-id="9a26e-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="9a26e-112">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Uzstādīšana** > **Preventīvā uzturēšana** > **Uzturēšanas cikli**.</span><span class="sxs-lookup"><span data-stu-id="9a26e-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="9a26e-113">Noklikšķiniet uz **Jauns**, lai izveidotu jaunu uzturēšanas ciklu.</span><span class="sxs-lookup"><span data-stu-id="9a26e-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="9a26e-114">Laukā **Uzturēšanas cikls** ievadiet ID un laukā **Nosaukums** ievadiet uzturēšanas cikla nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="9a26e-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="9a26e-115">Laukā **Sākuma datums** atlasiet cikla sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="9a26e-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="9a26e-116">Laukos **Pabeigt dienu laikā** un **Pabeigt stundu laikā** jūs varat ievadīt sagaidāmo beigu datumu dienās vai stundās.</span><span class="sxs-lookup"><span data-stu-id="9a26e-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="9a26e-117">Paredzamais beigu datums tiek aprēķināts relatīvi iepretim sākuma datumam, kurš tiek aprēķināts uzturēšanas grafika rindu izveides laikā.</span><span class="sxs-lookup"><span data-stu-id="9a26e-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="9a26e-118">Piemēram, jūs varat ievadīt "7" laukā **Pabeigt dienu laikā**, lai norādītu, ka attiecīgo darbu vajadzētu pabeigt nedēļas laikā kopš sākuma datuma.</span><span class="sxs-lookup"><span data-stu-id="9a26e-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="9a26e-119">Pārslēgšanas pogā **Automātiskā izveide** atlasiet "Jā", ja darba pasūtījumus vajadzētu automātiski izveidot no uzturēšanas grafika līnijām, kuras ir izveidotas no šī uzturēšanas cikla.</span><span class="sxs-lookup"><span data-stu-id="9a26e-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="9a26e-120">Laukā **Darba pasūtījuma tips** atlasiet darba pasūtījuma tipu, kuru jāizmanto darba pasūtījumiem, kuri izveidoti no šī uzturēšanas cikla.</span><span class="sxs-lookup"><span data-stu-id="9a26e-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="9a26e-121">Laukā **Servisa līmenis** atlasiet darba pasūtījuma servisa līmeni, kuru jāizmanto darba pasūtījumiem, kuri izveidoti no šī uzturēšanas cikla.</span><span class="sxs-lookup"><span data-stu-id="9a26e-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="9a26e-122">Kopsavilkuma cilnē **Līdzekļu rindas** noklikšķiniet **Pievienot**, lai uzturēšanas ciklam pievienotu līdzekli.</span><span class="sxs-lookup"><span data-stu-id="9a26e-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="9a26e-123">Rindas numurs tiek automātiski ievadīts laukā **Rindas numurs**, lai norādītu uzturēšanas cikla līdzekļu secību.</span><span class="sxs-lookup"><span data-stu-id="9a26e-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="9a26e-124">Laukā **Līdzeklis** atlasiet līdzekli.</span><span class="sxs-lookup"><span data-stu-id="9a26e-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="9a26e-125">Laukā **Uzturēšanas darba tips** atlasiet līdzekļa uzturēšanas darba tipu.</span><span class="sxs-lookup"><span data-stu-id="9a26e-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="9a26e-126">Ja nepieciešams, atlasiet **Uzturēšanas darba tipa variantu** un **Amatu**, kas saistīts ar uzturēšanas darba tipu.</span><span class="sxs-lookup"><span data-stu-id="9a26e-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="9a26e-127">Laukā **Perioda tips** atlasiet atkārtošanos (dienu, nedēļu u.c.).</span><span class="sxs-lookup"><span data-stu-id="9a26e-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="9a26e-128">Laukā **Perioda biežums** ievadiet uzturēšanas cikla atkārtošanos skaitu.</span><span class="sxs-lookup"><span data-stu-id="9a26e-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="9a26e-129">Piemērs: Ja jūs esat laukā **Perioda tips** atlasījuši "Diena" un jūs ievadāt šajā laukā ciparu "7", jaunas uzturēšanas cikla rindas tiek izveidotas preventīvas uzturēšanas plānošanas laikā reizi nedēļā.</span><span class="sxs-lookup"><span data-stu-id="9a26e-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="9a26e-130">Laukā **Sākuma datums** atlasiet sākuma datumu līdzeklim, kuru iekļausit uzturēšanas ciklā.</span><span class="sxs-lookup"><span data-stu-id="9a26e-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="9a26e-131">Šis datums var atšķirties no sākuma datuma, kas ir uzstādīts uzturēšanas ciklā.</span><span class="sxs-lookup"><span data-stu-id="9a26e-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="9a26e-132">Lai uzturēšanas ciklam pievienotu vairāk līdzekļu, atkārtojiet 9. līdz 16. darbību.</span><span class="sxs-lookup"><span data-stu-id="9a26e-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="9a26e-133">Kopsavilkuma cilnē **Funkcionālā novietojuma rindas** noklikšķiniet **Pievienot**, lai uzturēšanas ciklam pievienotu funkcionālo novietojumu.</span><span class="sxs-lookup"><span data-stu-id="9a26e-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="9a26e-134">Augstāk skatiet attiecīgo lauku aprakstu.</span><span class="sxs-lookup"><span data-stu-id="9a26e-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="9a26e-135">Ir pieejami tie paši lauki, kuri līdzekļa rindas izveidošanai, taču, ja nepieciešams, jūs varat arī funkcionālajam novietojumam atlasīt **Ražotāju** un **Modeli**.</span><span class="sxs-lookup"><span data-stu-id="9a26e-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="9a26e-136">Ja jūs rindā atlasāt vienīgi funkcionālo novietojumu, taču neatlasāt neko opcijās **Līdzekļa tips**, **Ražotājs**, **Modelis**, **Uzturēšanas darba tips**, **Uzturēšanas darba tipa variants** un **Amats**, visi līdzekļi, kas ir saistīti ar šo funkcionālo novietojumu uzturēšanas plānošanas laikā tiks iekļauti uzturēšanas ciklā.</span><span class="sxs-lookup"><span data-stu-id="9a26e-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="9a26e-137">Kopsavilkuma cilnē **Kopas** noklikšķiniet uz **Pievienot**, lai atlasītu darba pasūtījumu kopu, kuru ietvert uzturēšanas ciklā.</span><span class="sxs-lookup"><span data-stu-id="9a26e-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="9a26e-138">Vienam uzturēšanas ciklam var pievienot vairākas darba pasūtījumu kopas.</span><span class="sxs-lookup"><span data-stu-id="9a26e-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="9a26e-139">Saglabājiet savu uzstādījumu.</span><span class="sxs-lookup"><span data-stu-id="9a26e-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="9a26e-140">Lauki **Līdzekļi** un **Rindas**, kas atrodas ātrās cilnes **Galvene** grupā **Detalizēta informācija** uzrāda kopējo līdzekļu un rindu skaitu, kuras ir saistītas ar atlasīto uzturēšanas ciklu.</span><span class="sxs-lookup"><span data-stu-id="9a26e-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

<span data-ttu-id="9a26e-141">Nākamajā ilustrācijā ir redzams piemērs uzturēšanas ciklam, kurā ietilpst trīs līdzekļi.</span><span class="sxs-lookup"><span data-stu-id="9a26e-141">The illustration below shows and example of a maintenance round containing three assets.</span></span>

![1. attēls](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="9a26e-143">Plānot uzturēšanas ciklus</span><span class="sxs-lookup"><span data-stu-id="9a26e-143">Schedule maintenance rounds</span></span>

<span data-ttu-id="9a26e-144">Kad esat uzstādījis uzturēšanas ciklu, jūs palaižat grafika darbu, lai ieplānotu visus darbus, kas ir saistīti ar uzturēšanas ciklu.</span><span class="sxs-lookup"><span data-stu-id="9a26e-144">When you've set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="9a26e-145">Noklikšķiniet uz **Līdzekļu pārvaldība** > **Periodiski** > **Preventīvā uzturēšana** > **Ieplānot uzturēšanas ciklus** vai **Līdzekļu pārvaldība** > **Vispārīgi** > **Uzturēšanas grafiks** > **Visas uzturēšanas grafiks** vai **Atvērt uzturēšanas grafika rindas** vai **Atvērt uzturēšanas grafiku kopas** > atlasiet uzturēšanas grafika rindu sarakstā > pogas **Uzturēšanas cikli**.</span><span class="sxs-lookup"><span data-stu-id="9a26e-145">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="9a26e-146">Laukā **Periods** atlasiet perioda tipu, kuru izmantot plānošanas darbam.</span><span class="sxs-lookup"><span data-stu-id="9a26e-146">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="9a26e-147">Laukā **Perioda biežums** ievadiet periodu skaitu, kurus iekļaut plānošanas darbā.</span><span class="sxs-lookup"><span data-stu-id="9a26e-147">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="9a26e-148">Plānošanas sākums ir esošais datums.</span><span class="sxs-lookup"><span data-stu-id="9a26e-148">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="9a26e-149">Pārslēgšanas pogā **Automātiskā izveide** atlasiet "Jā", ja darba pasūtījumu vajadzētu automātiski izveidot no uzturēšanas grafika līnijām, kuras ir izveidotas no šī uzturēšanas cikla.</span><span class="sxs-lookup"><span data-stu-id="9a26e-149">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="9a26e-150">Ja šī pārslēgšanas poga ir iestatīta uz "Jā" un pārslēgšanas poga **Automātiskā izveide** arī ir iestatīta uz "Jā" uzturēšanas ciklā veidlapā **Uzturēšanas cikli**, darba pasūtījumi tiek izveidoti, pamatojoties uz uzturēšanas cikla rindām, un tiek izveidotas arī uzturēšanas grafika rindas ar statusu "Darba pasūtījums izveidots".</span><span class="sxs-lookup"><span data-stu-id="9a26e-150">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="9a26e-151">Ja tikai viena pārslēgšanas poga **Automātiskā izveide** arī ir iestatīta uz "Jā" šajā nolaižamajā sarakstā vai veidlapā **Uzturēšanas cikli**, tiek izveidotas uzturēšanas grafika rindas ar statusu "Izveidota".</span><span class="sxs-lookup"><span data-stu-id="9a26e-151">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="9a26e-152">Tāda gadījumā darba pasūtījumi netiek izveidoti.</span><span class="sxs-lookup"><span data-stu-id="9a26e-152">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="9a26e-153">Nepieciešamības gadījumā jūs varat atlasīt konkrētus ciklus vai citu plānota darba sākuma datumu.</span><span class="sxs-lookup"><span data-stu-id="9a26e-153">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="9a26e-154">Noklikšķiniet uz **Filtrēt** un pievienojiet iekļaujamos ciklus.</span><span class="sxs-lookup"><span data-stu-id="9a26e-154">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="9a26e-155">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="9a26e-155">Click **OK**.</span></span>

7. <span data-ttu-id="9a26e-156">Tagad jūs varat redzēt uzturēšanas ciklu darbus opcijā **Līdzekļu pārvaldība** > **Vispārīgi** > **Uzturēšanas grafiks** > **Visi uzturēšanas grafiki** vai **Atvērt uzturēšanas grafika rindas**.</span><span class="sxs-lookup"><span data-stu-id="9a26e-156">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="9a26e-157">Ja ieplānotie cikli ir saistīti ar darba pasūtījumu kopu, jūs arī redzēsit uzturēšanas saraksta rindas opcijā **Atvērt uzturēšanas grafika kopas**.</span><span class="sxs-lookup"><span data-stu-id="9a26e-157">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="9a26e-158">Uzturēšanas grafika rindām, kuras izveidotas no cikla, ir atsauces tips "Uzturēšanas cikli".</span><span class="sxs-lookup"><span data-stu-id="9a26e-158">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

<span data-ttu-id="9a26e-159">Divās nākamajās ilustrācijās ir parādīts darba grafiks dialoglodziņā **Plānot uzturēšanas ciklus** un uzturēšanas grafika rindas, kas izveidotas **Visos uzturēšanas grafikos**, pamatojoties uz šo plānoto darbu.</span><span class="sxs-lookup"><span data-stu-id="9a26e-159">The two illustrations below show a schedule job in the **Schedule maintenance rounds** dialog, and the maintenance schedule lines created in **All maintenance schedule** based on that schedule job.</span></span>

![2. attēls](media/14-preventive-maintenance.png)

![3. attēls](media/15-preventive-maintenance.png)

- <span data-ttu-id="9a26e-162">Kad darba pasūtījums tiek manuāli izveidots līdzekļiem, uz kuriem attiecas piegādātāja garantija, tiek parādīts dialoglodziņš, lai informētu lietotāju par garantiju.</span><span class="sxs-lookup"><span data-stu-id="9a26e-162">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="9a26e-163">Pēc tam darba pasūtījuma izveidi var atcelt.</span><span class="sxs-lookup"><span data-stu-id="9a26e-163">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="9a26e-164">Garantijas saistības pārbaude tiek izlaista tiem darba pasūtījumiem, kuri ir izveidoti automātiski.</span><span class="sxs-lookup"><span data-stu-id="9a26e-164">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="9a26e-165">Ātrajā cilnē **Palaist fonā** jūs uzstādīt pakešuzdevumu, lai ieplānotu ciklus regulāros intervālos.</span><span class="sxs-lookup"><span data-stu-id="9a26e-165">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="9a26e-166">Ja cikls ir ietvers vairākās darba pasūtījumu kopās (skatīt [Darba pasūtījumu kopas](../work-orders/work-order-pools.md)), katrai kopai tiek uzrādīts viens ieraksts opcijā **Atvērt uzturēšanas grafiku kopas**.</span><span class="sxs-lookup"><span data-stu-id="9a26e-166">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="9a26e-167">Tas tiek darīts, lai optimizētu filtrēšanas opcijas darba pasūtījumu kopām.</span><span class="sxs-lookup"><span data-stu-id="9a26e-167">This is done to optimize the filtering options for work order pools.</span></span>


---
title: Duālā ieraksta pārskats
description: Šī tēma sniedz apskatu par duālo ierakstu. Duālais ieraksts ir infrastruktūra, kas nodrošina gandrīz reāllaika mijiedarbību starp Microsoft Dynamics 365 modeļa vadītajām programmām un Finance and Operations programmām.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 85530cf644c7b7ffe922a6fb3288f4e05c5df91c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685617"
---
# <a name="dual-write-overview"></a><span data-ttu-id="24c1b-104">Duālā ieraksta pārskats</span><span class="sxs-lookup"><span data-stu-id="24c1b-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="24c1b-105">Kas ir duālais ieraksts?</span><span class="sxs-lookup"><span data-stu-id="24c1b-105">What is dual-write?</span></span>

<span data-ttu-id="24c1b-106">Duālais ieraksts ir standarta infrastruktūra, kas nodrošina gandrīz reāllaika mijiedarbību starp Customer Engagement programmām un Finance and Operations programmām.</span><span class="sxs-lookup"><span data-stu-id="24c1b-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="24c1b-107">Kad dati par debitoriem, precēm, cilvēkiem un operācijām pārsniedz programmas robežas, tiek nodrošinātas visas organizācijas struktūrvienības.</span><span class="sxs-lookup"><span data-stu-id="24c1b-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="24c1b-108">Duālais ieraksts nodrošina cieši saistītu divvirzienu integrāciju starp Finance and Operations programmām un Dataverse.</span><span class="sxs-lookup"><span data-stu-id="24c1b-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="24c1b-109">Visas Finance and Operations programmas datu izmaiņas izraisa Dataverse ierakstus, un jebkuras datu izmaiņas, kas rodas Dataverse rada ierakstus Finance and Operations programmām.</span><span class="sxs-lookup"><span data-stu-id="24c1b-109">Any data change in Finance and Operations apps causes writes to Dataverse, and any data change in Dataverse causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="24c1b-110">Šī automatizētā datu plūsma nodrošina integrētu lietotāja pieredzi programmās.</span><span class="sxs-lookup"><span data-stu-id="24c1b-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Datu relācija starp programmām](media/dual-write-overview.jpg)

<span data-ttu-id="24c1b-112">Duālajam ierakstam ir divi aspekti: *infrastruktūras* aspekts un *programmas* aspekts.</span><span class="sxs-lookup"><span data-stu-id="24c1b-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="24c1b-113">Infrastruktūra</span><span class="sxs-lookup"><span data-stu-id="24c1b-113">Infrastructure</span></span>

<span data-ttu-id="24c1b-114">Duālā ieraksta infrastruktūra ir paplašināma un uzticama, un tajā ir iekļauti šādi galvenie līdzekļi:</span><span class="sxs-lookup"><span data-stu-id="24c1b-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="24c1b-115">Sinhrona un divvirzienu datu plūsma starp programmām</span><span class="sxs-lookup"><span data-stu-id="24c1b-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="24c1b-116">Sinhronizācija kopā ar atskaņošanas, pauzes un izlīdzināšanas režīmiem, lai atbalstītu sistēmu tiešsaistes un bezsaistes/asinhrono režīmu laikā.</span><span class="sxs-lookup"><span data-stu-id="24c1b-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="24c1b-117">Iespēja sinhronizēt sākotnējos datus starp programmām</span><span class="sxs-lookup"><span data-stu-id="24c1b-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="24c1b-118">Kombinētais darbību un kļūdu žurnālu skats datu administratoriem</span><span class="sxs-lookup"><span data-stu-id="24c1b-118">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="24c1b-119">Iespēja konfigurēt pielāgotus brīdinājumus un sliekšņus un pieteikties paziņojumiem</span><span class="sxs-lookup"><span data-stu-id="24c1b-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="24c1b-120">Intuitīvs lietotāja interfeiss (UI) filtrēšanai un pārveidei</span><span class="sxs-lookup"><span data-stu-id="24c1b-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="24c1b-121">Iespēja iestatīt un skatīt elementu atkarības un attiecības</span><span class="sxs-lookup"><span data-stu-id="24c1b-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="24c1b-122">Paplašināmība gan standarta, gan pielāgotajām tabulām un kartēm</span><span class="sxs-lookup"><span data-stu-id="24c1b-122">Extensibility for both standard and custom tables and maps</span></span>
+ <span data-ttu-id="24c1b-123">Uzticama programmas dzīves cikla pārvaldība</span><span class="sxs-lookup"><span data-stu-id="24c1b-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="24c1b-124">Standarta iestatījumu pieredze jauniem debitoriem</span><span class="sxs-lookup"><span data-stu-id="24c1b-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="24c1b-125">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="24c1b-125">Application</span></span>

<span data-ttu-id="24c1b-126">Duālais ieraksts izveido kartēšanu starp koncepcijām Finance and Operations programmās un koncepcijās, kas iekļautas Customer Engagement programmās.</span><span class="sxs-lookup"><span data-stu-id="24c1b-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="24c1b-127">Šī integrācija atbalsta šādus scenārijus:</span><span class="sxs-lookup"><span data-stu-id="24c1b-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="24c1b-128">Integrētie debitoru pamatdati</span><span class="sxs-lookup"><span data-stu-id="24c1b-128">Integrated customer master</span></span>
+ <span data-ttu-id="24c1b-129">Piekļuve klientu lojalitātes programmas kartēm un atlīdzības punktiem</span><span class="sxs-lookup"><span data-stu-id="24c1b-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="24c1b-130">Vienota preču šablonu pieredze</span><span class="sxs-lookup"><span data-stu-id="24c1b-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="24c1b-131">Organizācijas hierarhijas apzināšanās</span><span class="sxs-lookup"><span data-stu-id="24c1b-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="24c1b-132">Integrētie kreditoru pamatdati</span><span class="sxs-lookup"><span data-stu-id="24c1b-132">Integrated vendor master</span></span>
+ <span data-ttu-id="24c1b-133">Piekļuve finanšu un nodokļu atsauces datiem</span><span class="sxs-lookup"><span data-stu-id="24c1b-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="24c1b-134">Cenas programmas pieredze pēc pieprasījuma</span><span class="sxs-lookup"><span data-stu-id="24c1b-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="24c1b-135">Integrēta "no potenciālā klienta uz naudu" tipa pieredze</span><span class="sxs-lookup"><span data-stu-id="24c1b-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="24c1b-136">Iespēja apkalpot gan iekšējos līdzekļus, gan debitora līdzekļus, izmantojot uz vietas esošos aģentus</span><span class="sxs-lookup"><span data-stu-id="24c1b-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="24c1b-137">Integrēta piegādes-apmaksas pieredze</span><span class="sxs-lookup"><span data-stu-id="24c1b-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="24c1b-138">Klienta datu un dokumentu integrētās aktivitātes un piezīmes</span><span class="sxs-lookup"><span data-stu-id="24c1b-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="24c1b-139">Iespēja meklēt rīcībā esošo krājumu pieejamību un detalizētu informāciju</span><span class="sxs-lookup"><span data-stu-id="24c1b-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="24c1b-140">"Projekta-naudas" pieredze</span><span class="sxs-lookup"><span data-stu-id="24c1b-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="24c1b-141">Iespēja apstrādāt vairākas adreses un lomas, izmantojot puses koncepciju</span><span class="sxs-lookup"><span data-stu-id="24c1b-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="24c1b-142">Viena avota pārvaldība lietotājiem</span><span class="sxs-lookup"><span data-stu-id="24c1b-142">Single source management for users</span></span>
+ <span data-ttu-id="24c1b-143">Integrētie kanāli mazumtirdzniecībai un mārketingam</span><span class="sxs-lookup"><span data-stu-id="24c1b-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="24c1b-144">Ieskats akcijās un atlaidēs</span><span class="sxs-lookup"><span data-stu-id="24c1b-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="24c1b-145">Pakalpojuma pieprasījuma funkcijas</span><span class="sxs-lookup"><span data-stu-id="24c1b-145">Request-for-service functions</span></span>
+ <span data-ttu-id="24c1b-146">Racionalizētas pakalpojuma darbības</span><span class="sxs-lookup"><span data-stu-id="24c1b-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="24c1b-147">Galvenie iemesli duālā ieraksta lietošanai</span><span class="sxs-lookup"><span data-stu-id="24c1b-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="24c1b-148">Duālais ieraksts nodrošina datu integrāciju Microsoft Dynamics 365 programmās.</span><span class="sxs-lookup"><span data-stu-id="24c1b-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="24c1b-149">Šīs spēcīgās struktūras saista vides un ļauj dažādām biznesa programmām strādāt kopā.</span><span class="sxs-lookup"><span data-stu-id="24c1b-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="24c1b-150">Lūk, galvenie iemesli, kāpēc jums jāizmanto duālais ieraksts:</span><span class="sxs-lookup"><span data-stu-id="24c1b-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="24c1b-151">Duālais ieraksts nodrošina cieši saistītu, gandrīz reāllaika un divvirzienu integrāciju starp Finance and Operations programmām un modeļa vadītām programmām pakalpojumā Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="24c1b-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="24c1b-152">Šī integrācija padara Microsoft Dynamics 365 par vienas pieturas aģentūru visiem jūsu biznesa risinājumiem.</span><span class="sxs-lookup"><span data-stu-id="24c1b-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="24c1b-153">Klienti, kuri lieto Dynamics 365 Finance un Dynamics 365 Supply Chain Management, bet kas neizmanto Microsoft risinājumus klientu attiecību pārvaldībai (CRM), pāriet uz Dynamics 365 tā duālā ieraksta atbalsta dēļ.</span><span class="sxs-lookup"><span data-stu-id="24c1b-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="24c1b-154">Dati no debitoriem, precēm, operācijām, projektiem, kā arī no lietu interneta (IoT) tiek automātiski pārsūtīti uz Dataverse ar duālo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="24c1b-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Dataverse through dual-write.</span></span> <span data-ttu-id="24c1b-155">Šis savienojums ir noderīgs uzņēmumiem, kas ir ieinteresēti Power Platform paplašināšanā.</span><span class="sxs-lookup"><span data-stu-id="24c1b-155">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="24c1b-156">Duālā ieraksta infrastruktūrā tiek ievērots bezkoda/zemā koda princips.</span><span class="sxs-lookup"><span data-stu-id="24c1b-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="24c1b-157">Ir nepieciešami minimāli tehniskie pūliņi, lai paplašinātu standarta "no tabulas līdz tabulai" kartes un iekļautu pielāgotas kartes.</span><span class="sxs-lookup"><span data-stu-id="24c1b-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="24c1b-158">Duālais ieraksts atbalsta gan tiešsaistes, gan bezsaistes režīmu.</span><span class="sxs-lookup"><span data-stu-id="24c1b-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="24c1b-159">Microsoft ir vienīgais uzņēmums, kas piedāvā atbalstu tiešsaistes un bezsaistes režīmiem.</span><span class="sxs-lookup"><span data-stu-id="24c1b-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="24c1b-160">Ko duālais ieraksts nozīmē Customer Engagement programmu izstrādātājiem un arhitektiem?</span><span class="sxs-lookup"><span data-stu-id="24c1b-160">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="24c1b-161">Duālais ieraksts automatizē datu plūsmu starp Finance and Operations programmām un Customer Engagement programmām.</span><span class="sxs-lookup"><span data-stu-id="24c1b-161">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="24c1b-162">Duālais ieraksts sastāv no diviem AppSource risinājumiem, kas ir instalēti risinājumā Dataverse.</span><span class="sxs-lookup"><span data-stu-id="24c1b-162">Dual-write consists of two AppSource solutions that are installed on Dataverse.</span></span> <span data-ttu-id="24c1b-163">Risinājumi paplašina elementu shēmu, spraudņus un darbplūsmas risinājumā Dataverse , lai tās varētu mērogot līdz ERP lielumam.</span><span class="sxs-lookup"><span data-stu-id="24c1b-163">The solutions expand the entity schema, plugins, and workflows on Dataverse so that they can scale to ERP size.</span></span> <span data-ttu-id="24c1b-164">Veiksmīgai īstenošanai Customer Engagement programma, izstrādātājiem un arhitektiem ir jāsaprot šīs izmaiņas un jāsadarbojas ar kolēģiem Finance and Operations lietojumprogrammās.</span><span class="sxs-lookup"><span data-stu-id="24c1b-164">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="24c1b-165">Lai izveidotu paritāti ar Finance and Operations pieteikumiem, duālais ieraksts veic dažas būtiskas izmaiņas Dataverse shēmā.</span><span class="sxs-lookup"><span data-stu-id="24c1b-165">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Dataverse schema.</span></span> <span data-ttu-id="24c1b-166">Ja jūs saprotat plānu, varat izvairīties no daļas no dizaina un attīstības pārstrādāšanas nākotnē.</span><span class="sxs-lookup"><span data-stu-id="24c1b-166">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="24c1b-167">Kad duālā ieraksta AppSource pakotne ir instalēta, risinājumam Dataverse būs jauni jēdzieni, piemēram, uzņēmums un puse.</span><span class="sxs-lookup"><span data-stu-id="24c1b-167">When the dual-write AppSource package is installed, Dataverse will have new concepts such as company and party.</span></span> <span data-ttu-id="24c1b-168">Šie jēdzieni palīdz lietojumprogrammām iebūvēt Dataverse, ieskaitot Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, un Dynamics 365 Field Service, lai mijiedarbotos ar Finance and Operations programmām.</span><span class="sxs-lookup"><span data-stu-id="24c1b-168">These concepts help applications built on Dataverse, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="24c1b-169">Aktivitātes un piezīmes ir vienotas un paplašinātas, lai atbalstītu gan C1 (sistēmas lietotājus), gan C2 (sistēmas klientus).</span><span class="sxs-lookup"><span data-stu-id="24c1b-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="24c1b-170">Lai izvairītos no datu zuduma valūtas pārraidīšanas laikā starp Finance and Operations programmām un Dataverse, jūs varēsiet paplašināt decimāldaļas vietu skaitu Customer Engagement programmu valūtas datu veidā.</span><span class="sxs-lookup"><span data-stu-id="24c1b-170">To prevent data loss during currency transmission between Finance and Operations apps and the Dataverse, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="24c1b-171">Līdzeklis pārtulko esošas rindas jaunajā paplašinātajā stāvoklī metadatu slānī.</span><span class="sxs-lookup"><span data-stu-id="24c1b-171">The feature autotranslates existing rows to the new extended state at the metadata layer.</span></span> <span data-ttu-id="24c1b-172">Šī procesa laikā valūtas vērtība tiek pārrēķināta uz decimālajiem datiem, nevis naudas datiem, un valūtas vērtība atbalsta 10 decimāldaļu vietas.</span><span class="sxs-lookup"><span data-stu-id="24c1b-172">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="24c1b-173">Šis līdzeklis ir izvēles iespēja, un organizācijām, kurām nav nepieciešams vairāk par 4 decimāldaļas cipariem, nav jāpiesakās.</span><span class="sxs-lookup"><span data-stu-id="24c1b-173">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="24c1b-174">Lai iegūtu papildu informāciju, skatiet [Valūtas datu veida migrācija duālajam ierakstam](currrency-decimal-places.md).</span><span class="sxs-lookup"><span data-stu-id="24c1b-174">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="24c1b-175">[Datuma efektivitāte](../../dev-tools/date-effectivity.md) tiks pievienota Dataverse.</span><span class="sxs-lookup"><span data-stu-id="24c1b-175">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Dataverse.</span></span> <span data-ttu-id="24c1b-176">Tā atbalstīs pagātnes, tagadnes un nākotnes datus vienā elementā.</span><span class="sxs-lookup"><span data-stu-id="24c1b-176">It will support past, present, and future data on the same entity.</span></span>

+ <span data-ttu-id="24c1b-177">Preču [vienību pārveidošanas](../../../../supply-chain/pim/tasks/manage-unit-measure.md) tiek atbalstītas precēm, piedāvājumiem, pasūtījumiem un rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="24c1b-177">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="24c1b-178">Papildinformāciju par gaidāmajām izmaiņām skatiet sadaļā [Kas jauns vai mainīts duālā rakstā](whats-new-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="24c1b-178">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>


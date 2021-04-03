---
title: Duālā ieraksta pārskats
description: Duālais ieraksts ir standarta infrastruktūra, kas nodrošina gandrīz reāllaika mijiedarbību starp Customer Engagement programmām un Finance and Operations programmām.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6cc02b483a2975dd3be28032ea7e90b540945492
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561282"
---
# <a name="dual-write-overview"></a><span data-ttu-id="e9a85-103">Duālā ieraksta pārskats</span><span class="sxs-lookup"><span data-stu-id="e9a85-103">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="e9a85-104">Kas ir duālais ieraksts?</span><span class="sxs-lookup"><span data-stu-id="e9a85-104">What is dual-write?</span></span>

<span data-ttu-id="e9a85-105">Duālais ieraksts ir standarta infrastruktūra, kas nodrošina gandrīz reāllaika mijiedarbību starp Customer Engagement programmām un Finance and Operations programmām.</span><span class="sxs-lookup"><span data-stu-id="e9a85-105">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="e9a85-106">Kad dati par debitoriem, precēm, cilvēkiem un operācijām pārsniedz programmas robežas, tiek nodrošinātas visas organizācijas struktūrvienības.</span><span class="sxs-lookup"><span data-stu-id="e9a85-106">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="e9a85-107">Duālais ieraksts nodrošina cieši saistītu divvirzienu integrāciju starp Finance and Operations programmām un Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e9a85-107">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="e9a85-108">Visas Finance and Operations programmas datu izmaiņas izraisa Dataverse ierakstus, un jebkuras datu izmaiņas, kas rodas Dataverse rada ierakstus Finance and Operations programmām.</span><span class="sxs-lookup"><span data-stu-id="e9a85-108">Any data change in Finance and Operations apps causes writes to Dataverse, and any data change in Dataverse causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="e9a85-109">Šī automatizētā datu plūsma nodrošina integrētu lietotāja pieredzi programmās.</span><span class="sxs-lookup"><span data-stu-id="e9a85-109">This automated data flow provides an integrated user experience across the apps.</span></span>

![Datu relācija starp programmām](media/dual-write-overview.jpg)

<span data-ttu-id="e9a85-111">Duālajam ierakstam ir divi aspekti: *infrastruktūras* aspekts un *programmas* aspekts.</span><span class="sxs-lookup"><span data-stu-id="e9a85-111">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="e9a85-112">Infrastruktūra</span><span class="sxs-lookup"><span data-stu-id="e9a85-112">Infrastructure</span></span>

<span data-ttu-id="e9a85-113">Duālā ieraksta infrastruktūra ir paplašināma un uzticama, un tajā ir iekļauti šādi galvenie līdzekļi:</span><span class="sxs-lookup"><span data-stu-id="e9a85-113">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="e9a85-114">Sinhrona un divvirzienu datu plūsma starp programmām</span><span class="sxs-lookup"><span data-stu-id="e9a85-114">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="e9a85-115">Sinhronizācija kopā ar atskaņošanas, pauzes un izlīdzināšanas režīmiem, lai atbalstītu sistēmu tiešsaistes un bezsaistes/asinhrono režīmu laikā.</span><span class="sxs-lookup"><span data-stu-id="e9a85-115">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="e9a85-116">Iespēja sinhronizēt sākotnējos datus starp programmām</span><span class="sxs-lookup"><span data-stu-id="e9a85-116">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="e9a85-117">Kombinētais darbību un kļūdu žurnālu skats datu administratoriem</span><span class="sxs-lookup"><span data-stu-id="e9a85-117">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="e9a85-118">Iespēja konfigurēt pielāgotus brīdinājumus un sliekšņus un pieteikties paziņojumiem</span><span class="sxs-lookup"><span data-stu-id="e9a85-118">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="e9a85-119">Intuitīvs lietotāja interfeiss (UI) filtrēšanai un pārveidei</span><span class="sxs-lookup"><span data-stu-id="e9a85-119">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="e9a85-120">Iespēja iestatīt un skatīt tabulu atkarības un attiecības</span><span class="sxs-lookup"><span data-stu-id="e9a85-120">Ability to set and view table dependencies and relationships</span></span>
+ <span data-ttu-id="e9a85-121">Paplašināmība gan standarta, gan pielāgotajām tabulām un kartēm</span><span class="sxs-lookup"><span data-stu-id="e9a85-121">Extensibility for both standard and custom tables and maps</span></span>
+ <span data-ttu-id="e9a85-122">Uzticama programmas dzīves cikla pārvaldība</span><span class="sxs-lookup"><span data-stu-id="e9a85-122">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="e9a85-123">Standarta iestatījumu pieredze jauniem debitoriem</span><span class="sxs-lookup"><span data-stu-id="e9a85-123">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="e9a85-124">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="e9a85-124">Application</span></span>

<span data-ttu-id="e9a85-125">Duālais ieraksts izveido kartēšanu starp koncepcijām Finance and Operations programmās un koncepcijās, kas iekļautas Customer Engagement programmās.</span><span class="sxs-lookup"><span data-stu-id="e9a85-125">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="e9a85-126">Šī integrācija atbalsta šādus scenārijus:</span><span class="sxs-lookup"><span data-stu-id="e9a85-126">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="e9a85-127">Integrētie debitoru pamatdati</span><span class="sxs-lookup"><span data-stu-id="e9a85-127">Integrated customer master</span></span>
+ <span data-ttu-id="e9a85-128">Piekļuve klientu lojalitātes programmas kartēm un atlīdzības punktiem</span><span class="sxs-lookup"><span data-stu-id="e9a85-128">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="e9a85-129">Vienota preču šablonu pieredze</span><span class="sxs-lookup"><span data-stu-id="e9a85-129">Unified product mastering experience</span></span>
+ <span data-ttu-id="e9a85-130">Organizācijas hierarhijas apzināšanās</span><span class="sxs-lookup"><span data-stu-id="e9a85-130">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="e9a85-131">Integrētie kreditoru pamatdati</span><span class="sxs-lookup"><span data-stu-id="e9a85-131">Integrated vendor master</span></span>
+ <span data-ttu-id="e9a85-132">Piekļuve finanšu un nodokļu atsauces datiem</span><span class="sxs-lookup"><span data-stu-id="e9a85-132">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="e9a85-133">Cenas programmas pieredze pēc pieprasījuma</span><span class="sxs-lookup"><span data-stu-id="e9a85-133">On-demand price engine experience</span></span>
+ <span data-ttu-id="e9a85-134">Integrēta "no potenciālā klienta uz naudu" tipa pieredze</span><span class="sxs-lookup"><span data-stu-id="e9a85-134">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="e9a85-135">Iespēja apkalpot gan iekšējos līdzekļus, gan debitora līdzekļus, izmantojot uz vietas esošos aģentus</span><span class="sxs-lookup"><span data-stu-id="e9a85-135">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="e9a85-136">Integrēta piegādes-apmaksas pieredze</span><span class="sxs-lookup"><span data-stu-id="e9a85-136">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="e9a85-137">Klienta datu un dokumentu integrētās aktivitātes un piezīmes</span><span class="sxs-lookup"><span data-stu-id="e9a85-137">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="e9a85-138">Iespēja meklēt rīcībā esošo krājumu pieejamību un detalizētu informāciju</span><span class="sxs-lookup"><span data-stu-id="e9a85-138">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="e9a85-139">"Projekta-naudas" pieredze</span><span class="sxs-lookup"><span data-stu-id="e9a85-139">Project-to-cash experience</span></span>
+ <span data-ttu-id="e9a85-140">Iespēja apstrādāt vairākas adreses un lomas, izmantojot puses koncepciju</span><span class="sxs-lookup"><span data-stu-id="e9a85-140">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="e9a85-141">Viena avota pārvaldība lietotājiem</span><span class="sxs-lookup"><span data-stu-id="e9a85-141">Single source management for users</span></span>
+ <span data-ttu-id="e9a85-142">Integrētie kanāli mazumtirdzniecībai un mārketingam</span><span class="sxs-lookup"><span data-stu-id="e9a85-142">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="e9a85-143">Ieskats akcijās un atlaidēs</span><span class="sxs-lookup"><span data-stu-id="e9a85-143">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="e9a85-144">Pakalpojuma pieprasījuma funkcijas</span><span class="sxs-lookup"><span data-stu-id="e9a85-144">Request-for-service functions</span></span>
+ <span data-ttu-id="e9a85-145">Racionalizētas pakalpojuma darbības</span><span class="sxs-lookup"><span data-stu-id="e9a85-145">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="e9a85-146">Galvenie iemesli duālā ieraksta lietošanai</span><span class="sxs-lookup"><span data-stu-id="e9a85-146">Top reasons to use dual-write</span></span>

<span data-ttu-id="e9a85-147">Duālais ieraksts nodrošina datu integrāciju Microsoft Dynamics 365 programmās.</span><span class="sxs-lookup"><span data-stu-id="e9a85-147">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="e9a85-148">Šīs spēcīgās struktūras saista vides un ļauj dažādām biznesa programmām strādāt kopā.</span><span class="sxs-lookup"><span data-stu-id="e9a85-148">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="e9a85-149">Lūk, galvenie iemesli, kāpēc jums jāizmanto duālais ieraksts:</span><span class="sxs-lookup"><span data-stu-id="e9a85-149">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="e9a85-150">Duālais ieraksts nodrošina cieši saistītu, gandrīz reāllaika un divvirzienu integrāciju starp Finance and Operations programmām un modeļa vadītām programmām pakalpojumā Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e9a85-150">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="e9a85-151">Šī integrācija padara Microsoft Dynamics 365 par vienas pieturas aģentūru visiem jūsu biznesa risinājumiem.</span><span class="sxs-lookup"><span data-stu-id="e9a85-151">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="e9a85-152">Klienti, kuri lieto Dynamics 365 Finance un Dynamics 365 Supply Chain Management, bet kas neizmanto Microsoft risinājumus klientu attiecību pārvaldībai (CRM), pāriet uz Dynamics 365 tā duālā ieraksta atbalsta dēļ.</span><span class="sxs-lookup"><span data-stu-id="e9a85-152">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="e9a85-153">Dati no debitoriem, precēm, operācijām, projektiem, kā arī no lietu interneta (IoT) tiek automātiski pārsūtīti uz Dataverse ar duālo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="e9a85-153">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Dataverse through dual-write.</span></span> <span data-ttu-id="e9a85-154">Šis savienojums ir noderīgs uzņēmumiem, kas ir ieinteresēti Power Platform paplašināšanā.</span><span class="sxs-lookup"><span data-stu-id="e9a85-154">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="e9a85-155">Duālā ieraksta infrastruktūrā tiek ievērots bezkoda/zemā koda princips.</span><span class="sxs-lookup"><span data-stu-id="e9a85-155">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="e9a85-156">Ir nepieciešami minimāli tehniskie pūliņi, lai paplašinātu standarta "no tabulas līdz tabulai" kartes un iekļautu pielāgotas kartes.</span><span class="sxs-lookup"><span data-stu-id="e9a85-156">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="e9a85-157">Duālais ieraksts atbalsta gan tiešsaistes, gan bezsaistes režīmu.</span><span class="sxs-lookup"><span data-stu-id="e9a85-157">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="e9a85-158">Microsoft ir vienīgais uzņēmums, kas piedāvā atbalstu tiešsaistes un bezsaistes režīmiem.</span><span class="sxs-lookup"><span data-stu-id="e9a85-158">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="e9a85-159">Ko duālais ieraksts nozīmē Customer Engagement programmu izstrādātājiem un arhitektiem?</span><span class="sxs-lookup"><span data-stu-id="e9a85-159">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="e9a85-160">Duālais ieraksts automatizē datu plūsmu starp Finance and Operations programmām un Customer Engagement programmām.</span><span class="sxs-lookup"><span data-stu-id="e9a85-160">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="e9a85-161">Duālais ieraksts sastāv no diviem AppSource risinājumiem, kas ir instalēti risinājumā Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e9a85-161">Dual-write consists of two AppSource solutions that are installed on Dataverse.</span></span> <span data-ttu-id="e9a85-162">Risinājumi paplašina tabulu shēmu, spraudņus un darbplūsmas risinājumā Dataverse , lai tās varētu mērogot līdz ERP lielumam.</span><span class="sxs-lookup"><span data-stu-id="e9a85-162">The solutions expand the table schema, plugins, and workflows on Dataverse so that they can scale to ERP size.</span></span> <span data-ttu-id="e9a85-163">Veiksmīgai īstenošanai Customer Engagement programma, izstrādātājiem un arhitektiem ir jāsaprot šīs izmaiņas un jāsadarbojas ar kolēģiem Finance and Operations lietojumprogrammās.</span><span class="sxs-lookup"><span data-stu-id="e9a85-163">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="e9a85-164">Lai izveidotu paritāti ar Finance and Operations pieteikumiem, duālais ieraksts veic dažas būtiskas izmaiņas Dataverse shēmā.</span><span class="sxs-lookup"><span data-stu-id="e9a85-164">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Dataverse schema.</span></span> <span data-ttu-id="e9a85-165">Ja jūs saprotat plānu, varat izvairīties no daļas no dizaina un attīstības pārstrādāšanas nākotnē.</span><span class="sxs-lookup"><span data-stu-id="e9a85-165">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="e9a85-166">Kad duālā ieraksta AppSource pakotne ir instalēta, risinājumam Dataverse būs jauni jēdzieni, piemēram, uzņēmums un puse.</span><span class="sxs-lookup"><span data-stu-id="e9a85-166">When the dual-write AppSource package is installed, Dataverse will have new concepts such as company and party.</span></span> <span data-ttu-id="e9a85-167">Šie jēdzieni palīdz lietojumprogrammām iebūvēt Dataverse, ieskaitot Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, un Dynamics 365 Field Service, lai mijiedarbotos ar Finance and Operations programmām.</span><span class="sxs-lookup"><span data-stu-id="e9a85-167">These concepts help applications built on Dataverse, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="e9a85-168">Aktivitātes un piezīmes ir vienotas un paplašinātas, lai atbalstītu gan C1 (sistēmas lietotājus), gan C2 (sistēmas klientus).</span><span class="sxs-lookup"><span data-stu-id="e9a85-168">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="e9a85-169">Lai izvairītos no datu zuduma valūtas pārraidīšanas laikā starp Finance and Operations programmām un Dataverse, jūs varēsiet paplašināt decimāldaļas vietu skaitu Customer Engagement programmu valūtas datu veidā.</span><span class="sxs-lookup"><span data-stu-id="e9a85-169">To prevent data loss during currency transmission between Finance and Operations apps and the Dataverse, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="e9a85-170">Līdzeklis pārtulko esošas rindas jaunajā paplašinātajā stāvoklī metadatu slānī.</span><span class="sxs-lookup"><span data-stu-id="e9a85-170">The feature autotranslates existing rows to the new extended state at the metadata layer.</span></span> <span data-ttu-id="e9a85-171">Šī procesa laikā valūtas vērtība tiek pārrēķināta uz decimālajiem datiem, nevis naudas datiem, un valūtas vērtība atbalsta 10 decimāldaļu vietas.</span><span class="sxs-lookup"><span data-stu-id="e9a85-171">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="e9a85-172">Šis līdzeklis ir izvēles iespēja, un organizācijām, kurām nav nepieciešams vairāk par 4 decimāldaļas cipariem, nav jāpiesakās.</span><span class="sxs-lookup"><span data-stu-id="e9a85-172">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="e9a85-173">Lai iegūtu papildu informāciju, skatiet [Valūtas datu veida migrācija duālajam ierakstam](currrency-decimal-places.md).</span><span class="sxs-lookup"><span data-stu-id="e9a85-173">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="e9a85-174">[Datuma efektivitāte](../../dev-tools/date-effectivity.md) tiks pievienota Dataverse.</span><span class="sxs-lookup"><span data-stu-id="e9a85-174">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Dataverse.</span></span> <span data-ttu-id="e9a85-175">Tā atbalstīs pagātnes, tagadnes un nākotnes datus vienā tabulā.</span><span class="sxs-lookup"><span data-stu-id="e9a85-175">It will support past, present, and future data on the same table.</span></span>

+ <span data-ttu-id="e9a85-176">Preču [vienību pārveidošanas](../../../../supply-chain/pim/tasks/manage-unit-measure.md) tiek atbalstītas precēm, piedāvājumiem, pasūtījumiem un rēķiniem.</span><span class="sxs-lookup"><span data-stu-id="e9a85-176">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="e9a85-177">Papildinformāciju par gaidāmajām izmaiņām skatiet sadaļā [Kas jauns vai mainīts duālā rakstā](whats-new-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="e9a85-177">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
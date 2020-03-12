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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 12c6a39700a260c138fab67ed370f94b3aa04213
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/20/2020
ms.locfileid: "3075994"
---
# <a name="dual-write-overview"></a><span data-ttu-id="fba79-104">Duālā ieraksta pārskats</span><span class="sxs-lookup"><span data-stu-id="fba79-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

## <a name="what-is-dual-write"></a><span data-ttu-id="fba79-105">Kas ir duālais ieraksts?</span><span class="sxs-lookup"><span data-stu-id="fba79-105">What is dual-write?</span></span>

<span data-ttu-id="fba79-106">Duālais ieraksts ir standarta infrastruktūra, kas nodrošina gandrīz reāllaika mijiedarbību starp Microsoft Dynamics 365 modeļa vadītajām programmām un Finance and Operations programmām.</span><span class="sxs-lookup"><span data-stu-id="fba79-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="fba79-107">Kad dati par debitoriem, precēm, cilvēkiem un operācijām pārsniedz programmas robežas, tiek nodrošinātas visas organizācijas struktūrvienības.</span><span class="sxs-lookup"><span data-stu-id="fba79-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="fba79-108">Duālais ieraksts nodrošina cieši saistītu divvirzienu integrāciju starp Finance and Operations programmām un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fba79-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="fba79-109">Visas Finance and Operations programmas datu izmaiņas izraisa Common Data Service ierakstus, un jebkuras datu izmaiņas, kas rodas Common Data Service rada ierakstus Finance and Operations programmām.</span><span class="sxs-lookup"><span data-stu-id="fba79-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="fba79-110">Šī automatizētā datu plūsma nodrošina integrētu lietotāja pieredzi programmās.</span><span class="sxs-lookup"><span data-stu-id="fba79-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Datu relācija starp programmām](media/dual-write-overview.jpg)

<span data-ttu-id="fba79-112">Duālajam ierakstam ir divi aspekti: *infrastruktūras* aspekts un *programmas* aspekts.</span><span class="sxs-lookup"><span data-stu-id="fba79-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="fba79-113">Infrastruktūra</span><span class="sxs-lookup"><span data-stu-id="fba79-113">Infrastructure</span></span>

<span data-ttu-id="fba79-114">Duālā ieraksta infrastruktūra ir paplašināma un uzticama, un tajā ir iekļauti šādi galvenie līdzekļi:</span><span class="sxs-lookup"><span data-stu-id="fba79-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="fba79-115">Sinhrona un divvirzienu datu plūsma starp programmām</span><span class="sxs-lookup"><span data-stu-id="fba79-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="fba79-116">Sinhronizācija kopā ar atskaņošanas, pauzes un izlīdzināšanas režīmiem, lai atbalstītu sistēmu tiešsaistes un bezsaistes/asinhrono režīmu laikā.</span><span class="sxs-lookup"><span data-stu-id="fba79-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="fba79-117">Iespēja sinhronizēt sākotnējos datus starp programmām</span><span class="sxs-lookup"><span data-stu-id="fba79-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="fba79-118">Konsolidētais darbību un kļūdu žurnālu skats datu administratoriem</span><span class="sxs-lookup"><span data-stu-id="fba79-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="fba79-119">Iespēja konfigurēt pielāgotus brīdinājumus un sliekšņus un pieteikties paziņojumiem</span><span class="sxs-lookup"><span data-stu-id="fba79-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="fba79-120">Intuitīvs lietotāja interfeiss (UI) filtrēšanai un pārveidei</span><span class="sxs-lookup"><span data-stu-id="fba79-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="fba79-121">Iespēja iestatīt un skatīt elementu atkarības un attiecības</span><span class="sxs-lookup"><span data-stu-id="fba79-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="fba79-122">Paplašināmība gan standarta, gan pielāgotajām entītijām un kartēm</span><span class="sxs-lookup"><span data-stu-id="fba79-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="fba79-123">Uzticama programmas dzīves cikla pārvaldība</span><span class="sxs-lookup"><span data-stu-id="fba79-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="fba79-124">Standarta iestatījumu pieredze jauniem debitoriem</span><span class="sxs-lookup"><span data-stu-id="fba79-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="fba79-125">Pieteikums</span><span class="sxs-lookup"><span data-stu-id="fba79-125">Application</span></span>

<span data-ttu-id="fba79-126">Duālais ieraksts izveido kartēšanu starp koncepcijām Finance and Operations programmās un koncepcijās, kas iekļautas modeļa vadītajās Dynamics 365 programmās.</span><span class="sxs-lookup"><span data-stu-id="fba79-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="fba79-127">Šī integrācija atbalsta šādus scenārijus:</span><span class="sxs-lookup"><span data-stu-id="fba79-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="fba79-128">Integrētie debitoru pamatdati</span><span class="sxs-lookup"><span data-stu-id="fba79-128">Integrated customer master</span></span>
+ <span data-ttu-id="fba79-129">Piekļuve klientu lojalitātes programmas kartēm un atlīdzības punktiem</span><span class="sxs-lookup"><span data-stu-id="fba79-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="fba79-130">Vienota preču šablonu pieredze</span><span class="sxs-lookup"><span data-stu-id="fba79-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="fba79-131">Organizācijas hierarhijas apzināšanās</span><span class="sxs-lookup"><span data-stu-id="fba79-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="fba79-132">Integrētie kreditoru pamatdati</span><span class="sxs-lookup"><span data-stu-id="fba79-132">Integrated vendor master</span></span>
+ <span data-ttu-id="fba79-133">Piekļuve finanšu un nodokļu atsauces datiem</span><span class="sxs-lookup"><span data-stu-id="fba79-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="fba79-134">Cenas programmas pieredze pēc pieprasījuma</span><span class="sxs-lookup"><span data-stu-id="fba79-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="fba79-135">Integrēta "no potenciālā klienta uz naudu" tipa pieredze</span><span class="sxs-lookup"><span data-stu-id="fba79-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="fba79-136">Iespēja apkalpot gan iekšējos līdzekļus, gan debitora līdzekļus, izmantojot uz vietas esošos aģentus</span><span class="sxs-lookup"><span data-stu-id="fba79-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="fba79-137">Integrēta piegādes-apmaksas pieredze</span><span class="sxs-lookup"><span data-stu-id="fba79-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="fba79-138">Klienta datu un dokumentu integrētās aktivitātes un piezīmes</span><span class="sxs-lookup"><span data-stu-id="fba79-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="fba79-139">Iespēja meklēt rīcībā esošo krājumu pieejamību un detalizētu informāciju</span><span class="sxs-lookup"><span data-stu-id="fba79-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="fba79-140">"Projekta-naudas" pieredze</span><span class="sxs-lookup"><span data-stu-id="fba79-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="fba79-141">Iespēja apstrādāt vairākas adreses un lomas, izmantojot puses koncepciju</span><span class="sxs-lookup"><span data-stu-id="fba79-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="fba79-142">Viena avota pārvaldība lietotājiem</span><span class="sxs-lookup"><span data-stu-id="fba79-142">Single source management for users</span></span>
+ <span data-ttu-id="fba79-143">Integrētie kanāli mazumtirdzniecībai un mārketingam</span><span class="sxs-lookup"><span data-stu-id="fba79-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="fba79-144">Ieskats akcijās un atlaidēs</span><span class="sxs-lookup"><span data-stu-id="fba79-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="fba79-145">Pakalpojuma pieprasījuma funkcijas</span><span class="sxs-lookup"><span data-stu-id="fba79-145">Request-for-service functions</span></span>
+ <span data-ttu-id="fba79-146">Racionalizētas pakalpojuma darbības</span><span class="sxs-lookup"><span data-stu-id="fba79-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="fba79-147">Galvenie iemesli duālā ieraksta lietošanai</span><span class="sxs-lookup"><span data-stu-id="fba79-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="fba79-148">Duālais ieraksts nodrošina datu integrāciju Microsoft Dynamics 365 programmās.</span><span class="sxs-lookup"><span data-stu-id="fba79-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="fba79-149">Šīs spēcīgās struktūras saista vides un ļauj dažādām biznesa programmām strādāt kopā.</span><span class="sxs-lookup"><span data-stu-id="fba79-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="fba79-150">Lūk, galvenie iemesli, kāpēc jums jāizmanto duālais ieraksts:</span><span class="sxs-lookup"><span data-stu-id="fba79-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="fba79-151">Duālais ieraksts nodrošina cieši saistītu, gandrīz reāllaika un divvirzienu integrāciju starp Finance and Operations programmām un modeļa vadītām programmām pakalpojumā Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fba79-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="fba79-152">Šī integrācija padara Microsoft Dynamics 365 par vienas pieturas aģentūru visiem jūsu biznesa risinājumiem.</span><span class="sxs-lookup"><span data-stu-id="fba79-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="fba79-153">Klienti, kuri lieto Dynamics 365 Finance un Dynamics 365 Supply Chain Management, bet kas neizmanto Microsoft risinājumus klientu attiecību pārvaldībai (CRM), pāriet uz Dynamics 365 tā duālā ieraksta atbalsta dēļ.</span><span class="sxs-lookup"><span data-stu-id="fba79-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="fba79-154">Dati no debitoriem, precēm, operācijām, projektiem, kā arī no lietu interneta (IoT) tiek automātiski pārsūtīti uz Common Data Service ar duālo ierakstu.</span><span class="sxs-lookup"><span data-stu-id="fba79-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="fba79-155">Šis savienojums ir ļoti noderīgs uzņēmumiem, kas ir ieinteresēti Microsoft Power Platform paplašināšanā.</span><span class="sxs-lookup"><span data-stu-id="fba79-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="fba79-156">Duālā ieraksta infrastruktūrā tiek ievērots bezkoda/zemā koda princips.</span><span class="sxs-lookup"><span data-stu-id="fba79-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="fba79-157">Ir nepieciešami minimāli tehniskie pūliņi, lai paplašinātu standarta "no tabulas līdz tabulai" kartes un iekļautu pielāgotas kartes.</span><span class="sxs-lookup"><span data-stu-id="fba79-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="fba79-158">Duālais ieraksts atbalsta gan tiešsaistes, gan bezsaistes režīmu.</span><span class="sxs-lookup"><span data-stu-id="fba79-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="fba79-159">Microsoft ir vienīgais uzņēmums, kas piedāvā atbalstu tiešsaistes un bezsaistes režīmiem.</span><span class="sxs-lookup"><span data-stu-id="fba79-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="fba79-160">Ko duālais ieraksts nozīmē CRM preču lietotājiem un arhitektiem?</span><span class="sxs-lookup"><span data-stu-id="fba79-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="fba79-161">Duālais ieraksts automatizē datu plūsmu starp Finance and Operations programmām un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fba79-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="fba79-162">Turpmākajos laidienos jēdzieni modeļa darbinātās programmās pakalpojumā Dynamics 365 (piemēram, klients, kontaktpersona, piedāvājums un pasūtījums) tiks mērogoti uz vidusmēra tirgu un vidusmēra tirgus klientiem.</span><span class="sxs-lookup"><span data-stu-id="fba79-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="fba79-163">Pirmajā laidienā lielākā daļa automatizācijas tiek apstrādāta ar duālā ieraksta risinājumiem.</span><span class="sxs-lookup"><span data-stu-id="fba79-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="fba79-164">Turpmākajos laidienos šie risinājumi kļūs par daļu no Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="fba79-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="fba79-165">Izprotot gaidāmās izmaiņas Common Data Service, jūs varat ietaupīt savus pūliņus ilgākā termiņā.</span><span class="sxs-lookup"><span data-stu-id="fba79-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="fba79-166">Dažas no būtiskām izmaiņām:</span><span class="sxs-lookup"><span data-stu-id="fba79-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="fba79-167">Common Data Service būs jaunas koncepcijas, piemēram, uzņēmums un puse.</span><span class="sxs-lookup"><span data-stu-id="fba79-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="fba79-168">Šīs koncepcijas ietekmēs visas programmas, kas ir iebūvētas Common Data Service, piemēram, Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service un Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="fba79-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="fba79-169">Aktivitātes un piezīmes ir vienotas un paplašinātas, lai atbalstītu gan C1 (sistēmas lietotājus), gan C2 (sistēmas klientus).</span><span class="sxs-lookup"><span data-stu-id="fba79-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="fba79-170">Dažas no gaidāmajām Common Data Service izmaiņām:</span><span class="sxs-lookup"><span data-stu-id="fba79-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="fba79-171">Decimālais datu tips aizstās naudas datu tipu.</span><span class="sxs-lookup"><span data-stu-id="fba79-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="fba79-172">Datu efektivitāte atbalstīs pagātnes, tagadnes un nākotnes datus vienuviet.</span><span class="sxs-lookup"><span data-stu-id="fba79-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="fba79-173">Būs vairāk atbalsta valūtas un maiņas kursiem, un tiks pārskatīts **Maiņas kursa** programmu programmēšanas interfeiss (API).</span><span class="sxs-lookup"><span data-stu-id="fba79-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="fba79-174">Tiks atbalstīta mērvienību konvertēšana.</span><span class="sxs-lookup"><span data-stu-id="fba79-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="fba79-175">Lai iegūtu papildu informāciju par gaidāmajām izmaiņām, skatiet šeit: [Dati Common Data Service– 1. un 2. fāze](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap).</span><span class="sxs-lookup"><span data-stu-id="fba79-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/extensibility/extensibility-roadmap).</span></span>

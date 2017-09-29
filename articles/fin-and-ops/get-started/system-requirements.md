---
title: "Sistēmas prasības mākoņa izvietojumiem"
description: "Šajā tēmā ir uzskaitītas sistēmas prasības pašreizējai Microsoft Dynamics 365 for Finance and Operations Enterprise edition versijai mākoņa izvietojumiem."
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 5230911e1febc66b294f1331846373a472789adf
ms.openlocfilehash: 46eacb2a01c3bfcc7144c7d8c39ee0189fd72e16
ms.contentlocale: lv-lv
ms.lasthandoff: 08/04/2017

---

# <a name="system-requirements-for-cloud-deployments"></a><span data-ttu-id="e1018-103">Sistēmas prasības mākoņa izvietojumiem</span><span class="sxs-lookup"><span data-stu-id="e1018-103">System requirements for cloud deployments</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e1018-104">Šajā tēmā ir uzskaitītas sistēmas prasības pašreizējai Microsoft Dynamics 365 for Finance and Operations Enterprise edition versijai mākoņa izvietojumiem.</span><span class="sxs-lookup"><span data-stu-id="e1018-104">This topic lists the system requirements for the current version of Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, for cloud deployments.</span></span> <span data-ttu-id="e1018-105">Pirms Finance and Operations instalēšanas, ja nepieciešams, pārbaudiet, vai jūsu izmantotā sistēma atbilst minimālajām tīkla, aparatūras un programmatūras prasībām vai pārsniedz tās.</span><span class="sxs-lookup"><span data-stu-id="e1018-105">Before you install Finance and Operations, when this step is appropriate, verify that the system that you're working with meets or exceeds the minimum network, hardware, and software requirements.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="e1018-106">Atbalstītās tīmekļa pārlūkprogrammas</span><span class="sxs-lookup"><span data-stu-id="e1018-106">Supported web browsers</span></span>
<span data-ttu-id="e1018-107">Tīmekļa programmu var palaist jebkurā no tālāk uzskaitītajām tīmekļa pārlūkprogrammām, kas darbojas norādītajās operētājsistēmās.</span><span class="sxs-lookup"><span data-stu-id="e1018-107">The web application can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="e1018-108">Microsoft Edge (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10</span><span class="sxs-lookup"><span data-stu-id="e1018-108">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="e1018-109">Internet Explorer 11 operētājsistēmā Windows 10, Windows 8.1 vai Windows 7</span><span class="sxs-lookup"><span data-stu-id="e1018-109">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="e1018-110">Google Chrome (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10, Windows 8.1, Windows 8, Windows 7 vai Google Nexus 10 planšetdatorā</span><span class="sxs-lookup"><span data-stu-id="e1018-110">Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet</span></span>
-   <span data-ttu-id="e1018-111">Apple Safari (jaunākā publiski pieejamā versija) operētājsistēmā Mac OS X 10.10 (Yosemite), 10.11 (El Capitan), 10.12 (Sierra) vai Apple iPad</span><span class="sxs-lookup"><span data-stu-id="e1018-111">Apple Safari (latest publicly available version) on Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) or 10.12 (Sierra), or Apple iPad</span></span>

<span data-ttu-id="e1018-112">Lai atrastu katras tīmekļa pārlūkprogrammas visjaunāko laidienu, dodieties uz programmatūras ražotāja vietni.</span><span class="sxs-lookup"><span data-stu-id="e1018-112">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> -   <span data-ttu-id="e1018-113">Lai uzdevumu ierakstītājam atļautu ekrānuzņēmuma attēlu tveršanu un iekļaušanu ģenerētajos Microsoft Word dokumentos, jāinstalē Chrome paplašinājuma pirmsizlaides versija.</span><span class="sxs-lookup"><span data-stu-id="e1018-113">You must install a pre-release Chrome extension to enable Task Recorder to capture screenshots and include them in Microsoft Word documents that are generated.</span></span> <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   <span data-ttu-id="e1018-114">Darbplūsmas redaktors tiek startēts kā ClickOnce programma.</span><span class="sxs-lookup"><span data-stu-id="e1018-114">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="e1018-115">ClickOnce programmas atbalsta tikai Microsoft Edge un Internet Explorer (atbalstītā Microsoft Windows versijā).</span><span class="sxs-lookup"><span data-stu-id="e1018-115">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="e1018-116">Darbplūsmas redaktora ClickOnce programmai ir nepieciešama 64 bitu saderīga operētājsistēma.</span><span class="sxs-lookup"><span data-stu-id="e1018-116">The Workflow Editor ClickOnce application requires a 64-bit-compatible operating system.</span></span>
> -   <span data-ttu-id="e1018-117">Pārskatu noformētājs finanšu pārskatiem tiek startēts kā ClickOnce programma.</span><span class="sxs-lookup"><span data-stu-id="e1018-117">The Report Designer for Financial reporting is started as a ClickOnce application.</span></span> <span data-ttu-id="e1018-118">Tam ir nepieciešama saderīga 64 bitu operētājsistēma.</span><span class="sxs-lookup"><span data-stu-id="e1018-118">It requires a 64-bit-compatible operating system.</span></span> <span data-ttu-id="e1018-119">Ja lietojat pārlūkprogrammu Chrome, lai varētu lejupielādēt pārskatu veidošanas klientu, ir jāinstalē paplašinājums ClickOnce.</span><span class="sxs-lookup"><span data-stu-id="e1018-119">If you’re using Chrome, you must install a ClickOnce extension to download the Report Designer client.</span></span> <span data-ttu-id="e1018-120">Ja lietojat pārlūkprogrammu Chrome inkognito režīmā, pārliecinieties, ka paplašinājums ClickOnce ir arī iespējots inkognito režīmā.</span><span class="sxs-lookup"><span data-stu-id="e1018-120">If you use Chrome in Incognito mode, make sure that the ClickOnce extension is also enabled for Incognito mode.</span></span>
> -   <span data-ttu-id="e1018-121">Lai priekšskatītu PDF failus, ieteicams izmantot modernas pārlūkprogrammas, piemēram, Microsoft Edge (jaunāko publiski pieejamo versiju) operētājsistēmā Windows 10 vai Google Chrome (jaunāko publiski pieejamo versiju) operētājsistēmā Windows 10, Windows 8.1, Windows 8, Windows 7 vai Google Nexus 10 planšetdatoros.</span><span class="sxs-lookup"><span data-stu-id="e1018-121">To preview PDF files, we recommend that you use browsers such as Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>

### <a name="supported-web-browsers-for-retail-cloud-pos"></a><span data-ttu-id="e1018-122">Retail Cloud POS atbalstītās tīmekļa pārlūkprogrammas</span><span class="sxs-lookup"><span data-stu-id="e1018-122">Supported web browsers for Retail Cloud POS</span></span>

<span data-ttu-id="e1018-123">Retail Cloud POS var palaist jebkurā no tālāk uzskaitītajām tīmekļa pārlūkprogrammām, kas darbojas norādītajās operētājsistēmās.</span><span class="sxs-lookup"><span data-stu-id="e1018-123">Retail Cloud POS can run in any of the following web browsers that run on the specified operating systems:</span></span>

-   <span data-ttu-id="e1018-124">Microsoft Edge (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10</span><span class="sxs-lookup"><span data-stu-id="e1018-124">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
-   <span data-ttu-id="e1018-125">Internet Explorer 11 operētājsistēmā Windows 10, Windows 8.1 vai Windows 7</span><span class="sxs-lookup"><span data-stu-id="e1018-125">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
-   <span data-ttu-id="e1018-126">Chrome (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10, Windows 8.1 vai Windows 7</span><span class="sxs-lookup"><span data-stu-id="e1018-126">Chrome (latest publicly available version) on Windows 10, Windows 8.1, or Windows 7</span></span>

## <a name="network-requirements"></a><span data-ttu-id="e1018-127">Tīkla prasības</span><span class="sxs-lookup"><span data-stu-id="e1018-127">Network requirements</span></span>
-   <span data-ttu-id="e1018-128">Programma Finance and Operations ir izstrādāta tīkliem, kuru latentums nepārsniedz 250–300 milisekundes (ms).</span><span class="sxs-lookup"><span data-stu-id="e1018-128">Finance and Operations is designed for networks that have a latency of 250–300 milliseconds (ms) or less.</span></span> <span data-ttu-id="e1018-129">Tas ir latentums no pārlūkprogrammas klienta līdz Microsoft Azure datu centram, kurā tiek viesota programmatūra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e1018-129">This latency is the latency from a browser client to the Microsoft Azure datacenter that hosts Finance and Operations.</span></span> <span data-ttu-id="e1018-130">Ieteicams pārbaudīt tīkla latentumu vietnē <http://www.azurespeed.com>.</span><span class="sxs-lookup"><span data-stu-id="e1018-130">We recommend that you test network latency at <http://www.azurespeed.com>.</span></span>
-   <span data-ttu-id="e1018-131">Joslas platuma prasības programmai Finance and Operations ir atkarīgas no scenārija.</span><span class="sxs-lookup"><span data-stu-id="e1018-131">Bandwidth requirements for Finance and Operations depend on your scenario.</span></span> <span data-ttu-id="e1018-132">Tipiskākajiem scenārijiem ir nepieciešams joslas platums, kas ir lielāks par 50 kilobaitiem sekundē (KB/s).</span><span class="sxs-lookup"><span data-stu-id="e1018-132">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span> <span data-ttu-id="e1018-133">Tomēr scenārijiem, kuriem ir augstas lietderīgās slodzes prasības, piemēram, scenārijiem, kuros ir ietvertas darbvietas vai kuru ietvaros tiek veikta plaša pielāgošana, ieteicams izmantot lielāku joslas platumu.</span><span class="sxs-lookup"><span data-stu-id="e1018-133">However, we recommend more bandwidth for scenarios that have high payload requirements, such as scenarios that involve workspaces or extensive customization.</span></span>

<span data-ttu-id="e1018-134">Parasti programmatūra Finance and Operations ir optimizēta internetam.</span><span class="sxs-lookup"><span data-stu-id="e1018-134">In general, Finance and Operations is optimized for the internet.</span></span> <span data-ttu-id="e1018-135">Ciklu skaits no pārlūkprogrammas klienta uz Azure datu centru ir pavisam neliels, un visa lietderīgā slodze tiek saspiesta.</span><span class="sxs-lookup"><span data-stu-id="e1018-135">The number of round trips from a browser client to the Azure datacenter is very small, and the whole payload is compressed.</span></span> 

> [!WARNING]
> <span data-ttu-id="e1018-136">Neaprēķiniet nepieciešamo joslas platumu no klienta novietojuma, reizinot lietotāju skaitu ar minimālo nepieciešamo joslas platumu.</span><span class="sxs-lookup"><span data-stu-id="e1018-136">Don't calculate bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="e1018-137">Noteikta novietojuma vienlaicīgu izmantošanu ir ļoti grūti aprēķināt.</span><span class="sxs-lookup"><span data-stu-id="e1018-137">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="e1018-138">Debitoriem, kurus uztrauc joslas platuma prasības, izmantojiet Finance and Operations priekšskatījuma versiju.</span><span class="sxs-lookup"><span data-stu-id="e1018-138">Customers who are concerned about bandwidth requirements should use a preview version of Finance and Operations.</span></span>

## <a name="net-framework-requirements"></a><span data-ttu-id="e1018-139">.NET Framework prasības</span><span class="sxs-lookup"><span data-stu-id="e1018-139">.NET Framework requirements</span></span>
<span data-ttu-id="e1018-140">Programmai Finance and Operations ir nepieciešama Microsoft .NET Framework versija 4.6.2 visām ClickOnce programmām, piemēram, dokumentu maršrutēšanas aģentam.</span><span class="sxs-lookup"><span data-stu-id="e1018-140">Finance and Operations requires the Microsoft .NET Framework version 4.6.2 for all ClickOnce applications, such as the document routing agent.</span></span> <span data-ttu-id="e1018-141">Instalācijas instrukcijas skatiet sadaļā [.NET Framework instalācija](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="e1018-141">For installation instructions, see [Installing the .NET Framework](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="e1018-142">Atbalstītās Microsoft Office programmas</span><span class="sxs-lookup"><span data-stu-id="e1018-142">Supported Microsoft Office applications</span></span>
<span data-ttu-id="e1018-143">Finance and Operations mākoņa un lokālajos izvietojumos tiek atbalstītas tālāk norādītās Microsoft Office programmas.</span><span class="sxs-lookup"><span data-stu-id="e1018-143">The following Microsoft Office applications are supported in cloud and on-premises deployments of Finance and Operations:</span></span>

-   <span data-ttu-id="e1018-144">Lai palaistu Microsoft Excel un Word pievienojumprogrammas, jābūt instalētai programmai Microsoft Office 2016 operētājsistēmai Windows vai Mac.</span><span class="sxs-lookup"><span data-stu-id="e1018-144">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="e1018-145">Plašāku informāciju par versijas prasībām skatiet sadaļā [Office integrācijas problēmu novēršana](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="e1018-145">For more information about version requirements, see [Office integration troubleshooting](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).</span></span>
-   <span data-ttu-id="e1018-146">Lai skatītu dokumentus, kas izveidoti, izmantojot funkcijas Eksportēt programmā Excel vai Eksportēt programmā Word, ir jābūt instalētai programmai Microsoft Office 2007 vai jaunākai versijai.</span><span class="sxs-lookup"><span data-stu-id="e1018-146">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="retail-modern-pos-requirements"></a><span data-ttu-id="e1018-147">Retail Modern POS prasības</span><span class="sxs-lookup"><span data-stu-id="e1018-147">Retail Modern POS requirements</span></span>

> [!NOTE]
> <span data-ttu-id="e1018-148">Ja Retail Modern POS tiek izmantota bezsaistes datu bāze, datoram ir jāatbilst visām Microsoft SQL Server sistēmas prasībām.</span><span class="sxs-lookup"><span data-stu-id="e1018-148">If Retail Modern POS will use an offline database, the computer must meet all system requirements for Microsoft SQL Server.</span></span> <span data-ttu-id="e1018-149">Retail Modern POS bezsaistes datu bāze darbojas ar Microsoft SQL Server 2012 3. servisa pakotni vai jaunāku versiju, Microsoft SQL Server 2014 2. servisa pakotni vai jaunāku versiju un Microsoft SQL Server 2016.</span><span class="sxs-lookup"><span data-stu-id="e1018-149">A Retail Modern POS offline database will work on Microsoft SQL Server 2012 with Service Pack 3 or later, Microsoft SQL Server 2014 with Service Pack 2 or later, and Microsoft SQL Server 2016.</span></span> <span data-ttu-id="e1018-150">Ieteicams vienmēr izmantot jaunāko pieejamo versiju un instalēt jaunākās servisa pakotnes.</span><span class="sxs-lookup"><span data-stu-id="e1018-150">We recommend that you always use the latest version that is available, and that you install all the latest service packs.</span></span>

### <a name="supported-operating-systems"></a><span data-ttu-id="e1018-151">Atbalstītās operētājsistēmas</span><span class="sxs-lookup"><span data-stu-id="e1018-151">Supported operating systems</span></span>

-   <span data-ttu-id="e1018-152">Retail Modern POS ir 32 bitu programma, taču tā darbojas gan x86, gan x64 arhitektūrā.</span><span class="sxs-lookup"><span data-stu-id="e1018-152">Retail Modern POS is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="e1018-153">Programma Retail Modern POS tiek atbalstīta tikai operētājsistēmā Windows 10 Pro, Enterprise un Enterprise Long Term Servicing Branch (LTSB) versijās.</span><span class="sxs-lookup"><span data-stu-id="e1018-153">Retail Modern POS is supported only on Windows 10 Pro, Enterprise, and Enterprise Long Term Servicing Branch (LTSB) editions.</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="e1018-154">Minimālās sistēmas prasības</span><span class="sxs-lookup"><span data-stu-id="e1018-154">Minimum system requirements</span></span>

-   <span data-ttu-id="e1018-155">Minimālā atbalstītā izšķirtspēja ir 1280 × 1024.</span><span class="sxs-lookup"><span data-stu-id="e1018-155">The minimum supported resolution is 1,280 × 1,024.</span></span>
-   <span data-ttu-id="e1018-156">Datoram, kurā tiek izmantota programma Retail Modern POS, jāatbilst šādām prasībām:</span><span class="sxs-lookup"><span data-stu-id="e1018-156">The computer that Retail Modern POS runs on must meet these requirements:</span></span>

    -   <span data-ttu-id="e1018-157">Tam jābūt vismaz divkodolu procesoram, kura takts frekvence ir vismaz 2 gigaherci (GHz).</span><span class="sxs-lookup"><span data-stu-id="e1018-157">It must have, at a minimum, a dual-core processor that runs at no less than 2 gigahertz (GHz).</span></span>
    -   <span data-ttu-id="e1018-158">Nepieciešama vismaz 3 gigabaitu (GB) brīvpiekļuves atmiņa (RAM).</span><span class="sxs-lookup"><span data-stu-id="e1018-158">It must have, at a minimum, 3 gigabytes (GB) of random-access memory (RAM).</span></span>
    -   <span data-ttu-id="e1018-159">Nepieciešama piekļuve internetam.</span><span class="sxs-lookup"><span data-stu-id="e1018-159">It must have internet access.</span></span>

## <a name="retail-hardware-station-requirements"></a><span data-ttu-id="e1018-160">Retail hardware station prasības</span><span class="sxs-lookup"><span data-stu-id="e1018-160">Retail hardware station requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="e1018-161">Atbalstītās operētājsistēmas</span><span class="sxs-lookup"><span data-stu-id="e1018-161">Supported operating systems</span></span>

-   <span data-ttu-id="e1018-162">Retail hardware station ir 32 bitu programma, taču tā darbojas gan x86, gan x64 arhitektūrā.</span><span class="sxs-lookup"><span data-stu-id="e1018-162">Retail hardware station is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="e1018-163">Programma Retail hardware station tiek atbalstīta šādās operētājsistēmās:</span><span class="sxs-lookup"><span data-stu-id="e1018-163">Retail hardware station is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="e1018-164">Windows 7 Professional, Enterprise un Ultimate versijas</span><span class="sxs-lookup"><span data-stu-id="e1018-164">Windows 7 Professional, Enterprise, and Ultimate editions</span></span> 
    
        > [!NOTE]
        > <span data-ttu-id="e1018-165">Operētājsistēma Windows 7 tiek atbalstīta tikai tad, ja sistēmā ir manuāli instalēta pārlūkprogramma Internet Explorer 11.</span><span class="sxs-lookup"><span data-stu-id="e1018-165">Windows 7 is supported only if Internet Explorer 11 is manually installed on the system.</span></span>

    -   <span data-ttu-id="e1018-166">Windows 8.1 1. atjauninājums Professional, Enterprise un Embedded versijas</span><span class="sxs-lookup"><span data-stu-id="e1018-166">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="e1018-167">Windows 10 Pro, Enterprise un Enterprise LTSB versijas</span><span class="sxs-lookup"><span data-stu-id="e1018-167">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="e1018-168">Minimālās sistēmas prasības</span><span class="sxs-lookup"><span data-stu-id="e1018-168">Minimum system requirements</span></span>

<span data-ttu-id="e1018-169">Datoram ir jāatbilst visām sistēmas prasībām tālāk minēto vienumu instalēšanai un izmantošanai:</span><span class="sxs-lookup"><span data-stu-id="e1018-169">The computer must meet all system requirements for installing and using the following items:</span></span>

-   <span data-ttu-id="e1018-170">Interneta informācijas pakalpojumi (IIS)</span><span class="sxs-lookup"><span data-stu-id="e1018-170">Internet Information Services (IIS)</span></span>
-   <span data-ttu-id="e1018-171">Trešās puses aparatūra</span><span class="sxs-lookup"><span data-stu-id="e1018-171">Third-party hardware</span></span>

## <a name="retail-store-scale-unit-requirements"></a><span data-ttu-id="e1018-172">Retail Store Scale Unit prasības</span><span class="sxs-lookup"><span data-stu-id="e1018-172">Retail Store Scale Unit requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="e1018-173">Atbalstītās operētājsistēmas</span><span class="sxs-lookup"><span data-stu-id="e1018-173">Supported operating systems</span></span>

-   <span data-ttu-id="e1018-174">Retail Store Scale Unit ir 32 bitu programma, taču tā darbojas gan x86, gan x64 arhitektūrā.</span><span class="sxs-lookup"><span data-stu-id="e1018-174">Retail Store Scale Unit is a 32-bit application, but it will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="e1018-175">Programma Retail Store Scale Unit tiek atbalstīta šādās operētājsistēmās:</span><span class="sxs-lookup"><span data-stu-id="e1018-175">Retail Store Scale Unit is supported on the following operating systems:</span></span>

    -   <span data-ttu-id="e1018-176">Windows 7 Professional, Enterprise un Ultimate versijas</span><span class="sxs-lookup"><span data-stu-id="e1018-176">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="e1018-177">Windows 8.1 1. atjauninājums Professional, Enterprise un Embedded versijas</span><span class="sxs-lookup"><span data-stu-id="e1018-177">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="e1018-178">Windows 10 Pro, Enterprise un Enterprise LTSB versijas</span><span class="sxs-lookup"><span data-stu-id="e1018-178">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="e1018-179">Minimālās sistēmas prasības</span><span class="sxs-lookup"><span data-stu-id="e1018-179">Minimum system requirements</span></span>

-   <span data-ttu-id="e1018-180">4 GB RAM</span><span class="sxs-lookup"><span data-stu-id="e1018-180">4 GB of RAM</span></span>
-   <span data-ttu-id="e1018-181">1,6 GHz maksimālais centrālā procesora ātrums katram kodolam (Ir jābūt vismaz diviem kodoliem.)</span><span class="sxs-lookup"><span data-stu-id="e1018-181">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="e1018-182">Vismaz 10 GB brīvās vietas (Kanāla datu bāzei var būt nepieciešams lielāks vietas daudzums.)</span><span class="sxs-lookup"><span data-stu-id="e1018-182">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

### <a name="recommended-system-requirements"></a><span data-ttu-id="e1018-183">Ieteicamās sistēmas prasības</span><span class="sxs-lookup"><span data-stu-id="e1018-183">Recommended system requirements</span></span>

-   <span data-ttu-id="e1018-184">6 GB RAM</span><span class="sxs-lookup"><span data-stu-id="e1018-184">6 GB of RAM</span></span>
-   <span data-ttu-id="e1018-185">2,4 GHz i7 (vai ekvivalents) maksimālais centrālā procesora ātrums katram kodolam (Ieteicami vismaz četri kodoli.)</span><span class="sxs-lookup"><span data-stu-id="e1018-185">2.4 GHz i7 (or equivalent) peak CPU speed per core (Four cores are recommended.)</span></span>
-   <span data-ttu-id="e1018-186">Vismaz 10 GB brīvās vietas (Kanāla datu bāzei var būt nepieciešams lielāks vietas daudzums.)</span><span class="sxs-lookup"><span data-stu-id="e1018-186">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="connector-requirements"></a><span data-ttu-id="e1018-187">Savienotāja prasības</span><span class="sxs-lookup"><span data-stu-id="e1018-187">Connector requirements</span></span>
### <a name="supported-operating-systems"></a><span data-ttu-id="e1018-188">Atbalstītās operētājsistēmas</span><span class="sxs-lookup"><span data-stu-id="e1018-188">Supported operating systems</span></span>

-   <span data-ttu-id="e1018-189">Microsoft Dynamics AX savienotājam ir divas atsevišķas instalēšanas programmas — viena Async Server Connector pakalpojumam un otra Dynamics AX 2012 R3 reāllaika pakalpojumam.</span><span class="sxs-lookup"><span data-stu-id="e1018-189">The Connector for Microsoft Dynamics AX has two separate installers, one for Async Server Connector service and one for Real-time service for Dynamics AX 2012 R3.</span></span>
-   <span data-ttu-id="e1018-190">Abi komponenti ir 32 bitu programmas, taču tie darbojas gan x86, gan x64 arhitektūrā.</span><span class="sxs-lookup"><span data-stu-id="e1018-190">Both components are 32-bit applications, but they will run on both x86 and x64 architectures.</span></span>
-   <span data-ttu-id="e1018-191">Abi komponenti tiek atbalstīti šādas operētājsistēmās:</span><span class="sxs-lookup"><span data-stu-id="e1018-191">Both components are supported on the following operating systems:</span></span>

    -   <span data-ttu-id="e1018-192">Windows 7 Professional, Enterprise un Ultimate versijas</span><span class="sxs-lookup"><span data-stu-id="e1018-192">Windows 7 Professional, Enterprise, and Ultimate editions</span></span>
    -   <span data-ttu-id="e1018-193">Windows 8.1 1. atjauninājums Professional, Enterprise un Embedded versijas</span><span class="sxs-lookup"><span data-stu-id="e1018-193">Windows 8.1 Update 1 Professional, Enterprise, and Embedded editions</span></span>
    -   <span data-ttu-id="e1018-194">Windows 10 Pro, Enterprise un Enterprise LTSB versijas</span><span class="sxs-lookup"><span data-stu-id="e1018-194">Windows 10 Pro, Enterprise, and Enterprise LTSB editions</span></span>
    -   <span data-ttu-id="e1018-195">Microsoft Windows Server 2012 R2 un Microsoft Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e1018-195">Microsoft Windows Server 2012 R2 and Microsoft Windows Server 2016</span></span>

### <a name="minimum-system-requirements"></a><span data-ttu-id="e1018-196">Minimālās sistēmas prasības</span><span class="sxs-lookup"><span data-stu-id="e1018-196">Minimum system requirements</span></span>
-   <span data-ttu-id="e1018-197">2 GB RAM (ieteicams 4 GB RAM)</span><span class="sxs-lookup"><span data-stu-id="e1018-197">2 GB of RAM (4 GB of RAM are recommended.)</span></span>
-   <span data-ttu-id="e1018-198">1,6 GHz maksimālais centrālā procesora ātrums katram kodolam (Ir jābūt vismaz diviem kodoliem.)</span><span class="sxs-lookup"><span data-stu-id="e1018-198">1.6 GHz peak CPU speed per core (Two cores are the minimum.)</span></span>
-   <span data-ttu-id="e1018-199">Vismaz 10 GB brīvās vietas (Kanāla datu bāzei var būt nepieciešams lielāks vietas daudzums.)</span><span class="sxs-lookup"><span data-stu-id="e1018-199">At least 10 GB of free space (The channel database can require a large amount of space.)</span></span>

## <a name="requirements-for-development-on-local-vms"></a><span data-ttu-id="e1018-200">Prasības izstrādei lokālās virtuālajās mašīnās</span><span class="sxs-lookup"><span data-stu-id="e1018-200">Requirements for development on local VMs</span></span>
<span data-ttu-id="e1018-201">Informāciju par prasībām attiecībā uz izstrādi vietējās virtuālajās mašīnās (VM) skatiet sadaļā [VM, kuras darbojas lokāli](../dev-tools/access-instances.md).</span><span class="sxs-lookup"><span data-stu-id="e1018-201">For information about the requirements for development on local virtual machines (VMs), see [VM running on-premises](../dev-tools/access-instances.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="e1018-202">Skatiet arī</span><span class="sxs-lookup"><span data-stu-id="e1018-202">See also</span></span>

[<span data-ttu-id="e1018-203">Iegūt Dynamics 365 for Finance and Operations izdevuma Enterprise iepazīšanās kopiju</span><span class="sxs-lookup"><span data-stu-id="e1018-203">Get an evaluation copy of Dynamics 365 for Finance and Operations, Enterprise edition</span></span>](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)


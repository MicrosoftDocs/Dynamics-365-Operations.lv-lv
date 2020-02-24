---
title: Sistēmas prasības
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 72379e91ace61f5e33ac6cab259b5c32902c7b3b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009756"
---
# <a name="system-requirements"></a><span data-ttu-id="99947-102">Sistēmas prasības</span><span class="sxs-lookup"><span data-stu-id="99947-102">System requirements</span></span>

<span data-ttu-id="99947-103">Šajā rakstā aprakstītas prasības Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="99947-103">This article describes requirements for Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="99947-104">Tajā ir arī norādītas valstis un reģioni, kur ir pieejama Human Resources, un informācija par valodām un lokalizāciju, kas jāizmanto Human Resources datiem.</span><span class="sxs-lookup"><span data-stu-id="99947-104">It also outlines the countries and regions where Human Resources is available, and information about languages and localization for Human Resources data.</span></span>

## <a name="supported-web-browsers"></a><span data-ttu-id="99947-105">Atbalstītās tīmekļa pārlūkprogrammas</span><span class="sxs-lookup"><span data-stu-id="99947-105">Supported web browsers</span></span>

<span data-ttu-id="99947-106">Human Resources var palaist jebkurā no tālāk uzskaitītajām tīmekļa pārlūkprogrammām, kas darbojas norādītajās operētājsistēmās.</span><span class="sxs-lookup"><span data-stu-id="99947-106">Human Resources can run in any of the following web browsers that run on the specified operating systems:</span></span> 

*   <span data-ttu-id="99947-107">Microsoft Edge (jaunākā publiski pieejamā versija) operētājsistēmā Windows 10</span><span class="sxs-lookup"><span data-stu-id="99947-107">Microsoft Edge (latest publicly available version) on Windows 10</span></span>
*   <span data-ttu-id="99947-108">Internet Explorer 11 operētājsistēmā Windows 10, Windows 8.1 vai Windows 7</span><span class="sxs-lookup"><span data-stu-id="99947-108">Internet Explorer 11 on Windows 10, Windows 8.1, or Windows 7</span></span>
*   <span data-ttu-id="99947-109">Google Chrome (jaunākā publiski pieejamā versija)</span><span class="sxs-lookup"><span data-stu-id="99947-109">Google Chrome (latest publicly available version)</span></span>
*   <span data-ttu-id="99947-110">Apple Safari (jaunākā publiski pieejamā versija)</span><span class="sxs-lookup"><span data-stu-id="99947-110">Apple Safari (latest publicly available version)</span></span>

<span data-ttu-id="99947-111">Lai atrastu katras tīmekļa pārlūkprogrammas visjaunāko laidienu, dodieties uz programmatūras ražotāja vietni.</span><span class="sxs-lookup"><span data-stu-id="99947-111">To find the latest release for each web browser, go to the software manufacturer’s website.</span></span> 

> [!NOTE]
> * <span data-ttu-id="99947-112">Lai tvertu attēlus, kas izveidoti Uzdevumu reģistrētājā un iekļautu tos Microsoft Word dokumentos, ir jābūt instalētam Chrome paplašinājumam.</span><span class="sxs-lookup"><span data-stu-id="99947-112">To capture images that are generated from Task Recorder and include them in Microsoft Word documents, you must have a Chrome extension installed.</span></span> 
> * <span data-ttu-id="99947-113">Darbplūsmas redaktors tiek startēts kā ClickOnce programma.</span><span class="sxs-lookup"><span data-stu-id="99947-113">The Workflow Editor is started as a ClickOnce application.</span></span> <span data-ttu-id="99947-114">ClickOnce programmas atbalsta tikai Microsoft Edge un Internet Explorer (atbalstītā Microsoft Windows versijā).</span><span class="sxs-lookup"><span data-stu-id="99947-114">Only Microsoft Edge and Internet Explorer (on a supported version of Microsoft Windows) support ClickOnce applications.</span></span> <span data-ttu-id="99947-115">Darbplūsmas redaktora ClickOnce programmai ir nepieciešama 64 bitu saderīga operētājsistēma.</span><span class="sxs-lookup"><span data-stu-id="99947-115">The Workflow Editor ClickOnce application requires a 64-bit compatible operating system.</span></span>
> * <span data-ttu-id="99947-116">Lai priekšskatītu PDF failus, ieteicams izmantot modernas pārlūkprogrammas, piemēram, Microsoft Edge (jaunāko publiski pieejamo versiju) operētājsistēmā Windows 10 vai Google Chrome (jaunāko publiski pieejamo versiju) operētājsistēmā Windows 10, Windows 8.1, Windows 8, Windows 7 vai Google Nexus 10 planšetdatoros.</span><span class="sxs-lookup"><span data-stu-id="99947-116">To preview PDF files, we recommend that you use modern browsers like Microsoft Edge (latest publicly available version) on Windows 10, or Google Chrome (latest publicly available version) on Windows 10, Windows 8.1, Windows 8, Windows 7, or Google Nexus 10 tablet.</span></span>
>   <span data-ttu-id="99947-117">Tīkla prasības</span><span class="sxs-lookup"><span data-stu-id="99947-117">Network requirements</span></span>
> * <span data-ttu-id="99947-118">Human Resources ir izstrādāta tīkliem, kuru latentums nepārsniedz 250–300 milisekundes (ms).</span><span class="sxs-lookup"><span data-stu-id="99947-118">Human Resources is designed for networks with latency of 250-300 milliseconds (ms) or less.</span></span> <span data-ttu-id="99947-119">Tas ir latentums no pārlūkprogrammas klienta līdz Microsoft Azure datu centram, kurā tiek viesota Human Resources.</span><span class="sxs-lookup"><span data-stu-id="99947-119">This is the latency from a browser client to the Microsoft Azure data center that hosts Human Resources.</span></span> <span data-ttu-id="99947-120">Ieteicams pārbaudīt tīkla latentumu vietnē [www.azurespeed.com](https://www.azurespeed.com "Azure latentuma pārbaude").</span><span class="sxs-lookup"><span data-stu-id="99947-120">We recommend that you test network latency at [www.azurespeed.com](https://www.azurespeed.com "Azure Latency Test").</span></span>
> * <span data-ttu-id="99947-121">Joslas platuma prasības Human Resources ir atkarīgas no jūsu scenārija.</span><span class="sxs-lookup"><span data-stu-id="99947-121">Bandwidth requirements for Human Resources depend on your scenario.</span></span> <span data-ttu-id="99947-122">Tipiskākajiem scenārijiem ir nepieciešams joslas platums, kas ir lielāks par 50 kilobaitiem sekundē (KB/s).</span><span class="sxs-lookup"><span data-stu-id="99947-122">Most typical scenarios require a bandwidth of more than 50 kilobytes per second (KBps).</span></span>
> 
> [!WARNING]
> <span data-ttu-id="99947-123">Neaprēķiniet nepieciešamo joslas platumu no klienta novietojuma, reizinot lietotāju skaitu ar minimālo nepieciešamo joslas platumu.</span><span class="sxs-lookup"><span data-stu-id="99947-123">Don't compute bandwidth requirements from a client location by multiplying the number of users by the minimum bandwidth requirements.</span></span> <span data-ttu-id="99947-124">Noteikta novietojuma vienlaicīgu izmantošanu ir ļoti grūti aprēķināt.</span><span class="sxs-lookup"><span data-stu-id="99947-124">The concurrent usage of a given location is very difficult to calculate.</span></span> <span data-ttu-id="99947-125">Debitoriem, kurus uztrauc joslas platuma prasības, izmantojiet Human Resources izmēģinājuma versiju.</span><span class="sxs-lookup"><span data-stu-id="99947-125">For customers who are concerned about bandwidth requirements, use a trial version of Human Resources.</span></span>

## <a name="supported-microsoft-office-applications"></a><span data-ttu-id="99947-126">Atbalstītās Microsoft Office programmas</span><span class="sxs-lookup"><span data-stu-id="99947-126">Supported Microsoft Office applications</span></span>

* <span data-ttu-id="99947-127">Lai palaistu Microsoft Excel un Word pievienojumprogrammas, jābūt instalētai programmai Microsoft Office 2016 operētājsistēmai Windows vai Mac.</span><span class="sxs-lookup"><span data-stu-id="99947-127">To run the Microsoft Excel and Word add-ins, you must have Microsoft Office 2016 for Windows or Mac installed.</span></span> <span data-ttu-id="99947-128">Plašāku informāciju par versijas prasībām skatiet sadaļā [Office integrācijas problēmu novēršana](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integrācijas problēmu novēršana").</span><span class="sxs-lookup"><span data-stu-id="99947-128">For more details about version requirements, see [Office integration troubleshooting](../dev-itpro/office-integration/office-integration-troubleshooting.md "Office integration troubleshooting").</span></span>
* <span data-ttu-id="99947-129">Lai skatītu dokumentus, kas izveidoti, izmantojot funkcijas Eksportēt programmā Excel vai Eksportēt programmā Word, ir jābūt instalētai programmai Microsoft Office 2007 vai jaunākai versijai.</span><span class="sxs-lookup"><span data-stu-id="99947-129">To view documents that are generated by the Export to Excel or Export to Word functionality, you must have Microsoft Office 2007 or later installed.</span></span>

## <a name="regional-availability-languages-and-localization"></a><span data-ttu-id="99947-130">Reģionālā pieejamība, valodas un lokalizācija</span><span class="sxs-lookup"><span data-stu-id="99947-130">Regional availability, languages, and localization</span></span>

<span data-ttu-id="99947-131">Varat lejupielādēt PDF failu ar valstīm, reģioniem un valodām, ko atbalsta Human Resources, lapā [Microsoft Dynamics 365 starptautiskā pieejamība](https://docs.microsoft.com/dynamics365/get-started/availability).</span><span class="sxs-lookup"><span data-stu-id="99947-131">You can download a PDF file of the countries, regions, and languages Human Resources supports at [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span> 

> [!NOTE]
> <span data-ttu-id="99947-132">Lietotāja interfeiss ir lokalizēts citās valodās, bet visi lietotāja dati tiek saglabāti tajā valodā, kādā tika ievadīti.</span><span class="sxs-lookup"><span data-stu-id="99947-132">While the user interface is localized into other languages, all user data is stored in the language in which it was entered.</span></span> <span data-ttu-id="99947-133">Varat izveidot e-pasta ziņojumus un veidnes citās valodās, taču dati, piemēram, plānošanas informācija, pagaidām ir pieejami tikai angļu valodā.</span><span class="sxs-lookup"><span data-stu-id="99947-133">You can create emails and templates in other languages, but data such as scheduling information is only available in English at this time.</span></span>

<span data-ttu-id="99947-134">Ja esat izstrādātājs un vēlaties izveidot valstij vai reģionam specifiskus pielāgojumus vai izveidot risinājumu valstij vai reģionam, ko Microsoft pašlaik neatbalsta, skatiet lapu [Globalizācija](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span><span class="sxs-lookup"><span data-stu-id="99947-134">If you're a developer interested in creating country- or region-specific customizations, or in creating a solution for a country or region not currently supported by Microsoft, see [Globalization](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).</span></span>

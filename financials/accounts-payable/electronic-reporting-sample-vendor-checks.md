---
title: "Elektronisko pārskatu kreditoru čeku paraugi"
description: "Šajā tēmā ir sniegta vispārīga informācija pat to, kā izmantot elektronisko pārskatu čeku paraugu formātus."
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 97d374230cc6e833b9f585de000e1252f2a78b9d
ms.openlocfilehash: 694ae59cdf06d68394b2a546c5a112964458016a
ms.contentlocale: lv-lv
ms.lasthandoff: 08/30/2017

---

[!include[banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a><span data-ttu-id="e6427-103">Elektronisko pārskatu čeku paraugu formāti</span><span class="sxs-lookup"><span data-stu-id="e6427-103">Electronic reporting sample check formats</span></span>

<span data-ttu-id="e6427-104">Varat izmantot elektronisko pārskatu (ER) veidošanas rīku, lai formatētu kreditoru čekus.</span><span class="sxs-lookup"><span data-stu-id="e6427-104">You can use Electronic reporting (ER) to format vendor checks.</span></span> <span data-ttu-id="e6427-105">Tirgū ir pieejami daudzi bankām specifiski un čeka nodrošinātājiem specifiski čeku formāti.</span><span class="sxs-lookup"><span data-stu-id="e6427-105">Many bank-specific and check provider–specific check formats are available on the market.</span></span> <span data-ttu-id="e6427-106">ER rīka repozitorija maksājumu čeku modelī ir ietverti čeku paraugu formāti.</span><span class="sxs-lookup"><span data-stu-id="e6427-106">Sample check formats have been included in the Payment check model in the ER tool repository.</span></span> <span data-ttu-id="e6427-107">Šiem čeku paraugiem ir šādi apzīmējumi: **Čeks vidū (ASV)** un **Čeks augšpusē, aprēķins apakšpusē (ASV)**.</span><span class="sxs-lookup"><span data-stu-id="e6427-107">These sample checks are labeled **Check in the middle (US)** and **Check on top stub below (US)**.</span></span>

## <a name="what-check-formats-are-currently-supported"></a><span data-ttu-id="e6427-108">Kādi čeku formāti pašlaik tiek atbalstīti?</span><span class="sxs-lookup"><span data-stu-id="e6427-108">What check formats are currently supported?</span></span>

<span data-ttu-id="e6427-109">Vienmēr apmeklējiet koplietojamo līdzekļu bibliotēku pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) un skatiet jaunāko pieejamo pamatlīdzekļa tipa **GER konfigurācija** failu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="e6427-109">You should always go to the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS) and view the current list of available files that have an asset type of **GER configuration**.</span></span> <span data-ttu-id="e6427-110">Nākamajā sadaļā “Kas man ir jāiestata?” ir ietverta saite uz tēmu, kurā ir paskaidrots, kā izveidot LCS repozitoriju, lai varētu pārskatīt pieejamās konfigurācijas un importēt atlasītās konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="e6427-110">The next section, “What do I have to set up?,” includes a link to a topic that explains how to create an LCS repository so that you can review available configurations and import selected configurations.</span></span>

<span data-ttu-id="e6427-111">Programmatūras Microsoft Dynamics 365 for Finance and Operations izdevumā Enterprise ir ietverts čeka parauga formāts, kurā čeks atrodas augšpusē un tam seko divas pārskaitījuma sadaļas.</span><span class="sxs-lookup"><span data-stu-id="e6427-111">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, includes a sample format where the check is on top, followed by two remittance sections.</span></span> <span data-ttu-id="e6427-112">Tajā ir ietverts arī čeka parauga formāts, kurā čeks atrodas pa vidu starp divām pārskaitījuma sadaļām.</span><span class="sxs-lookup"><span data-stu-id="e6427-112">It also includes a sample format where the check is in the middle, between two remittance sections.</span></span> <span data-ttu-id="e6427-113">Šie čeku paraugu formāti atbilst Deluxe uzņēmējdarbības čeku formātiem.</span><span class="sxs-lookup"><span data-stu-id="e6427-113">These sample formats correspond to Deluxe business checks formats.</span></span>

## <a name="what-do-i-have-to-set-up"></a><span data-ttu-id="e6427-114">Kas man ir jāiestata?</span><span class="sxs-lookup"><span data-stu-id="e6427-114">What do I have to set up?</span></span>

- <span data-ttu-id="e6427-115">Pirms čeku drukāšanas, izmantojot ER izveides rīku, ER konfigurāciju kopā ir jāimportē vismaz viena aktīva čeka konfigurācija.</span><span class="sxs-lookup"><span data-stu-id="e6427-115">Before you can print checks by using ER, at least one active check configuration must be imported into your ER configurations.</span></span> <span data-ttu-id="e6427-116">Norādījumus skatiet sadaļā [Elektronisko atskaišu veidošanas konfigurāciju lejupielāde no Lifecycle Services](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span><span class="sxs-lookup"><span data-stu-id="e6427-116">For instructions, see [Download Electronic reporting configurations from Lifecycle Services](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).</span></span>
- <span data-ttu-id="e6427-117">Konfigurējot bankas konta skaidras naudas un bankas vadības čekus, atzīmējiet izvēles rūtiņu **Vispārīgs elektroniskās eksportēšanas formāts** un pēc tam kā eksportēšanas formāta konfigurāciju atlasiet atbilstošo čeka formātu.</span><span class="sxs-lookup"><span data-stu-id="e6427-117">When you configure Cash and bank management checks for the bank account, select the **Generic electronic Export format** check box, and then select the appropriate check format as an export format configuration.</span></span>
- <span data-ttu-id="e6427-118">Ir jānorāda arī pārskaitījuma sadaļā drukājamo kvīts rindu skaits.</span><span class="sxs-lookup"><span data-stu-id="e6427-118">You must also specify the number of slip lines that will be printed on the remittance.</span></span> <span data-ttu-id="e6427-119">Aprēķinot šo skaitu, noteikti pieskaitiet galvenes rindas.</span><span class="sxs-lookup"><span data-stu-id="e6427-119">Be sure to include the header rows when you calculate this number.</span></span> <span data-ttu-id="e6427-120">Abiem čeku paraugu formātiem ieteicamais kvīts rindu skaits ir 17.</span><span class="sxs-lookup"><span data-stu-id="e6427-120">For the two sample check formats, the recommended number of slip lines is 17.</span></span> <span data-ttu-id="e6427-121">Taču šis skaits mainīsies atkarībā no jūsu čeku kopas un printera draiveriem.</span><span class="sxs-lookup"><span data-stu-id="e6427-121">However, this number will vary, depending on your check stock and your printer drivers.</span></span>
- <span data-ttu-id="e6427-122">Ir ieteicams izdrukāt izmēģinājuma čeku, lai pārbaudītu čeka izkārtojumu.</span><span class="sxs-lookup"><span data-stu-id="e6427-122">We recommend that you print a test check to validate the check layout.</span></span> <span data-ttu-id="e6427-123">Lai izdrukātu izmēģinājuma čeku, atlasiet opciju **Drukāt paraugu**.</span><span class="sxs-lookup"><span data-stu-id="e6427-123">To print a test check, select the **Print test** option.</span></span> <span data-ttu-id="e6427-124">Čeku paraugu formāti vislabāk darbojas tad, ja programmas Microsoft Excel printera papildu rekvizītu sadaļā ir iestatīta opcijas **Piemales** vērtība **Nav**.</span><span class="sxs-lookup"><span data-stu-id="e6427-124">The sample check formats work best when **Margins** is set to **None** in the advanced printer properties for Microsoft Excel.</span></span> <span data-ttu-id="e6427-125">Pēc izmēģinājuma čeka izdrukāšanas iespējojiet Excel izvades rediģēšanu un konfigurējiet lapas izkārtojumu, visām piemalēm iestatot vērtību **0** (nulle).</span><span class="sxs-lookup"><span data-stu-id="e6427-125">After the test check has been generated, enable editing of the Excel output, and configure the page layout so that all margins are set to **0** (zero).</span></span> <span data-ttu-id="e6427-126">Salīdziniet čeku izmēģinājuma kopijas ar čeku kopu un pielāgojiet iestatījumus, līdz izkārtojums jūs apmierina.</span><span class="sxs-lookup"><span data-stu-id="e6427-126">Compare the test copy of the checks to your check stock, and adjust the settings until you're satisfied with the alignment.</span></span>
- <span data-ttu-id="e6427-127">Kad maksājumu žurnālā ģenerējat konfigurētā bankas konta maksājumus, tiek drukāti norādītā formāta čeki.</span><span class="sxs-lookup"><span data-stu-id="e6427-127">When you generate payments for the configured bank account in the payment journal, the checks will be printed by using the specified format.</span></span>

<span data-ttu-id="e6427-128">Papildinformāciju skatiet tēmā [Elektronisko pārskatu veidošanas formāta mainīšana](/dynamics365/unified-operations/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template).</span><span class="sxs-lookup"><span data-stu-id="e6427-128">For more information, see [Modify an Electronic reporting format](/dynamics365/unified-operations/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template).</span></span>


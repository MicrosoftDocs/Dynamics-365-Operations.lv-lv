---
title: Parādīt lapas blakus, izmantojot līdzekli Atvērt jaunā logā
description: Šajā rakstā ir paskaidrots, kā parādīt lapas līdzās.
author: aneesmsft
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17611
ms.assetid: fc589d76-3927-4486-ab83-e86b9b47ba2c
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7144f26c0977fbc420b804728151262b2f166bc0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 09/27/2019
ms.locfileid: "2180695"
---
# <a name="show-pages-side-by-side-by-using-the-open-in-new-window-feature"></a><span data-ttu-id="80f09-103">Parādīt lapas blakus, izmantojot līdzekli Atvērt jaunā logā</span><span class="sxs-lookup"><span data-stu-id="80f09-103">Show pages side by side by using the Open in new window feature</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80f09-104">Šajā rakstā ir paskaidrots, kā parādīt lapas līdzās.</span><span class="sxs-lookup"><span data-stu-id="80f09-104">This article explains how to display pages side-by-side.</span></span>

<span data-ttu-id="80f09-105">Iespējams, vēlēsieties skatīt vairākas lappuses līdzās, lai ātri veiktu uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="80f09-105">You may want to view multiple pages side-by-side to complete tasks quickly.</span></span> <span data-ttu-id="80f09-106">Piemēram, iespējams, vēlēsieties apstiprināt vai ievadīt rindas vairāk nekā vienā žurnālā.</span><span class="sxs-lookup"><span data-stu-id="80f09-106">As an example, you might want to validate or enter lines in more than one journal.</span></span> <span data-ttu-id="80f09-107">Parasti, lai to izdarītu, ir jāpāriet atpakaļ un uz priekšu no lapas, kurā ir parādīts žurnālu saraksts, uz lapu, kurā ir parādītas attiecīgā žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="80f09-107">Typically, to do this you would have to go back and forth between the page that displays a list of journals, and the page that displays lines for a given journal.</span></span> <span data-ttu-id="80f09-108">Tomēr līdzeklis **Atvērt jaunā logā** ļauj parādīt šīs lapas blakus, lai jūs varētu ātri veikt uzdevumus.</span><span class="sxs-lookup"><span data-stu-id="80f09-108">However, the **Open in new window** feature enables you to display these pages side-by-side so that you can perform your tasks quickly.</span></span>

<span data-ttu-id="80f09-109">Turpinot iepriekš minēto piemēru, skatot rindas, varat noklikšķināt uz ikonas **Atvērt jaunā logā**.</span><span class="sxs-lookup"><span data-stu-id="80f09-109">Continuing with the example mentioned above, when viewing the lines, you can click the **Open in new window** icon.</span></span>

<span data-ttu-id="80f09-110">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span><span class="sxs-lookup"><span data-stu-id="80f09-110">[![open-in-new-window-icon](./media/open-in-new-window-icon.png)](./media/open-in-new-window-icon.png)</span></span>

<span data-ttu-id="80f09-111">Noklikšķinot uz ikonas **Atvērt jaunā logā**, rindu lapa tiek atvērta jaunā uznirstošā pārlūkprogrammā, un pēc tam sākotnējā pārlūkprogramma pāriet atpakaļ vēsturē uz lapu, kurā tika rādīts žurnālu saraksts.</span><span class="sxs-lookup"><span data-stu-id="80f09-111">Clicking the **Open in new window** icon opens the lines page in a new, pop-up browser, and then navigates the original browser back in history to the page that displayed the list of journals.</span></span> <span data-ttu-id="80f09-112">Pēc tam var parādīt abas lapas līdzas.</span><span class="sxs-lookup"><span data-stu-id="80f09-112">You can then display both pages side-by-side.</span></span> <span data-ttu-id="80f09-113">Kad esat pabeidzis žurnāla skatīšanu, žurnālu saraksta lapā varat mainīt atlasīto žurnālu un rindu lapa uznirstošajā logā automātiski parādīs jaunatlasītā žurnāla rindas.</span><span class="sxs-lookup"><span data-stu-id="80f09-113">When you are done viewing a journal, you can change the selected journal on the journal list page, and the lines page in the pop-up window will automatically display the lines of the newly selected journal.</span></span>

<span data-ttu-id="80f09-114">[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span><span class="sxs-lookup"><span data-stu-id="80f09-114">[![pages-show-side-by-side](./media/pages-show-side-by-side.png)](./media/pages-show-side-by-side.png)</span></span>

<span data-ttu-id="80f09-115">Dinamiskā saistīšana un atsvaidzināšana tiek veikta atbilstoši attiecībām, kas pastāv starp datiem, kuri ir šo lapu pamatā.</span><span class="sxs-lookup"><span data-stu-id="80f09-115">The dynamic linking and refreshing happens due to the relations that exist between the data that is backing these pages.</span></span> <span data-ttu-id="80f09-116">Ja sistēmai nav informācijas par attiecībām starp datiem, uznirstošais logs netiks automātiski atsvaidzināts, reaģējot uz izmaiņām tā izcelsmes logā.</span><span class="sxs-lookup"><span data-stu-id="80f09-116">If the system is not aware of the relation between the data, the pop-up window will not refresh automatically in response to a change in the window it originated from.</span></span>

<span data-ttu-id="80f09-117">Dažām lapām ir vairāki skati, piemēram, režģa skata, virsrakstu skats un detalizētas informācijas skats.</span><span class="sxs-lookup"><span data-stu-id="80f09-117">Some pages have multiple views such as the Grid view, Header view, and Details view.</span></span> <span data-ttu-id="80f09-118">Ikona **Atvērt jaunā logā** atver visu lapu jaunā pārlūkprogrammas logā.</span><span class="sxs-lookup"><span data-stu-id="80f09-118">The **Open in new window** icon causes the entire page to be opened in the new browser window.</span></span> <span data-ttu-id="80f09-119">Tādēļ nav iespējams saglabāt vienas lapas divus skatus līdzās, izmantojot līdzekli **Atvērt jaunā logā**.</span><span class="sxs-lookup"><span data-stu-id="80f09-119">Therefore, you cannot keep two views of the same page side-by-side using the **Open in new window** feature.</span></span> <span data-ttu-id="80f09-120">Tomēr gandrīz visās šādās lapās ir navigācijas saraksts, ko varat izmantot, lai pārslēgtos starp ierakstiem un sasniegtu līdzīgu pieredzi.</span><span class="sxs-lookup"><span data-stu-id="80f09-120">However, almost all such pages have a navigation list that you can use to switch between records and achieve a similar experience.</span></span>

<span data-ttu-id="80f09-121">Pirms izmantojat līdzekli **Atvērt jaunā logā**, ir nepieciešams konfigurēt pārlūkprogrammas uznirstošo elementu bloķētāju, lai tas atļautu uznirstošos elementus no vietnes URL.</span><span class="sxs-lookup"><span data-stu-id="80f09-121">Before using the **Open in new window** feature, you should configure your browser's pop-up blocker to allow pop-ups from the URL of the site.</span></span> <span data-ttu-id="80f09-122">Piemēram, varat atļaut uznirstošos elementus no “\*. dynamics.com”.</span><span class="sxs-lookup"><span data-stu-id="80f09-122">As an example, you could allow pop-ups from "\*.dynamics.com".</span></span>

<span data-ttu-id="80f09-123">Līdzeklis **Atvērt jaunā logā** ir pieejams tikai tad, ja logā ir atvērta vairāk nekā viena lapa.</span><span class="sxs-lookup"><span data-stu-id="80f09-123">The **Open in new window** feature is only available when there is more than one page open in the window.</span></span> <span data-ttu-id="80f09-124">Turklāt uznirstošais logs automātiski aizveras, kad vairs nav atvērta neviena lapa (t. i., aizverot pēdējo lappusi attiecīgajā logā).</span><span class="sxs-lookup"><span data-stu-id="80f09-124">Also, the pop-up window automatically closes when there are no more pages open (that is, when the last page in that window is closed).</span></span> <span data-ttu-id="80f09-125">Sistēma arī aizver atvērtās lapas, kad pārejat uz citu programmas apgabalu.</span><span class="sxs-lookup"><span data-stu-id="80f09-125">The system also closes open pages when you navigate to a different area in the application.</span></span> <span data-ttu-id="80f09-126">Tādēļ, ja ir atvērti uznirstošie logi un jūs pārejat uz citu apgabalu programmā, uznirstošie logi tiek automātiski aizvērti, jo sistēma aizvēra lapas attiecīgajos logos.</span><span class="sxs-lookup"><span data-stu-id="80f09-126">Therefore, if you have pop-up windows open and navigate to a different area in the application, the pop-up windows are automatically closed because the pages in those windows were closed by the system.</span></span>

<span data-ttu-id="80f09-127">Uznirstošo logu augšējā joslā ir parādīta informācija par uzņēmumu, kurā lapa tika atvērta, un tā ir tikai lasāma.</span><span class="sxs-lookup"><span data-stu-id="80f09-127">The top bar in the pop-up windows displays information about the company the page was opened in and is read-only.</span></span> <span data-ttu-id="80f09-128">Uznirstošie logi ir atkarīgi arī no pārlūkprogrammas galvenā loga.</span><span class="sxs-lookup"><span data-stu-id="80f09-128">The pop-up windows also rely on the main browser window.</span></span> <span data-ttu-id="80f09-129">Ja galvenais logs tiek aizvērts vai atsvaidzināts, visi atvērtie uznirstošie logi kļūst tikai lasāmi.</span><span class="sxs-lookup"><span data-stu-id="80f09-129">If the main window is closed or refreshed, all open pop-up windows will become read only.</span></span> <span data-ttu-id="80f09-130">Tas nozīmē, ka joprojām varat apskatīt informāciju šajos logos, bet nevarēsiet ar to mijiedarboties.</span><span class="sxs-lookup"><span data-stu-id="80f09-130">This means that you can still view the information in these windows, but you will not be able to interact with it.</span></span>

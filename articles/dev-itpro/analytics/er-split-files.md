---
title: "Ģenerēto XML failu sadalīšana, pamatojoties uz faila lielumu un satura daudzumu"
description: "Šajā tēmā ir sniegta informācija par to, kā sadalīt ģenerētos failus, pamatojoties uz faila lielumu un satura vienumu daudzumu."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 8c3899d5c6602b3afe13b447b40f0b4dcc701448
ms.contentlocale: lv-lv
ms.lasthandoff: 08/13/2018

---

# <a name="split-generated-xml-files-based-on-file-size-and-content-quantity"></a><span data-ttu-id="b9e95-103">Ģenerēto XML failu sadalīšana, pamatojoties uz faila lielumu un satura daudzumu</span><span class="sxs-lookup"><span data-stu-id="b9e95-103">Split generated XML files based on file size and content quantity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b9e95-104">Varat noformēt elektronisko pārskatu (Electronic Reporting — ER) formātus, lai izejošos dokumentus ģenerētu XML formātā.</span><span class="sxs-lookup"><span data-stu-id="b9e95-104">You can design Electronic reporting (ER) formats to generate outgoing documents in XML format.</span></span> <span data-ttu-id="b9e95-105">Reizēm šos dokumentus var pieņemt tikai tad, ja tie atbilst noteiktiem kritērijiem, piemēram, maksimālajam faila lielumam vai maksimālajam noteiktu XML zaru skaitam.</span><span class="sxs-lookup"><span data-stu-id="b9e95-105">Sometimes, those documents can be accepted only when they meet specific criteria, such a maximum file size or a maximum number of some XML nodes.</span></span> <span data-ttu-id="b9e95-106">Varat noformēt ER formātus tā, lai ģenerētu elektroniskos dokumentus, kas atbilst šo dokumentu saņēmēju norādītajām prasībām.</span><span class="sxs-lookup"><span data-stu-id="b9e95-106">You can design ER formats to generate electronic documents that satisfy the requirements that the recipients of those documents specify.</span></span>

- <span data-ttu-id="b9e95-107">FILE formāta elementam varat definēt faila lieluma ierobežojumu kā ER izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="b9e95-107">For the FILE format element, you can define a limit on the file size as an ER expression.</span></span> <span data-ttu-id="b9e95-108">Ja ER pārskata ģenerēšanas laikā definētais ierobežojums tiek pārsniegts, ER beidz veidot pašreizējo failu un pēc tam pāriet pie nākamā faila veidošanas.</span><span class="sxs-lookup"><span data-stu-id="b9e95-108">If the defined limit is exceeded when an ER report is generated, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="b9e95-109">Ikvienam XML ELEMENT formātam elementu skaita ierobežojumu varat definēt kā ER izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="b9e95-109">For any XML ELEMENT format, you can define a limit on the number of elements as an ER expression.</span></span> <span data-ttu-id="b9e95-110">Ja ģenerētajā failā XML zaru skaits pārsniedz definēto ierobežojumu, kad tiek palaists ER pārskats, ER beidz veidot pašreizējo failu un pēc tam pāriet pie nākamā faila veidošanas.</span><span class="sxs-lookup"><span data-stu-id="b9e95-110">If the number of XML nodes in the file that is generated exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="b9e95-111">Ikvienam XML SEQUENCE formāta elementam bērnelementu skaita ierobežojumu varat definēt kā ER izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="b9e95-111">For any XML SEQUENCE format element, you can define a limit on the number of child elements as an ER expression.</span></span> <span data-ttu-id="b9e95-112">Ja ģenerētajā failā formāta elementa ligzdoto XML zaru skaits pārsniedz definēto ierobežojumu, kad tiek palaists ER pārskats, ER beidz veidot pašreizējo failu un pēc tam pāriet pie nākamā faila veidošanas.</span><span class="sxs-lookup"><span data-stu-id="b9e95-112">If the number of nested XML nodes of the format element in the generated file exceeds the defined limit when an ER report is run, ER finishes creating the current file and then moves on to create the next file.</span></span>
- <span data-ttu-id="b9e95-113">Jebkuru XML ELEMENT formāta elementu varat atzīmēt kā nedalāmu.</span><span class="sxs-lookup"><span data-stu-id="b9e95-113">You can mark any XML ELEMENT format element as non-breakable.</span></span> <span data-ttu-id="b9e95-114">Tādējādi formāta elementā ģenerētos XML zaru ligzdotos elementus varat paturēt vienā ģenerētajā failā.</span><span class="sxs-lookup"><span data-stu-id="b9e95-114">In this way, you can keep the nested items of XML nodes that are generated under the format element in a single generated file.</span></span>

<span data-ttu-id="b9e95-115">Lai ģenerētajam failam pievienotu XML zarus, papildus XML ELEMENT un XML SEQUENCE formāta elementu lietošanai varat izmantot RAW XML formāta elementu.</span><span class="sxs-lookup"><span data-stu-id="b9e95-115">In addition to using the XML ELEMENT and XML SEQUENCE format elements to add XML nodes to the generated file, you can use the RAW XML format element.</span></span> <span data-ttu-id="b9e95-116">Taču zari, ko pievienojat, izmantojot RAW XML formāta elementu, netiek ņemti vērā, kad tiek aprēķināts zaru skaits, lai novērtētu elementu skaita ierobežojumus.</span><span class="sxs-lookup"><span data-stu-id="b9e95-116">However, nodes that you add by using the RAW XML format element aren't considered when the number of nodes is calculated to evaluate the limits on the number of elements.</span></span>

<span data-ttu-id="b9e95-117">Ja konfigurējat failu galamērķus FILE formāta elementam, kas ir konfigurēts ģenerētās izvades sadalīšanai katru reizi, kad tiek pārsniegti noteikti ierobežojumi, katra ģenerētās izvades daļa tiek nosūtīta uz konfigurētā faila galamērķi kā atsevišķs fails.</span><span class="sxs-lookup"><span data-stu-id="b9e95-117">If you configured file destinations for a FILE format element that has been configured to split the generated output whenever specific limits are exceeded, each piece of generated output is sent to the configured file destination as an individual file.</span></span> <span data-ttu-id="b9e95-118">Lai piešķirtu unikālu nosaukumu failiem, kas tiek izveidoti, sadalot izvadi, jums ir jākonfigurē ER izteiksme FILE formāta elementam.</span><span class="sxs-lookup"><span data-stu-id="b9e95-118">To uniquely name the files that are created by splitting the output, you must configure an ER expression for the FILE format element.</span></span> <span data-ttu-id="b9e95-119">Ja ietverat ER datu avotu ar tipu NUMBER SEQUENCE, numuru sērija pieaug katrai sadalītās izvades daļai.</span><span class="sxs-lookup"><span data-stu-id="b9e95-119">If you include an ER data source of the NUMBER SEQUENCE type, the number sequence will be incremented for each piece of the split output.</span></span>

<span data-ttu-id="b9e95-120">Lai par šo līdzekli uzzinātu vairāk, noskatieties uzdevuma ceļvedi **ER XML failu sadalīšana, pamatojoties uz faila lielumu vai satura vienumu daudzumu**, kas veido daļu no biznesa procesa **7.5.4.3 IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)** un ko var lejupielādēt no [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="b9e95-120">To learn more about this feature, play the **ER Split XML files based on the file size or content item quantity** task guide, which is part of the **7.5.4.3 Acquire/Develop IT service/solution components (10677)** business process and can be downloaded from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="b9e95-121">Šajā uzdevumu ceļvedī ir izklāstīts ER formāta konfigurēšanas process, lai sadalītu ģenerētos failus, pamatojoties uz faila lieluma un satura vienumu daudzuma ierobežojumiem.</span><span class="sxs-lookup"><span data-stu-id="b9e95-121">This task guide walks you through the process of configuring an ER format to split generated files based on limits on the file size and content item quantity.</span></span> <span data-ttu-id="b9e95-122">Lai izpildītu šo uzdevuma ceļvedi, jums ir nepieciešams lejupielādēt tālāk norādītos failus.</span><span class="sxs-lookup"><span data-stu-id="b9e95-122">To complete the task guide, you must download the following files:</span></span>

- [<span data-ttu-id="b9e95-123">ER modeļa konfigurācija — XmlFilesSplittingModel.xml</span><span class="sxs-lookup"><span data-stu-id="b9e95-123">ER model configuration - XmlFilesSplittingModel.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)
- [<span data-ttu-id="b9e95-124">ER formāta konfigurācija — XmlFilesSplittingFormat.xml</span><span class="sxs-lookup"><span data-stu-id="b9e95-124">ER format configuration - XmlFilesSplittingFormat.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111)

## <a name="additional-resources"></a><span data-ttu-id="b9e95-125">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="b9e95-125">Additional resources</span></span>
[<span data-ttu-id="b9e95-126">Elektroniskās pārskatu veidošanas adresāti</span><span class="sxs-lookup"><span data-stu-id="b9e95-126">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)

[<span data-ttu-id="b9e95-127">Formulas veidotājs elektronisko atskaišu veidošanā</span><span class="sxs-lookup"><span data-stu-id="b9e95-127">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)


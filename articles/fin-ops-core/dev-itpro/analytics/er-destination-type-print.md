---
title: ER galamērķa printera tips
description: Šajā tēmā sniegta informācija par to, kā konfigurēt arhīva mērķi katrai MAPEI vai FAILA komponentam elektronisko pārskatu (ER) formātā.
author: NickSelin
manager: AnnBe
ms.date: 02/24/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 19613d9dfba21d591d96a2df45bedb80c043b3a7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561954"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="30216-103">Printera mērķis</span><span class="sxs-lookup"><span data-stu-id="30216-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="30216-104">Varat nosūtīt ģenerētu dokumentu tieši uz tīkla printeri, lai veiktu tiešo drukāšanu.</span><span class="sxs-lookup"><span data-stu-id="30216-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="30216-105">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="30216-105">Prerequisites</span></span>

<span data-ttu-id="30216-106">Pirms sākat, vispirms jāinstalē un jākonfigurē dokumentu maršrutēšanas aģents un pēc tam jāreģistrē tīkla printeri.</span><span class="sxs-lookup"><span data-stu-id="30216-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="30216-107">Plašāku informāciju skatiet tēmā [Dokumentu maršrutēšanas aģenta instalēšana, lai iespējotu tīkla drukāšanu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent)</span><span class="sxs-lookup"><span data-stu-id="30216-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="30216-108">Galamērķa printera pieejamības nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="30216-108">Make the Printer destination available</span></span>

<span data-ttu-id="30216-109">Lai nodrošinātu galamērķa **Printeris** pieejamību pašreizējā Microsoft Dynamics 365 Finance instancē, dodieties uz darbvietu **Līdzekļu pārvaldība** un ieslēdziet tālāk norādītos līdzekļus norādītajā secībā.</span><span class="sxs-lookup"><span data-stu-id="30216-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="30216-110">Elektronisko pārskatu izejošo dokumentu konvertēšana no Microsoft Office dokumentu formāta uz PDF formātu</span><span class="sxs-lookup"><span data-stu-id="30216-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="30216-111">Dokumentu maršrutēšanas aģents kā izejošo dokumentu elektronisko pārskatu veidošanas adresāts</span><span class="sxs-lookup"><span data-stu-id="30216-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="30216-112">[![ER printera galamērķa līdzekļa ieslēgšana līdzekļu pārvaldībā](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="30216-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="30216-113">Piemērojamība</span><span class="sxs-lookup"><span data-stu-id="30216-113">Applicability</span></span>

<span data-ttu-id="30216-114">Galamērķi **Printeris** var konfigurēt tikai tādiem failu komponentiem, kas tiek izmantoti izlaides ģenerēšanai drukājamā PDF formātā (PDF faila apvienošanas vai PDF failu formāta elementi) vai Microsoft Office Excel/Word formātā (Excel fails).</span><span class="sxs-lookup"><span data-stu-id="30216-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="30216-115">Kad izvade tiek ģenerēta PDF formātā, tā tiek nosūtīta uz printeri.</span><span class="sxs-lookup"><span data-stu-id="30216-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="30216-116">Ja izvade tiek ģenerēta Microsoft Office formātā, tā tiek automātiski konvertēta PDF formātā un pēc tam nosūtīta uz printeri.</span><span class="sxs-lookup"><span data-stu-id="30216-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="30216-117">Ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="30216-117">Limitations</span></span>

<span data-ttu-id="30216-118">Galamērķis **Printeris** ir ieviests tikai mākoņa izvietojumiem.</span><span class="sxs-lookup"><span data-stu-id="30216-118">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="30216-119">Galamērķa Printeris izmantošana</span><span class="sxs-lookup"><span data-stu-id="30216-119">Use the Printer destination</span></span>

1. <span data-ttu-id="30216-120">Lai nosūtītu ģenerēto dokumentu uz printeri, atlasiet opcijai **Iespējots** iestatījumu **Jā**.</span><span class="sxs-lookup"><span data-stu-id="30216-120">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="30216-121">Laukā **Printera nosaukums** atlasiet nepieciešamo tīkla printeri.</span><span class="sxs-lookup"><span data-stu-id="30216-121">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="30216-122">Atlasiet opcijai **Vai saglabāt drukāšanas arhīvā?** iestatījumu **Jā**, lai saglabātu ģenerēto izvadi drukāšanas arhīvā un tas būtu pieejams turpmākai drukāšanai.</span><span class="sxs-lookup"><span data-stu-id="30216-122">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="30216-123">Lai vēlāk piekļūtu arhivētai izvadei, dodieties uz **Organizācijas administrēšana** \> **Pieprasījumi un pārskati** \> **Pārskatu arhīvs**.</span><span class="sxs-lookup"><span data-stu-id="30216-123">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="30216-124">[![Galamērķa Printeris izmantošana](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="30216-124">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="30216-125">Konfigurējot galamērķi **Printeris**, opcijai **Pārveidot PDF formātā** nav jābūt ieslēgtai.</span><span class="sxs-lookup"><span data-stu-id="30216-125">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="30216-126">PDF pārvēršana drukāšanas nolūkiem notiks arī tad, ja opcija ir izslēgta.</span><span class="sxs-lookup"><span data-stu-id="30216-126">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="30216-127">Lai izmantotu konkrētu [lapas orientāciju](electronic-reporting-destinations.md#SelectPdfPageOrientation), drukājot izejošo dokumentu Excel formātā, ir jāieslēdz opcija **Konvertēt PDF formātā**.</span><span class="sxs-lookup"><span data-stu-id="30216-127">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="30216-128">Ja opcija **Konvertēt PDF formātā** ir iestatīta uz **Jā**, kļūst pieejams lauks **Lapas orientācija**.</span><span class="sxs-lookup"><span data-stu-id="30216-128">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="30216-129">Laukā **Lapas orientācija** var atlasīt lapas orientāciju.</span><span class="sxs-lookup"><span data-stu-id="30216-129">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="30216-130">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="30216-130">Additional resources</span></span>

- [<span data-ttu-id="30216-131">Elektronisko pārskatu veidošanas (ER) apskats</span><span class="sxs-lookup"><span data-stu-id="30216-131">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="30216-132">Elektroniskās pārskatu veidošanas (ER) adresāti</span><span class="sxs-lookup"><span data-stu-id="30216-132">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

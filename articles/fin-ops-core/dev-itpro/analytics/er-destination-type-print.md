---
title: ER galamērķa printera tips
description: Šajā tēmā sniegta informācija par to, kā konfigurēt arhīva mērķi katrai MAPEI vai FAILA komponentam elektronisko pārskatu (ER) formātā.
author: NickSelin
manager: AnnBe
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: c6e298f62ec69f349eb713d66313e535c7e01881
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094083"
---
# <a name="printer-destination"></a><a name="PrinterDestinationType"></a><span data-ttu-id="905f7-103">Printera mērķis</span><span class="sxs-lookup"><span data-stu-id="905f7-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="905f7-104">Varat nosūtīt ģenerētu dokumentu tieši uz tīkla printeri, lai veiktu tiešo drukāšanu.</span><span class="sxs-lookup"><span data-stu-id="905f7-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="905f7-105">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="905f7-105">Prerequisites</span></span>

<span data-ttu-id="905f7-106">Pirms sākat, vispirms jāinstalē un jākonfigurē dokumentu maršrutēšanas aģents un pēc tam jāreģistrē tīkla printeri.</span><span class="sxs-lookup"><span data-stu-id="905f7-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="905f7-107">Plašāku informāciju skatiet tēmā [Dokumentu maršrutēšanas aģenta instalēšana, lai iespējotu tīkla drukāšanu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent)</span><span class="sxs-lookup"><span data-stu-id="905f7-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="905f7-108">Galamērķa printera pieejamības nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="905f7-108">Make the Printer destination available</span></span>

<span data-ttu-id="905f7-109">Lai nodrošinātu galamērķa **Printeris** pieejamību pašreizējā Microsoft Dynamics 365 Finance instancē, dodieties uz darbvietu **Līdzekļu pārvaldība** un ieslēdziet tālāk norādītos līdzekļus norādītajā secībā.</span><span class="sxs-lookup"><span data-stu-id="905f7-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="905f7-110">Elektronisko pārskatu izejošo dokumentu konvertēšana no Microsoft Office dokumentu formāta uz PDF formātu</span><span class="sxs-lookup"><span data-stu-id="905f7-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="905f7-111">Dokumentu maršrutēšanas aģents kā izejošo dokumentu elektronisko pārskatu veidošanas adresāts</span><span class="sxs-lookup"><span data-stu-id="905f7-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="905f7-112">[![ER printera galamērķa līdzekļa ieslēgšana līdzekļu pārvaldībā](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="905f7-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="905f7-113">Piemērojamība</span><span class="sxs-lookup"><span data-stu-id="905f7-113">Applicability</span></span>

<span data-ttu-id="905f7-114">Galamērķi **Printeris** var konfigurēt tikai tādiem failu komponentiem, kas tiek izmantoti izlaides ģenerēšanai drukājamā PDF formātā (PDF faila apvienošanas vai PDF failu formāta elementi) vai Microsoft Office Excel/Word formātā (Excel fails).</span><span class="sxs-lookup"><span data-stu-id="905f7-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="905f7-115">Kad izvade tiek ģenerēta PDF formātā, tā tiek nosūtīta uz printeri.</span><span class="sxs-lookup"><span data-stu-id="905f7-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="905f7-116">Ja izvade tiek ģenerēta Microsoft Office formātā, tā tiek automātiski konvertēta PDF formātā un pēc tam nosūtīta uz printeri.</span><span class="sxs-lookup"><span data-stu-id="905f7-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="905f7-117">Ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="905f7-117">Limitations</span></span>

<span data-ttu-id="905f7-118">Šis līdzeklis ir priekšskatījuma līdzeklis, un tas ir pakļauts lietošanas noteikumiem, kas aprakstīti sadaļā [Microsoft Dynamics 365 priekšskatījumu papildu lietošanas noteikumi](https://go.microsoft.com/fwlink/?linkid=2105274).</span><span class="sxs-lookup"><span data-stu-id="905f7-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="905f7-119">Galamērķis **Printeris** ir ieviests tikai mākoņa izvietojumiem.</span><span class="sxs-lookup"><span data-stu-id="905f7-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="905f7-120">Galamērķa Printeris izmantošana</span><span class="sxs-lookup"><span data-stu-id="905f7-120">Use the Printer destination</span></span>

1. <span data-ttu-id="905f7-121">Lai nosūtītu ģenerēto dokumentu uz printeri, atlasiet opcijai **Iespējots** iestatījumu **Jā**.</span><span class="sxs-lookup"><span data-stu-id="905f7-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="905f7-122">Laukā **Printera nosaukums** atlasiet nepieciešamo tīkla printeri.</span><span class="sxs-lookup"><span data-stu-id="905f7-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="905f7-123">Atlasiet opcijai **Vai saglabāt drukāšanas arhīvā?** iestatījumu **Jā**, lai saglabātu ģenerēto izvadi drukāšanas arhīvā un tas būtu pieejams turpmākai drukāšanai.</span><span class="sxs-lookup"><span data-stu-id="905f7-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="905f7-124">Lai vēlāk piekļūtu arhivētai izvadei, dodieties uz **Organizācijas administrēšana** \> **Pieprasījumi un pārskati** \> **Pārskatu arhīvs**.</span><span class="sxs-lookup"><span data-stu-id="905f7-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="905f7-125">[![Galamērķa Printeris izmantošana](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="905f7-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="905f7-126">Konfigurējot galamērķi **Printeris**, opcijai **Pārveidot PDF formātā** nav jābūt ieslēgtai.</span><span class="sxs-lookup"><span data-stu-id="905f7-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="905f7-127">PDF pārvēršana drukāšanas nolūkiem notiks arī tad, ja opcija ir izslēgta.</span><span class="sxs-lookup"><span data-stu-id="905f7-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

<span data-ttu-id="905f7-128">Lai izmantotu konkrētu [lapas orientāciju](electronic-reporting-destinations.md#SelectPdfPageOrientation), drukājot izejošo dokumentu Excel formātā, ir jāieslēdz opcija **Konvertēt PDF formātā**.</span><span class="sxs-lookup"><span data-stu-id="905f7-128">To use a specific [page orientation](electronic-reporting-destinations.md#SelectPdfPageOrientation) when you print an outbound document in Excel format, you must turn on the **Convert to PDF** option.</span></span> <span data-ttu-id="905f7-129">Ja opcija **Konvertēt PDF formātā** ir iestatīta uz **Jā**, kļūst pieejams lauks **Lapas orientācija**.</span><span class="sxs-lookup"><span data-stu-id="905f7-129">When you set the **Convert to PDF** option to **Yes**, the **Page orientation** field becomes available.</span></span> <span data-ttu-id="905f7-130">Laukā **Lapas orientācija** var atlasīt lapas orientāciju.</span><span class="sxs-lookup"><span data-stu-id="905f7-130">In the **Page orientation** field, you can select a page orientation.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="905f7-131">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="905f7-131">Additional resources</span></span>

- [<span data-ttu-id="905f7-132">Elektronisko pārskatu veidošanas (ER) apskats</span><span class="sxs-lookup"><span data-stu-id="905f7-132">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="905f7-133">Elektroniskās pārskatu veidošanas (ER) adresāti</span><span class="sxs-lookup"><span data-stu-id="905f7-133">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)

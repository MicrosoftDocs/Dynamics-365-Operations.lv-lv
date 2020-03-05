---
title: ER galamērķa printera tips
description: Šajā tēmā ir izskaidrots, kā konfigurēt galamērķa printeri katram MAPES vai FAILA komponentam elektroniskās ziņošanas (ER) formātā, kas ir konfigurēts izejošo dokumentu ģenerēšanai vai nu PDF, vai Microsoft Office formātā (Excel\Word).
author: NickSelin
manager: AnnBe
ms.date: 01/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DocuType, ERSolutionTable, ERFormatDestinationTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-04-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 58e067baa130458e3a8e788d978604f208140a03
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019887"
---
# <a name="PrinterDestinationType"></a><span data-ttu-id="cb2c4-103">Galamērķa printeris</span><span class="sxs-lookup"><span data-stu-id="cb2c4-103">Printer destination</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb2c4-104">Varat nosūtīt ģenerētu dokumentu tieši uz tīkla printeri, lai veiktu tiešo drukāšanu.</span><span class="sxs-lookup"><span data-stu-id="cb2c4-104">You can send a generated document directly to a network printer for direct printing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cb2c4-105">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="cb2c4-105">Prerequisites</span></span>

<span data-ttu-id="cb2c4-106">Pirms sākat, vispirms jāinstalē un jākonfigurē dokumentu maršrutēšanas aģents un pēc tam jāreģistrē tīkla printeri.</span><span class="sxs-lookup"><span data-stu-id="cb2c4-106">Before you begin, you must install and configure the Document Routing Agent, and then register the network printers.</span></span> <span data-ttu-id="cb2c4-107">Plašāku informāciju skatiet tēmā [Dokumentu maršrutēšanas aģenta instalēšana, lai iespējotu tīkla drukāšanu](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent)</span><span class="sxs-lookup"><span data-stu-id="cb2c4-107">For more information, see [Install the Document Routing Agent to enable network printing](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/install-document-routing-agent).</span></span>

## <a name="make-the-printer-destination-available"></a><span data-ttu-id="cb2c4-108">Galamērķa printera pieejamības nodrošināšana</span><span class="sxs-lookup"><span data-stu-id="cb2c4-108">Make the Printer destination available</span></span>

<span data-ttu-id="cb2c4-109">Lai nodrošinātu galamērķa **Printeris** pieejamību pašreizējā Microsoft Dynamics 365 Finance instancē, dodieties uz darbvietu **Līdzekļu pārvaldība** un ieslēdziet tālāk norādītos līdzekļus norādītajā secībā.</span><span class="sxs-lookup"><span data-stu-id="cb2c4-109">To make the **Printer** destination available in the current instance of Microsoft Dynamics 365 Finance, go to the **Feature management** workspace, and turn on the following features, in this order:</span></span>

1. <span data-ttu-id="cb2c4-110">Elektronisko pārskatu izejošo dokumentu konvertēšana no Microsoft Office dokumentu formāta uz PDF formātu</span><span class="sxs-lookup"><span data-stu-id="cb2c4-110">Convert Electronic Reporting outbound documents from Microsoft Office formats to PDF</span></span>
2. <span data-ttu-id="cb2c4-111">Dokumentu maršrutēšanas aģents kā izejošo dokumentu elektronisko pārskatu veidošanas adresāts</span><span class="sxs-lookup"><span data-stu-id="cb2c4-111">Document Routing Agent as Electronic Reporting destination for outbound documents</span></span>

<span data-ttu-id="cb2c4-112">[![ER printera galamērķa līdzekļa ieslēgšana līdzekļu pārvaldībā](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span><span class="sxs-lookup"><span data-stu-id="cb2c4-112">[![Turning on the ER printer destination feature in Feature management](./media/ER_Destinations-EnablePrinterDestinationFeature.png)](./media/ER_Destinations-EnablePrinterDestinationFeature.png)</span></span>

### <a name="applicability"></a><span data-ttu-id="cb2c4-113">Piemērojamība</span><span class="sxs-lookup"><span data-stu-id="cb2c4-113">Applicability</span></span>

<span data-ttu-id="cb2c4-114">Galamērķi **Printeris** var konfigurēt tikai tādiem failu komponentiem, kas tiek izmantoti izlaides ģenerēšanai drukājamā PDF formātā (PDF faila apvienošanas vai PDF failu formāta elementi) vai Microsoft Office Excel/Word formātā (Excel fails).</span><span class="sxs-lookup"><span data-stu-id="cb2c4-114">The **Printer** destination can be configured only for file components that are used to generate output in either printable PDF format (PDF Merger or PDF file format elements) or Microsoft Office Excel/Word format (Excel file).</span></span> <span data-ttu-id="cb2c4-115">Kad izvade tiek ģenerēta PDF formātā, tā tiek nosūtīta uz printeri.</span><span class="sxs-lookup"><span data-stu-id="cb2c4-115">When output is generated in PDF format, it's sent to a printer.</span></span> <span data-ttu-id="cb2c4-116">Ja izvade tiek ģenerēta Microsoft Office formātā, tā tiek automātiski konvertēta PDF formātā un pēc tam nosūtīta uz printeri.</span><span class="sxs-lookup"><span data-stu-id="cb2c4-116">When output is generated in Microsoft Office format, it's automatically converted to PDF format and then sent to a printer.</span></span>

### <a name="limitations"></a><span data-ttu-id="cb2c4-117">Ierobežojumi</span><span class="sxs-lookup"><span data-stu-id="cb2c4-117">Limitations</span></span>

<span data-ttu-id="cb2c4-118">Šis līdzeklis ir priekšskatījuma līdzeklis, un tas ir pakļauts lietošanas noteikumiem, kas aprakstīti sadaļā [Microsoft Dynamics 365 priekšskatījumu papildu lietošanas noteikumi](https://go.microsoft.com/fwlink/?linkid=2105274).</span><span class="sxs-lookup"><span data-stu-id="cb2c4-118">This feature is a preview feature and is subject to the terms of use that are described in [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](https://go.microsoft.com/fwlink/?linkid=2105274).</span></span>

<span data-ttu-id="cb2c4-119">Galamērķis **Printeris** ir ieviests tikai mākoņa izvietojumiem.</span><span class="sxs-lookup"><span data-stu-id="cb2c4-119">The **Printer** destination is implemented only for cloud deployments.</span></span>

### <a name="use-the-printer-destination"></a><span data-ttu-id="cb2c4-120">Galamērķa Printeris izmantošana</span><span class="sxs-lookup"><span data-stu-id="cb2c4-120">Use the Printer destination</span></span>

1. <span data-ttu-id="cb2c4-121">Lai nosūtītu ģenerēto dokumentu uz printeri, atlasiet opcijai **Iespējots** iestatījumu **Jā**.</span><span class="sxs-lookup"><span data-stu-id="cb2c4-121">Set the **Enabled** option to **Yes** to send a generated document to a printer.</span></span>
2. <span data-ttu-id="cb2c4-122">Laukā **Printera nosaukums** atlasiet nepieciešamo tīkla printeri.</span><span class="sxs-lookup"><span data-stu-id="cb2c4-122">In the **Printer name** field, select the required network printer.</span></span>
3. <span data-ttu-id="cb2c4-123">Atlasiet opcijai **Vai saglabāt drukāšanas arhīvā?** iestatījumu **Jā**, lai saglabātu ģenerēto izvadi drukāšanas arhīvā un tas būtu pieejams turpmākai drukāšanai.</span><span class="sxs-lookup"><span data-stu-id="cb2c4-123">Set the **Save in print archive?** option to **Yes** to store the generated output in the print archive, so that it's available for further printing.</span></span> <span data-ttu-id="cb2c4-124">Lai vēlāk piekļūtu arhivētai izvadei, dodieties uz **Organizācijas administrēšana** \> **Pieprasījumi un pārskati** \> **Pārskatu arhīvs**.</span><span class="sxs-lookup"><span data-stu-id="cb2c4-124">To access archived output later, go to **Organization administration** \> **Inquiries and reports** \> **Report archive**.</span></span>

<span data-ttu-id="cb2c4-125">[![Galamērķa Printeris izmantošana](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span><span class="sxs-lookup"><span data-stu-id="cb2c4-125">[![Using the Printer destination](./media/ER_Destinations-PrinterDestination.png)](./media/ER_Destinations-PrinterDestination.png)</span></span>

> [!NOTE]
> <span data-ttu-id="cb2c4-126">Konfigurējot galamērķi **Printeris**, opcijai **Pārveidot PDF formātā** nav jābūt ieslēgtai.</span><span class="sxs-lookup"><span data-stu-id="cb2c4-126">The **Convert to PDF** option doesn't have to be turned on when you configure the **Printer** destination.</span></span> <span data-ttu-id="cb2c4-127">PDF pārvēršana drukāšanas nolūkiem notiks arī tad, ja opcija ir izslēgta.</span><span class="sxs-lookup"><span data-stu-id="cb2c4-127">The PDF conversion for printing purposes will occur even if the option is turned off.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb2c4-128">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="cb2c4-128">Additional resources</span></span>

- [<span data-ttu-id="cb2c4-129">Elektronisko pārskatu veidošanas (ER) apskats</span><span class="sxs-lookup"><span data-stu-id="cb2c4-129">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="cb2c4-130">Elektroniskās pārskatu veidošanas (ER) adresāti</span><span class="sxs-lookup"><span data-stu-id="cb2c4-130">Electronic reporting (ER) destinations</span></span>](electronic-reporting-destinations.md)
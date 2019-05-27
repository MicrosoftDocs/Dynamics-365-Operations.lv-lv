---
title: Pielāgotas glabāšanas vietas norādīšana ģenerētajiem dokumentiem
description: Šajā tēmā izskaidrots, kā paplašināt elektronisko pārskatu veidošanas (Electronic Reporting — ER) formātu ģenerēto dokumentu glabāšanas vietu sarakstu.
author: NickSelin
manager: AnnBe
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-3-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 3ea9de81045dfd01ffec2c8a1d98ea2ba4f2c49a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1552841"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a><span data-ttu-id="a2e83-103">Pielāgotas glabāšanas vietas norādīšana ģenerētajiem dokumentiem</span><span class="sxs-lookup"><span data-stu-id="a2e83-103">Specify a custom storage location for generated documents</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a2e83-104">Elektronisko pārskatu veidošanas (ER) struktūras lietojumprogrammas interfeiss (API) ļauj paplašināt ER formātu ģenerēto dokumentu glabāšanas vietu sarakstu.</span><span class="sxs-lookup"><span data-stu-id="a2e83-104">The application programming interface (API) of the Electronic reporting (ER) framework lets you extend the list of storage locations for documents that ER formats generate.</span></span> <span data-ttu-id="a2e83-105">Šī tēma ietver pārskatu par galvenajiem uzdevumiem, kas jums jāveic, lai pievienotu pielāgotu glabāšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="a2e83-105">This topic includes an overview of the main tasks that you must complete to add a custom storage location.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="a2e83-106">Priekšnosacījumi</span><span class="sxs-lookup"><span data-stu-id="a2e83-106">Prerequisites</span></span>

<span data-ttu-id="a2e83-107">Jums jāizvieto Microsoft Dynamics 365 for Finance and Operations topoloģija, kas atbalsta pastāvīgu būvēšanu.</span><span class="sxs-lookup"><span data-stu-id="a2e83-107">You must deploy a Microsoft Dynamics 365 for Finance and Operations topology that supports continuous build.</span></span> <span data-ttu-id="a2e83-108">(Papildinformāciju skatiet tēmā [Tādu topoloģiju izvietošana, kuras atbalsta pastāvīgu būvēšanu un testu automatizēšanu](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Jums jābūt piekļuvei šai Finance and Operations topoloģijai kādā no tālāk minētajām lomām:</span><span class="sxs-lookup"><span data-stu-id="a2e83-108">(For more information, see [Deploy topologies that support continuous build and test automation](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) You must have access to this Finance and Operations topology for one of the following roles:</span></span>

- <span data-ttu-id="a2e83-109">Elektroniskā pārskata izstrādātājs</span><span class="sxs-lookup"><span data-stu-id="a2e83-109">Electronic reporting developer</span></span>
- <span data-ttu-id="a2e83-110">Elektronisko pārskatu veidošanas funkcionālais konsultants</span><span class="sxs-lookup"><span data-stu-id="a2e83-110">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="a2e83-111">Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="a2e83-111">System administrator</span></span>

<span data-ttu-id="a2e83-112">Jums jābūt arī piekļuvei šīs Finance and Operations topoloģijas izstrādes videi.</span><span class="sxs-lookup"><span data-stu-id="a2e83-112">You must also have access to the development environment for this Finance and Operations topology.</span></span>

## <a name="create-or-import-an-er-format-configuration"></a><span data-ttu-id="a2e83-113">ER formāta konfigurācijas izveide vai importēšana</span><span class="sxs-lookup"><span data-stu-id="a2e83-113">Create or import an ER format configuration</span></span>

<span data-ttu-id="a2e83-114">Pašreizējā Finance and Operations topoloģijā [izveidojiet jaunu ER formātu](tasks/er-format-configuration-2016-11.md), lai ģenerētu dokumentus, kuriem plānojat pievienot pielāgotu glabāšanas vietu.</span><span class="sxs-lookup"><span data-stu-id="a2e83-114">In the current Finance and Operations topology, [create a new ER format](tasks/er-format-configuration-2016-11.md) to generate documents that you plan to add a custom storage location for.</span></span> <span data-ttu-id="a2e83-115">Vai arī [importējiet šajā topoloģijā jau izveidotu ER formātu](general-electronic-reporting-manage-configuration-lifecycle.md).</span><span class="sxs-lookup"><span data-stu-id="a2e83-115">Alternatively, [import an existing ER format into this topology](general-electronic-reporting-manage-configuration-lifecycle.md).</span></span>

![Formāta veidotāja lapa](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> <span data-ttu-id="a2e83-117">ER formātā, ko izveidojat vai importējat, jābūt vismaz vienam no šādiem formāta elementiem:</span><span class="sxs-lookup"><span data-stu-id="a2e83-117">The ER format that you create or import must contain at least one of the following format elements:</span></span>
>
> - <span data-ttu-id="a2e83-118">Fails</span><span class="sxs-lookup"><span data-stu-id="a2e83-118">File</span></span>
> - <span data-ttu-id="a2e83-119">Mape</span><span class="sxs-lookup"><span data-stu-id="a2e83-119">Folder</span></span>
> - <span data-ttu-id="a2e83-120">Apvienotājs</span><span class="sxs-lookup"><span data-stu-id="a2e83-120">Merger</span></span>
> - <span data-ttu-id="a2e83-121">Pielikums</span><span class="sxs-lookup"><span data-stu-id="a2e83-121">Attachment</span></span>

## <a name="create-a-new-document-type"></a><span data-ttu-id="a2e83-122">Jauna dokumenta tipa izveide</span><span class="sxs-lookup"><span data-stu-id="a2e83-122">Create a new document type</span></span>

<span data-ttu-id="a2e83-123">Lai norādītu, kā tiek maršrutēti ER formāta ģenerētie dokumenti, jums ir jākonfigurē [ER galamērķi](electronic-reporting-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="a2e83-123">To specify how documents that an ER format generates are routed, you must configure [ER destinations](electronic-reporting-destinations.md).</span></span> <span data-ttu-id="a2e83-124">Katram ER galamērķim, kas ir konfigurēts tā, lai ģenerētos dokumentus saglabātu kā failus, jums ir jānorāda dokumentu pārvaldības struktūras dokumenta veids.</span><span class="sxs-lookup"><span data-stu-id="a2e83-124">In each ER destination that is configured to store generated documents as files, you must specify a document type of the Document management framework.</span></span> <span data-ttu-id="a2e83-125">Lai maršrutētu dokumentus, ko ģenerē dažādi ER formāti, var lietot dažādus dokumentu veidus.</span><span class="sxs-lookup"><span data-stu-id="a2e83-125">Different document types can be used to route documents that different ER formats generate.</span></span>

1. <span data-ttu-id="a2e83-126">Pievienojiet jaunu [dokumenta veidu](../../fin-and-ops/organization-administration/configure-document-management.md) ER formātam, ko iepriekš izveidojāt vai importējāt.</span><span class="sxs-lookup"><span data-stu-id="a2e83-126">Add a new [document type](../../fin-and-ops/organization-administration/configure-document-management.md) for the ER format that you created or imported earlier.</span></span> <span data-ttu-id="a2e83-127">Nākamajā ilustrācijā dokumenta veids ir **FileX**.</span><span class="sxs-lookup"><span data-stu-id="a2e83-127">In the illustration that follows, the document type is **FileX**.</span></span>
2. <span data-ttu-id="a2e83-128">Lai atšķirtu šo dokumenta veidu no citiem dokumentu veidiem, iekļaujiet konkrētu atslēgvārdu tā nosaukumā.</span><span class="sxs-lookup"><span data-stu-id="a2e83-128">To differentiate this document type from other document types, include a specific keyword in its name.</span></span> <span data-ttu-id="a2e83-129">Piemēram, nākamajā ilustrācijā nosaukums ir **(LOCAL) folder** ((LOKĀLA) mape).</span><span class="sxs-lookup"><span data-stu-id="a2e83-129">For example, in the illustration that follows, the name is **(LOCAL) folder**.</span></span>
3. <span data-ttu-id="a2e83-130">Laukā **Klase** norādiet **Pievienot failu**.</span><span class="sxs-lookup"><span data-stu-id="a2e83-130">In the **Class** field, specify **Attach file**.</span></span>
4. <span data-ttu-id="a2e83-131">Laukā **Grupa** norādiet **Fails**.</span><span class="sxs-lookup"><span data-stu-id="a2e83-131">In the **Group** field, specify **File**.</span></span>

![Dokumentu veidu lapa](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> <span data-ttu-id="a2e83-133">Dokumentu veidi ir atkarīgi no uzņēmuma.</span><span class="sxs-lookup"><span data-stu-id="a2e83-133">Document types are company-specific.</span></span> <span data-ttu-id="a2e83-134">Lai izmantotu ER formātu ar konfigurēto galamērķi vairākos uzņēmumos, jums ir jākonfigurē atsevišķs dokumenta veids katram uzņēmumam.</span><span class="sxs-lookup"><span data-stu-id="a2e83-134">To use an ER format with a configured destination in multiple companies, you must configure a separate document type in each company.</span></span>

## <a name="review-source-code"></a><span data-ttu-id="a2e83-135">Pirmkoda pārskatīšana</span><span class="sxs-lookup"><span data-stu-id="a2e83-135">Review source code</span></span>

<span data-ttu-id="a2e83-136">Pārskatiet metodes **insertFile()** kodu klasei **ERDocuManagement**.</span><span class="sxs-lookup"><span data-stu-id="a2e83-136">Review the code of the **insertFile()** method of the **ERDocuManagement** class.</span></span> <span data-ttu-id="a2e83-137">Ievērojiet, ka tiek parādīts notikums **AttachingFile()**, kamēr ierakstam tiek pievienots ģenerētais fails.</span><span class="sxs-lookup"><span data-stu-id="a2e83-137">Notice that the **AttachingFile()** event is raised while the generated file is attached to a record.</span></span>

```
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

<span data-ttu-id="a2e83-138">Notikums **AttachingFile()** tiek parādīts, kad tiek apstrādāti tālāk norādītie ER galamērķi.</span><span class="sxs-lookup"><span data-stu-id="a2e83-138">The **AttachingFile()** event is raised when the following ER destinations are processed:</span></span>

- <span data-ttu-id="a2e83-139">**Arhīvs** — ja tiek izmantots šis galamērķis, tabulā ERFormatMappingRunJobTable tiek izveidots jauns ieraksts par izpildīto ER formātu.</span><span class="sxs-lookup"><span data-stu-id="a2e83-139">**Archive** – When this destination is used, a new record for the ER format that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="a2e83-140">Lauks **Arhivēts** šajā ierakstā ir iestatīts uz **Aplams**.</span><span class="sxs-lookup"><span data-stu-id="a2e83-140">The **Archived** field in this record is set to **False**.</span></span> <span data-ttu-id="a2e83-141">Ja ER formāts ir veiksmīgi izpildīts, ģenerētais dokuments tiek pievienots šim ierakstam, un tiek parādīts notikums **AttachingFile()**.</span><span class="sxs-lookup"><span data-stu-id="a2e83-141">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="a2e83-142">Dokumenta veids, kas atlasīts šajā ER galamērķī, nosaka pievienotā faila glabāšanas vietu (Microsoft Azure krātuve vai Microsoft SharePoint mape).</span><span class="sxs-lookup"><span data-stu-id="a2e83-142">The document type that is selected in this ER destination determines the storage location for the attached file (Microsoft Azure Storage or a Microsoft SharePoint folder).</span></span>
- <span data-ttu-id="a2e83-143">**Darbu arhīvs** — ja tiek izmantots šis galamērķis, tabulā ERFormatMappingRunJobTable tiek izveidots jauns ieraksts par izpildīto ER formātu.</span><span class="sxs-lookup"><span data-stu-id="a2e83-143">**Job archive** – When this destination is used, a new record for the ER form that is run is created in the ERFormatMappingRunJobTable table.</span></span> <span data-ttu-id="a2e83-144">Lauks **Arhivēts** šajā ierakstā ir iestatīts uz **Pareizs**.</span><span class="sxs-lookup"><span data-stu-id="a2e83-144">The **Archived** field in this record is set to **True**.</span></span> <span data-ttu-id="a2e83-145">Ja ER formāts ir veiksmīgi izpildīts, ģenerētais dokuments tiek pievienots šim ierakstam, un tiek parādīts notikums **AttachingFile()**.</span><span class="sxs-lookup"><span data-stu-id="a2e83-145">If the ER format is successfully run, the generated document is attached to this record, and the **AttachingFile()** event is raised.</span></span> <span data-ttu-id="a2e83-146">Dokumenta veids, kas ir konfigurēts ER parametros, nosaka pievienotā faila glabāšanas vietu (Azure krātuve vai SharePoint mape).</span><span class="sxs-lookup"><span data-stu-id="a2e83-146">The document type that is configured in the ER parameters determines the storage location for the attached file (Azure Storage or a SharePoint folder).</span></span>

![Elektronisko pārskatu veidošanas parametru lapa](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a><span data-ttu-id="a2e83-148">ER galamērķa konfigurēšana</span><span class="sxs-lookup"><span data-stu-id="a2e83-148">Configure an ER destination</span></span>

1. <span data-ttu-id="a2e83-149">Konfigurējiet arhivēto galamērķi vienam no iepriekš minētajiem izveidotā vai importētā ER formāta elementiem (fails, mape, apvienotājs vai pielikums).</span><span class="sxs-lookup"><span data-stu-id="a2e83-149">Configure the archived destination for one of the previously mentioned elements (file, folder, merger, or attachment) of the ER format that you created or imported.</span></span> <span data-ttu-id="a2e83-150">Norādes skatiet tēmā [ER galamērķu konfigurēšana](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span><span class="sxs-lookup"><span data-stu-id="a2e83-150">For guidance, see [ER Configure destinations](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).</span></span>
2. <span data-ttu-id="a2e83-151">Izmantojiet dokumenta veidu, kuru iepriekš pievienojāt konfigurētajam galamērķim.</span><span class="sxs-lookup"><span data-stu-id="a2e83-151">Use the document type that you added earlier for the configured destination.</span></span> <span data-ttu-id="a2e83-152">(Piemēram, šajā tēmā dokumenta veids ir **FileX**.)</span><span class="sxs-lookup"><span data-stu-id="a2e83-152">(For the example in this topic, the document type is **FileX**.)</span></span>

![Dialoglodziņš Galamērķu iestatījumi](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a><span data-ttu-id="a2e83-154">Pirmkoda modificēšana</span><span class="sxs-lookup"><span data-stu-id="a2e83-154">Modify source code</span></span>

1. <span data-ttu-id="a2e83-155">Pievienojiet jaunu klasi savam Microsoft Visual Studio projektam un ievadiet kodu, lai abonētu notikumu **AttachingFile()**, kas tika minēts iepriekš.</span><span class="sxs-lookup"><span data-stu-id="a2e83-155">Add a new class to your Microsoft Visual Studio project, and write code to subscribe to the **AttachingFile()** event that was mentioned earlier.</span></span> <span data-ttu-id="a2e83-156">(Papildinformāciju par izmantoto paplašināmības modeli skatiet tēmā [Atbildēšana, izmantojot EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Piemēram, jaunai klasei ievadiet kodu, kas veic tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="a2e83-156">(For more information about the extensibility pattern that is used, see [Respond by using EventHandlerResult](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) For example, in the new class, write code that performs the following actions:</span></span>

    1. <span data-ttu-id="a2e83-157">Saglabājiet ģenerētos failus vietējās failu sistēmas mapē serverī, kurā darbojas pakalpojums Application Object Server (AOS).</span><span class="sxs-lookup"><span data-stu-id="a2e83-157">Store generated files in a folder of the local file system of the server that runs the Application Object Server (AOS) service.</span></span>
    2. <span data-ttu-id="a2e83-158">Saglabājiet šos ģenerētos failus tikai tad, ja tiek izmantots jaunais dokumenta veids (piemēram, veids **FileX**, kura nosaukumā ir atslēgvārds “(LOCAL)”), kamēr fails tiek pievienots ierakstam ER izpildes darbu žurnālā.</span><span class="sxs-lookup"><span data-stu-id="a2e83-158">Store these generated files only when the new document type (for example, the **FileX** type that has the "(LOCAL)" keyword in its name) is used while a file is attached to the record in the ER execution job log.</span></span>

    ```
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. <span data-ttu-id="a2e83-159">Atjaunojiet savu projektu</span><span class="sxs-lookup"><span data-stu-id="a2e83-159">Rebuild your project.</span></span>

## <a name="run-the-er-format-that-you-created-or-imported"></a><span data-ttu-id="a2e83-160">Izveidotā vai importētā ER formāta palaišana</span><span class="sxs-lookup"><span data-stu-id="a2e83-160">Run the ER format that you created or imported</span></span>

1. <span data-ttu-id="a2e83-161">Izpildiet izveidoto vai importēto ER formātu.</span><span class="sxs-lookup"><span data-stu-id="a2e83-161">Execute the ER format that you created or imported.</span></span>
2. <span data-ttu-id="a2e83-162">Dodieties uz **Organizācijas administrēšana \> Elektronisko pārskatu veidošana \> Elektronisko pārskatu veidošanas darbi**.</span><span class="sxs-lookup"><span data-stu-id="a2e83-162">Go to **Organization administration \> Electronic reporting \> Electronic reporting jobs**.</span></span> <span data-ttu-id="a2e83-163">Atrodiet ierakstu, kas bija izveidots šim izpildes darbam un kuram ir pievienots ģenerētais fails.</span><span class="sxs-lookup"><span data-stu-id="a2e83-163">Find the record that was created for this execution job, and that has the generated file attached to it.</span></span>
3. <span data-ttu-id="a2e83-164">Izpētiet vietējo mapi **c:\\0**, lai atrastu pašu ģenerēto failu.</span><span class="sxs-lookup"><span data-stu-id="a2e83-164">Explore the local **C:\\0** folder to find same generated file.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2e83-165">Papildu resursi</span><span class="sxs-lookup"><span data-stu-id="a2e83-165">Additional resources</span></span>

- [<span data-ttu-id="a2e83-166">Elektroniskās pārskatu veidošanas adresāti</span><span class="sxs-lookup"><span data-stu-id="a2e83-166">Electronic reporting destinations</span></span>](electronic-reporting-destinations.md)
- [<span data-ttu-id="a2e83-167">Paplašināmības mājas lapa</span><span class="sxs-lookup"><span data-stu-id="a2e83-167">Extensibility home page</span></span>](../extensibility/extensibility-home-page.md)

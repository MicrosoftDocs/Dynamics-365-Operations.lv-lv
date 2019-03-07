---
title: Ienākošo dokumentu parsēšana Excel formātā
description: Šajā tēmā ir sniegta informācija par elektronisko pārskatu izveides (Electronic Reporting — ER) formātu izstrādi ienākošo Microsoft Excel failu satura parsēšanai.
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 490a9325be25908564a40478a1ee29feea67fc02
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "367482"
---
# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="f6f3c-103">Ienākošo dokumentu parsēšana Excel formātā</span><span class="sxs-lookup"><span data-stu-id="f6f3c-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f6f3c-104">Varat izstrādāt tādus elektronisko pārskatu izveides (ER) formātus ienākošo Microsoft Excel failus parsēšanai, kas atveido Microsoft Excel darbgrāmatās (XLSX formāta failos) ietvertos datus.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="f6f3c-105">Pēc tam saturu no šiem failiem varat izmantot, lai atjauninātu programmas datus.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="f6f3c-106">Tas ir noderīgi tālāk norādītajos gadījumos.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-106">This is useful if you:</span></span>

- <span data-ttu-id="f6f3c-107">Esat noformējis jaunu modeli un formātu un vēlaties tos pārbaudīt izpildlaikā.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="f6f3c-108">Tādā gadījumā programma Excel simulē faktiskos programmas datus.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="f6f3c-109">Pārvaldāt datus ārpus jūsu programmas programmā Excel un vēlaties šos datus importēt, lai iesniegtu noteiktu pārskatu.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="f6f3c-110">Lai uzzinātu vairāk par šo līdzekli, noskatieties uzdevumu ceļvežus **ER: datu importēšana no Microsoft Excel faila (1. daļa. Formāta izstrāde)** un **ER: datu importēšana no Microsoft Excel faila (2. daļa. Datu importēšana)** (tie ir ietverti biznesa procesā 7.5.4.3. IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)).</span><span class="sxs-lookup"><span data-stu-id="f6f3c-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="f6f3c-111">Šajos uzdevumu ceļvežos ir izklāstīts, kā ienākošo Excel failu var parsēt, izmantojot ER formātu, lai importētu informāciju no ienākošiem dokumentiem un atjauninātu programmas datus.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="f6f3c-112">Šo uzdevumu ceļvežu failus varat lejupielādēt no [Microsoft lejupielādes centra](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="f6f3c-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="f6f3c-113">Lai izpildītu iepriekš minētos uzdevumu ceļvežus, lejupielādējiet tālāk norādītos failus.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="f6f3c-114">Satura apraksts</span><span class="sxs-lookup"><span data-stu-id="f6f3c-114">Content description</span></span>                         | <span data-ttu-id="f6f3c-115">Fails</span><span class="sxs-lookup"><span data-stu-id="f6f3c-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="f6f3c-116">Ienākošais fails .XLSX formātā — veidne</span><span class="sxs-lookup"><span data-stu-id="f6f3c-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="f6f3c-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="f6f3c-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="f6f3c-118">Ienākošais fails .XLSX formātā — datu paraugs</span><span class="sxs-lookup"><span data-stu-id="f6f3c-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="f6f3c-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="f6f3c-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="f6f3c-120">Ja vēl neesat atskaņojis tālāk norādīto uzdevuma ceļvedi, [ER Nepieciešamo konfigurāciju izveide datu importēšanai no ārēja faila](./tasks/er-required-configurations-import-data.md) pašreizējā Dynamics 365 for Finance and Operation programmā, lejupielādējiet tālāk norādīto failu.</span><span class="sxs-lookup"><span data-stu-id="f6f3c-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Dynamics 365 for Finance and Operation application, download the following file.</span></span>

| <span data-ttu-id="f6f3c-121">Satura apraksts</span><span class="sxs-lookup"><span data-stu-id="f6f3c-121">Content description</span></span>    | <span data-ttu-id="f6f3c-122">Fails</span><span class="sxs-lookup"><span data-stu-id="f6f3c-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="f6f3c-123">ER modeļa konfigurācija</span><span class="sxs-lookup"><span data-stu-id="f6f3c-123">ER model configuration</span></span> | [<span data-ttu-id="f6f3c-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="f6f3c-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |

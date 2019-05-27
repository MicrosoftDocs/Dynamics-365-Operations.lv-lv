---
title: Elektronisko pārskatu veidošanas formātu modificēšana, atkārtoti lietojot Excel veidnes
description: Šajā tēmā ir sniegta informācija par to, kā var izmainīt biznesa dokumentu ģenerēšanai izmantoto elektronisko pārskatu veidošanas (ER) formātu, atkārtoti lietojot izmainītu Excel veidni.
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8707f7b184bb66648edd0e48672c5514a0a5caf1
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545011"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a><span data-ttu-id="c7769-103">Elektronisko pārskatu veidošanas formātu modificēšana, atkārtoti lietojot Excel veidnes</span><span class="sxs-lookup"><span data-stu-id="c7769-103">Modify Electronic reporting formats by reapplying Excel templates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c7769-104">Elektronisko pārskatu veidošanas (ER) rīks tiek izmantots elektroniska formāta biznesa dokumentu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="c7769-104">The Electronic reporting (ER) tool is used to generate business documents in an electronic format.</span></span> <span data-ttu-id="c7769-105">Ja vēlaties ģenerēt biznesa dokumentu, jums ir jāizveido ER formāta un pēc tam jāizmanto ER noformētājs, lai definētu biznesa dokumenta izkārtojumu un norādītu tajā ietveramos datus.</span><span class="sxs-lookup"><span data-stu-id="c7769-105">To generate a business document, you must create an ER format, and then use the ER designer to define the layout of the business document and specify the data that should be included in it.</span></span> <span data-ttu-id="c7769-106">Pēc tam varat izpildīt ER formātu, lai ģenerētu biznesa dokumentu.</span><span class="sxs-lookup"><span data-stu-id="c7769-106">You can then run the ER format to generate the business document.</span></span>

<span data-ttu-id="c7769-107">ER rīku var izmantot biznesa dokumentu ģenerēšanai Microsoft Excel failu formātā.</span><span class="sxs-lookup"><span data-stu-id="c7769-107">The ER tool can be used to generate business documents as Microsoft Excel files.</span></span> <span data-ttu-id="c7769-108">Kā šo dokumentu veidnes varat izmantot Excel dokumentus.</span><span class="sxs-lookup"><span data-stu-id="c7769-108">You can use an Excel document as a template for these documents.</span></span> <span data-ttu-id="c7769-109">Lai ER noformētājā definētu dokumenta izkārtojumu, varat definētajā ER formātā importēt tā Excel dokumenta saturu, ko vēlaties izmantot kā veidni.</span><span class="sxs-lookup"><span data-stu-id="c7769-109">To define the document layout in the ER designer, you can import the contents of the Excel document that you want to use as a template into the defined ER format.</span></span> <span data-ttu-id="c7769-110">Lai saņemtu papildinformāciju un izmēģinātu šo scenāriju, atskaņojiet uzdevuma ceļvedi **Konfigurācijas noformēšana pārskatu ģenerēšanai OPENXML formātā (ER)** (daļa no 7.5.4.3. biznesa procesa IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)).</span><span class="sxs-lookup"><span data-stu-id="c7769-110">For more details, and to practice this scenario, play the task guide **ER Design a configuration for generating reports in OPENXML format** (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span>

<span data-ttu-id="c7769-111">Ja rediģējat Excel dokumentu, kas tiek izmantots kā biznesa dokumenta veidne, jauna ER funkcionalitāte sniedz iespēju ER formātam atkārtoti lietot atjaunināto veidni.</span><span class="sxs-lookup"><span data-stu-id="c7769-111">If you edit the Excel document that is used as a template for a business document, new ER functionality lets you reapply the updated template to the ER format.</span></span> <span data-ttu-id="c7769-112">Pēc tam ER formāts tiek atjaunināts atbilstoši atjauninātajai veidnei.</span><span class="sxs-lookup"><span data-stu-id="c7769-112">The ER format is then updated so that it adheres to the updated template.</span></span> <span data-ttu-id="c7769-113">Lai saņemtu papildinformāciju par šo funkcionalitāti, atskaņojiet uzdevuma ceļvedi **Formāta izmainīšana, atkārtoti lietojot Excel veidni (ER)** (daļa no 7.5.5.3. biznesa procesa IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10683)).</span><span class="sxs-lookup"><span data-stu-id="c7769-113">For more details about this functionality, play the task guide **ER Modify a format by reapplying an Excel template** (part of the 7.5.5.3 Acquire/Develop IT service/solution components (10683) business process).</span></span> <span data-ttu-id="c7769-114">Veicot uzdevuma ceļveža darbību, kuras ietvaros importējat atjauninātu veidni, izmantojiet maksājumu pārskata Excel faila SampleVendPaymWsReport2 izmainīto veidni.</span><span class="sxs-lookup"><span data-stu-id="c7769-114">In the task guide step where you import an updated template, use the modified template of the Payment Report Excel file, SampleVendPaymWsReport2, as a template.</span></span>

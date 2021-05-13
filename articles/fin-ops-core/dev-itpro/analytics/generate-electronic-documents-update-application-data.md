---
title: Elektronisko dokumentu ģenerēšana un programmas datu atjaunināšana, izmantojot ER
description: Varat veidot elektronisko pārskatu (Electronic Reporting — ER) formātus, ko var izmantot izejošo elektronisko dokumentu ģenerēšanai.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f66a173c7d66f915a7802e42caf1a36f661eea1
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944321"
---
# <a name="generate-electronic-documents-and-update-application-data-by-using-er"></a><span data-ttu-id="d100d-103">Elektronisko dokumentu ģenerēšana un programmas datu atjaunināšana, izmantojot ER</span><span class="sxs-lookup"><span data-stu-id="d100d-103">Generate electronic documents and update application data by using ER</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d100d-104">Varat veidot elektronisko pārskatu (Electronic Reporting — ER) formātus, ko var izmantot izejošo elektronisko dokumentu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="d100d-104">You can design Electronic reporting (ER) formats that can be used in the application to generate outgoing electronic documents.</span></span> <span data-ttu-id="d100d-105">Varat arī izstrādāt ER formātus, kas parsē ienākošos elektroniskos dokumentus un izmanto šajos dokumentos ietverto saturu, lai atjauninātu programmas datus.</span><span class="sxs-lookup"><span data-stu-id="d100d-105">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span>

<span data-ttu-id="d100d-106">Ar šo funkcionalitāti viens ER formāts var tikt izmantots, gan lai ģenerētu izejošos elektroniskos dokumentus, gan lai pēc tam atjauninātu programmas datus.</span><span class="sxs-lookup"><span data-stu-id="d100d-106">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="d100d-107">Šo līdzekli var lietot tālāk aprakstītajos scenārijos.</span><span class="sxs-lookup"><span data-stu-id="d100d-107">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="d100d-108">Lai novērstu iespēju, ka programmas dati tiek atkārtoti izmantoti turpmākajos procesos, programmas datus varat atzīmēt uzreiz pēc to lietošanas elektronisko dokumentu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="d100d-108">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="d100d-109">Varat, piemēram, maksājumu transakcijas atzīmēt kā jau apstrādāts uzreiz pēc tam, kad tās ir iekļautas ģenerētā maksājumu ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="d100d-109">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="d100d-110">Lai saglabātu apstrādes informāciju elektroniskajiem dokumentiem, kas ir ģenerēti, izmantojot ER loģiku.</span><span class="sxs-lookup"><span data-stu-id="d100d-110">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="d100d-111">Piemēram, unikālu identifikāciju maksājuma ziņojumam, kas tiek ģenerēts, izmantojot ER izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="d100d-111">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="d100d-112">Šī izteiksme ir balstīta uz ER dialoglodziņā ievadīto informāciju, kad ER formāts tiek palaists dokumentu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="d100d-112">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="d100d-113">Lai uzzinātu vairāk par šo līdzekli, atskaņojiet ER uzdevumu ceļvežu kopu Dokumentu ģenerēšana, saglabājot izmaiņas programmas datos (daļa no 7.5.4.3. biznesa procesa IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)), kur ir sniegti detalizēti norādījumi par Intrastat pārskatu izveidi un arhivēšanu.</span><span class="sxs-lookup"><span data-stu-id="d100d-113">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="d100d-114">Lai izpildītu noteiktas šajos uzdevumu ceļvežos iekļautās darbības, ir nepieciešami tālāk norādītie faili.</span><span class="sxs-lookup"><span data-stu-id="d100d-114">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="d100d-115">Lejupielādējiet un saglabājiet šos failus lokālajā datorā.</span><span class="sxs-lookup"><span data-stu-id="d100d-115">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="d100d-116">ER datu modeļa konfigurācija: Intrastat (modelis)</span><span class="sxs-lookup"><span data-stu-id="d100d-116">ER data model configuration: Intrastat (model)</span></span>](https://download.microsoft.com/download/9/c/e/9ceeacbe-c13e-422e-96f2-594c4a6b45b7/Intrastatmodel.xml)
- [<span data-ttu-id="d100d-117">ER modeļa kartējuma konfigurācija: Intrastat (kartēšana)</span><span class="sxs-lookup"><span data-stu-id="d100d-117">ER model mapping configuration: Intrastat (mapping)</span></span>](https://download.microsoft.com/download/2/1/d/21ddaaeb-64c5-4408-a35f-1ccb922d40a4/Intrastatmapping.xml)
- [<span data-ttu-id="d100d-118">ER formāta konfigurācija: Intrastat (formāts)</span><span class="sxs-lookup"><span data-stu-id="d100d-118">ER format configuration: Intrastat (format)</span></span>](https://download.microsoft.com/download/8/b/b/8bbb8891-e88d-4739-b92a-2d1d2fffcb79/Intrastatformat.xml)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

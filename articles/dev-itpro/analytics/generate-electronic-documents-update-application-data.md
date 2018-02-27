---
title: "Ģenerēt elektroniskos dokumentus un atjaunināt programmas datus, izmantojot elektronisko pārskatu veidošanas rīku"
description: "Varat veidot elektronisko pārskatu (Electronic Reporting — ER) formātus, ko programmā Finance and Operations var izmantot izejošo elektronisko dokumentu ģenerēšanai. Varat arī izstrādāt ER formātus, kas parsē ienākošos elektroniskos dokumentus un izmanto šajos dokumentos ietverto saturu, lai atjauninātu programmas datus."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: e2447274016f517db3ec0eb8f55c6b3163822f50
ms.contentlocale: lv-lv
ms.lasthandoff: 02/27/2018

---

# <a name="generate-electronic-documents-and-update-application-data-using-the-electronic-reporting-tool"></a><span data-ttu-id="c7594-104">Ģenerēt elektroniskos dokumentus un atjaunināt programmas datus, izmantojot elektronisko pārskatu veidošanas rīku</span><span class="sxs-lookup"><span data-stu-id="c7594-104">Generate electronic documents and update application data using the Electronic reporting tool</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c7594-105">Varat veidot elektronisko pārskatu (Electronic Reporting — ER) formātus, ko programmā Finance and Operations var izmantot izejošo elektronisko dokumentu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="c7594-105">You can design Electronic reporting (ER) formats that can be used in the Finance and Operations application to generate outgoing electronic documents.</span></span> <span data-ttu-id="c7594-106">Varat arī izstrādāt ER formātus, kas parsē ienākošos elektroniskos dokumentus un izmanto šajos dokumentos ietverto saturu, lai atjauninātu programmas datus.</span><span class="sxs-lookup"><span data-stu-id="c7594-106">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span> 

<span data-ttu-id="c7594-107">Ar šo funkcionalitāti viens ER formāts var tikt izmantots, gan lai ģenerētu izejošos elektroniskos dokumentus, gan lai pēc tam atjauninātu programmas datus.</span><span class="sxs-lookup"><span data-stu-id="c7594-107">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="c7594-108">Šo līdzekli var lietot tālāk aprakstītajos scenārijos.</span><span class="sxs-lookup"><span data-stu-id="c7594-108">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="c7594-109">Lai novērstu iespēju, ka programmas dati tiek atkārtoti izmantoti turpmākajos procesos, programmas datus varat atzīmēt uzreiz pēc to lietošanas elektronisko dokumentu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="c7594-109">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="c7594-110">Varat, piemēram, maksājumu transakcijas atzīmēt kā jau apstrādāts uzreiz pēc tam, kad tās ir iekļautas ģenerētā maksājumu ziņojumā.</span><span class="sxs-lookup"><span data-stu-id="c7594-110">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="c7594-111">Lai saglabātu apstrādes informāciju elektroniskajiem dokumentiem, kas ir ģenerēti, izmantojot ER loģiku.</span><span class="sxs-lookup"><span data-stu-id="c7594-111">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="c7594-112">Piemēram, unikālu identifikāciju maksājuma ziņojumam, kas tiek ģenerēts, izmantojot ER izteiksmi.</span><span class="sxs-lookup"><span data-stu-id="c7594-112">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="c7594-113">Šī izteiksme ir balstīta uz ER dialoglodziņā ievadīto informāciju, kad ER formāts tiek palaists dokumentu ģenerēšanai.</span><span class="sxs-lookup"><span data-stu-id="c7594-113">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="c7594-114">Lai uzzinātu vairāk par šo līdzekli, atskaņojiet ER uzdevumu ceļvežu kopu Dokumentu ģenerēšana, saglabājot izmaiņas programmas datos (daļa no 7.5.4.3. biznesa procesa IT pakalpojumu/risinājumu komponentu iegāde/izstrāde (10677)), kur ir sniegti detalizēti norādījumi par Intrastat pārskatu izveidi un arhivēšanu.</span><span class="sxs-lookup"><span data-stu-id="c7594-114">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="c7594-115">Lai izpildītu noteiktas šajos uzdevumu ceļvežos iekļautās darbības, ir nepieciešami tālāk norādītie faili.</span><span class="sxs-lookup"><span data-stu-id="c7594-115">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="c7594-116">Lejupielādējiet un saglabājiet šos failus lokālajā datorā.</span><span class="sxs-lookup"><span data-stu-id="c7594-116">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="c7594-117">ER datu modeļa konfigurācija: Intrastat (modelis)</span><span class="sxs-lookup"><span data-stu-id="c7594-117">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="c7594-118">ER modeļa kartējuma konfigurācija: Intrastat (kartēšana)</span><span class="sxs-lookup"><span data-stu-id="c7594-118">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="c7594-119">ER formāta konfigurācija: Intrastat (formāts)</span><span class="sxs-lookup"><span data-stu-id="c7594-119">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)


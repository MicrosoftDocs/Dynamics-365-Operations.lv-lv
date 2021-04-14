---
title: Ienākošo dokumentu parsēšana JSON formātā
description: Šajā tēmā ir paskaidrots, kā iestatīt elektronisko pārskatu (ER) formātus, lai parsētu ienākošos dokumentus JavaScript Object Notation (JSON) formātā.
author: kfend
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 4e598dc15b619c2f6a0525ea18c371484ca26fa4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755158"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="72ca2-103">Ienākošo dokumentu parsēšana JSON formātā</span><span class="sxs-lookup"><span data-stu-id="72ca2-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="72ca2-104">Varat izstrādāt elektronisko pārskatu (ER) formātus, lai parsētu ienākošos elektroniskos dokumentus, kuri attēlo datus teksta formātā, kas ir balstīts uz JavaScript (citiem vārdiem sakot, failus JavaScript Object Notation \[JSON\] formātā).</span><span class="sxs-lookup"><span data-stu-id="72ca2-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="72ca2-105">Lai uzzinātu vairāk par šo līdzekli, lejupielādējiet failus tālāk redzamajā tabulā un pēc tam atskaņojiet uzdevuma ceļvedi ER Izveidot formāta konfigurāciju, lai importētu datus no ārēja JSON faila.</span><span class="sxs-lookup"><span data-stu-id="72ca2-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="72ca2-106">Šajā uzdevuma ceļvedī ir parādīts, kā ER formātu var izmantot, lai parsētu ienākošo JSON failu, lai atjauninātu programmas datus.</span><span class="sxs-lookup"><span data-stu-id="72ca2-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="72ca2-107">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="72ca2-107">Title</span></span>                                  | <span data-ttu-id="72ca2-108">Faila nosaukums</span><span class="sxs-lookup"><span data-stu-id="72ca2-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="72ca2-109">ER formāta konfigurācija</span><span class="sxs-lookup"><span data-stu-id="72ca2-109">ER format configuration</span></span>                | [<span data-ttu-id="72ca2-110">Formāts kreditoru trans_JSON.xml importēšanai</span><span class="sxs-lookup"><span data-stu-id="72ca2-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="72ca2-111">Ienākošā faila .csv formātā paraugs</span><span class="sxs-lookup"><span data-stu-id="72ca2-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="72ca2-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="72ca2-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="72ca2-113">Prasības</span><span class="sxs-lookup"><span data-stu-id="72ca2-113">Requirements</span></span>

<span data-ttu-id="72ca2-114">Pirms izpildāt uzdevuma ceļvedi ER Izveidot formāta konfigurāciju, lai importētu datus no ārēja JSON faila, ir jānodrošina šāda prasība:</span><span class="sxs-lookup"><span data-stu-id="72ca2-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="72ca2-115">Pamatelementi JSON failā var būt tikai objekta elementi.</span><span class="sxs-lookup"><span data-stu-id="72ca2-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="72ca2-116">Objekta ligzdotajiem elementiem ir jābūt rekvizītu elementiem, lai tiktu izveidota derīga JSON struktūra.</span><span class="sxs-lookup"><span data-stu-id="72ca2-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="72ca2-117">JSON masīvi var būt tikai objekta rekvizītu elementu ligzdoti elementi.</span><span class="sxs-lookup"><span data-stu-id="72ca2-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="72ca2-118">JSON masīvi var saturēt tikai JSON objektus.</span><span class="sxs-lookup"><span data-stu-id="72ca2-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="72ca2-119">Tie nevar saturēt tiešas virknes/skaitliskas vērtības un ligzdotus masīvus.</span><span class="sxs-lookup"><span data-stu-id="72ca2-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="72ca2-120">Elementi šajos masīvos tiks parsēti tādā secībā, kādā tie ir norādīti formātā.</span><span class="sxs-lookup"><span data-stu-id="72ca2-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="72ca2-121">Tiek ņemti vērā katra JSON objekta daudzkārtīguma iestatījumi.</span><span class="sxs-lookup"><span data-stu-id="72ca2-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="72ca2-122">Turklāt jums ir jāizpilda uzdevuma ceļvedis [ER Izveidot nepieciešamās konfigurācijas datu importēšanai no ārējā faila elektronisko pārskatu veidošanai](tasks/er-required-configurations-import-data.md), ja vēl neesat to izpildījis.</span><span class="sxs-lookup"><span data-stu-id="72ca2-122">Additionally, you must complete the [ER Create required configurations to import data from an external file](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="72ca2-123">Lai izpildītu šo uzdevuma ceļvedi, lejupielādējiet tālāk norādīto failu.</span><span class="sxs-lookup"><span data-stu-id="72ca2-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="72ca2-124">Virsraksts</span><span class="sxs-lookup"><span data-stu-id="72ca2-124">Title</span></span>                  | <span data-ttu-id="72ca2-125">Faila nosaukums</span><span class="sxs-lookup"><span data-stu-id="72ca2-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="72ca2-126">ER modeļa konfigurācija</span><span class="sxs-lookup"><span data-stu-id="72ca2-126">ER model configuration</span></span> | [<span data-ttu-id="72ca2-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="72ca2-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
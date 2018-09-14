--- 
title: "ISO20022 pārvietošanai kredītā konfigurācijas importēšana"
description: "Šī procedūra parāda, kā importēt kreditora maksājuma elektronisko pārskatu veidošanas konfigurāciju."
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 3fbd2e39f488696ebe8db5579ed88595e246ce97
ms.contentlocale: lv-lv
ms.lasthandoff: 09/14/2018

---
# <a name="import-iso20022-credit-transfer-configuration"></a><span data-ttu-id="a324d-103">ISO20022 pārvietošanai kredītā konfigurācijas importēšana</span><span class="sxs-lookup"><span data-stu-id="a324d-103">Import ISO20022 credit transfer configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a324d-104">Šī procedūra parāda, kā importēt kreditora maksājuma elektronisko pārskatu veidošanas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="a324d-104">This procedure shows how to import a vendor payment electronic reporting configuration.</span></span> <span data-ttu-id="a324d-105">Vācijas ISO 20022 kredīta pārskaitījuma formāts tiek izmantots kā piemērs.</span><span class="sxs-lookup"><span data-stu-id="a324d-105">The German ISO 20022 credit transfer format is used as an example.</span></span> <span data-ttu-id="a324d-106">Šo procedūru var izmantot citiem pieejamajiem elektronisko pārskatu veidošanas formātiem.</span><span class="sxs-lookup"><span data-stu-id="a324d-106">This procedure can be used for other available electronic reporting format.</span></span> 

<span data-ttu-id="a324d-107">Šis uzdevums tika izveidots, izmantojot demonstrācijas datu uzņēmumu DEMF, bet jūs varat izmantot jebkuru demonstrācijas datu uzņēmumu, lai pabeigtu šo uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="a324d-107">This task was created using the demo data company DEMF but you can use any demo data company to complete this task.</span></span>

<span data-ttu-id="a324d-108">Šis ir pirmais no pieciem uzdevumus, kas kopumā parāda kreditoru maksājumu process, izmantojot elektronisko pārskatu veidošanas konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="a324d-108">This is the first of five tasks, that together illustrate the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="a324d-109">Šī procedūra ir paredzēta līdzeklim, kas tika pievienots Dynamics 365 for Operations versijā 1611.</span><span class="sxs-lookup"><span data-stu-id="a324d-109">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="a324d-110">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="a324d-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a324d-111">Sarakstā pieejamās konfigurācijas nodrošinātāji, atlasiet Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a324d-111">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="a324d-112">Noklikšķiniet uz Iestatīt aktīvu.</span><span class="sxs-lookup"><span data-stu-id="a324d-112">Click Set active.</span></span>
4. <span data-ttu-id="a324d-113">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="a324d-113">Click Repositories.</span></span>
5. <span data-ttu-id="a324d-114">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="a324d-114">Click Open.</span></span>
6. <span data-ttu-id="a324d-115">Noklikšķiniet uz Rādīt filtrus.</span><span class="sxs-lookup"><span data-stu-id="a324d-115">Click Show filters.</span></span>
7. <span data-ttu-id="a324d-116">Lietojiet šādus filtrus: Ievadiet filtrēšanas vērtību “ISO20022 kredīta pārskaitījums (DE)” laukā “Konfigurācijas nosaukums”, izmantojot “sākas ar” filtra operatoru</span><span class="sxs-lookup"><span data-stu-id="a324d-116">Apply the following filters: Enter a filter value of "ISO20022 Credit transfer (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="a324d-117">Vai atrodiet konfigurāciju sarakstā, atlasiet to un pārvietojiet to uz importa uzdevumu.</span><span class="sxs-lookup"><span data-stu-id="a324d-117">Alternatively, you can find the configuration in the list, select it, and then move it to the Import task.</span></span>  
8. <span data-ttu-id="a324d-118">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="a324d-118">Click Import.</span></span>
    * <span data-ttu-id="a324d-119">Ja poga Importēt nav pieejama, tas nozīmē, ka šī konfigurācija jau ir importēta.</span><span class="sxs-lookup"><span data-stu-id="a324d-119">If the Import button is not available, it means that the configuration has  already been imported.</span></span>  
9. <span data-ttu-id="a324d-120">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="a324d-120">Click Yes.</span></span>



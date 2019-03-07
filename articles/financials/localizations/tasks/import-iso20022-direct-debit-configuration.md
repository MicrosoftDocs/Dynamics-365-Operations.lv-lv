---
title: ISO20022 tiešā debeta konfigurācijas importēšana
description: Šī procedūra parāda, kā importēt debitora maksājuma elektronisko pārskatu veidošanas konfigurāciju.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1757a1477e46f71e327bb70cf4780767b7509e55
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "333074"
---
# <a name="import-iso20022-direct-debit-configuration"></a><span data-ttu-id="97f79-103">ISO20022 tiešā debeta konfigurācijas importēšana</span><span class="sxs-lookup"><span data-stu-id="97f79-103">Import ISO20022 direct debit configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97f79-104">Šī procedūra parāda, kā importēt debitora maksājuma elektronisko pārskatu veidošanas konfigurāciju.</span><span class="sxs-lookup"><span data-stu-id="97f79-104">This procedure demonstrates how to import a customer payment electronic reporting configuration.</span></span> <span data-ttu-id="97f79-105">Šī procedūra izmanto ISO 20022 tiešā debeta formātu kā piemēru.</span><span class="sxs-lookup"><span data-stu-id="97f79-105">This procedure uses the ISO 20022 direct debit format as an example.</span></span> 



<span data-ttu-id="97f79-106">Šī procedūra tika izveidota, izmantojot demonstrācijas datu uzņēmumu DEMF, bet jūs varat izmantot jebkuru demonstrācijas datu uzņēmumu šim nolūkam.</span><span class="sxs-lookup"><span data-stu-id="97f79-106">This procedure was created using the demo data company DEMF but you can use any demo data company for this purpose.</span></span>



<span data-ttu-id="97f79-107">Šī ir pirmā no piecām procedūrām, kas demonstrē debitora maksājuma procesu, izmantojot elektronisko atskaišu konfigurācijas.</span><span class="sxs-lookup"><span data-stu-id="97f79-107">This is the first of five procedures that demonstrate the customer payment process using electronic reporting configurations.</span></span>

1. <span data-ttu-id="97f79-108">Pārejiet uz sadaļu Organizācijas administrēšana > Darbvietas > Elektronisko pārskatu veidošana.</span><span class="sxs-lookup"><span data-stu-id="97f79-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="97f79-109">Sarakstā pieejamās konfigurācijas nodrošinātāji, atlasiet Microsoft.</span><span class="sxs-lookup"><span data-stu-id="97f79-109">In the list of available configuration providers, select Microsoft.</span></span>
3. <span data-ttu-id="97f79-110">Noklikšķiniet uz Iestatīt aktīvu.</span><span class="sxs-lookup"><span data-stu-id="97f79-110">Click Set active.</span></span>
4. <span data-ttu-id="97f79-111">Noklikšķiniet uz Repozitoriji.</span><span class="sxs-lookup"><span data-stu-id="97f79-111">Click Repositories.</span></span>
5. <span data-ttu-id="97f79-112">Noklikšķiniet uz Atvērt.</span><span class="sxs-lookup"><span data-stu-id="97f79-112">Click Open.</span></span>
6. <span data-ttu-id="97f79-113">Noklikšķiniet uz Rādīt filtrus.</span><span class="sxs-lookup"><span data-stu-id="97f79-113">Click Show filters.</span></span>
7. <span data-ttu-id="97f79-114">Lietojiet šādus filtrus: Ievadiet filtrēšanas vērtību “ISO20022 tiešais debets (DE)” laukā “Konfigurācijas nosaukums”, izmantojot “sākas ar” filtra operatoru</span><span class="sxs-lookup"><span data-stu-id="97f79-114">Apply the following filters: Enter a filter value of "ISO20022 Direct debit (DE)" on the "Configuration name" field using the "begins with" filter operator</span></span>
    * <span data-ttu-id="97f79-115">Pēc izvēles jūs varat atrast konfigurāciju sarakstā, atlasīt to, un izlaist šo darbību.</span><span class="sxs-lookup"><span data-stu-id="97f79-115">Optionally, you can find the configuration in the list, select it, and skip this step.</span></span>  
8. <span data-ttu-id="97f79-116">Noklikšķiniet uz Importēt.</span><span class="sxs-lookup"><span data-stu-id="97f79-116">Click Import.</span></span>
    * <span data-ttu-id="97f79-117">Ja poga Importēt nav pieejama, tas nozīmē, ka šī konfigurācija jau ir importēta.</span><span class="sxs-lookup"><span data-stu-id="97f79-117">If the Import button is not available, it means that the configuration has been imported already.</span></span>  
9. <span data-ttu-id="97f79-118">Noklikšķiniet uz Jā.</span><span class="sxs-lookup"><span data-stu-id="97f79-118">Click Yes.</span></span>


---
title: Ar Finance and Operations programmu jaunināšanu saistītu problēmu novēršana
description: Šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas saistītas ar atjauninājumiem Finance and Operations lietojumprogrammās.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172881"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="4d49b-103">Ar Finance and Operations programmu jaunināšanu saistītu problēmu novēršana</span><span class="sxs-lookup"><span data-stu-id="4d49b-103">Troubleshoot issues related to upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="4d49b-104">Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="4d49b-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="4d49b-105">Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas saistītas ar atjauninājumiem Finance and Operations lietojumprogrammās.</span><span class="sxs-lookup"><span data-stu-id="4d49b-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d49b-106">Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="4d49b-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="4d49b-107">Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="4d49b-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="4d49b-108">Datu bāzes sinhronizēšanas kļūdas</span><span class="sxs-lookup"><span data-stu-id="4d49b-108">Database synchronization errors</span></span>

<span data-ttu-id="4d49b-109">**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="4d49b-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="4d49b-110">Iespējams, mēģinot izmantot **DualWriteProjectConfiguration** elementu, lai atjauninātu Finance and Operations programmu uz 30. platformas atjauninājumu, saņemat kļūdas ziņojumu, kas līdzīgs šim piemēram.</span><span class="sxs-lookup"><span data-stu-id="4d49b-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** entity to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="4d49b-111">Lai novērstu problēmu, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="4d49b-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="4d49b-112">Piesakieties programmas Finance and Operations virtuālajā mašīnā (VM).</span><span class="sxs-lookup"><span data-stu-id="4d49b-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="4d49b-113">Atveriet Visual Studio kā administrators un atveriet lietojumprogrammas objektu koku (AOT).</span><span class="sxs-lookup"><span data-stu-id="4d49b-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="4d49b-114">Meklēt **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="4d49b-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="4d49b-115">Lietojumprogrammas objektu kokā ar peles labo pogu noklikšķiniet uz **DualWriteProjectConfiguration** un atlasiet **Pievienot jaunajam projektam**.</span><span class="sxs-lookup"><span data-stu-id="4d49b-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="4d49b-116">Atlasiet **Labi**, lai izveidotu jaunu projektu, kas izmanto noklusējuma opcijas.</span><span class="sxs-lookup"><span data-stu-id="4d49b-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="4d49b-117">Risinājumu pārlūkā ar peles labo pogu noklikšķiniet uz **Projekta rekvizīti** un iestatiet opciju **Sinhronizēt datu bāzi būvējumā** uz **Patiess**.</span><span class="sxs-lookup"><span data-stu-id="4d49b-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="4d49b-118">Izveidojiet projektu un apstipriniet, ka būvējums ir veiksmīgs.</span><span class="sxs-lookup"><span data-stu-id="4d49b-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="4d49b-119">Izvēlnē **Dynamics 365** atlasiet **Sinhronizēt datu bāzi.**</span><span class="sxs-lookup"><span data-stu-id="4d49b-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="4d49b-120">Atlasiet **Sinhronizēt**, lai veiktu pilnīgu datu bāzes sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="4d49b-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="4d49b-121">Kad pilnīga datu bāzes sinhronizācija ir veiksmīgi pabeigta, atkārtoti palaidiet datu bāzes sinhronizācijas darbību pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) un pēc nepieciešamības izmantojiet manuālos jaunināšanas skriptus, lai varētu turpināt atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="4d49b-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-entity-fields-issue-on-maps"></a><span data-ttu-id="4d49b-122">Trūkstošu elementu lauku problēma kartēs</span><span class="sxs-lookup"><span data-stu-id="4d49b-122">Missing entity fields issue on maps</span></span>

<span data-ttu-id="4d49b-123">**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="4d49b-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="4d49b-124">Lapā **Duālais ieraksts** var tikt parādīts kļūdas ziņojums, kas līdzīgs šim piemēram:</span><span class="sxs-lookup"><span data-stu-id="4d49b-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="4d49b-125">*Nav avota lauka \<lauka nosaukums\> sistēmā.*</span><span class="sxs-lookup"><span data-stu-id="4d49b-125">*Missing source field \<field name\> in the schema.*</span></span>

![Trūkstošā avota lauka kļūdas ziņojuma piemērs](media/error_missing_field.png)

<span data-ttu-id="4d49b-127">Lai atrisinātu problēmu, vispirms veiciet šīs darbības, lai nodrošinātu, ka lauki atrodas entītijā.</span><span class="sxs-lookup"><span data-stu-id="4d49b-127">To fix the issue, first follow these steps to make sure that the fields are in the entity.</span></span>

1. <span data-ttu-id="4d49b-128">Piesakieties programmas Finance and Operations VM.</span><span class="sxs-lookup"><span data-stu-id="4d49b-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="4d49b-129">Dodieties uz **Darbvietas \>Datu pārvaldība**, atlasiet elementu **Struktūras parametri** un pēc tam cilnē **Elementa iestatījumi** atlasiet **Atsvaidzināt elementu sarakstu**, lai atsvaidzinātu elementus.</span><span class="sxs-lookup"><span data-stu-id="4d49b-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Entity settings** tab, select **Refresh entity list** to refresh the entities.</span></span>
3. <span data-ttu-id="4d49b-130">Dodieties uz **Darbvietas \>Datu pārvaldība**, atlasiet cilni **Datu elementi** un pārliecinieties, ka elements ir uzskaitīts.</span><span class="sxs-lookup"><span data-stu-id="4d49b-130">Go to **Workspaces \> Data management**, select the **Data entities** tab, and make sure that the entity is listed.</span></span> <span data-ttu-id="4d49b-131">Ja elements nav uzskaitīts, piesakieties Finance and Operations programmas VM, un pārliecinieties, ka šis elements ir pieejams.</span><span class="sxs-lookup"><span data-stu-id="4d49b-131">If the entity isn't listed, sign in to the VM for the Finance and Operations app, and make sure the entity is available.</span></span>
4. <span data-ttu-id="4d49b-132">Atveriet lapu **Elementa kartēšana** no lapas **Duālais ieraksts** Finance and Operations lietojumprogrammā.</span><span class="sxs-lookup"><span data-stu-id="4d49b-132">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="4d49b-133">Atlasiet **Atsvaidzināt elementu sarakstu**, lai automātiski aizpildītu laukus elementu kartējumos.</span><span class="sxs-lookup"><span data-stu-id="4d49b-133">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

<span data-ttu-id="4d49b-134">Ja problēma joprojām nav novērsta, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="4d49b-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d49b-135">Izpildot šīs darbības, elements tiek dzēsts un atkārtoti pievienots.</span><span class="sxs-lookup"><span data-stu-id="4d49b-135">These steps guide you through the process of deleting an entity and then adding it again.</span></span> <span data-ttu-id="4d49b-136">Lai izvairītos no problēmām, noteikti veiciet darbības precīzi.</span><span class="sxs-lookup"><span data-stu-id="4d49b-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="4d49b-137">Finance and Operations programmā atveriet **Darbvietas \>Datu pārvaldība**un atlasiet elementu **Datu elementi**.</span><span class="sxs-lookup"><span data-stu-id="4d49b-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data entities** tile.</span></span>
2. <span data-ttu-id="4d49b-138">Atrodiet elementu, kuram trūkst lauka.</span><span class="sxs-lookup"><span data-stu-id="4d49b-138">Find the entity that is missing the field.</span></span> <span data-ttu-id="4d49b-139">Atzīmējiet mērķa elementa, sagatavošanas tabulas, elementa nosaukuma un citu kolonnu vērtības.</span><span class="sxs-lookup"><span data-stu-id="4d49b-139">Make a note of the target entity, staging table, entity name, and other column values.</span></span>
3. <span data-ttu-id="4d49b-140">Ja kāda no jūsu apstrādes grupām ir atkarīga no šī elementa, pirms elementa dzēšanas atbilstoši apstrādājiet grupas.</span><span class="sxs-lookup"><span data-stu-id="4d49b-140">If any of your processing groups depend on this entity, take appropriate action for the processing groups before you delete the entity.</span></span>
4. <span data-ttu-id="4d49b-141">Dzēsiet elementu, kuram trūkst lauka.</span><span class="sxs-lookup"><span data-stu-id="4d49b-141">Delete the entity that is missing the field.</span></span>
5. <span data-ttu-id="4d49b-142">Atlasiet **Jauns** un pievienojiet elementu atpakaļ.</span><span class="sxs-lookup"><span data-stu-id="4d49b-142">Select **New**, and add the entity back.</span></span> <span data-ttu-id="4d49b-143">Norādiet vērtības, kuras atzīmējāt 2. darbības laikā.</span><span class="sxs-lookup"><span data-stu-id="4d49b-143">Specify the values that you made a note of in step 2.</span></span>
6. <span data-ttu-id="4d49b-144">Atveriet lapu **Elementa kartēšana** no lapas **Duālais ieraksts** Finance and Operations lietojumprogrammā.</span><span class="sxs-lookup"><span data-stu-id="4d49b-144">Open the **Entity mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
7. <span data-ttu-id="4d49b-145">Atlasiet **Atsvaidzināt elementu sarakstu**, lai automātiski aizpildītu laukus elementu kartējumos.</span><span class="sxs-lookup"><span data-stu-id="4d49b-145">Select **Refresh entity list** to automatically fill the fields in the entity mappings.</span></span>

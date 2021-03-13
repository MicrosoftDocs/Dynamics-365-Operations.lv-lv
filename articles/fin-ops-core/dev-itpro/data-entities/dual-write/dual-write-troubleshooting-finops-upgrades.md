---
title: Problēmu novēršana saistībā ar Finance and Operations programmu jauninājumiem
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: a11ce426d7f30b6b124bd2022514a0201c2b332c
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/06/2021
ms.locfileid: "5131225"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a><span data-ttu-id="720b5-103">Problēmu novēršana saistībā ar Finance and Operations programmu jauninājumiem</span><span class="sxs-lookup"><span data-stu-id="720b5-103">Troubleshoot issues from upgrades of Finance and Operations apps</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="720b5-104">Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse.</span><span class="sxs-lookup"><span data-stu-id="720b5-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="720b5-105">Konkrēti, šajā tēmā sniegta informācija par problēmu novēršanu, kas var palīdzēt novērst problēmas, kas saistītas ar atjauninājumiem Finance and Operations lietojumprogrammās.</span><span class="sxs-lookup"><span data-stu-id="720b5-105">Specifically, it provides information that can help you fix issues that are related to upgrades of Finance and Operations apps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="720b5-106">Dažas no problēmām, kas risinātas šajā tēmā, var būt nepieciešama vai nu sistēmas administratora loma, vai Microsoft Azure Active Directory (Azure AD) nomnieka administratora akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="720b5-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="720b5-107">Katras problēmas sadaļā ir paskaidrots, vai ir nepieciešama īpaša loma vai akreditācijas dati.</span><span class="sxs-lookup"><span data-stu-id="720b5-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="database-synchronization-errors"></a><span data-ttu-id="720b5-108">Datu bāzes sinhronizēšanas kļūdas</span><span class="sxs-lookup"><span data-stu-id="720b5-108">Database synchronization errors</span></span>

<span data-ttu-id="720b5-109">**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="720b5-109">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="720b5-110">Iespējams, mēģinot izmantot **DualWriteProjectConfiguration** tabulu, lai atjauninātu Finance and Operations programmu uz 30. platformas atjauninājumu, saņemat kļūdas ziņojumu, kas līdzīgs šim piemēram.</span><span class="sxs-lookup"><span data-stu-id="720b5-110">You might receive an error message that resembles the following example when you try to use the **DualWriteProjectConfiguration** table to update a Finance and Operations app to Platform update 30.</span></span>

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

<span data-ttu-id="720b5-111">Lai novērstu problēmu, izpildiet šīs darbības.</span><span class="sxs-lookup"><span data-stu-id="720b5-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="720b5-112">Piesakieties programmas Finance and Operations virtuālajā mašīnā (VM).</span><span class="sxs-lookup"><span data-stu-id="720b5-112">Sign in to the virtual machine (VM) for the Finance and Operations app.</span></span>
2. <span data-ttu-id="720b5-113">Atveriet Visual Studio kā administrators un atveriet lietojumprogrammas objektu koku (AOT).</span><span class="sxs-lookup"><span data-stu-id="720b5-113">Open Visual Studio as an admin, and open the Application Object Tree (AOT).</span></span>
3. <span data-ttu-id="720b5-114">Meklēt **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="720b5-114">Search for **DualWriteProjectConfiguration**.</span></span>
4. <span data-ttu-id="720b5-115">Lietojumprogrammas objektu kokā ar peles labo pogu noklikšķiniet uz **DualWriteProjectConfiguration** un atlasiet **Pievienot jaunajam projektam**.</span><span class="sxs-lookup"><span data-stu-id="720b5-115">In the AOT, right-click **DualWriteProjectConfiguration**, and select **Add to new project**.</span></span> <span data-ttu-id="720b5-116">Atlasiet **Labi**, lai izveidotu jaunu projektu, kas izmanto noklusējuma opcijas.</span><span class="sxs-lookup"><span data-stu-id="720b5-116">Select **OK** to create the new project that uses default options.</span></span>
5. <span data-ttu-id="720b5-117">Risinājumu pārlūkā ar peles labo pogu noklikšķiniet uz **Projekta rekvizīti** un iestatiet opciju **Sinhronizēt datu bāzi būvējumā** uz **Patiess**.</span><span class="sxs-lookup"><span data-stu-id="720b5-117">In Solution Explorer, right-click **Project properties**, and set **Synchronize Database on Build** to **True**.</span></span>
6. <span data-ttu-id="720b5-118">Izveidojiet projektu un apstipriniet, ka būvējums ir veiksmīgs.</span><span class="sxs-lookup"><span data-stu-id="720b5-118">Build the project, and confirm that the build is successful.</span></span>
7. <span data-ttu-id="720b5-119">Izvēlnē **Dynamics 365** atlasiet **Sinhronizēt datu bāzi.**</span><span class="sxs-lookup"><span data-stu-id="720b5-119">On the **Dynamics 365** menu, select **Synchronize database**.</span></span>
8. <span data-ttu-id="720b5-120">Atlasiet **Sinhronizēt**, lai veiktu pilnīgu datu bāzes sinhronizāciju.</span><span class="sxs-lookup"><span data-stu-id="720b5-120">Select **Synchronize** to do a full database synchronization.</span></span>
9. <span data-ttu-id="720b5-121">Kad pilnīga datu bāzes sinhronizācija ir veiksmīgi pabeigta, atkārtoti palaidiet datu bāzes sinhronizācijas darbību pakalpojumā Microsoft Dynamics Lifecycle Services (LCS) un pēc nepieciešamības izmantojiet manuālos jaunināšanas skriptus, lai varētu turpināt atjaunināšanu.</span><span class="sxs-lookup"><span data-stu-id="720b5-121">After the full database synchronization is successful, rerun the database synchronization step in Microsoft Dynamics Lifecycle Services (LCS) and use the manual upgrade scripts as applicable, so that you can proceed with the update.</span></span>

## <a name="missing-table-columns-issue-on-maps"></a><span data-ttu-id="720b5-122">Kartēs trūkst tabulas kolonnu izejas plūsmas</span><span class="sxs-lookup"><span data-stu-id="720b5-122">Missing table columns issue on maps</span></span>

<span data-ttu-id="720b5-123">**Problēmas novēršanai nepieciešamā loma:** Sistēmas administrators</span><span class="sxs-lookup"><span data-stu-id="720b5-123">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="720b5-124">Lapā **Duālais ieraksts** var tikt parādīts kļūdas ziņojums, kas līdzīgs šim piemēram:</span><span class="sxs-lookup"><span data-stu-id="720b5-124">On the **Dual-write** page, you might receive an error message that resembles the following example:</span></span>

<span data-ttu-id="720b5-125">*Nav avota lauka \<field name\> sistēmā.*</span><span class="sxs-lookup"><span data-stu-id="720b5-125">*Missing source field \<field name\> in the schema.*</span></span>

![Trūkstošās avota kolonnas kļūdas ziņojuma piemērs](media/error_missing_field.png)

<span data-ttu-id="720b5-127">Lai atrisinātu problēmu, vispirms veiciet šīs darbības, lai nodrošinātu, ka kolonnas atrodas tabulā.</span><span class="sxs-lookup"><span data-stu-id="720b5-127">To fix the issue, first follow these steps to make sure that the columns are in the table.</span></span>

1. <span data-ttu-id="720b5-128">Piesakieties programmas Finance and Operations VM.</span><span class="sxs-lookup"><span data-stu-id="720b5-128">Sign in to the VM for the Finance and Operations app.</span></span>
2. <span data-ttu-id="720b5-129">Dodieties uz **Darbvietas \> Datu pārvaldība**, atlasiet elementu **Struktūras parametri** un pēc tam cilnē **Tabulas iestatījumi** atlasiet **Atsvaidzināt elementu sarakstu**, lai atsvaidzinātu tabulas.</span><span class="sxs-lookup"><span data-stu-id="720b5-129">Go to **Workspaces \> Data management**, select the **Framework parameters** tile, and then, on the **Table settings** tab, select **Refresh table list** to refresh the tables.</span></span>
3. <span data-ttu-id="720b5-130">Dodieties uz **Darbvietas \> Datu pārvaldība**, atlasiet cilni **Datu tabulas** un pārliecinieties, ka tabula ir uzskaitīta.</span><span class="sxs-lookup"><span data-stu-id="720b5-130">Go to **Workspaces \> Data management**, select the **Data tables** tab, and make sure that the table is listed.</span></span> <span data-ttu-id="720b5-131">Ja elements nav uzskaitīts, piesakieties Finance and Operations programmas VM, un pārliecinieties, ka šī tabula ir pieejama.</span><span class="sxs-lookup"><span data-stu-id="720b5-131">If the table isn't listed, sign in to the VM for the Finance and Operations app, and make sure the table is available.</span></span>
4. <span data-ttu-id="720b5-132">Atveriet lapu **Tabulas kartēšana** no lapas **Duālais ieraksts** Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="720b5-132">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="720b5-133">Atlasiet **Atsvaidzināt elementu sarakstu**, lai automātiski aizpildītu kolonnas tabulas kartējumos.</span><span class="sxs-lookup"><span data-stu-id="720b5-133">Select **Refresh table list** to automatically fill the columns in the table mappings.</span></span>

<span data-ttu-id="720b5-134">Ja problēma joprojām nav novērsta, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="720b5-134">If the issue still isn't fixed, follow these steps.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="720b5-135">Izpildot šīs darbības, tabula tiek dzēsta un atkārtoti pievienota.</span><span class="sxs-lookup"><span data-stu-id="720b5-135">These steps guide you through the process of deleting a table and then adding it again.</span></span> <span data-ttu-id="720b5-136">Lai izvairītos no problēmām, noteikti veiciet darbības precīzi.</span><span class="sxs-lookup"><span data-stu-id="720b5-136">To avoid issues, be sure to follow the steps exactly.</span></span>

1. <span data-ttu-id="720b5-137">Finance and Operations programmā atveriet **Darbvietas \> Datu pārvaldība** un atlasiet elementu **Datu tabulas**.</span><span class="sxs-lookup"><span data-stu-id="720b5-137">In the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Data tables** tile.</span></span>
2. <span data-ttu-id="720b5-138">Atrodiet tabulu, kuraim trūkst atribūts.</span><span class="sxs-lookup"><span data-stu-id="720b5-138">Find the table that is missing the attribute.</span></span> <span data-ttu-id="720b5-139">Rīkjoslā noklikšķiniet uz **Modificēt mērķa kartēšanu**.</span><span class="sxs-lookup"><span data-stu-id="720b5-139">Click **Modify target mapping** in the toolbar.</span></span>
3. <span data-ttu-id="720b5-140">Rūtī **Kartes iestatīšana mērķim** noklikšķiniet uz **Ģenerēt kartēšanu**.</span><span class="sxs-lookup"><span data-stu-id="720b5-140">On the **Map staging to target** pane, click **Generate mapping**.</span></span>
4. <span data-ttu-id="720b5-141">Atveriet lapu **Tabulas kartēšana** no lapas **Duālais ieraksts** Finance and Operations programmā.</span><span class="sxs-lookup"><span data-stu-id="720b5-141">Open the **Table mapping** page from the **Dual-write** page in the Finance and Operations app.</span></span>
5. <span data-ttu-id="720b5-142">Ja atribūts kartē netiek automātiski aizpildīts, pievienojiet to manuāli, noklikšķinot uz pogu **Pievienot atribūtu** un pēc tam noklikšķinot uz **Saglabāt**.</span><span class="sxs-lookup"><span data-stu-id="720b5-142">If the attribute is not auto-populated on the map, add it manually by clicking **Add attribute** button and then clicking **Save**.</span></span> 
6. <span data-ttu-id="720b5-143">Atlasiet karti un noklikšķiniet uz **Palaist**.</span><span class="sxs-lookup"><span data-stu-id="720b5-143">Select the map and click **Run**.</span></span>

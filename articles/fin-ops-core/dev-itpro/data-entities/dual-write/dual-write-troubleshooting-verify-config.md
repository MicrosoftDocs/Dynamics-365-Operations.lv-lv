---
title: Pārbaudiet duālā ieraksta konfigurāciju Finance and Operations programmās un pakalpojumā Dataverse
description: Šajā tēmā ir paskaidrots, kā varat noteikt, vai programmā Finance and Operations un Dataverse ir konfigurēts duālais ieraksts.
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
ms.openlocfilehash: 361d6555b60e02832c337b6f416b2b3627b6d365
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/06/2021
ms.locfileid: "5129311"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a><span data-ttu-id="b9e5a-103">Pārbaudiet duālā ieraksta konfigurāciju Finance and Operations programmās un pakalpojumā Dataverse</span><span class="sxs-lookup"><span data-stu-id="b9e5a-103">Verify dual-write configuration in Finance and Operations apps and Dataverse</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="b9e5a-104">Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Dataverse.</span><span class="sxs-lookup"><span data-stu-id="b9e5a-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="b9e5a-105">Konkrēti, tajā ir paskaidrots, kā varat noteikt, vai programmā Finance and Operations un Dataverse ir konfigurēts duālais ieraksts.</span><span class="sxs-lookup"><span data-stu-id="b9e5a-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Dataverse.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="b9e5a-106">Pārbaudiet, vai duālais ieraksts ir konfigurēts Finance and Operations programmā</span><span class="sxs-lookup"><span data-stu-id="b9e5a-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="b9e5a-107">Lai noteiktu, vai kļūdas, kas tiek parādītas, mēģinot saglabāt rindu atjauninājumu, nāk no duālā ieraksta, vispirms pārbaudiet, vai duālais ieraksts ir konfigurēts.</span><span class="sxs-lookup"><span data-stu-id="b9e5a-107">To determine whether the errors that you see when you try to save rows for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="b9e5a-108">Ja Finance and Operations programmā jums ir administratora privilēģijas, dodieties uz **Darbvietas \>Datu pārvaldība** un atlasiet elementu **Duālais ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="b9e5a-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="b9e5a-109">Ja tiek parādīta informācija par saistītajām vidēm un darbojošos tabulu karšu sarakstu, duālais ieraksts tiek konfigurēts.</span><span class="sxs-lookup"><span data-stu-id="b9e5a-109">If the details of the linked environments and the list of table maps that are running are shown, dual-write is configured.</span></span>

    ![Programmas Finance and Operations savienojuma pārbaude ar administratora privilēģijām](media/verify_fin_ops_1.png)

+ <span data-ttu-id="b9e5a-111">Ja jums nav administratora privilēģiju, tiek parādīts kļūdas ziņojums *Nevar ierakstīt datus elementā \<entity name\>*.</span><span class="sxs-lookup"><span data-stu-id="b9e5a-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="b9e5a-112">Šī attēla piemērā nevar izveidot klienta rindu Finance and Operations programmā, jo ir konfigurēts duālais ieraksts, bet pakalpojumā Dataverse nepastāv klientu grupas un maksājumu nosacījumu atsauces dati.</span><span class="sxs-lookup"><span data-stu-id="b9e5a-112">In the example in the following illustration, you can't create a customer row in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Dataverse.</span></span>

    ![Programmas Finance and Operations savienojuma pārbaude bez administratora privilēģijām](media/verify_fin_ops_2.png)

<span data-ttu-id="b9e5a-114">Informāciju par to, kā novērst problēmas, veidojot datus Finance and Operations programmās, skatiet sadaļā [Tiešsaistes sinhronizācijas problēmu novēršana](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="b9e5a-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a><span data-ttu-id="b9e5a-115">Pārbaudiet, vai duālais ieraksts ir konfigurēts pakalpojumā Dataverse</span><span class="sxs-lookup"><span data-stu-id="b9e5a-115">Verify that dual-write is configured in Dataverse</span></span>

<span data-ttu-id="b9e5a-116">Kad izveidojat datus, ja tiek parādīta kolonna **Uzņēmums** pakalpojuma Dataverse lapās, duālais ieraksts ir konfigurēts.</span><span class="sxs-lookup"><span data-stu-id="b9e5a-116">When you create data, if you see the **Company** column on pages in Dataverse, dual-write is configured.</span></span>

![Dataverse savienojuma pārbaude](media/verify_cds.png)

<span data-ttu-id="b9e5a-118">Informāciju par to, kā novērst problēmas, veidojot datus pakalpojumā Dataverse, skatiet sadaļā [Tiešsaistes sinhronizācijas problēmu novēršana](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="b9e5a-118">For information about how to fix issues when you create data in Dataverse, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="b9e5a-119">Lai iegūtu informāciju par to, kā skatīt informāciju par kļūdām, ar kurām saskaraties, veidojot datus pakalpojumā Dataverse, skatiet rakstā [Iespējot un skatīt spraudņa trasēšanas žurnālu pakalpojumā Dataverse, lai skatītu kļūdas informāciju](dual-write-troubleshooting.md#enable-view-trace).</span><span class="sxs-lookup"><span data-stu-id="b9e5a-119">For information about how to view error details if you encounter any errors while you create data in Dataverse, see [Enable and view the plug-in trace log in Dataverse to view error details](dual-write-troubleshooting.md#enable-view-trace).</span></span>

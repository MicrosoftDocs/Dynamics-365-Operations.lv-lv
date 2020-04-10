---
title: Pārbaudiet, vai duālais ieraksts ir konfigurēts Finance and Operations programmās un Common Data Service
description: Šajā tēmā ir paskaidrots, kā varat noteikt, vai programmā Finance and Operations un Common Data Service ir konfigurēts duālais ieraksts.
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
ms.openlocfilehash: 2f2ba2564ad3e8e444e27fcc0c586ddf252afabd
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172649"
---
# <a name="verify-that-dual-write-is-configured-in-finance-and-operations-apps-and-common-data-service"></a><span data-ttu-id="5ed45-103">Pārbaudiet, vai duālais ieraksts ir konfigurēts Finance and Operations programmās un Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5ed45-103">Verify that dual-write is configured in Finance and Operations apps and Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="5ed45-104">Šajā rakstā ir sniegta informācija par problēmu novēršanu duālā ieraksta integrācijai starp Finance and Operations programmām un Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="5ed45-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="5ed45-105">Konkrēti, tajā ir paskaidrots, kā varat noteikt, vai programmā Finance and Operations un Common Data Service ir konfigurēts duālais ieraksts.</span><span class="sxs-lookup"><span data-stu-id="5ed45-105">Specifically, it explains how you can determine whether dual-write is configured in Finance and Operations apps and in Common Data Service.</span></span>

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a><span data-ttu-id="5ed45-106">Pārbaudiet, vai duālais ieraksts ir konfigurēts Finance and Operations programmā</span><span class="sxs-lookup"><span data-stu-id="5ed45-106">Verify that dual-write is configured in a Finance and Operations app</span></span>

<span data-ttu-id="5ed45-107">Lai noteiktu, vai kļūdas, kas tiek parādītas, mēģinot saglabāt ierakstu atjauninājumu, nāk no duālā ieraksta, vispirms pārbaudiet, vai duālais ieraksts ir konfigurēts.</span><span class="sxs-lookup"><span data-stu-id="5ed45-107">To determine whether the errors that you see when you try to save records for update come from dual-write, first verify that dual-write is configured.</span></span>

+ <span data-ttu-id="5ed45-108">Ja Finance and Operations programmā jums ir administratora privilēģijas, dodieties uz **Darbvietas \>Datu pārvaldība** un atlasiet elementu **Duālais ieraksts**.</span><span class="sxs-lookup"><span data-stu-id="5ed45-108">If you have admin privileges in the Finance and Operations app, go to **Workspaces \> Data management**, and select the **Dual-write** tile.</span></span> <span data-ttu-id="5ed45-109">Ja tiek parādīta informācija par saistītajām vidēm un darbojošos elementu karšu sarakstu, duālais ieraksts tiek konfigurēts.</span><span class="sxs-lookup"><span data-stu-id="5ed45-109">If the details of the linked environments and the list of entity maps that are running are shown, dual-write is configured.</span></span>

    ![Programmas Finance and Operations savienojuma pārbaude ar administratora privilēģijām](media/verify_fin_ops_1.png)

+ <span data-ttu-id="5ed45-111">Ja jums nav administratora privilēģiju, tiek parādīts kļūdas ziņojums *Nevar ierakstīt datus elementā \<elementa nosaukums\>*.</span><span class="sxs-lookup"><span data-stu-id="5ed45-111">If you don't have admin privileges, you will receive an error message, *Unable to write data to entity \<entity name\>*.</span></span> <span data-ttu-id="5ed45-112">Šī attēla piemērā nevar izveidot klienta ierakstu Finance and Operations programmā, jo ir konfigurēts duālais ieraksts, bet pakalpojumā Common Data Service nepastāv klientu grupas un maksājumu nosacījumu atsauces dati.</span><span class="sxs-lookup"><span data-stu-id="5ed45-112">In the example in the following illustration, you can't create a customer record in the Finance and Operations app, because dual-write is configured, but the customer group and payment terms reference data don't exist in Common Data Service.</span></span>

    ![Programmas Finance and Operations savienojuma pārbaude bez administratora privilēģijām](media/verify_fin_ops_2.png)

<span data-ttu-id="5ed45-114">Informāciju par to, kā novērst problēmas, veidojot datus Finance and Operations programmās, skatiet sadaļā [Tiešsaistes sinhronizācijas problēmu novēršana](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="5ed45-114">For information about how to fix issues when you create data in Finance and Operations apps, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

## <a name="verify-that-dual-write-is-configured-in-common-data-service"></a><span data-ttu-id="5ed45-115">Pārbaudiet, vai duālais ieraksts ir konfigurēts pakalpojumā Common Data Service</span><span class="sxs-lookup"><span data-stu-id="5ed45-115">Verify that dual-write is configured in Common Data Service</span></span>

<span data-ttu-id="5ed45-116">Kad izveidojat datus, ja tiek parādīts lauks **Uzņēmums** pakalpojuma Common Data Service lapās, duālais ieraksts ir konfigurēts.</span><span class="sxs-lookup"><span data-stu-id="5ed45-116">When you create data, if you see the **Company** field on pages in Common Data Service, dual-write is configured.</span></span>

![Common Data Service savienojuma pārbaude](media/verify_cds.png)

<span data-ttu-id="5ed45-118">Informāciju par to, kā novērst problēmas, veidojot datus pakalpojumā Common Data Service, skatiet sadaļā [Tiešsaistes sinhronizācijas problēmu novēršana](dual-write-troubleshooting-live-sync.md).</span><span class="sxs-lookup"><span data-stu-id="5ed45-118">For information about how to fix issues when you create data in Common Data Service, see [Troubleshoot live synchronization issues](dual-write-troubleshooting-live-sync.md).</span></span>

<span data-ttu-id="5ed45-119">Lai iegūtu informāciju par to, kā skatīt informāciju par kļūdām, ar kurām saskaraties, veidojot datus pakalpojumā Common Data Service, skatiet rakstā [Iespējot un skatīt spraudņa trasēšanas žurnālu pakalpojumā Common Data Service, lai skatītu kļūdas informāciju](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span><span class="sxs-lookup"><span data-stu-id="5ed45-119">For information about how to view error details if you encounter any errors while you create data in Common Data Service, see [Enable and view the plug-in trace log in Common Data Service to view error details](dual-write-troubleshooting.md#enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details).</span></span>

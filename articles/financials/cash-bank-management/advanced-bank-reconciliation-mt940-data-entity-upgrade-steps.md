---
title: Detalizētas bankas darbību saskaņošanas MT940 importēšana – Salikta datu elementa jaunināšana
description: Secības numurs jāpievieno bankas izraksta importēšanas elementam, lai atbalstītu MT940 formātu.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 221594
ms.assetid: dddc99ae-56ae-48df-856a-131079c17dcb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 6c0eeb59726422177ed1122767b9d3142a1311a2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/29/2019
ms.locfileid: "343792"
---
# <a name="advanced-bank-reconciliation-mt940-import--composite-data-entity-upgrade"></a><span data-ttu-id="016e5-103">Detalizētas bankas darbību saskaņošanas MT940 importēšana – Salikta datu elementa jaunināšana</span><span class="sxs-lookup"><span data-stu-id="016e5-103">Advanced bank reconciliation MT940 Import – Composite data entity upgrade</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="016e5-104">Secības numurs jāpievieno bankas izraksta importēšanas elementam, lai atbalstītu MT940 formātu.</span><span class="sxs-lookup"><span data-stu-id="016e5-104">A sequence number needs to be added to the bank statement import entity to support the MT940 format.</span></span> 

<span data-ttu-id="016e5-105">Lai pievienotu bankas izraksta importēšanas elementu MT940 formāta atbalstam, veiciet šādas darbības.</span><span class="sxs-lookup"><span data-stu-id="016e5-105">Use the following steps to add the bank statement import entity to support the MT940 format.</span></span>

1.  <span data-ttu-id="016e5-106">Kompilējiet un sinhronizējiet:</span><span class="sxs-lookup"><span data-stu-id="016e5-106">Compile and synchronize the following:</span></span>
    -   <span data-ttu-id="016e5-107">Salikts elements\\BankStatementImportEntity</span><span class="sxs-lookup"><span data-stu-id="016e5-107">Composite Entity\\BankStatementImportEntity</span></span>
    -   <span data-ttu-id="016e5-108">Elements\\BankStatementBalanceEntity</span><span class="sxs-lookup"><span data-stu-id="016e5-108">Entity\\BankStatementBalanceEntity</span></span>
    -   <span data-ttu-id="016e5-109">Elements\\BankStatementDocumentEntity</span><span class="sxs-lookup"><span data-stu-id="016e5-109">Entity\\BankStatementDocumentEntity</span></span>
    -   <span data-ttu-id="016e5-110">Elements\\BankStatementEntity</span><span class="sxs-lookup"><span data-stu-id="016e5-110">Entity\\BankStatementEntity</span></span>
    -   <span data-ttu-id="016e5-111">Elements\\BankStatementLineEntity</span><span class="sxs-lookup"><span data-stu-id="016e5-111">Entity\\BankStatementLineEntity</span></span>
    -   <span data-ttu-id="016e5-112">Tabulas\\BankStatementStaging</span><span class="sxs-lookup"><span data-stu-id="016e5-112">Tables\\BankStatementStaging</span></span>

2.  <span data-ttu-id="016e5-113">Datu pārvaldība\\datu projekti.</span><span class="sxs-lookup"><span data-stu-id="016e5-113">Data management\\data projects.</span></span>
    1.  <span data-ttu-id="016e5-114">Ielādēt MT940 projekta(-u) importēšanu</span><span class="sxs-lookup"><span data-stu-id="016e5-114">Load MT940 import project(s)</span></span>
        1.  <span data-ttu-id="016e5-115">Mainīt XSLT.</span><span class="sxs-lookup"><span data-stu-id="016e5-115">Change XSLT.</span></span>
            -   <span data-ttu-id="016e5-116">Noklikšķiniet uz **Skatīt karti**.</span><span class="sxs-lookup"><span data-stu-id="016e5-116">Click **View map**.</span></span>
            -   <span data-ttu-id="016e5-117">Noklikšķiniet uz **Skatīt karti** uz bankas izraksta dokumenta.</span><span class="sxs-lookup"><span data-stu-id="016e5-117">Click **View map** on the bank statement document.</span></span>
            -   <span data-ttu-id="016e5-118">Noklikšķiniet uz **Transformācijas**</span><span class="sxs-lookup"><span data-stu-id="016e5-118">Click **Transformations**</span></span>
            -   <span data-ttu-id="016e5-119">Dzēst BankReconiliation-to-Composite.xslt failu.</span><span class="sxs-lookup"><span data-stu-id="016e5-119">Delete the BankReconiliation-to-Composite.xslt file.</span></span>
            -   <span data-ttu-id="016e5-120">Pievienot jaunu faila BankReconiliation Composite.xsl versiju.</span><span class="sxs-lookup"><span data-stu-id="016e5-120">Add the new version of BankReconiliation-to-Composite.xsl.</span></span>

        2.  <span data-ttu-id="016e5-121">Atklāt **Sērijas numuru** izkārtojumā **Avota dati**.</span><span class="sxs-lookup"><span data-stu-id="016e5-121">Expose the **Sequence Number** on **Source Data** layout.</span></span>
            1.  <span data-ttu-id="016e5-122">Avota datu formāts = XML elements.</span><span class="sxs-lookup"><span data-stu-id="016e5-122">Source data format = XML-Element.</span></span>
            2.  <span data-ttu-id="016e5-123">Elementa nosaukums = Bankas izraksti.</span><span class="sxs-lookup"><span data-stu-id="016e5-123">Entity name = Bank statements.</span></span>
            3.  <span data-ttu-id="016e5-124">Augšupielādēt datu failu = SampleBankCompositeEntity.xml jauna versija.</span><span class="sxs-lookup"><span data-stu-id="016e5-124">Upload data file = new version SampleBankCompositeEntity.xml.</span></span>
            4.  <span data-ttu-id="016e5-125">Noklikšķiniet uz **Jā**, lai pārrakstītu esošo failu.</span><span class="sxs-lookup"><span data-stu-id="016e5-125">Click **Yes** to overwrite the existing file.</span></span>
            5.  <span data-ttu-id="016e5-126">Noklikšķiniet uz **Jā**, lai ģenerētu jaunu kartējumu.</span><span class="sxs-lookup"><span data-stu-id="016e5-126">Click **Yes** to generate a new mapping.</span></span>
            6.  <span data-ttu-id="016e5-127">Apstipriniet, ka S**equenceNumber** ir kartēts.</span><span class="sxs-lookup"><span data-stu-id="016e5-127">Verify that S**equenceNumber** is mapped.</span></span>
                -   <span data-ttu-id="016e5-128">Noklikšķiniet uz **Skatīt karti** uz bankas izraksta elementa.</span><span class="sxs-lookup"><span data-stu-id="016e5-128">Click **View Map** on the statement entity.</span></span>
                -   <span data-ttu-id="016e5-129">Apstipriniet, ka **SequenceNumber** ir kartēts no Avota uz Sagatavošanu.</span><span class="sxs-lookup"><span data-stu-id="016e5-129">Verify that **SequenceNumber** is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="016e5-130">Importēt jauno izrakstu.</span><span class="sxs-lookup"><span data-stu-id="016e5-130">Import the new statement.</span></span>





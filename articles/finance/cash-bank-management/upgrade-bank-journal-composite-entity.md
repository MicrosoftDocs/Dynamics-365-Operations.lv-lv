---
title: Atjaunināt bankas žurnāla salikto elementu
description: Lai saliktajam elementam BankJournalEntity pievienotu papildu lauku BankTransactionType, ir nepieciešams izpildīt tālāk aprakstītās darbības.
author: ShylaThompson
manager: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221654
ms.assetid: adb8146b-eb21-4be2-a338-a5b299fcc9a0
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: e6c990208f26dde26b7adc306198f7cd16e0e69b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4978918"
---
# <a name="update-the-bank-journal-composite-entity"></a><span data-ttu-id="b4ec4-103">Atjaunināt bankas žurnāla salikto elementu</span><span class="sxs-lookup"><span data-stu-id="b4ec4-103">Update the bank journal composite entity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4ec4-104">Lai saliktajam elementam BankJournalEntity pievienotu papildu lauku BankTransactionType, ir nepieciešams izpildīt tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="b4ec4-104">The following steps are needed in order to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

<span data-ttu-id="b4ec4-105">Lai saliktajam elementam BankJournalEntity pievienotu papildu lauku BankTransactionType, izpildiet tālāk aprakstītās darbības.</span><span class="sxs-lookup"><span data-stu-id="b4ec4-105">Use the following steps to add the additional BankTransactionType field to the composite BankJournalEntity.</span></span>

1.  <span data-ttu-id="b4ec4-106">Kompilējiet un sinhronizējiet tālāk uzskaitītos bankas žurnālu saliktos elementus, elementus un sagatavošanas tabulas.</span><span class="sxs-lookup"><span data-stu-id="b4ec4-106">Compile and synchronize the following bank journal composite entities, entities, and staging tables:</span></span>
    -   <span data-ttu-id="b4ec4-107">Saliktais elements\\BankJournalEntity</span><span class="sxs-lookup"><span data-stu-id="b4ec4-107">Composite Entity\\BankJournalEntity</span></span>
    -   <span data-ttu-id="b4ec4-108">Elements\\BankJournalHeaderEntity</span><span class="sxs-lookup"><span data-stu-id="b4ec4-108">Entity\\BankJournalHeaderEntity</span></span>
    -   <span data-ttu-id="b4ec4-109">Elements\\BankJournalLineEntity</span><span class="sxs-lookup"><span data-stu-id="b4ec4-109">Entity\\BankJournalLineEntity</span></span>
    -   <span data-ttu-id="b4ec4-110">Tabula\\BankJournalHeaderStaging</span><span class="sxs-lookup"><span data-stu-id="b4ec4-110">Table\\BankJournalHeaderStaging</span></span>
    -   <span data-ttu-id="b4ec4-111">Tabula\\BankJournalLineStaging</span><span class="sxs-lookup"><span data-stu-id="b4ec4-111">Table\\BankJournalLineStaging</span></span>

2.  <span data-ttu-id="b4ec4-112">Datu pārvaldība\\datu projekti</span><span class="sxs-lookup"><span data-stu-id="b4ec4-112">Data management\\data projects</span></span>
    -   <span data-ttu-id="b4ec4-113">Atklājiet tipu **Bankas transakcija** izkārtojumā **Avota dati**.</span><span class="sxs-lookup"><span data-stu-id="b4ec4-113">Expose the **Bank Transaction** type on **Source Data** layout.</span></span>
        -   <span data-ttu-id="b4ec4-114">Avota datu formāts = XML elements</span><span class="sxs-lookup"><span data-stu-id="b4ec4-114">Source data format = XML-Element</span></span>
        -   <span data-ttu-id="b4ec4-115">Elementa nosaukums = Bankas žurnāls</span><span class="sxs-lookup"><span data-stu-id="b4ec4-115">Entity name = Bank Journal</span></span>
        -   <span data-ttu-id="b4ec4-116">Augšupielādes datu fails = jaunas versijas SampleBankJournalCompositeEntity.xml</span><span class="sxs-lookup"><span data-stu-id="b4ec4-116">Upload data file = new version SampleBankJournalCompositeEntity.xml</span></span>
        -   <span data-ttu-id="b4ec4-117">Noklikšķiniet uz **Jā**, lai pārrakstītu esošo failu.</span><span class="sxs-lookup"><span data-stu-id="b4ec4-117">Click **Yes** to overwrite the existing file.</span></span>
        -   <span data-ttu-id="b4ec4-118">Noklikšķiniet uz **Jā**, lai ģenerētu kartējumu no sākuma.</span><span class="sxs-lookup"><span data-stu-id="b4ec4-118">Click **Yes** to generate mapping from scratch.</span></span>
        -   <span data-ttu-id="b4ec4-119">Pārbaudiet, vai ir kartēts Bankas transakcijas tips.</span><span class="sxs-lookup"><span data-stu-id="b4ec4-119">Verify that the Bank Transaction Type is mapped.</span></span>
            -   <span data-ttu-id="b4ec4-120">Noklikšķiniet uz **Skatīt karti** elementā Rinda.</span><span class="sxs-lookup"><span data-stu-id="b4ec4-120">Click **View map** on Line entity.</span></span>
            -   <span data-ttu-id="b4ec4-121">Pārbaudiet, vai Bankas transakcijas tips ir kartēts no avota uz sagatavošanu.</span><span class="sxs-lookup"><span data-stu-id="b4ec4-121">Verify that Bank Transaction type is mapped from Source to Staging.</span></span>

3.  <span data-ttu-id="b4ec4-122">Importēt jauno izrakstu.</span><span class="sxs-lookup"><span data-stu-id="b4ec4-122">Import the new statement.</span></span>





---
title: Pārejas korekciju žurnāla ierakstus grāmatošana līdzekļu nomā
description: Šī tēma apraksta funkcionalitāti, kas ļauj jums nomas portfeli pārveidot pēc jaunajiem nomas uzskaites standartiem, uzskaites standartu kodifikācijas tēmas 842 (ASC 842) un starptautiskajiem finanšu pārskatu standartiem 16 (IFRS 16).
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 4af7b9dc7a03a6d17ff34ffc726eb87e848dd785
ms.sourcegitcommit: f0f5545a8ff99583e0131f435d91c64bb68a1c38
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 10/30/2020
ms.locfileid: "4445805"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="b468e-103">Pārejas korekciju žurnāla ierakstus grāmatošana līdzekļu nomā</span><span class="sxs-lookup"><span data-stu-id="b468e-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b468e-104">Šī tēma apraksta funkcionalitāti, kas ļauj jums nomas portfeli pārveidot pēc jaunajiem nomas uzskaites standartiem: uzskaites standartu kodifikācijas tēmas 842 (ASC 842), kas ir standarts vispāratzītos uzskaites principos ASV (US GAAP) un starptautiskajiem finanšu pārskatu standartiem 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="b468e-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="b468e-105">Informāciju par to, kā iestatīt grāmatu pārejai uz jaunajiem standartiem, skatiet šeit: [Nomas grāmatu iestatīšana](set-up-lease-books.md).</span><span class="sxs-lookup"><span data-stu-id="b468e-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="b468e-106">Veidojot pārejas korekcijas žurnāla ierakstu, tiek ģenerēts žurnāla ieraksts.</span><span class="sxs-lookup"><span data-stu-id="b468e-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="b468e-107">Šis ieraksts ataino bilances ietekmi uz nomas reģistrēšanu saskaņā ar jaunajiem standartiem minētajā datumā.</span><span class="sxs-lookup"><span data-stu-id="b468e-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="b468e-108">Atbilstošais līdzekļu kontā šajā datumā tiek debetēta uzskaites summa, un saistību konts tiek kreditēts.</span><span class="sxs-lookup"><span data-stu-id="b468e-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="b468e-109">Starpība tiek debetēta vai kreditēta saglabātajiem ienākumiem.</span><span class="sxs-lookup"><span data-stu-id="b468e-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="b468e-110">Lai grāmatotu pārejas korekciju saskaņā ar jaunajiem uzskaites standartiem, veiciet tālāk norādītās darbības.</span><span class="sxs-lookup"><span data-stu-id="b468e-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="b468e-111">Lapā **Nomas kopsavilkums** atlasiet nomu un pēc tam atlasiet **Grāmatas**.</span><span class="sxs-lookup"><span data-stu-id="b468e-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="b468e-112">Grāmatā atlasiet **Maksājumu grafiks**.</span><span class="sxs-lookup"><span data-stu-id="b468e-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="b468e-113">Dialoglodziņā **Maksājumu grafiks** atlasiet **Apstiprināt**.</span><span class="sxs-lookup"><span data-stu-id="b468e-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="b468e-114">Pēc tam aizveriet dialoglodziņu.</span><span class="sxs-lookup"><span data-stu-id="b468e-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="b468e-115">Atlasiet **Pārejas korekcija**.</span><span class="sxs-lookup"><span data-stu-id="b468e-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b468e-116">Pārejas korekciju var izveidot tikai nomas grāmatām, kas piešķirtas grāmatai, kur ir pieejams lauks **Pārejas grāmata**.</span><span class="sxs-lookup"><span data-stu-id="b468e-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="b468e-117">Ja vērtība laukā **Nomas sākums** ir vēlāks par pārejas datumu, vērtība laukā **Pārejas korekcija** netiks atjaunināta.</span><span class="sxs-lookup"><span data-stu-id="b468e-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="b468e-118">Lai skatītu žurnāla ierakstu, atlasiet **Līdzekļu nomas žurnāli**.</span><span class="sxs-lookup"><span data-stu-id="b468e-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="b468e-119">Atlasiet jauno žurnālu un pēc tam atlasiet **Grāmatot**.</span><span class="sxs-lookup"><span data-stu-id="b468e-119">Select the new journal, and then select **Post**.</span></span>

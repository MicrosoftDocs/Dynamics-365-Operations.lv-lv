---
title: Debitoru un preču ienesīguma novērtēšana
description: Šajā rakstā ir paskaidrots, kā var izmantot atmiņā saglabāto un reāllaika analīzi, lai piekļūtu informācijai par debitoru un preču ienesīgumu no Microsoft Dynamics 365 for Retail datiem, pētītu šo informāciju un gūtu ieskatus par to.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SysOperationsTemplateForm, RetailStoreManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 52902
ms.assetid: 1a77d04b-2985-4bee-9138-c216fe0483de
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 28d4eeaa3fcae33f817690ad496b4b123a5838ce
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561368"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="d2832-103">Novērtēt debitoru un preču ienesīgumu</span><span class="sxs-lookup"><span data-stu-id="d2832-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d2832-104">Šajā rakstā ir paskaidrots, kā var izmantot atmiņā saglabāto un reāllaika analīzi, lai piekļūtu informācijai par debitoru un preču ienesīgumu no Microsoft Dynamics 365 for Retail datiem, pētītu šo informāciju un gūtu ieskatus par to.</span><span class="sxs-lookup"><span data-stu-id="d2832-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span>

<span data-ttu-id="d2832-105">Programmā Dynamics 365 for Retail lietotāji var pētīt labāko debitoru (10–100) ienesīgumu dažādos organizācijas hierarhijas līmeņos, pamatojoties uz kādu no tālāk norādītajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="d2832-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="d2832-106">Pārdošanas summa</span><span class="sxs-lookup"><span data-stu-id="d2832-106">Sales amount</span></span>
- <span data-ttu-id="d2832-107">Daudzums</span><span class="sxs-lookup"><span data-stu-id="d2832-107">Quantity</span></span>
- <span data-ttu-id="d2832-108">Bruto peļņas norma</span><span class="sxs-lookup"><span data-stu-id="d2832-108">Gross profit margin</span></span>
- <span data-ttu-id="d2832-109">Uzcenojuma procenti</span><span class="sxs-lookup"><span data-stu-id="d2832-109">Margin percentage</span></span>

<span data-ttu-id="d2832-110">Lai veiktu šo izvērtēšanu, var izmantot inovatīvo pārskatu **Lielākie debitori**, kuru var atvērt, izmantojot vienu no tālāk norādītajiem ceļiem.</span><span class="sxs-lookup"><span data-stu-id="d2832-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="d2832-111">Darbvieta **Mazumtirdzniecības veikala pārvaldība** &gt; **Mazumtirdzniecība** &gt; **Kanāli** &gt; **Mazumtirdzniecības veikala pārvaldība** &gt; **Pārskati** &gt; **Lielāko debitoru pārskats**</span><span class="sxs-lookup"><span data-stu-id="d2832-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="d2832-112">Sadaļa **Pieprasījumi un pārskati** &gt; **Mazumtirdzniecība** &gt; **Pieprasījumi un pārskati** &gt; **Pārdošanas pārskati** &gt; **Lielāko debitoru pārskats**</span><span class="sxs-lookup"><span data-stu-id="d2832-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="d2832-113">Līdzīgi lietotāji var pētīt augstākās kvalitātes preču (10–100) rentabilitāti dažādos organizācijas hierarhijas līmeņos, ņemot vēra tālāk norādītos kritērijus.</span><span class="sxs-lookup"><span data-stu-id="d2832-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="d2832-114">Pārdošanas summa</span><span class="sxs-lookup"><span data-stu-id="d2832-114">Sales amount</span></span>
- <span data-ttu-id="d2832-115">Daudzums</span><span class="sxs-lookup"><span data-stu-id="d2832-115">Quantity</span></span>
- <span data-ttu-id="d2832-116">Bruto peļņas norma</span><span class="sxs-lookup"><span data-stu-id="d2832-116">Gross profit margin</span></span>
- <span data-ttu-id="d2832-117">Uzcenojuma procenti</span><span class="sxs-lookup"><span data-stu-id="d2832-117">Margin percentage</span></span>

<span data-ttu-id="d2832-118">Lai veiktu šo izvērtēšanu, var izmantot standarta komplektācijā iekļauto pārskatu **Labākās preces**, kuru var atvērt, izmantojot vienu no tālāk norādītajiem ceļiem.</span><span class="sxs-lookup"><span data-stu-id="d2832-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="d2832-119">Darbvieta **Mazumtirdzniecības veikala pārvaldība** &gt; **Mazumtirdzniecība** &gt; **Kanāli** &gt; **Mazumtirdzniecības veikala pārvaldība** &gt; **Pārskati** &gt; **Labāko preču pārskats**</span><span class="sxs-lookup"><span data-stu-id="d2832-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="d2832-120">Darbvieta **Kategorijas un preču pārvaldība** &gt; **Mazumtirdzniecība** &gt; **Preces un kategorijas** &gt; **Mazumtirdzniecības veikala pārvaldība** &gt; **Pārskati** &gt; **Labāko preču pārskats**</span><span class="sxs-lookup"><span data-stu-id="d2832-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="d2832-121">Sadaļa **Pieprasījumi un pārskati** &gt; **Mazumtirdzniecība** &gt; **Pieprasījumi un pārskati** &gt; **Pārdošanas pārskati** &gt; **Labāko preču pārskats**</span><span class="sxs-lookup"><span data-stu-id="d2832-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>

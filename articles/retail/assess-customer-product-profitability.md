---
title: "Debitoru un preču ienesīguma novērtēšana"
description: "Šajā rakstā ir paskaidrots, kā varat izmantot atmiņā saglabāto datu un reāllaika analīzi, la piekļūtu informācijai par debitoriem un preču ienesīgumu, pētītu šo informāciju un gūtu par to ieskatus, izmantojot Microsoft Dynamics 365 for Retail datus."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
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
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: dd6fb75b4ea7a82e179c236ea4bb7f2fd2ce6cb8
ms.contentlocale: lv-lv
ms.lasthandoff: 05/08/2018

---

# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="322aa-103">Novērtēt debitoru un preču ienesīgumu</span><span class="sxs-lookup"><span data-stu-id="322aa-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="322aa-104">Šajā rakstā ir paskaidrots, kā varat izmantot atmiņā saglabāto datu un reāllaika analīzi, la piekļūtu informācijai par debitoriem un preču ienesīgumu, pētītu šo informāciju un gūtu par to ieskatus, izmantojot Microsoft Dynamics 365 for Retail datus.</span><span class="sxs-lookup"><span data-stu-id="322aa-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Microsoft Dynamics 365 for Retail data.</span></span> 

<span data-ttu-id="322aa-105">Programmatūrā Dynamics 365 for Retail lietotāji var pētīt labāko debitoru (no 10 līdz 100) ienesīgumu dažādos organizācijas hierarhijas līmeņos, pamatojoties uz vienu no tālāk norādītajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="322aa-105">As part of Dynamics 365 for Retail, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="322aa-106">Pārdošanas summa</span><span class="sxs-lookup"><span data-stu-id="322aa-106">Sales amount</span></span>
-   <span data-ttu-id="322aa-107">Daudzums</span><span class="sxs-lookup"><span data-stu-id="322aa-107">Quantity</span></span>
-   <span data-ttu-id="322aa-108">Bruto peļņas norma</span><span class="sxs-lookup"><span data-stu-id="322aa-108">Gross profit margin</span></span>
-   <span data-ttu-id="322aa-109">Uzcenojuma procenti</span><span class="sxs-lookup"><span data-stu-id="322aa-109">Margin percentage</span></span>

<span data-ttu-id="322aa-110">Lai veiktu šo izvērtēšanu, var izmantot inovatīvo pārskatu **Lielākie debitori**, kuru var atvērt, izmantojot vienu no tālāk norādītajiem ceļiem.</span><span class="sxs-lookup"><span data-stu-id="322aa-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="322aa-111">Darbvieta **Mazumtirdzniecības veikala pārvaldība** &gt; **Mazumtirdzniecība** &gt; **Kanāli** &gt; **Mazumtirdzniecības veikala pārvaldība** &gt; **Pārskati** &gt; **Lielāko debitoru pārskats**</span><span class="sxs-lookup"><span data-stu-id="322aa-111">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top customers report**</span></span>
-   <span data-ttu-id="322aa-112">Sadaļa **Pieprasījumi un pārskati** &gt; **Mazumtirdzniecība** &gt; **Pieprasījumi un pārskati** &gt; **Pārdošanas pārskati** &gt; **Lielāko debitoru pārskats**</span><span class="sxs-lookup"><span data-stu-id="322aa-112">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="322aa-113">Līdzīgi lietotāji var pētīt augstākās kvalitātes preču (10–100) rentabilitāti dažādos organizācijas hierarhijas līmeņos, ņemot vēra tālāk norādītos kritērijus.</span><span class="sxs-lookup"><span data-stu-id="322aa-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

-   <span data-ttu-id="322aa-114">Pārdošanas summa</span><span class="sxs-lookup"><span data-stu-id="322aa-114">Sales amount</span></span>
-   <span data-ttu-id="322aa-115">Daudzums</span><span class="sxs-lookup"><span data-stu-id="322aa-115">Quantity</span></span>
-   <span data-ttu-id="322aa-116">Bruto peļņas norma</span><span class="sxs-lookup"><span data-stu-id="322aa-116">Gross profit margin</span></span>
-   <span data-ttu-id="322aa-117">Uzcenojuma procenti</span><span class="sxs-lookup"><span data-stu-id="322aa-117">Margin percentage</span></span>

<span data-ttu-id="322aa-118">Lai veiktu šo izvērtēšanu, var izmantot standarta komplektācijā iekļauto pārskatu **Labākās preces**, kuru var atvērt, izmantojot vienu no tālāk norādītajiem ceļiem.</span><span class="sxs-lookup"><span data-stu-id="322aa-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

-   <span data-ttu-id="322aa-119">Darbvieta **Mazumtirdzniecības veikala pārvaldība** &gt; **Mazumtirdzniecība** &gt; **Kanāli** &gt; **Mazumtirdzniecības veikala pārvaldība** &gt; **Pārskati** &gt; **Labāko preču pārskats**</span><span class="sxs-lookup"><span data-stu-id="322aa-119">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="322aa-120">Darbvieta **Kategorijas un preču pārvaldība** &gt; **Mazumtirdzniecība** &gt; **Preces un kategorijas** &gt; **Mazumtirdzniecības veikala pārvaldība** &gt; **Pārskati** &gt; **Labāko preču pārskats**</span><span class="sxs-lookup"><span data-stu-id="322aa-120">**Category and product management** workspace &gt; **Retail** &gt; **Products and categories** &gt; **Retail store management** &gt; **Reports** &gt; **Top products report**</span></span>
-   <span data-ttu-id="322aa-121">Sadaļa **Pieprasījumi un pārskati** &gt; **Mazumtirdzniecība** &gt; **Pieprasījumi un pārskati** &gt; **Pārdošanas pārskati** &gt; **Labāko preču pārskats**</span><span class="sxs-lookup"><span data-stu-id="322aa-121">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>





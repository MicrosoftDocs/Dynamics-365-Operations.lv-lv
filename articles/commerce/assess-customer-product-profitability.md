---
title: Debitoru un preču ienesīguma novērtēšana
description: Šajā rakstā ir paskaidrots, kā var izmantot atmiņā saglabāto un reāllaika analīzi, lai piekļūtu informācijai par debitoru un preču ienesīgumu no Dynamics 365 Commerce datiem, pētītu šo informāciju un gūtu ieskatus par to.
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
ms.openlocfilehash: 3218a29995791ce0d9a42d5b6d898d6e548f0f1d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023239"
---
# <a name="assess-customer-and-product-profitability"></a><span data-ttu-id="e762b-103">Novērtēt debitoru un preču ienesīgumu</span><span class="sxs-lookup"><span data-stu-id="e762b-103">Assess customer and product profitability</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e762b-104">Šajā rakstā ir paskaidrots, kā var izmantot atmiņā saglabāto un reāllaika analīzi, lai piekļūtu informācijai par debitoru un preču ienesīgumu no Dynamics 365 Commerce datiem, pētītu šo informāciju un gūtu ieskatus par to.</span><span class="sxs-lookup"><span data-stu-id="e762b-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about customers and product profitability from your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="e762b-105">Programmā Commerce lietotāji var pētīt labāko debitoru (10–100) ienesīgumu dažādos organizācijas hierarhijas līmeņos, pamatojoties uz kādu no tālāk norādītajiem kritērijiem.</span><span class="sxs-lookup"><span data-stu-id="e762b-105">As part of Commerce, users can study profitability for the top customers (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="e762b-106">Pārdošanas summa</span><span class="sxs-lookup"><span data-stu-id="e762b-106">Sales amount</span></span>
- <span data-ttu-id="e762b-107">Daudzums</span><span class="sxs-lookup"><span data-stu-id="e762b-107">Quantity</span></span>
- <span data-ttu-id="e762b-108">Bruto peļņas norma</span><span class="sxs-lookup"><span data-stu-id="e762b-108">Gross profit margin</span></span>
- <span data-ttu-id="e762b-109">Uzcenojuma procenti</span><span class="sxs-lookup"><span data-stu-id="e762b-109">Margin percentage</span></span>

<span data-ttu-id="e762b-110">Lai veiktu šo izvērtēšanu, var izmantot inovatīvo pārskatu **Lielākie debitori**, kuru var atvērt, izmantojot vienu no tālāk norādītajiem ceļiem.</span><span class="sxs-lookup"><span data-stu-id="e762b-110">For this assessment, you can use the out-of-box **Top customers** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="e762b-111">Darbvieta **Veikala pārvaldība** &gt; **Mazumtirdzniecība un komercija** &gt; **Kanāli** &gt; **Veikala pārvaldība** &gt; **Pārskati** &gt; **Lielāko debitoru pārskats**</span><span class="sxs-lookup"><span data-stu-id="e762b-111">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top customers report**</span></span>
- <span data-ttu-id="e762b-112">Sadaļa **Pieprasījumi un pārskati** &gt; **Mazumtirdzniecība un komercija** &gt; **Pieprasījumi un pārskati** &gt; **Pārdošanas pārskati** &gt; **Lielāko debitoru pārskats**</span><span class="sxs-lookup"><span data-stu-id="e762b-112">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top customers report**</span></span>

<span data-ttu-id="e762b-113">Līdzīgi lietotāji var pētīt augstākās kvalitātes preču (10–100) rentabilitāti dažādos organizācijas hierarhijas līmeņos, ņemot vēra tālāk norādītos kritērijus.</span><span class="sxs-lookup"><span data-stu-id="e762b-113">Likewise, users can study profitability for the top products (10 to 100) across different levels of the organization hierarchy, based on one of the following criteria:</span></span>

- <span data-ttu-id="e762b-114">Pārdošanas summa</span><span class="sxs-lookup"><span data-stu-id="e762b-114">Sales amount</span></span>
- <span data-ttu-id="e762b-115">Daudzums</span><span class="sxs-lookup"><span data-stu-id="e762b-115">Quantity</span></span>
- <span data-ttu-id="e762b-116">Bruto peļņas norma</span><span class="sxs-lookup"><span data-stu-id="e762b-116">Gross profit margin</span></span>
- <span data-ttu-id="e762b-117">Uzcenojuma procenti</span><span class="sxs-lookup"><span data-stu-id="e762b-117">Margin percentage</span></span>

<span data-ttu-id="e762b-118">Lai veiktu šo izvērtēšanu, var izmantot standarta komplektācijā iekļauto pārskatu **Labākās preces**, kuru var atvērt, izmantojot vienu no tālāk norādītajiem ceļiem.</span><span class="sxs-lookup"><span data-stu-id="e762b-118">For this assessment, you can use the out-of-box **Top products** report, which you can open from any of the following locations:</span></span>

- <span data-ttu-id="e762b-119">Darbvieta **Veikala pārvaldība** &gt; **Mazumtirdzniecība un komercija** &gt; **Kanāli** &gt; **Veikala pārvaldība** &gt; **Pārskati** &gt; **Labāko preču pārskats**</span><span class="sxs-lookup"><span data-stu-id="e762b-119">**Store management** workspace &gt; **Retail and Commerce** &gt; **Channels** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="e762b-120">Darbvieta **Kategorijas un preču pārvaldība** &gt; **Mazumtirdzniecība un komercija** &gt; **Preces un kategorijas** &gt; **Veikala pārvaldība** &gt; **Pārskati** &gt; **Labāko preču pārskats**</span><span class="sxs-lookup"><span data-stu-id="e762b-120">**Category and product management** workspace &gt; **Retail and Commerce** &gt; **Products and categories** &gt; **Store management** &gt; **Reports** &gt; **Top products report**</span></span>
- <span data-ttu-id="e762b-121">Sadaļa **Pieprasījumi un pārskati** &gt; **Mazumtirdzniecība un komercija** &gt; **Pieprasījumi un pārskati** &gt; **Pārdošanas pārskati** &gt; **Labāko preču pārskats**</span><span class="sxs-lookup"><span data-stu-id="e762b-121">**Inquiries and reports** section &gt; **Retail and Commerce** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Top products report**</span></span>
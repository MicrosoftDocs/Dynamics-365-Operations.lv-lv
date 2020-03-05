---
title: Veikala veiktspējas analizēšana
description: Šajā rakstā ir paskaidrots, kā var izmantot atmiņā saglabāto un reāllaika analīzi, lai piekļūtu, pārskatītu un gūtu informāciju par veikala veiktspēju, balstoties uz Dynamics 365 Commerce datiem.
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailChannelReport, RetailChannelManagementWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 57811
ms.assetid: 495a66f0-491a-4688-842d-51c33c37676f
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8d95bb0927de5a1906efe180cb9e725c380a724f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/01/2020
ms.locfileid: "3023297"
---
# <a name="analyze-store-performance"></a><span data-ttu-id="c3347-103">Veikala veiktspējas analīze</span><span class="sxs-lookup"><span data-stu-id="c3347-103">Analyze store performance</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c3347-104">Šajā rakstā ir paskaidrots, kā var izmantot atmiņā saglabāto un reāllaika analīzi, lai piekļūtu, pārskatītu un gūtu informāciju par veikala veiktspēju, balstoties uz Dynamics 365 Commerce datiem.</span><span class="sxs-lookup"><span data-stu-id="c3347-104">This article explains how you can use the in-memory and real-time analytics to access, explore, and gain insight about store performance, based on your Dynamics 365 Commerce data.</span></span>

<span data-ttu-id="c3347-105">Izmantojot programmu Retail, lietotāji var izpētīt veikala reāllaika veiktspēju dažādos organizācijas hierarhijas līmeņos atlasītajā periodā, atverot standarta pārskatu **Kanāla kopsavilkums** no jebkuras tālāk minētās atrašanās vietas.</span><span class="sxs-lookup"><span data-stu-id="c3347-105">As part of Retail, users can study store performance in real time across different levels of the organization hierarchy over a selected period by opening the out-of-box **Channel summary** report from any of the following locations:</span></span>

- <span data-ttu-id="c3347-106">Darbvieta **Mazumtirdzniecības veikala pārvaldība** &gt; **Mazumtirdzniecība** &gt; **Kanāli** &gt; **Mazumtirdzniecības veikala pārvaldība** &gt; **Pārskati** &gt; **Kanāla kopsavilkuma pārskats**</span><span class="sxs-lookup"><span data-stu-id="c3347-106">**Retail store management** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store management** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="c3347-107">Darbvieta **Mazumtirdzniecības veikala finanses** &gt; **Mazumtirdzniecība** &gt; **Kanāli** &gt; **Mazumtirdzniecības veikala finanses** &gt; **Pārskati** &gt; **Kanāla kopsavilkuma pārskats**</span><span class="sxs-lookup"><span data-stu-id="c3347-107">**Retail store financials** workspace &gt; **Retail** &gt; **Channels** &gt; **Retail store financials** &gt; **Reports** &gt; **Channel summary report**</span></span>
- <span data-ttu-id="c3347-108">Sadaļa **Pieprasījumi un pārskati** &gt; **Mazumtirdzniecība** &gt; **Pieprasījumi un pārskati** &gt; **Pārdošanas pārskati** &gt; **Kanāla kopsavilkuma pārskats**</span><span class="sxs-lookup"><span data-stu-id="c3347-108">**Inquiries and reports** section &gt; **Retail** &gt; **Inquiries and reports** &gt; **Sales reports** &gt; **Channel summary report**</span></span>

<span data-ttu-id="c3347-109">Šis pārskats pēc veikala veiktspējas analīzes nodrošina tālāk norādīto apkopojumu momentuzņēmumu.</span><span class="sxs-lookup"><span data-stu-id="c3347-109">This report provides a snapshot of following summaries as part of store performance:</span></span>

- <span data-ttu-id="c3347-110">Bruto pārdošanas kopsavilkums</span><span class="sxs-lookup"><span data-stu-id="c3347-110">Gross sales summary</span></span>
- <span data-ttu-id="c3347-111">Norēķinu veida kopsavilkums</span><span class="sxs-lookup"><span data-stu-id="c3347-111">Tender type summary</span></span>
- <span data-ttu-id="c3347-112">Nodokļu kopsavilkums</span><span class="sxs-lookup"><span data-stu-id="c3347-112">Tax summary</span></span>
- <span data-ttu-id="c3347-113">Informācijas par cenas pārlabošanas notikumiem kopsavilkums</span><span class="sxs-lookup"><span data-stu-id="c3347-113">Price overrides summary</span></span>
- <span data-ttu-id="c3347-114">Informācijas par atlaidēm kopsavilkums</span><span class="sxs-lookup"><span data-stu-id="c3347-114">Discounts summary</span></span>
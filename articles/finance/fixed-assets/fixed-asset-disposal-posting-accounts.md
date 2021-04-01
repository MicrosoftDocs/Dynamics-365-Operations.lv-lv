---
title: Pamatlīdzekļu norakstīšanas grāmatošanas konti
description: Šajā tēmā ir paskaidrots, kā iestatīt līdzekļu norakstīšanas Virsgrāmatas grāmatošanas kontus.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 3461
ms.assetid: dfdc0730-e030-48cc-8d93-15bdc7b23776
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 92b653d50744884d56c19601cff74c420eb1b397
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5240974"
---
# <a name="fixed-asset-disposal-posting-accounts"></a><span data-ttu-id="98bdd-103">Pamatlīdzekļu norakstīšanas grāmatošanas konti</span><span class="sxs-lookup"><span data-stu-id="98bdd-103">Fixed asset disposal posting accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98bdd-104">Šajā tēmā ir paskaidrots, kā iestatīt līdzekļu norakstīšanas Virsgrāmatas grāmatošanas kontus.</span><span class="sxs-lookup"><span data-stu-id="98bdd-104">This topic explains how to set up general ledger posting accounts for disposing of assets.</span></span>

<span data-ttu-id="98bdd-105">Lapas Pamatlīdzekļu grāmatošanas metodes kopsavilkuma cilnē Virsgrāmatas konti atlasiet opcijas Izslēgšana — pārdošana un Izslēgšana — brāķis, lai iestatītu grāmatošanu virsgrāmatā.</span><span class="sxs-lookup"><span data-stu-id="98bdd-105">In the Fixed asset posting profiles page, on the Ledger accounts FastTab, select Disposal - sale and Disposal - scrap to set up postings to the ledger.</span></span>

<span data-ttu-id="98bdd-106">Abiem darbību veidiem tiek kreditēts virsgrāmatas konts, kas paredzēts pamatlīdzekļa norakstīšanas vērtībai.</span><span class="sxs-lookup"><span data-stu-id="98bdd-106">For both transaction types, the ledger account is credited for the disposal value of the fixed asset.</span></span> <span data-ttu-id="98bdd-107">Debets tiek grāmatots korespondējošā kontā, kurš var būt, piemēram, bankas konts.</span><span class="sxs-lookup"><span data-stu-id="98bdd-107">The debit is posted to an offset account, which might be, for example, a bank account.</span></span> <span data-ttu-id="98bdd-108">Ja pamatlīdzeklis tiek pārdots debitoram, korespondējošā konta vietā tiek izmantots debitora konts.</span><span class="sxs-lookup"><span data-stu-id="98bdd-108">If a fixed asset is sold to a customer, the customer account is used instead of the offset account.</span></span>

<span data-ttu-id="98bdd-109">Noklikšķiniet uz Izslēgšana un pēc tam noklikšķiniet uz Pārdošana vai Brāķis un pēc tam detalizēti iestatiet kontus, lai atgūtu pamatlīdzekļa atlikušo vērtību.</span><span class="sxs-lookup"><span data-stu-id="98bdd-109">Click Disposal and then click Sale or Scrap, and then set up detailed accounts to reverse the net book value of the fixed asset.</span></span> <span data-ttu-id="98bdd-110">Varat arī ievadīt informāciju lapas Izslēgšanas parametri laukos Grāmatot vērtību un Pārdošanas vērtības kontējuma tips.</span><span class="sxs-lookup"><span data-stu-id="98bdd-110">You can also enter information in the Post value and Sales value type fields in the Disposal parameters page.</span></span> 

<span data-ttu-id="98bdd-111">Mazvērtīgas kopas līdzekļa norakstīšanas darbība samazina mazvērtīgās kopas atlikušo vērtību tikai par norakstīto summu.</span><span class="sxs-lookup"><span data-stu-id="98bdd-111">The disposal transaction for an asset in a low-value pool reduces the net book value of the low-value pool by the disposed amount only.</span></span> <span data-ttu-id="98bdd-112">Taču, ja līdzekļa pārdošanas vērtība pārsniedz mazvērtīgās kopas atlikušo vērtību, atlikusī vērtība tiek samazināta līdz nullei.</span><span class="sxs-lookup"><span data-stu-id="98bdd-112">However, when the sale of an asset exceeds the net book value of the low-value pool, the net book value is reduced to zero.</span></span>







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
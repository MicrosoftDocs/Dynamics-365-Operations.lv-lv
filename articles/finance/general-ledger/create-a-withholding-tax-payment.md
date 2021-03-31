---
title: Ieturētā nodokļa maksājuma izveide
description: Ieturētā nodokļa maksājuma uzdevums sedz ieturētā nodokļa bilances no kreditoru ieturētā nodokļa kontos un noteiktajam periodam atlīdzina tās ieturētā nodokļa maksājumu kontā. Šajā tēmā ir uzskaitīti soļi ieturētā nodokļa maksājuma iestatīšanai.
author: roschlom
manager: AnnBe
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2020-01-12
ms.dyn365.ops.version: AX 10.0.16
ms.openlocfilehash: eae914ccafad12426cadd91c0950bada23548005
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212281"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="05008-104">Ieturētā nodokļa maksājuma izveide</span><span class="sxs-lookup"><span data-stu-id="05008-104">Create a withholding tax payment</span></span>

<span data-ttu-id="05008-105">Ieturētā nodokļa maksājuma uzdevums sedz ieturētā nodokļa bilances no kreditoru ieturētā nodokļa kontos un noteiktajam periodam atlīdzina tās ieturētā nodokļa maksājumu kontā.</span><span class="sxs-lookup"><span data-stu-id="05008-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="05008-106">Šajā tēmā ir uzskaitīti soļi ieturētā nodokļa maksājuma iestatīšanai.</span><span class="sxs-lookup"><span data-stu-id="05008-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="05008-107">Ieturētā nodokļa kompensācija (no debitoriem) netiek ņemta vērā, kad tiek aprēķināts ieturētā nodokļa maksājums.</span><span class="sxs-lookup"><span data-stu-id="05008-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="05008-108">Pārejiet uz **Navigācijas rūts > Moduļi > Nodokļi > Deklarācijas > Ieturētais nodoklis > Ieturētā nodokļa maksājums**.</span><span class="sxs-lookup"><span data-stu-id="05008-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="05008-109">Laukā **Nomaksas periods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="05008-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="05008-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="05008-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="05008-111">Ievadiet datumu laukā **No datuma**.</span><span class="sxs-lookup"><span data-stu-id="05008-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="05008-112">Ievadiet datumu laukā **Transakcijas datums**.</span><span class="sxs-lookup"><span data-stu-id="05008-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="05008-113">Atlasiet **Atjaunināt**, lai ieturētā nodokļa maksājuma dokumentu grāmatotu ieturētā nodokļa apmaksas kontā.</span><span class="sxs-lookup"><span data-stu-id="05008-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="05008-114">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="05008-114">Click **OK**.</span></span>

![Ieturētā nodokļa maksājuma parametri](media/withholding-tax-payment.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Ieturētā nodokļa maksājuma izveide
description: Ieturētā nodokļa maksājuma uzdevums sedz ieturētā nodokļa bilances no kreditoru ieturētā nodokļa kontos un noteiktajam periodam atlīdzina tās ieturētā nodokļa maksājumu kontā. Šajā tēmā ir uzskaitīti soļi ieturētā nodokļa maksājuma iestatīšanai.
author: roschlom
ms.date: 01/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 72d80fbb3b2448f4b89fa7d7fa580387e1a3621c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832950"
---
# <a name="create-a-withholding-tax-payment"></a><span data-ttu-id="7676e-104">Ieturētā nodokļa maksājuma izveide</span><span class="sxs-lookup"><span data-stu-id="7676e-104">Create a withholding tax payment</span></span>

<span data-ttu-id="7676e-105">Ieturētā nodokļa maksājuma uzdevums sedz ieturētā nodokļa bilances no kreditoru ieturētā nodokļa kontos un noteiktajam periodam atlīdzina tās ieturētā nodokļa maksājumu kontā.</span><span class="sxs-lookup"><span data-stu-id="7676e-105">The Withholding tax payment job procedure settles withholding tax balances from Accounts payable on withholding tax accounts, and offsets them to the withholding tax settlement account for a given period.</span></span> <span data-ttu-id="7676e-106">Šajā tēmā ir uzskaitīti soļi ieturētā nodokļa maksājuma iestatīšanai.</span><span class="sxs-lookup"><span data-stu-id="7676e-106">This topic lists the steps for setting up a withholding tax payment.</span></span>

> [!NOTE] 
> <span data-ttu-id="7676e-107">Ieturētā nodokļa kompensācija (no debitoriem) netiek ņemta vērā, kad tiek aprēķināts ieturētā nodokļa maksājums.</span><span class="sxs-lookup"><span data-stu-id="7676e-107">Withholding tax offset (from accounts receivable) is not taken into account when a withholding tax payment is calculated.</span></span>

1. <span data-ttu-id="7676e-108">Pārejiet uz **Navigācijas rūts > Moduļi > Nodokļi > Deklarācijas > Ieturētais nodoklis > Ieturētā nodokļa maksājums**.</span><span class="sxs-lookup"><span data-stu-id="7676e-108">Go to **Navigation pane > Modules > Tax > Declarations > Withholding tax > Withholding tax payment**.</span></span>
2. <span data-ttu-id="7676e-109">Laukā **Nomaksas periods** noklikšķiniet uz nolaižamā saraksta pogas, lai atvērtu uzmeklēšanu.</span><span class="sxs-lookup"><span data-stu-id="7676e-109">In the **Settlement period** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="7676e-110">Sarakstā noklikšķiniet uz saites atlasītajā rindā.</span><span class="sxs-lookup"><span data-stu-id="7676e-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="7676e-111">Ievadiet datumu laukā **No datuma**.</span><span class="sxs-lookup"><span data-stu-id="7676e-111">In the **From date** field, enter a date.</span></span>
5. <span data-ttu-id="7676e-112">Ievadiet datumu laukā **Transakcijas datums**.</span><span class="sxs-lookup"><span data-stu-id="7676e-112">In the **Transaction date** field, enter a date.</span></span>
6. <span data-ttu-id="7676e-113">Atlasiet **Atjaunināt**, lai ieturētā nodokļa maksājuma dokumentu grāmatotu ieturētā nodokļa apmaksas kontā.</span><span class="sxs-lookup"><span data-stu-id="7676e-113">Select **Update** to post withholding tax payment voucher to the withholding tax settlement account.</span></span>
7. <span data-ttu-id="7676e-114">Noklikšķiniet uz **Labi**.</span><span class="sxs-lookup"><span data-stu-id="7676e-114">Click **OK**.</span></span>

![Ieturētā nodokļa maksājuma parametri](media/withholding-tax-payment.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
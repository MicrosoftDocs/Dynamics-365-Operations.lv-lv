---
title: Saskaņošanas iemeslu dēļ kā kredīta kontu var pievienot tikai galveno kontu
description: Kad transportēšanas pārvaldībā iestatāt saskaņošanas iemeslu, tikai galveno kontu var pievienot kā kredīta kontu.
author: Henrikan
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: TMSFBDetailReconcile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 708081370b27fd51ef9a2329d8392f4515353dcb
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026697"
---
# <a name="you-can-add-only-the-main-account-as-the-credit-account-for-reconciliation-reasons"></a><span data-ttu-id="7fcb0-103">Saskaņošanas iemeslu dēļ kā kredīta kontu var pievienot tikai galveno kontu</span><span class="sxs-lookup"><span data-stu-id="7fcb0-103">You can add only the main account as the credit account for reconciliation reasons</span></span>

<span data-ttu-id="7fcb0-104">KB numurs: 4603538</span><span class="sxs-lookup"><span data-stu-id="7fcb0-104">KB number: 4603538</span></span>

## <a name="symptoms"></a><span data-ttu-id="7fcb0-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="7fcb0-105">Symptoms</span></span>

<span data-ttu-id="7fcb0-106">Kad transportēšanas pārvaldībā iestatāt saskaņošanas iemeslu, tikai galveno kontu var pievienot kā kredīta kontu.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-106">When you set up a reconciliation reason in Transportation management, you can add only the main account as the credit account.</span></span> <span data-ttu-id="7fcb0-107">Kā kredīta kontu nevar pievienot izmaksu centru vai jebkādu citu dimensiju.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-107">You can't add a cost center or any other dimension as the credit account.</span></span> <span data-ttu-id="7fcb0-108">Tomēr debeta konts ļauj atlasīt citas dimensijas.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-108">However, the debit account lets you select other dimensions.</span></span>

## <a name="resolution"></a><span data-ttu-id="7fcb0-109">Novēršana</span><span class="sxs-lookup"><span data-stu-id="7fcb0-109">Resolution</span></span>

<span data-ttu-id="7fcb0-110">Ja saskaņošana nav veikta, lai maksātu kreditoram, bet lai kreditētu noteiktu galveno kontu, sistēma neļauj jums atlasīt kredīta konta finanšu dimensiju, kad ir iestatīts saskaņošanas iemesls.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-110">If the reconciliation isn't done to pay the vendor but to credit a specific main account, the system doesn't allow you to select a financial dimension for the credit account when you set up the reconciliation reason.</span></span>

<span data-ttu-id="7fcb0-111">Ja konta struktūrai kredīta galvenajam kontam nepieciešama specifiska finanšu dimensijas vērtība, iegūto kreditoru žurnālu nevar grāmatot automātiski, jo trūkst finanšu dimensijas vērtības.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-111">If the account structure requires a specific financial dimension value for the credit main account, the resulting vendor journal can't be posted automatically, because the financial dimension value is missing.</span></span> <span data-ttu-id="7fcb0-112">Tāpēc jums vispirms ir manuāli jānorāda kredīta konts, izmantojot **Rēķinu žurnāla** lapu.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-112">Therefore, you must first manually specify the credit account by using the **Invoice journal** page.</span></span>

<span data-ttu-id="7fcb0-113">Tā kā kredīta kontam ir nepieciešama dimensijas vērtība, kreditoru rēķinu žurnālu nevar automātiski grāmatot.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-113">Because a dimension value is required for the credit account, the vendor invoice journal can't be automatically posted.</span></span> <span data-ttu-id="7fcb0-114">Pēc tam, kad manuāli pievienojat dimensijas vērtību galvenajam kontam kredīta rindai, tā ir jāgrāmato manuāli.</span><span class="sxs-lookup"><span data-stu-id="7fcb0-114">You must manually post it after you manually add the dimension value to the main account for the credit line.</span></span>

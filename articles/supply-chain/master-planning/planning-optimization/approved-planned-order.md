---
title: Plānoto pasūtījumu apstiprināšana
description: Šajā tēmā ir aprakstīta plānošanas optimizācijas atbalstīto plānoto pasūtījumu apstiprināšana.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c29ede7ad8916a97b4a04b68f41961f79810e0c8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983573"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="835b0-103">Plānoto pasūtījumu apstiprināšana</span><span class="sxs-lookup"><span data-stu-id="835b0-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="835b0-104">Šajā tēmā ir sniegta informācija par to, kā atjaunināt plānoto pasūtījumu statusu plānošanas optimizācijā.</span><span class="sxs-lookup"><span data-stu-id="835b0-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="835b0-105">Ņemiet vērā, ka plānoto pasūtījumu apstiprināšana ir neobligāts solis, lai izveidotu apstiprinātu pasūtījumu no plānotā pasūtījuma.</span><span class="sxs-lookup"><span data-stu-id="835b0-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="835b0-106">Ieteicams apstiprināt modificētos plānotos pasūtījumus, pretējā gadījumā labojumi tiks ignorēti un pārrakstīti ar nākamo plānošanas izpildi.</span><span class="sxs-lookup"><span data-stu-id="835b0-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![Plānotā pasūtījumu plūsma](media/approved-planned-orders-1.png)

<span data-ttu-id="835b0-108">Lauks **Statuss** palīdz izlīdzināt jūsu progresu, izmantojot tālāk norādītās vērtības:</span><span class="sxs-lookup"><span data-stu-id="835b0-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="835b0-109">**Neapstrādāts:** Kad vispārējā plānošana ģenerē plānotos pasūtījumus, tiem tiek piešķirts statuss *Neapstrādāts*.</span><span class="sxs-lookup"><span data-stu-id="835b0-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="835b0-110">Plānotie pasūtījumi ar šo statusu tiks dzēsti nākamās plānošanas izpildes laikā.</span><span class="sxs-lookup"><span data-stu-id="835b0-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="835b0-111">**Pabeigts:** Ja izlemjat neapstiprināt plānoto pasūtījumu, varat mainīt statusu uz *Pabeigts* , lai norādītu, ka esat pabeiguši šī plānotā pasūtījuma novērtēšanu.</span><span class="sxs-lookup"><span data-stu-id="835b0-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="835b0-112">Ņemiet vērā, ka pret statusiem *Neapstrādāts* un *Pabeigts* sistēma izturas vienādi.</span><span class="sxs-lookup"><span data-stu-id="835b0-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="835b0-113">**Apstiprināts:** Ja vēlaties saglabāt labojumus vai plānojat apstiprināt plānoto pasūtījumu, mainiet statusu uz *Apstiprināts*.</span><span class="sxs-lookup"><span data-stu-id="835b0-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="835b0-114">Plānotos pasūtījumus ar statusu *Apstiprināts* tiek uzskatīti par fiksētiem un paredzamiem galvenās plānošanas pakalpojumiem, tāpēc tie netiek modificēti vai izdzēsti vēlāku vispārējās plānošanas palaišanu laikā.</span><span class="sxs-lookup"><span data-stu-id="835b0-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="835b0-115">Lai to sasniegtu, plānošanas loģika kopē *Apstiprinātos* plānotos pasūtījumus no vecās plāna versijas uz jauno plāna versiju vispārējās plānošanas laikā.</span><span class="sxs-lookup"><span data-stu-id="835b0-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="835b0-116">Ņemiet vērā, ka *Apstiprinātie* plānotie pasūtījumi tiek uzskatīti par piegādēm tikai noteiktajā galvenājā plānā.</span><span class="sxs-lookup"><span data-stu-id="835b0-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="835b0-117">Plānotos pasūtījumus var pārvaldīt no darbvietas  **Vispārējā plānošana**  , saraksta  **Plānotais pasūtījums**  vai saraksta  **Plānotie ražošanas pasūtījumi**,  **Plānotie pirkšanas pasūtījumi** un  **Plānotā pārsūtīšana**  .</span><span class="sxs-lookup"><span data-stu-id="835b0-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>

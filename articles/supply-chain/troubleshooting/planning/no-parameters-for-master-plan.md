---
title: Vispārējā plāna parametri nepastāv
description: Mēģinot apstiprināt plānoto pasūtījumu, tiek saņemts kļūdas ziņojums, kurā norādīts, ka vispārējām plānam nav parametru.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: lv-LV
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294130"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a><span data-ttu-id="18a16-103">Vispārējā plāna parametri nepastāv</span><span class="sxs-lookup"><span data-stu-id="18a16-103">Parameters for the master plan don't exist</span></span>

<span data-ttu-id="18a16-104">Kļūdas kods: SYS25368</span><span class="sxs-lookup"><span data-stu-id="18a16-104">Error code: SYS25368</span></span>

## <a name="symptoms"></a><span data-ttu-id="18a16-105">Simptomi</span><span class="sxs-lookup"><span data-stu-id="18a16-105">Symptoms</span></span>

<span data-ttu-id="18a16-106">Mēģinot apstiprināt plānoto pasūtījumu saņemsit šādu kļūdas ziņojumu:</span><span class="sxs-lookup"><span data-stu-id="18a16-106">When you try to firm a planned order, you receive the following error message:</span></span>

> <span data-ttu-id="18a16-107">Vispārējā plāna %1 parametri nav izveidoti.</span><span class="sxs-lookup"><span data-stu-id="18a16-107">Parameters for master plan %1 do not exist.</span></span>

## <a name="cause"></a><span data-ttu-id="18a16-108">Iemesls</span><span class="sxs-lookup"><span data-stu-id="18a16-108">Cause</span></span>

<span data-ttu-id="18a16-109">Konfigurācijas problēmu dēļ sistēma nevar atrast iestatījumus norādītajam plānam.</span><span class="sxs-lookup"><span data-stu-id="18a16-109">Because of configuration issues, the system can't find the settings for the specified plan.</span></span>

## <a name="resolution"></a><span data-ttu-id="18a16-110">Novēršana</span><span class="sxs-lookup"><span data-stu-id="18a16-110">Resolution</span></span>

- <span data-ttu-id="18a16-111">Dodieties uz **Vispārējā plānošana \> Iestatīšana \> Plāni \> Vispārējie plāni** un pārliecinieties, vai pastāv plāns ar norādīto nosaukumu.</span><span class="sxs-lookup"><span data-stu-id="18a16-111">Go to **Master planning \> Setup \> Plans \> Master plans**, and make sure that a plan that has the specified name exists.</span></span>
